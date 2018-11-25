# Interview-Preparation-Resources
Here I collect a list of useful resources for preparing for Interviews for the position of Software Engineer and Senior Software Engineer in Java

# DS Algo
 1) External Sorting http://faculty.simpson.edu/lydia.sinapova/www/cmsc250/LN250_Weiss/L17-ExternalSort.htm
# Java Resources
 1) Example of Volataile Keyword https://dzone.com/articles/java-volatile-keyword-0
 2) Producer consumer code https://caveofprogramming.com/java-multithreading/java-multithreading-producer-consumer-blockingqueue-part-7.html
 3) Concurrent HashMap working https://dzone.com/articles/how-concurrenthashmap-works-internally-in-java
 4) PermGen Space Leak https://plumbr.io/blog/memory-leaks/what-is-a-permgen-leak

# DB Resource 
1) Triggers : https://docs.oracle.com/cd/A57673_01/DOC/server/doc/SCN73/ch15.htm
2) Hierarchical Queries : http://mikehillyer.com/articles/managing-hierarchical-data-in-mysql/

# Questions 
https://stackoverflow.com/questions/1855170/when-should-we-use-intern-method-of-string-on-string-literals
https://blog.jooq.org/2013/10/09/sql-trick-row_number-is-to-select-what-dense_rank-is-to-select-distinct/

The serialization runtime associates with each serializable class a version number, called a serialVersionUID, which is used during deserialization to verify that the sender and receiver of a serialized object have loaded classes for that object that are compatible with respect to serialization. If the receiver has loaded a class for the object that has a different serialVersionUID than that of the corresponding sender's class, then deserialization will result in an  InvalidClassException. A serializable class can declare its own serialVersionUID explicitly by declaring a field named serialVersionUID that must be static, final, and of type long:

ANY-ACCESS-MODIFIER static final long serialVersionUID = 42L;
If a serializable class does not explicitly declare a serialVersionUID, then the serialization runtime will calculate a default serialVersionUID value for that class based on various aspects of the class, as described in the Java(TM) Object Serialization Specification. However, it is strongly recommended that all serializable classes explicitly declare serialVersionUID values, since the default serialVersionUID computation is highly sensitive to class details that may vary depending on compiler implementations, and can thus result in unexpected InvalidClassExceptions during deserialization. Therefore, to guarantee a consistent serialVersionUID value across different java compiler implementations, a serializable class must declare an explicit serialVersionUID value. It is also strongly advised that explicit serialVersionUID declarations use the private modifier where possible, since such declarations apply only to the immediately declaring class serialVersionUID fields are not useful as inherited members.

Cohesion and Coupling(https://stackoverflow.com/questions/3085285/difference-between-cohesion-and-coupling)

Cohesion refers to what the class (or module) can do. Low cohesion would mean that the class does a great variety of actions - it is broad, unfocused on what it should do. High cohesion means that the class is focused on what it should be doing, i.e. only methods relating to the intention of the class.

Example of Low Cohesion:

-------------------
| Staff           |
-------------------
| checkEmail()    |
| sendEmail()     |
| emailValidate() |
| PrintLetter()   |
-------------------
Example of High Cohesion:

----------------------------
| Staff                   |
----------------------------
| -salary                 |
| -emailAddr              |
----------------------------
| setSalary(newSalary)    |
| getSalary()             |
| setEmailAddr(newEmail)  |
| getEmailAddr()          |
----------------------------
As for coupling, it refers to how related or dependent two classes/modules are toward each other. For low coupled classes, changing something major in one class should not affect the other. High coupling would make it difficult to change and maintain your code; since classes are closely knit together, making a change could require an entire system revamp.

Good software design has high cohesion and low coupling.


https://www.journaldev.com/1540/decorator-design-pattern-in-java-example

Java 8 

Default Methods and static methods in interface
http://www.kousenit.com/java8/#_functional_interfaces_in_the_code_java_util_function_code_package
https://www.programcreek.com/2014/12/default-methods-in-java-8-and-multiple-inheritance/
