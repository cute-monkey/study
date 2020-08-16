# study（链表：学生姓名）
#include<stdio.h>
#include<stdlib.h> 
#include<string.h>
struct student{
	char name[10];
	struct student *next;
};
struct student *creat(){
	struct student *head,*number,*now;
	char p[10],a;
	
	head=(struct student*)malloc(sizeof(struct student));
	
	printf("请输入学生的名字：");
	scanf("%s",p);
	strcpy(head->name,p);
	getchar();
	number=head;
	
	printf("是否继续：");
	scanf("%c",&a);
	while(a!='N'){
		
	printf("请输入学生的名字：");
	scanf("%s",p);
	getchar();
	
	now=(struct student*)malloc(sizeof(struct student));
	strcpy(now->name,p);
	
	number->next=now;
	number=number->next;
	
	printf("是否继续：");
	scanf("%c",&a);
	
	}
	number->next=NULL;
	return head;
}
int main(void)
{
	struct student *p;
	p=creat();
	while(1){
		printf("%s \n",p->name);
		if(p->next!=NULL){
			p=p->next;
		}else{
			break;
		}
	}
	
}
