# Polymotphism
# Overloading
Overloading is the mechanism to have more than one method with same name but with different signature (parameters). A method can be overloaded on the basis of following properties

Have different number of parameter
  Having same number of parameters but of different type
  Having same number and type of parameters but in different orders
  A method cannot be overloaded on the basis of

Different return type
  Different access modifier
  Normal and optional parameters
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
