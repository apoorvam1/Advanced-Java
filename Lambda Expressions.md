Lambda Expressions introduced in Java 8 fall into the category of Functional Programming. 

What Are Lambda Expressions?
  Lambda expressions are used to represent the idea of Anonymous classes. These are the anonymous methods that are used to implement a functional interface.
  They provide the user/caller of the function the flexibility to define certain set of behavior. We will see how this could be achieved throughs examples in future sections.
  
What are Functional Interfaces? 
  Functional Interfaces are the interfaces that have exactly one abstract method. One very well known functional interface is Runnable. If we observe it has only one method defined. i.e run().
  
Where can they be used?
  - can be used in event listeners
  
How do we create a Lambda Expression?
  A lambda expression overrides the abstract method of a functional interface. 
  Example: 
    Here's is a functional Interface.
    
    @FunctionalInterface
    public interface SampleInterface {
        public void performSum(int a, int b);
    }
    
    Here's a method of a some class that creates a lambda expression to perform sum of 2 numbers.
    
    public void printSum() {
        SampleInterface si = (a, b) -> a + b;
        System.out.println(si.performSum(2, 3));
    }
    
Understanding a Lambda Expression
  Let's consider the same Lambda expression mentioned above, starting with a more detailed version of it. 
  
  1. SampleInterface si = (int a, int b) -> { return a + b; };
     Provide an implementation to the method performSum such that, when 2 arguments a and b of type integer are passed return      the sum of a and b. 
  When we closely observe we see that specifying the argument type is redundant as it'll be enforced by the abstract method     already. Hence comes the more simpler format.
  
  2. SimpleInterface si = (a, b) -> { a + b; };
  
  Single statement lambdas are called as 'lambda expressions'. These come with privilege of not necessarily having curly braces or return statements. But when a lambda has more than one statement, called as 'lambda block' those exceptions are not allowed. 
  

  
  
What are Default Methods?
Default Methods Vs Static Methods


