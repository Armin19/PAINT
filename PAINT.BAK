#include<iostream.h>
#include<conio.h>
#include<stdio.h>
void init();
void docommand(char c,int t);
int fcolor=7,bcolor=0;
int x,y;
int q;
int draw;

struct stack p{
  int i[100];
  int last=-1;
  void push(int x);
  int pop();
  int isEmpty(){ return last=-1;}
  int isFull(){ return last=99;}
void stack.push(int x){
if(!isFull()){
  last++;
  i[++last]=x;
}
int stack.pop(){
   if(!isEmpty()){
    return i[last]--j;
    }}
    return -1;



}
char funckey(int &t)
{
char c=getch();
if(c==0)
{
t=1;
c=getch();
}
else
t=0;
return c;
}
int far*screen=(int far*)0xB8000000;
int scr[2000];
void namayesh(int x,int y,int a,int frcolor,int bgcolor,int blink)
{
int v=frcolor+16*bgcolor+128*blink;
screen[y*80+x]=v*256+a;
}
int getscreen(int x,int y){
return screen[y*80+x];
}
void setscreen(int x,int y){
screen[y*80+x]=q;
}
void fill(int x,int y,int c){

if(screen[y*80+x]!=c);
else{
namayesh(x,y,219,fcolor,bcolor,0);
if(y>2)fill(x,y-1,c);
if(y<24)fill(x,y+1,c);
if(x>0)fill(x-1,y,c);
if(x<80)fill(x+1,y,c);
}

}
int main(){
	clrscr();
	init();
	int t;
	char c=funckey(t);
	while(t!=0 || c!=27){
	docommand(c,t);
	c=funckey(t);
	//fill(x,y);

}


return 0;
}
void init(){
draw=0;
fcolor=7;
bcolor=0;
x=40,y=12;
for(int i=0;i<80;i++)
   for(int j=0;j<25;j++)
      namayesh(i,j,219,fcolor,bcolor,0);
namayesh(0,1,'1',1,7,0);
namayesh(1,1,219,1,0,0);
namayesh(3,1,'2',1,7,0);
namayesh(4,1,219,2,0,0);
namayesh(6,1,'3',1,7,0);
namayesh(7,1,219,3,0,0);
namayesh(9,1,'4',1,7,0);
namayesh(10,1,219,4,0,0);
namayesh(12,1,'5',1,7,0);
namayesh(13,1,219,5,0,0);
namayesh(15,1,'6',1,7,0);
namayesh(16,1,219,6,0,0);
namayesh(18,1,'7',1,7,0);
namayesh(19,1,219,7,0,0);
namayesh(21,1,'P',1,7,0);
namayesh(22,1,'e',1,7,0);
namayesh(23,1,'n',1,7,0);
namayesh(24,1,':',1,7,0);
namayesh(25,1,'i',1,7,0);
namayesh(26,1,'n',1,7,0);
namayesh(27,1,'s',1,7,0);
namayesh(28,1,'e',1,7,0);
namayesh(29,1,'r',1,7,0);
namayesh(30,1,'t',1,7,0);
q=getscreen(x,y);
namayesh(x,y,'*',fcolor,bcolor,1);
}
FILE *myfile;
FILE *paint;

void docommand(char c,int t){
   if(t==0 &&(c=='s'||c=='S')){setscreen(x,y); myfile=fopen("C:\\TURBOC3\\bin\\paint.txt","w");
   for(int j=0;j<2000;j++)scr[j]=*(screen+j);
   fwrite(scr,2,2000,myfile);
   fclose(myfile);}
   if(t==0 &&(c=='o'||c=='O')){myfile=fopen("C:\\TURBOC3\\bin\\paint.txt","r");
   fread(scr,2,2000,myfile);
   for(int j=0;j<2000;j++)*(screen+j)=scr[j];
   getscreen(x,y);
   fclose(myfile);


   }
   if(t==0 &&(c=='f'||c=='F')){setscreen(x,y);fill(x,y,q);q=getscreen(x,y);}
   if(t==0 && c>47 && c<57)fcolor=c-48;
   if(t==1 &&c=='H'&& y>2){
     if (!draw)setscreen(x,y);
     else namayesh(x,y,219,fcolor,bcolor,0);
     y-=1;
     q=getscreen(x,y);
   }
   if(t==1&&c=='P'&& y<24){
     if (!draw)setscreen(x,y);
     else namayesh(x,y,219,fcolor,bcolor,0);
     y+=1;
     q=getscreen(x,y);
   }
   if(t==1&&c=='K'&& x>0){
     if (!draw)setscreen(x,y);
     else namayesh(x,y,219,fcolor,bcolor,0);
     x-=1;
     q=getscreen(x,y);
   }
   if(t==1&&c=='M'&& x<79){
     if (!draw)setscreen(x,y);
     else namayesh(x,y,219,fcolor,bcolor,0);
     x+=1;
     q=getscreen(x,y);
   }
   if(t==1&&c=='R'){draw=!draw;}
   namayesh(x,y,'*',fcolor,bcolor,1);

}






