
<!--- Binary Tree
--->
### 1. [Welcome](https://github.com/moscarelloscott/moscarelloscott/blob/main/CSE212.md) 2. [stack](https://github.com/moscarelloscott/moscarelloscott/blob/main/stack.md) 3. [linked list](https://github.com/moscarelloscott/moscarelloscott/blob/main/linkedlist.md)
# 4. [Binary Tree]

    Unlike the stack and Linked List, Binary Trees are Non-Linear, 
    they still use Nodes like the Linked List but do not have a head or tail, 
    instead the tree will have a single root at the top and children or leaves 
    at the bottom of the tree. A leaf is any node that does not have a child,
    so in this diagram we have 3 leaves.
    
    Binary Trees are good to use when searching for data, the trees have the ability 
    to insert, delete and traverse  the stored data.
    
   <img src="images/binary1.png" width= "45%" height="25%">  <img src="images/binary2.png" width= "45%" height="25%">
   
    In the example above #1 is a parent of #2 and # 2 is the child of #1, however # 2 is also the parent of #3
    When populating the Tree, the top node is always the ROOT, all the nodes to the left of the root will
    be smaller than the roots data and the nodes to the right will be larger than the root.
    This is also true for placing the children after the parent, notice #1 "24" is larger than the root of "20" 
    so it is placed in the node to the right, #2 "28" is larger than the parent node #1 "24, so it is placed
    to the right however #3 "23 is smaller than the parent #2 "28 so it is placed to the left of #2.
________________________________________________________________

    Just like the Linked List we must make a CLASS NODE for the Binary tree along with a CONSTRUCTOR function.
    Notice in the Constructor we assign a left and right node to store data of none for now.
    
~~~Python
    #Binary Tree
    #Start by creating a Class Node
 class Node:
     #Constructor
     def __init__(self, data):
            self.left = None
            self.right = None
            self.data = data
~~~
    Simple function to only fill the root of the tree by inputting 
    root = Node(10) and then call the function root.PrintTree1()
~~~Python
     def PrintTree1(self):
            print(self.data)   
~~~
    Here we are making a traversing tree placing the data into a column 
    with the smallest ontop and largest on the bottom
~~~Python
    #traversing Tree
     def insert(self, data):
        if self.data:
            if data < self.data:
                if self.left is None:
                    self.left = Node(data)
                else:
                    self.left.insert(data)
            elif data > self.data:
                if self.right is None:
                    self.right = Node(data)
                else:
                    self.right.insert(data)
            else:
                self.data = data
~~~
    The Inorder tree also runs from smallest to largest 
    but in a row instead of a column
~~~Python
                
        #Inorder TREE
        def PrintTree(self):
            if self.left:
            self.left.PrintTree()
        print(self.data)
        if self.right:
            self.right.PrintTree()
        def InOrder(self, root):
            res = []
            if root:
                res = self.InOrder(root.left)
                res.append(root.data)
                res = res + self.InOrder(root.right)       
            return res   
~~~
    
    Here we populate the tree and print out the data by calling the corasponding function
    
~~~Python
   print("\n___________input and output code_______________\n")   
   root = Node(10)
   root.PrintTree1()
   print("\nTraversing")
   root = Node(20)
   root.insert(16)
   root.insert(24)
   root.insert(3)
   root.insert(18)
   root.insert(28)
   root.insert(23)
   root.insert(25) 

~~~ 
                         20
                      /       \
                     16        24
                    /  \      /   \
                   3    18         28
                                  /   \
                                 23    
                                   \
                                     25

~~~Python
   
   root.PrintTree()
   print("\nInOrder")
   root = Node(20)
   root.insert(16)
   root.insert(24)
   root.insert(3)
   print(root.InOrder(root))
   print("\n____________Ending of code__________________")  
 ~~~
                                   20
                                  /   \
                                 16    24
                                /
                               3
                                 
                              
___________________________________________________________________________________
Now create a tree that will output  six numbers in a row and six numbers in a column
both with the same root data and a leaf on the right side but the rest of the data
must be different between the two tree types.

[VIDEO](https://moscarelloscott.github.io/project/index.html)
