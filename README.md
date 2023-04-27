# OCAJP-8-IZO-808-
##Random notes for IZO-808 exam concepts

1. After continue/break statement, we cannot write any statement directly inside loop, otherwise we will get compile time error saying unreachable statement. Here check braces carefully
2. It sorts numbers before letters and uppercase letters before lower case letters
3. Arrays Class 	deepEquals(Object[] a1,Object a2[])
4. When using throws, we can use superclass exception of the enclosing method exception, so here throws an IOException is legal.But it throws FileNotFoundException. So in the main method, catch block with FileNotFoundException executes.
5. Method code throws a NullPOInterExc but the catch block for classcastexception can’t catch the nullpointerexcption. So final block is executed then control is return to the main method. NOTE: final block followed by runtimeExcetpion is not printed. Only final block thing will be printed.
6. Method arguments and inside the method var reference should be different, if it’s same, we will get compile time error.
7. Loops careful with conditions and post/pre increments/decrements
8. We can’t use a conditional clause with just else(true/false). for if(true/false) and else if(true/false)
9. Read the question, before going for statement or answers
10. Overriding methods can change the return type only within the bounds of covariant returns, it simply means that overririding methods can return a subtype of the return type of superclass.
11. Java 8, static methods are allowed in the Interface
12.  print() compile time error println() no compile error in the printStream class
13.  int[2]={1,2,3} This code fails to compile due to an error at line 7, array constants can only be used in initializers. So we can’t use {1,2,3}.
14. /* text */ - The compiler ignores everything from /* to */
15. // text - The compiler ignores everything from // to the end of the line.
16. Be clear with variable scope like method level, class level, instance level, 
17. If we use a variable for the case, it needs to be a compile time constants.
18. 

