# Polymotphism
# Overloading
Overloading is the mechanism to have more than one method with same name but with different signature (parameters). A method can be overloaded on the basis of following properties

1. Have different number of parameter
2. Having same number of parameters but of different type
3. Having same number and type of parameters but in different orders
  
A method cannot be overloaded on the basis of

1. Different return type
2. Different access modifier
3. Normal and optional parameters
 
Some example valid examples:
  
Some example valid examples:

      public List<Customer> FindCustomer(String customer_name)
      {
        // your code
      }
      public List<Customer> FindCustomer(Int32 customer_Id)
      {
        // your code
      }
      public List<Customer> FindCustomer(String customer_name, String city)
      {
        // your code
      }
      public List<Customer> FindCustomer(String customer_name, Int32 customer_Id)
      {
        // your code
      }
      public List<Customer> FindCustomer(String customer_name, String city, String zip)
      {
        // your code
      }

Following are invalid overloading because we can not overload on the basis of different return type

      public List<Customer> FindCustomer(String customer_name)
      {
        // your code
      }
      public Customer FindCustomer(String customer_name)
      {
        // your code
      }
Following are also invalid overloading, because we cannot overload on the basis of access modifier

        public List<Customer> FindCustomer(String customer_name)
        {
          // your code
        }
        private List<Customer> FindCustomer(String customer_name)
        {
          // your code
        }

Following are also not valid, because we cannot overload normal and optional parameter

        public List<Customer> FindCustomer(String customer_name)
        {
          // your code
        }
        private List<Customer> FindCustomer(String customer_name = String.Empty)
        {
          // your code
        }  
        
In the same way we can overload constructor of a class by defining more than one constructor with different parameters which is known as constructor overloading.

It is also called:

1. Early Binding or
2. Compile Time Polymorphism or
3. Static binding


http://www.advancesharp.com/blog/1056/overloading-and-overriding-in-c-with-example

Overriding:
Overriding can be done in derived class, an override method provides a new implementation of a method inherited from parent class.

To override a method in base (parent) class it must be

virtual
abstract
override
We cannot override a base method which is in base class as

non-virtual
static
We cannot use the following modifiers to modify an override method in derived class

new
static
virtual
abstract
Let's see it with example:

public class Square 
{
  public double side;
  // Constructor:
  public Square(double side) 
  {  this.side = x; }

  public virtual double Area() 
  {   return side  * side ;  }
}
Note Area method is defined with virtual so it can be overridden in derived class, now lets derive a class cube from square and override it's Area method

class Cube: Square 
{
   // Constructor:
   public Cube(double side): base(x)    { }
   // Calling the Area base method:
   public override double Area() 
   { return (6*(base.Area())); }
}
It is also called:

Late Binding or
Run Time Polymorphism or
Dynamic binding
Conclusion:
Overloading can be done in same class
Overriding can be done in parent and derived class
Overloading in used when we need same method in same class with different parameters
Overriding is used when we need to redefine a method that has already been defined in parent class (using the exact same signature
Overloading is resolved at compile time
Overriding is resolved at run time
Some commonly asked interview questions:

Q. How’s method overriding different from overloading?

When overriding, we change the method behaviour for a derived class. Overloading simply creating more than one method with the same name but different parameters in same class.

Q. Is the following code correct?

class Program
{
  public static void Main()
  {
    ......
  }
  public void Sum(int N1, int N2)
  {
    var result = N1 + N2;
  }

  public int Sum(int N1, int N2)
  {
    return N1 + N2;
  }
}
ANS: No, If you note, the different is only in the return type. We cannot overload a method, only on the basis of different return type. A method can be overloaded if it have different number of parameters, different types of parameters or sequence of the parameters which change the data type say: method(int i, string x) and other method(string x, int i), it can be overloaded.
