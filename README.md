# Linkedlist-

// creating class 

public class Main { 
// Here Node is the primitive data type 
  Node head;
  // Crearing node class
  class Node {
    String data;
    Node next;
//Creating a constructor

    Node(String data) {
      this.data = data;
      this.next = null;
    }
  }
//Adding the node to the linked list
  public void addList(String data) {
    Node newNode = new Node(data);
    if (head == null) {
      head = newNode;
      return;
    }
    newNode.next = head;
    head = newNode;
  }
//Addding to last node of the linked list

  public void addLast(String data) {
    Node newNode = new Node(data); 
    if (head == null) {
      head = newNode;
      return;
    }
    Node currNode = head;
    while (currNode.next != null) {  // Traverssing till last to check that 
      currNode = currNode.next;
    }
    currNode.next = newNode;
  }
// printing the linked list

  public void printList() {
    Node currNode = head;
    while (currNode != null) {
      System.out.print(currNode.data + " -> ");
      currNode = currNode.next;
    }
    System.out.println("null");
  }
//Debug runner

  public static void main(String[] args) {
    Main list = new Main();
    list.addList("a");
    list.addLast("Three");
    list.printList();
  }
}
