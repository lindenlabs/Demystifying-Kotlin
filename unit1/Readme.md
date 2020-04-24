# Intro to Kotlin

## Objectives

- Define programming and programming languages.
- Print output to the console.

## Resources
- https://en.wikipedia.org/wiki/Kotlin_(programming_language)

### Documentation
- [Java History](http://papa.det.uvigo.es/~theiere/cursos/Curso_Java/history.html)
- [Oracle's Java Tutorials](https://docs.oracle.com/javase/tutorial/)
- [Print Statements](https://www.cis.upenn.edu/~matuszek/General/JavaSyntax/print-statements.html)
- [Primitive Data Types](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)
- [List of Java keywords (reserved words)](https://en.wikipedia.org/wiki/List_of_Java_keywords)
- [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html)
- [Kotlin style guide](https://kotlinlang.org/docs/reference/coding-conventions.html)

### Programming Environment
- [Java Repl](https://repl.it/languages/java)
- [Kotlin Repl](https://repl.it/languages/kotlin)

## Vocabulary
|Term|Definition|
|:-:|:---------|
|JVM|Java Virtual Machine, a virtual machine that interprets Java bytecode and enables your computer to run it as a program|
|virtual|the opposite of physical|
|virtual machine|a computer that doesn't exist as physical hardware, instead it is "emulated" by software|
|platform|environment in which a piece of software is executed.|
|interopable|(of computer systems or software) able to exchange and make use of information.|


# Workshop

Welcome! 🌻

### What is programming?

Programming is a creative process by which we can instruct a computer in how to do a task.

Why are computers useful?
- They are fast
- They are accurate
- They do not get bored

What are some reasons that programming is useful?

In a basic way, we could summarize programming as:

1. Figuring out, step-by-step, how you would solve a problem.
2. Explaining your solution to the computer in a shared language.

### What is a programming language?

A programming language is a language designed to be read and written by humans and to be interpreted and carried out by computers.

What are some examples of programming languages?

How are the programs we write interpreted and carried out by computers?

### What is Java?

Java is a programming language and computing platform that was released by Sun Microsystems (now Oracle) in 1995.

Java has long been the primary programming language used to develop Android apps.

Java was created to solve a problem: it was the first programming language in which programs could be written to run anywhere, regardless of operating system or microprocessor.

In Java, source code is written in plain text files ending with a `.java` extension.

These files are then compiled by the **javac** compiler into `.class` files containing Java **bytecode** -- the machine language of the Java Virtual Machine. The **java** tool then runs your program with an instance of the JVM tailored to your machine.

![diagram of flow from Java source to machine language](https://docs.oracle.com/javase/tutorial/figures/getStarted/helloWorld.gif)

### What is Kotlin?

Kotlin is a programming language and computing platform released by JetBrains (the same folks who created IntelliJ and Android Studio) in 2011.

From Wikipedia: Kotlin is a cross-platform, statically typed, general-purpose programming language with type inference. Kotlin is designed to interoperate fully with Java, and the JVM version of its standard library depends on the Java Class Library, but type inference allows its syntax to be more concise.

In Kotlin, source code is written in plain text files ending with a `.kt` extension.

In 2017, Google announced support for Kotlin in its Android Studio IDE. On 7 May 2019, Google announced that the Kotlin programming language is now its preferred language for Android app developers.

Kotlin is designed with Java Interoperability in mind. Existing Java code can be called from Kotlin in a natural way, and Kotlin code can be used from Java.

### Exercises

### Java Output

To output a string to the console, use `System.out.println(`**`"some string"`**`)`

```java
public class Hello {
    public static void main(String[] args) {
        // Outputs "Hello, world!" to the console
        System.out.println("Hello, world!");
    }
}
```

Go to [repl.it](https://repl.it/languages/kotlin) and try the same

#### Exercise: Printing to the Console


### Variables & data types

In programming, **variables** are kinds of values that can be stored and manipulated.

A variable's **data type** determines the values it may contain and the operations that may be performed on it. A **primitive data type** is a name for data types that are provided by the language as a basic building block. There are eight primitive data types in Java:

* **boolean** - represents a truth and has only two possible values, `true` or `false`. A boolean can be inverted with the `!` operator. Booleans can also be created by comparing two variables.

```java
boolean isCar = true;
boolean areWeThereYet = false;
boolean answer = 7 > 3;
```

```kotlin
val isCar: Boolean = false
val areWeThereYet: Boolean = false
val answer: Boolean = 7 > 3
```

* **byte** - a small integer between -128 and 127.

* **short** - a small integer between -32,768 and 32,767.

* **int** - an integer between -2<sup>31</sup> and 2<sup>31</sup>-1. In most cases this is the default type used to represent integer values.

* **long** - an integer  between -2<sup>63</sup> and 2<sup>63</sup>-1.

```java
byte myAge = 28;
short activeCitiBikesInNyc = 6603;
int yearsSinceDinosaurs = 65000000;
long humansOnEarth = 7400000000;
```

```kotlin
val myAge: Byte = 28
```

* **float** - a real number, single-precision 32-bit floating point. For our uses, **real numbers** are just numbers that can have decimals in them. For example, 2 is an integer but 2.1 is a real number.

* **double** - a real number, double-precision 64-bit floating point. In most cases this is the default type used to represent decimal values.

```
val percentOfPizza: Float = 33.3
val pi: Double = 3.14159265359
```

* **char** - a single [Unicode](http://unicode.org/charts/) character.


Two strings can be **concatenated** using the ```+``` operator:

```java
String hello = "Hello, " + "world!";
```

[Exercises: Exploring Data Types](exercises.md#data-types)

### Naming & assigning variables

Both Java and Kotlin are **strongly-typed** language, meaning variables are of an explicit type when they are assigned. Use `=` to assign a value to a variable.

```java
String myName = "Ramona";

boolean isSkyBlue = true;

char bang = '!';
```

### Variable naming conventions
Kotlin variables are conventionally named in *lowerCamelCase*: the first letter of each word after the first is capitalized. Variable names should use only ASCII letters and digits.

Good variable names are concise and meaningful. A well-selected name will help to convey your intent to subsequent programmers (including yourself!) who are tasked with reading your code.

```kotlin
// Some good variable names:

val favoriteColor: String

val tacoCount: Int;

val isNewUser:;
```


 What about these?
```kotlin
val thisVariableIsEqualToTwentyThreePointFive: Double = 23.5d

val LOL: Boolean

val HelloWorld: Boolean

val int: Int
```

See the Kotlin Style Guide [section on naming conventions](https://kotlinlang.org/docs/reference/coding-conventions.html#naming-rules) for more detailed guidance here.


### Math & Operators

We can use Java to perform basic arithmetic. The order of operations is just like standard arithmetic: parentheses, exponents, multiplication and division, addition and subtraction (PEMDAS).

```kotlin
// Addition
var result: Int = 4 + 5

// Subtraction
result = result - 1

// Multiplication
result = result * 2

// Division
result = result / 2

result = result + 8

// Modulo: "%" divides one operand by another and returns the remainder as its result.
result = result % 7

// You can also combine the arithmetic operators to create compound assignments:

result += 1

result -= 1

// The Unary operators require only one operand:

result++

++result

result--

--result

```

**Be careful when dividing integers!**  In Java, when you divide an integer by an integer, the answer will be an integer rounded towards zero from the real number value.

```java
// Integer division
int result = 7 / 2; // Evaluates to 3
int result = 3 / 4; // Evaluates to 0

// Double division
double result = 7.0/2.0;
```

| symbol |       use      |
|:------:|:--------------:|
|    +   |    Addition    |
|    -   |   Subtraction  |
|    *   | Multiplication |
|    /   |    Division    |
|    %   |     Modulo     |
|   ++   |    Increment   |
|   --   |    Decrement   |

[Exercises: Math and Arithmetic Expressions](exercises.md#math)

## More printing + Strings

String is the most commonly used class. It represents a "character string", or sequence of characters.

The full documentation for the String class is here: [Kotlin Docs: Strings](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/).

Let's complete some more exercises to experiment with Strings and printing:

[Exercises: Working with Strings](exercises.md#strings)
