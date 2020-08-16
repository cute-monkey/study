# study（链表，数字）
#include<stdio.h>
#include<stdlib.h>
struct point{
	int number;
	struct point *next;
};
struct point *creat(){
	struct point *now,*then,*ago;
	int i;
	char go;
	ago=(struct point*)malloc(sizeof(struct point));
	printf("请输入数字：");
	scanf("%d",&i);
	ago->number=i;
	now=ago;
	printf("是否继续？");
	getchar();
	scanf("%c",&go);
	while(i!=-1 && go!='n'){
		then=(struct point*)malloc(sizeof(struct point));
		printf("请输入数字："); 
		scanf("%d",&i);
		printf("是否继续？");
		getchar();
		scanf("%c",&go);
		then->number=i;
		now->next=then; 
		now=now->next;
	}
	now->next=NULL;
	return ago;
}
int main(){
	struct point *p;
	p=creat();
	while(p->next){
		printf("%d\n",p->number);
		p=p->next;
	}
	return 0;
}
