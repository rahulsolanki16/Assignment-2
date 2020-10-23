# ASSIGNMENT-2
#DATA STRUCTURES ASSIGNMENT-2 DOUBLE LINKED LIST

class Node:    
    def __init__(self,data):    
        self.data = data;    
        self.previous = None;    
        self.next = None;    
            
class DoublyLinkedList:       
    def __init__(self):    
        self.head = None;    
        self.foot = None;      
    def addNode(self, data):       
        newNode = Node(data);     
        if(self.head == None):    
            self.head = self.foot = newNode;    
            self.head.previous = None;       
            self.foot.next = None;    
        else:    
            self.foot.next = newNode;    
            newNode.previous = self.foot;     
            self.foot = newNode;    
            self.foot.next = None;    
    def display(self):    
        current = self.head;    
        if(self.head == None):    
            print("List is empty");    
            return;    
        print("Nodes of doubly linked list: ");    
        while(current != None):       
            print(current.data),;    
            current = current.next;    
                
dList = DoublyLinkedList();      
dList.addNode(1);    
dList.addNode(2);    
dList.addNode(3);    
dList.addNode(4);    
dList.addNode(5);       
dList.display()
