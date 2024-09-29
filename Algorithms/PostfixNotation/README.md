# Postfix notation

**Postfix notation** is a mathematical notation in which every operator follows all of its operands. 
It is also known as Reverse Polish Notation (RPN).

The expression of the form “a b operator” (ab+) i.e., when a pair of operands is followed by an operator.

### How it works:

Iterate the expression from left to right and keep on storing the operands into a stack. Once an operator is received, 
pop the two topmost elements and evaluate them and push the result in the stack again.

**Consider the expression: exp = *'2 3 1 * + 9 -'***

1. Scan 2, it’s a number, So push it into stack. Stack contains ‘2’.

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20230327162636/img1drawio.png">
</p>

2. Scan 3, again a number, push it to stack, stack now contains ‘2 3’ (from bottom to top) 

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20230327162656/img2drawio.png">
</p>

3. Scan 1, again a number, push it to stack, stack now contains ‘2 3 1’

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20230327162713/img3drawio.png">
</p>

4. Scan *, it’s an operator, pop two operands from stack, evaluate them and push the result back to stack, stack now contains ‘2 3 * 1 = 6’

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20230327162736/img4drawio.png">
</p>

5. Scan +, it’s an operator, pop two operands from stack, evaluate them and push the result back to stack, stack now contains ‘6 1 + 3 = 9’

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20230327162804/img5drawio.png">
</p>

6. Scan 9, it’s a number, push it to stack, stack now contains ‘9 9’

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20230327162956/img6drawio.png">
</p>

7. Scan -, it’s an operator, pop two operands from stack, evaluate them and push the result back to stack, stack now contains ‘9 9 - 9 = 0’

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20230327163018/img7drawio.png">
</p>

8. There are no more elements to scan, we return the top element from the stack (which is the only element left in a stack).

**So the result becomes -4.**

### Complexity

The time complexity of the postfix notation is O(n) where n is the number of elements in the expression.

### Implementation

- **[PostfixNotation.ipynb](PostfixNotation.ipynb)** - The main implementation of the Postfix Notation algorithm in Python.