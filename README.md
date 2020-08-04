# study（同余定理）
#include<stdio.h>
int min(int a,int b);
int max(int a,int b);
int main(int argc,char* argv[])

{
	int a=0,b=0,m,n,i=2,j=0;
	printf("请输入两个数：\n");
	scanf("%d%d",&a,&b);
	m=min(a,b);
	n=max(a,b);
	for(i;i<m;i++){
		if((n-m)%i==0){
			j=1;
			break;
		}
	}
	if(j==1){
		printf("%d和%d 对%d同余",a,b,i);
	}else{
		printf("%d和%d不同余",a,b);
	}
	return 0;
	
}
int min(int a,int b)
{
	int t=a;
	if(a>b){
		t=b;
	}
	return t;
}
int max(int a,int b)
{
	int t=a;
	if(a<b){
		t=b;
	}
	return t;
}
