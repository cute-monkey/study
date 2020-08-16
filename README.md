# study（链表，插入姓名）
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
	
	printf("请输入103寝室成员列表:");
	scanf("%s",p);
	strcpy(head->name,p);
	getchar();
	number=head;
	
	printf("就这？   ");
	scanf("%c",&a);
	while(a!='n'){
		
	printf("请继续输入103寝室成员列表:");
	scanf("%s",p);
	getchar();
	
	now=(struct student*)malloc(sizeof(struct student));
	strcpy(now->name,p);
	
	number->next=now;
	number=number->next;
	
	printf("就这，就这？！  ");
	scanf("%c",&a);
	
	}
	number->next=NULL;
	return head;
}
void insert(struct student*p){
	struct student *ago,*now;
	int position;
	char a[10];
	ago=(struct student*)malloc(sizeof(struct student));
	now=p;
	printf("你是不是忘了谁？ ");
	scanf("%s",a);
	strcpy(ago->name,a);
	getchar();
	printf("他应该在哪个位置呢  ");
	scanf("%d",&position);
	if(position>0){
	
	while(position>1){
		now=now->next;
		position--;
	}
	ago->next=now->next;
	now->next=ago;
	}else{
		p=ago;
		ago->next=now;
	}
	printf("103寝室的成员地位为：\n");
	while(1){
		printf("%s \n",p->name);
		if(p->next!=NULL){
			p=p->next;
		}else{
			break;
		}
	}
}
int main(void)
{
	struct student *p,*q;
	int position;
	p=creat();
	q=p;
	while(1){
		printf("%s \n",p->name);
		if(p->next!=NULL){
			p=p->next;
		}else{
			break;
		}
	}
	insert(q);
}
