# study（逆康托展开）
#include<stdio.h>
#include<math.h>
int main()
{
	int i=0,count,j,b[10]={0},k=1,m,n=0,q,sum=0,e[10]={0},g;
	int c[10]={0,1,2,3,4,5,6,7,8,9},d[10]={0};
	int a[]={1,1,2,6,24,120,720,5040,40320,362880,3628800};
	printf("请输入逆康托展开的数:\n");
	scanf("%d",&count);
	for(i;count>a[i]?1:0;i++);
	j=i-1;
	count-=1;
	for(;i>0;k++,j--,i--){
		b[k]=count/a[j];
		count%=a[j];
	}
	k--;
	g=k;
	for(int r=1;r<=g;r++,g--){
		e[g]=b[r];
	}
	g=k;
	for(k;k>=1;k--){
		q=k;
		n=0;
		m=q-1;
		for(q;q!=0;){
			for(m;m!=0;m--){
				c[q]>c[m];
				n++;
			}
		if(n==e[k]){
			d[k]=c[q];
			for(q;q<k;q++){
				c[q]=c[q+1];
			}
		 	
			break;
  	  	}
  	 		n=0;
  	 		q--;
  	 		m=q-1;
    	 }
 }
 	for(g;g>=1;g--){
 		sum+=d[g]*pow(10,g-1);
 	}
 	printf("%d",sum);
 	
	
}
（想了很久才想出来 如何去掉数组中一个任意的数字，并用剩下的数字组成新的数组）
