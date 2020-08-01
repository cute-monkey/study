# study（三角形海伦公式）
#include<stdio.h>
#include<math.h>
int main()
{
	float a,b,c,q,s;
	printf("请输入三角形的长，宽，高\n");
	scanf("%f%f%f",&a,&b,&c);
	q=(a+b+c)/2;
	s=q*(q-a)*(q-b)*(q-c);
	s=sqrt(s);
	printf("三角形的面积是%f",s);
	return 0;
}
