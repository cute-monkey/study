# study（高次方求模）
#include<stdio.h>
#include<math.h>
int main(int argc,char *argv[])
{
	long a,b,m,ans,sum;
	printf("请输入x的y次方 对k求模");
	scanf("%d%d%d",&a,&b,&m);
	if(b%2!=0){
		b--;
		ans=a%m;
		sum=pow(ans,b)*a;
		sum%=m;
		printf("模是%d",sum);
	}else{
		ans=a%m;
		sum=pow(ans,b);
		sum%=m;
		printf("模是%d",sum);
	}
}
