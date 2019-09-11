class Add {
    public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
        ListNode n1 = l1;
        ListNode n2 = l2;
        ListNode r = new ListNode(-1);
        ListNode t = r;
        while(n1 != null || n2 != null){
            if (n1 == null){
                r.val = n2.val;
                n2 = n2.next;
            }
            else if(n2 == null){
                r.val = n1.val;
                n1 = n1.next;
            }
            else{
                int add = n1.val + n2.val;
                int carry = add/10;
                int sum = add%10;
                r.val = sum;
                n1 = n1.next;
                n2 = n2.next;
                //n1.val += carry;
                if (carry > 0){
                    if (n1 == null && n2 == null){
                        n1 = new ListNode(carry);
                    }
                    else if(n1 != null && n2 == null){
                        n2 = new ListNode(carry);
                    }
                    else if (n1 == null && n2 != null){
                        n1 = new ListNode(carry);
                    }
                    else{
                        n1.val += carry;
                    }
                }
                
            }
            if (n1 != null || n2 != null){
                r.next = new ListNode(-1);
                r = r.next;
            }
        }
        return t;
        
    }     
    
}
