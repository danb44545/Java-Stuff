You need to specify a Main-Class in the jar file manifest. 
Oracle's tutorial contains a complete demonstration, but here's another one from scratch. You need two files: 
Test.java: 
public class Test
{
    public static void main(String[] args)
    {
        System.out.println("Hello world");
    }
} 
manifest.mf: 
Manifest-version: 1.0
Main-Class: Test 
Note that the text file must end with a new line or carriage return. The last line will not be parsed properly if it does not end with a new line or carriage return. 
Then run: 
javac Test.java
jar cfm test.jar manifest.mf Test.class
java -jar test.jar 
Output: 
Hello world 
