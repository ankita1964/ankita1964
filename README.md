//The attached code merges two Linked List such that the new Linked List still remains sorted.
node* merge(node *a,node *b){
    if(a==NULL){
        return b;
    }
    else if(b==NULL){
        return a;
    }
    node *c;
    if(a->data < b->data){
        c = a;
        c->next = merge(a->next,b);
    }
    else{
        c = b;
        c->next = merge(a,b->next);
    }
    return c;
}
