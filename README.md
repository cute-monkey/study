# study(最大公约数）
#include<stdio.h>
void min(int *a,int *b);
int main(int argc,char *argv[])
{
	int a,b,c;
	printf("求两个数的最大公约数\n");
	scanf("%d%d",&a,&b);
	min(&a,&b);
	while(b%a!=0){
		b%=a;
		min(&a,&b);
	}
	printf("最大公约数为%d\n",a);
	
} 
void min(int *a,int *b){
	int t;
	if(*a>*b){
		t=*a;
		*a=*b;
		*b=t;
	}
}
