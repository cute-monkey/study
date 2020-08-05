# study（三点排序）
#include<stdio.h>
int main(int argc,char*argv[]){
	int x1,x2,x3,y1,y2,y3,a,b,c,d,max;
	printf("请输入A,B,C三点的坐标:\n");
	scanf("%d%d%d%d%d%d",&x1,&y1,&x2,&y2,&x3,&y3);
	a=x2-x1,b=y2-y1,c=x3-x1,d=y3-y1;
	max=a*d-b*c;
	if(max>0){
		printf("三角形按逆时针排序\n");
	}else if(max<0){
		printf("三角形按顺时针排序\n");
	}else{
		printf("三点共线\n");
	}
} 
