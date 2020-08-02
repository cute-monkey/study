# study(康托展开）
#include<stdio.h>
int main(int argc,char *argv[])
{
	int a[]={1,1,2,6,24,120,720,5040,40320,362880,3628800};
	int num[10];
	int b,time=1,i=0,j,sum=0,c=0;
	printf("请输入数字大小：\n");
	scanf("%d",&b);
	for(;b!=0;time++){
		if(b>9){
		num[time]=b%10;}
		else {
		num[time]=b;
		}
		b/=10;
	}
	time-=1;
	for(time;time>=1;time--){
		j=time-1;
		for(j;j>=1;j--){
			if(num[time]>num[j]){
				i++;
			}
		}
		sum+=i*a[time-1];
		i=0;
	}
	printf("该数的康托展开值是%d ",sum+1);
	return 0;
}

编程的时候忘记初始化sum，导致结果一直不对 后来才发现 谨记此次教训
