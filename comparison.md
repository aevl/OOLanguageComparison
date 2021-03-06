### 1. Language purpose/genesis
 ##### Why was the language created?
 Java: Java was created to replace C/C++, be more portable, and enable creation of web applications [Oracle](http://www.oracle.com/technetwork/java/javase/overview/javahistory-index-198355.html)  
 C#: C# was developed with C/C++ in mind to help programmers move to a more portable platform.
 ##### What problems was the language trying to address?
 Java: Java was an attempt to solve problems in operating in a distributed computing enviroment by making itself available to multiple systems instead of just one.  
 C#: C# addressed the problems of C/C++ not being portable.
 ##### Is the language a reaction to a previous language or a replacement for another language?
 Java: Java was meant to act as a replacement for C/C++  
 C#: C# isn't so much a replacement as an extension of C/C++   

### 2. Unique features of the language
 ##### Does the language have any particularly unique features?
 Java: Has no pointers.  
 C#: Is not unique in that it is derived from it's predecessors.  

### 3. Name spaces
 ##### How are name spaces implemented?
 Java: Packages in Java cannot be nested. One source file can only have one package statement.  
 ```
 using System;
 ```   
 C#:    
 ```
 namespace namespace_name
{
   // code declarations
}
```  
 ##### How are name spaces used?
 Java: Packages are used to organize files or public types to avoid type conflicts  
 C#: Namespaces are used to organize programs  

### 4. Types
 ##### What types does the language support?
 Java: Primitive data types aren't objects. There is no primative string.   
 C#: Primitive data types are objects. Value type variables can be assigned a value directly. They are derived from the class System.ValueType. The value types directly contain data. Some examples are int, char, and float, which stores numbers, alphabets, and floating point numbers, respectively. There is a primitive string.  [Microsoft](https://msdn.microsoft.com/en-us/library/ms173104.aspx)
 ##### Are both reference and value types supported?
 Java: Java manipulates objects by reference but doesn't pass method arguments. It only passes values.   
 C#: Objects aren't passed at all. Objects are passed by value. A reference type cannot contain a null.  
 ##### Can new value types be created?
 Java: You can create a new value type.  
 C#: You cannot derive a new value type in C# however you can use structs.

### 5. Classes
 ##### Defining
 Java: A class is nothing but a blueprint or a template for creating different objects which defines its properties and behaviors. Java class objects exhibit the properties and behaviors defined by its class. A class can contain fields and methods to describe the behavior of an object.  
 C#: A class is a construct that enables you to create your own custom types by grouping together variables of other types, methods and events. A class is like a blueprint. It defines the data and behavior of a type. If the class is not declared as static, client code can use it by creating objects or instances which are assigned to a variable. The variable remains in memory until all references to it go out of scope. At that time, the CLR marks it as eligible for garbage collection. If the class is declared as static, then only one copy exists in memory and client code can only access it through the class itself, not an instance variable. For more information, see Static Classes and Static Class Members.
 ##### Creating new instances
 Java: Declare a class with the "class" keyword.  
 C#: Declare a class with the "class" keyword.  
 ##### Constructing/initializing
 Java: Access modifiers are used, including: Default, Public, Protected, Private. Constructors do not have a return type.    
 C#: Access modifiers are used, including: Public, Private, Protected, Internal. When a class or struct is created, its constructor is called. Constructors have the same name as the class or struct, and they usually initialize the data members of the new object. [Microsoft](https://msdn.microsoft.com/en-us/library/ms173115.aspx)   
 ##### Destructing/de-initializing
 Java: Because of the garbage collection, there is no ability to use a destructor.   
 C#: Destructos cannot be defined in structs, they are only used with classes. A class can only have one destructor and they cannot be inheirited or overloaded.  

 ### 6. Instance reference name in data type (class)
C#: this  
Java: this   

### 7. Properties
 Java: Getters and setters are written by the programmer  
 ```
 public class Month {
   private int month;

   public int getMonth(){
     return month;
   }
   public void setMonth(value){
     month = value;
   }
 }
 ```
 C#: getters and setters are written by the programmer  
 ```
 public class Month {
   private int month = 7; //Backing store

   public int Month {
     get {
       return month;
     }
     set {
       month = value;
     }
   }
 }
 ```
 ##### Backing variables?
 Java: No backing variables.  
 C#: As in the above example, a private field that stores the data exposed by a public property is called a backing store or backing field. Without them, the getter/setter would infinitely self-reference.  

 ##### Computed properties?
 Java: Not applicable.  
 C#: Has computed properties which computes a value rather than store them.  

### 8. Interfaces / protocols
Java: Uses an interface which is a referance type of a collection of methods that a class implements sucj as abstrat methods, constsants, default methods, static methods, and nested types.  
C#: Uses an interface which only contains the signature of methods, and a class implements them.  

### 9. Inheritance / extension
Java: Inheritance is when a subclass is derived or extended from a super class. This means the subclass inheritas all the members of the super class.  
C#: Built upon inheritance and the ability to inherit subclasses from super classes.  

### 10. Reflection
Java: Used to inspect classes, interfaces, and methods at runtime without knowing the names of them at complie time. Can instantiate new objects, invoke methods, and get/set variables.  
C#: Used to dynamically create an instance to types, get the type from an existing object and invoke its methods and fields, or bind types to an existing oject. Example below:  

```
int i = 42;  
System.Type type = i.GetType();  
System.Console.WriteLine(type);  
 ```

### 11. Memory management
 ##### How is it handled?
 Java: Garbage Collector   
 C#: Garbage Collector  
 ##### How does it work?
 Java: As long as an object is being referenced, the JVM considers it alive. Once an object is no longer referenced and therefore is not reachable by the application code, the garbage collector removes it and reclaims the unused memory.  
 C#: When the garbage collector performs a collection, it checks for objects in the managed heap that are no longer being used by the application and performs the necessary operations to reclaim their memory.
 ##### Garbage collection?
 Java: Yes.  
 C#: Yes  
 ##### Automatic reference counting?
Java: No.  
C#: No.  
### 12. Comparisons of references and values
 ##### How are values compared? (i.e. comparing two strings)
 Java: Primative data types are compared using == while objects are compared using .equals()

### 13. Null/nil references
 ##### Which does the language use? (null/nil/etc)
 Both Java and C# use null.

 ##### Does the language have features for handling null/nil references?
 Java: Has null-ignore invocation and null-safe types.  
 C#: Has a null-conditional operator that tests for null before performing member access.

### 14. Errors and exception handling
Both Java and C# have exception handling that is implemented using try-catch blocks

### 15. Lambda expressions, closures, or functions as types
Java: Lambda expressions reresented as objects, and are bound to a functional interface. A closure is a block of code that can be refereced with access to variables in scope.  
C#: An annonomous function used to create delegates. Used to write local functions that can be passed as arguments, or returned as values from  function. A closure is an annonomous method, and attached to a parent method. The parent method can be referenced in the annonomous method.

### 16. Implementation of listeners and event handlers
Java: The EventHandler class provides support for dynamically generating event listeners whose methods execute a simple statement involving an incoming event object and a target object.  The listeners generated are used to the constantly check for changed in the application and report then to the handler.  
```
myButton.addActionListener(
    (ActionListener)EventHandler.create(ActionListener.class, frame, "toFront"));

myButton.addActionListener(new ActionListener() {
    public void actionPerformed(ActionEvent e) {
        frame.toFront();
    }
});

```
C#: In C#, events are members of the publisher class.  Also in C# there are Trace Listeners instead over Trace messages are received by listeners. The purpose of a listener is to collect, store, and route tracing messages. Listeners direct the tracing output to an appropriate target, such as a log, window, or text file.  
```
window.ClickedEvent += MyEventHandler;

	
button1.Click += delegate(System.Object o, System.EventArgs e)
                  { System.Windows.Forms.MessageBox.Show("Click!"); };  
```


### 17. Singleton
Java: Singleton limits the class to a single one that controls access to resources such as databases and sockets. Implemented with a private constructor, and a static accessor method. Uses lazy instances, and is thread safe.    
C#: A class that only allows an instance of itself to be created. The instance is created inside the Instance property method, and can create subclasses from it. Can be made thread safe, and lazily instantiated.  

### 18. Procedural programming
 ##### Does the language support procedural programming?
 Procedural programming is not supoorted in Java or C#.

### 19. Functional programming
 ##### Does the language support functional programming?
Java: You could.  
C#: Yes  
```
final Array<Integer> a = array(1, 2, 3);
final Array<Integer> b = a.map(i -> i + 42);
arrayShow(intShow).println(b); // {43,44,45}

// combine into a single step
arrayShow(intShow).println(array(1, 2, 3).map(i -> i + 42));
```

### 20. Multithreading
 ##### Threads or thread-like abilities
 Java: Yes  
 C#: Yes
 ##### How is multitasking accomplished?
 Java: Multitasking is a process of executing multiple tasks simultaneously. We use multitasking to utilize the CPU. Multitasking can be achieved by two ways: Process-based Multitasking(Multiprocessing) and Thread-based Multitasking(Multithreading)  
 C#: The most reliable way to create a multithreaded application is to use the BackgroundWorker component. This class manages a separate thread dedicated to processing the method that you specify  
