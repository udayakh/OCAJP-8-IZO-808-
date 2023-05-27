# OCAJP-8-IZO-808-
##Random notes for IZO-808 exam concepts

1. After continue/break statement, we cannot write any statement directly inside loop, otherwise we will get compile time error saying unreachable statement. Here check braces carefully.
2. Collections.sort methods sorts numbers before letters and uppercase letters before lower case letters
3. Arrays Class have deepEquals(Object[] a1,Object a2[]) method
4. When using throws, we can use superclass exception of the enclosing method exception, so here throws an IOException is legal.But it throws FileNotFoundException. So in the main method, catch block with FileNotFoundException executes.
    public static void main(String[] args) throws FileNotFoundException {
           //throw new IOException(); this line won't work, it should be handled like below
            try {
                           throw new IOException();
            } catch (IOException e) {
            }
        }
5. Method code throws a NullPOInterExc but the catch block for classcastexception can’t catch the nullpointerexcption. So final block is executed then control is return to the main method. NOTE: final block followed by runtimeExcetpion is not printed. Only final block thing will be printed.
6. In the Method overloading: Method arguments and inside the method var reference should be different, if it’s same, we will get compile time error.
7. Loops careful with conditions and post/pre increments/decrements
8. We can’t use a conditional clause with just else(true/false). for if(true/false) and else if(true/false)
9. Read the question, before going for statement or answers
10. Overriding methods can change the return type only within the bounds of covariant returns, it simply means that overririding methods can return a subtype of the return type of superclass.
11. Java 8, static methods are allowed in the Interface
12.  Empty print method(System.out.print()) will cause compile time error println() no compile error in the printStream class
13.  int[2]={1,2,3} This code fails to compile, array constants can only be used in initializers. So we can’t use {1,2,3}.
14. /* text */ - The compiler ignores everything from /* to */
15. // text - The compiler ignores everything from // to the end of the line.
16. Be clear with variable scope like method level, class level, instance level, 
17. If we use a variable for the case, it needs to be a compile time constants.
18. StackOverflow,ArrayIndexOutOfBoundException,NullPointerException, ArrayIndexOutOfBoundsException, ClassCastException,.. thrown by JVM
19. A fully qualified means using the completed package details when acessing java class.
20. We can have methods with same name and same scope in the class.
21. if your passing int literal to the method, but method expecting short literal, compiler will fail, to pass this you need to cast.(short)10.
22. all the wrapper cllass are instaceof Object class.
23. carefull with className/variable identifier, sometimes they will give as switch(java keywords)
24. Before going to pre/post increment check var type.
25. int a[]=new int[3]; now 3 elements set to zero.
26. all good s/w design will go for high cohesion and low coupling
Cohesion refers to the degree to which the elements of a module/class belong together, it is suggested that the related code should be close to each other, so we should strive for high cohesion and bind all related code together as close as possible. It has to do with the elements within the module/class.
Coupling refers to the degree to which the different modules/classes depend on each other, it is suggested that all modules should be independent as far as possible, that's why low coupling. It has to do with the elements among different modules/classes.

27. -,+ are the unary operator
28. while Overriding methods, we an't throw new or broader checked exceptions, but we can throw new or broader unchecked exception
29. int x=10; static int y=x; will give compiletime error.static var can't access instance var value.
30. Integer class caches values between -128 to 127, when your comparing two interger with ==.
    Short,Integer and Long from -128 to 127.
31. int var will hava valeus from -2147483648 to 2147483647, if variable values reaches to min value, if you try to decremen it, it will shift to the max value.
32. Wrapper(Integer) Increment will cause NullpointerException at runtime.
33. We can't use any access modifier than public and default with top level classes.
34. The enum constructor must be either private or package scope(default). you cannot use public or protected constructors for a java enum.
35. || and && are called short circuiting operatiors bcz if, while evaluting a logical expression. at any stage, the value of the whole expression can be determined without evaluting the rest of the expression. then the remaining sub-expression are not evaluted.
36.  public is least restrictive and private is most restrivctive
37. Two dimensitonal array means it is basically an array of arrays.
38. An instace member belongs to a single instance, not the class as a whole. an instance is a member variable or a memmber method that belongs to a specific object intance.
39. A try statment must always have a catch associated with it.
40 . All mathematical(%,...) operators evaluate all the operands
41. ##Rules for a switch statement
    Only String, byte, char, short, int, (and their wrapper classes Byte, Character, Short, and Integer), and enums can be used as types of a switch variable. String is allowed since Java 7.
    
    The case constants must be assignable to the switch variable. For example, if your switch variable is of class String, your case labels must use Strings as well.
    The switch variable must be big enough to hold all the case constants. For example, if the switch variable is of type char, then none of the case constants can be greater than 65535 because a char's range is from 0 to 65535. For example, the following will not compile because 200 cannot be assigned to the variable b, which can only hold values from -128 to 127.
    
    byte b = 10;
    switch(b){
        case 100 : System.out.print(100); //OK
        case 200 :  System.out.print(200); //will not compile
    }
    
    All case labels should be COMPILE TIME CONSTANTS. This means, you can have literals such as 'a', 5, 10, or a final variable, the value of which is computed at compile time such as int I = 2*3; For example, the following is valid:
    
    int x = 10;
    final int I = 2*3;
    switch(x){ 
       case I : System.out.println(x); 
       //this is valid because I is a compile time constant
    }
    
    No two of the case constant expressions associated with a switch statement may have the same value.
    The default label is optional and at most one default label may be associated with the same switch statement.

