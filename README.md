class node:
    def __init__(self,data):
        self.data=None
        self.next=None
        self.prev=None
class Doubly_ll:
    def __init__(self):
        self.head=None
    def push(self,newval):
        newnode=node(newval)
        newnode.next=self.head
        if self.head is not None:
            self.head.prev=newnode
        self.head=newnode
    def printlist(self,node):
        while(node is not None):
            print(node.data)
            last=None
            node=node.next
dll=Doubly_ll()
dll.push(8)
dll.push(10)
dll.push(14)
dll.printlist(dll.head)
