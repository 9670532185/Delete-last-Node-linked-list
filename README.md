# Delete-last-Node-linked-list
public class DelLN {
    public Node Delnode(Node root)
    {
        if(root==null || root.next==null)
        {
            return null;
        }
        Node cur=root;
        Node prev=null;
        while(cur.next !=null)
        {
            prev=cur;
            cur=cur.next;
        }
        prev.next=null;
        return cur;
    }
    public void Print(Node root)
    {
        if(root ==null)
        {
            return ;
        }
        Node current=root;
        while(current!=null)
        {
            System.out.println(current.data);
            current=current.next;
        }
       // return current;
    }
    public static class Node{
        int data;
        Node next;
        Node(int data){
            this.data=data;
        }
    }
    public static void main(String[] args)
    {
      DelLN obj=new DelLN();
      Node root=new Node(2);
      Node root1=new Node(3);
      Node root2=new Node(4);
      root.next=root1;
      root1.next=root2;
      
      obj.Print(root);
      System.out.println();
     obj. Delnode(root);
     obj.Print(root);
    }
    
}