42. Abstract methods are meants to be overrirdent in the subclass.

43 . ##Boolean
    Boolean class has two constructors - Boolean(String) and Boolean(boolean)
    Boolean class has two static helper methods for creating booleans - parseBoolean and valueOf.
    Boolean.TRUE or Boolean.FALSE static members 

44. In the no-arg constructor block,if you use this(); method, it will cause Recursive constructor invokation
45. java keyword, can't be used as case labels
46. boolean b=false;
    int i=1;
    do{
    ++i;
     }while(b =!b);
    soup(i);
     remember here: first iteration b is true(b=true(!false)) and second iteration be is false(b=false(!true))
47. case full with variable declaration for loop statment, check if variable declared or not
   ex: int j=0;
   for(int i=10,j=2;J<i;i++,j++)//compiler error
   
48. break without a label, can occur only in a switch,while,do or for statements.
49. LocalDate,LocalTime and LocalDateTime are immutable 
50.  StringBuilder sb = new StringBuilder("SpaceStation");
     sb.delete(5, 6).insert(5, " S").toString().toUpperCase();
     System.out.println(sb);
    sb - > "SpaceStation"
    sb.delete(5, 6) -> "Spacetation"
    sb.insert(5, " S") -> "Space Station"
    sb.toString() -> Creates a new String object "Space Station"
    "Space Station".toUpperCase() -> Creates another String object "SPACE STATION" but the String object is not referred and used
51.  final int i1 = 1;
            final Integer i2 = 1;
            final String s1 = ":ONE";
            
            String str1 = i1 + s1;
            String str2 = i2 + s1;
            
            System.out.println(str1 == "1:ONE");
            System.out.println(str2 == "1:ONE");
    Please note that Strings computed by concatenation at compile time, will be referred by String Pool during execution. Compile time String concatenation happens when both of the operands are compile time constants, such as literal, final variable etc.
    Whereas, Strings computed by concatenation at run time (if the resultant expression is not constant expression) are newly created and therefore distinct
    For the statement, String str1 = i1 + s1;, i1 is a final variable of int type and s1 is a final variable of String type. Hence, `i1 + s1` is a constant expression which is computed at compile-time and results in String literal "1:ONE".
    This means during compilation, Java compiler translates the statement
    String str1 = i1 + s1; to
    String str1 = "1:ONE";
    As "1:ONE" is a String literal, hence at runtime it will be referred by String Pool.
    On the other hand, for the statement, String str2 = i2 + s1;, `i2 + s1` is not a constant expression because i2 is neither of primitive type nor of String type, hence it is computed at run-time and returns a non-pool String object "1:ONE".
    As, str1 refers to String Pool object "1:ONE", hence `str1 == "1:ONE"` returns true, whereas str2 refers to non-Pool String object "1:ONE" and hence `str2 == "1:ONE"` returns false.
52. Java doesn't allow to catch specific checked exceptions if these are not thrown by the statements inside try block.
    catch(FileNotFoundException ex) {} causes  compilation error in this case as System.out.println(1); will never throw FileNotFoundException.
    NOTE: Java allows to catch Exception type. catch(Exception ex) {} will never cause compilation error.
    
53. In the super class have static method, if extend that class created same method signature. 
    Ex; A a = new B();a.test(); // it will call parent test method. Because static method is method hidden.
54.  StringBuilder s1 = new StringBuilder("Java");
                    String s2 = "Love";
                    s1.append(s2);
                    s1.substring(4);// it will create a new String Object, it will not modify s1 object
                    int foundAt = s1.indexOf(s2);
                    System.out.println(foundAt);//4
55. minus operator used after string concatanation. it will cause compile time error
psvm(Strings[] args){
    int x=10,y=12;
    soup("output is "+x-y);
    }                     
56. below sop is unreachable 
String s[]={"a","b"};
    for(String str:s){
    continue;
    soup(str);
    }     
57. specific converwions of primitive types
 bye to short int long float double
 short to init long float double
  chat to int long float double
 int to long float double
 long to float double
 float to double
 
58
 

    
    
