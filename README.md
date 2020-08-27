# study
struct ListNode* oddEvenList(struct ListNode* head){
    if(head==NULL){
        return NULL;
    }
    struct ListNode * now,* then,*nowhead;
    now=head->next,then=head,nowhead=now;
    while(then && then->next&& now&&now->next){       
        then->next=now->next;
        then=then->next;
        now->next=then->next;
        now=now->next;
    }
    then->next=nowhead;
    return head;

}
