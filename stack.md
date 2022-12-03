<!---
moscarelloscott/moscarelloscott is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
 
### 1. [Welcome](https://github.com/moscarelloscott/moscarelloscott/blob/main/CSE212.md)  3. [linked list](https://github.com/moscarelloscott/moscarelloscott/blob/main/linkedlist.md) 4. [Binary Tree](https://github.com/moscarelloscott/moscarelloscott/blob/main/binarytree.md)
# 2. [stack](https://github.com/moscarelloscott/moscarelloscott/blob/main/stack.md)
 ## *Stack Introduction
	Python Stacks what is stack?
		 To start with it is a linear array structure of nodes stacked on top of each other that 
		 operate in the last in first out pattern or LIFO
		 Imagine a can of three tennis balls, the first one you put in goes to the bottom
		 then the second and finally the third.
		 Now if you want to get the first ball out of the can you will need to remove the third,
		 then the second and finally the first. 
	Why do we use stack?
		 Stack is the easier and more simple method to hold data out of the three example we are 
		 working with in this tutorial, it has a strict organizational ttern that must be follow 
		 and cannot pull objects from the bottom or middle of the stack unlike the other methods 
		 which can pull from any place in their array.
		 So,stack is best used when we want to maintain an organized directional flow.
		 stack is a great method for backtracking step by step from the end to the beginning.
	How do we add and remove objects?
		 The push operation is used to add objects by using the append command
		 The pop operation is used to remove the last object entered into the stack by using
		 the pop command.
		 In the example code we have an array called stackTutoral that starts out empty, to push
		 an object into this array we need to first use the arrays name followed by a period 
		 then the command to append and finally the object inside parentheses we want to enter
		 for example: arrayName.append(object desired)
		 If we wish to remove an object, we need to follow the same structure except changing
		 append to pop and leaving the parentheses empty IE: arrayName.pop()

    *Stack interger Example code    
~~~Python
          print("Stack Coding")
          stackTutoral = []
          print("with an empty array nothing will print")
          print(stackTutoral)
          print("by using append we will insert the number 1 into the array")
          stackTutoral.append(1)
          print(stackTutoral)
          print("again using append to insert the number 2")
          stackTutoral.append(2)
          print(stackTutoral)
          print("using pop we can remove the last object in the array")
          stackTutoral.pop()
          print(stackTutoral)
          cont = input("press enter to return to main menu")
          start()        
~~~
    *Stack string example code
~~~Python
	    stackString = []
	    print("enter a word: ")
	    a = input()
	    print("enter a word: ")
	    b = input()
	    stackString.append(a + b)
	    print(stackString)
~~~    
    *Stack Problem to solve
    rewrite the int code with the user being able to input 3 numbers of their choice.
    rewrite the string code to output "Python is Great"
    

[VIDEO](404)
