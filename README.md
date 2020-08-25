# study
（面试题 02.02. 返回倒数第 k 个节点）
（实现一种算法，找出单向链表中倒数第 k 个节点。返回该节点的值）
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     struct ListNode *next;
 * };
 */


int kthToLast(struct ListNode* head, int k){
    int i=1;
    struct ListNode*now;
    now=head;
    for(;now->next!=NULL;i++){
        now=now->next;
    }
    i-=k;
    while(i){
        i--;
        head=head->next;
    }
    return head->val;
}

