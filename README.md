# study（筛法求素数）
#include<stdio.h>
int main()
{
	int i=3,j=2,c=1;
	for(i;i<1000;i++){
	
	for(j=2;j<i;j++){
		if(i%j==0){
			c=0;
			break;
		}
	}
	if(c==1){
		printf("%d ",i);
	} c=1;
	 }
	return 0;
} 
(编程时，忘记c=1在循环完后，c的大小可能改变，需要在每一轮循环开始前重新赋值c=1）
