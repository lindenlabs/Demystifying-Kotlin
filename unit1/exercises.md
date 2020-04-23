Exercises

## What is kotlin

### Q1. kotlin-docs

Find the kotlin documentation online. What is the URL?


### Q2. java-vs-javascript

Explain in a few sentences what the difference is between Java and JavaScript.
<!-- end @acxbank -->


## Java output

<!-- @acxbank first-hello-world -->
### Q3. first-hello-world

```java
public class Hello {
    public static void main(String[] args) {
        // Outputs "Hello, world!" to the console
        System.out.println("Hello, world!");
    }
}
```



1. Print "Hello World" as an output in Kotlin 

2. Accept the user's name as input. Refactor your Hello World code to print "Hello, $name!" where $name is a variable of type String. 

<!-- end @acxbank -->


<!-- @acxbank print-concatenation -->
### Q4. print-concatenation

Given two separate strings "Hello, " and "world!", concatenate them together to print "Hello, world!" to the console.
<!-- end @acxbank -->


<!-- @acxbank hello-world-java-vs-android -->
### Q5. hello-world-java-vs-android

You're probably familiar now with this example, which prints "Hello, world!" to the console:

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

Take a look at the following block of Android code, which displays "Hello, world!" on the screen. What differences do you notice from the code above? What looks the same? *(Try to name at least 3 similarities and 3 differences!)*

```kotlin
public class HelloActivity : Activity() {

    override fun onCreate(savedInstanceState: Bundle) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_hello)

        val myTextView = findViewById(R.id.my_text_view) as TextView
        myTextView.text = "Hello, world!"
    }
}
```
<!-- end @acxbank -->


## Variables & data types


<!-- @acxbank string-vs-char -->
### Q6. string-vs-char

Explain the difference between `char` and `String`.
<!-- end @acxbank -->


## Naming & assigning variables


<!-- @acxbank assigning-variables -->
### Q10. assigning-variables

Assign variables for each of the following pieces of information.

For each one, be sure to choose a suitable data type and a descriptive name!

1. Your name.
2. The first letter of your last name.
3. Your favorite food.
4. The number of days in a week.
5. The number of days in a (non-leap) year.
6. Whether or not the current year is a leap year.
7. The first three digits of pi.
8. How many feet you'd guess there are between the earth and the sun.

<!-- end @acxbank -->


## Math & Operators

<!-- @acxbank integer-vs-floating-point -->
### Q11. integer-vs-floating-point

What is the difference between an integer and a floating-point number?
<!-- end @acxbank -->


<!-- @acxbank math-api -->
### Q12. math-api

Find the Java API for the Math class. Find the method `sqrt()`. What does it do? What is the data type of the parameter it accepts?
<!-- end @acxbank -->


## Strings

<!-- @acxbank string-api-intro -->
### Q13. string-api-intro

Consider the following string:

```java
String hannah = "Did Hannah see bees? Hannah did.";
```

1. What is the value displayed by the expression hannah.length()?

2. What is the value returned by the method call hannah.charAt(12)?

3. Write an expression that refers to the letter b in the string referred to by hannah.

<!-- end @acxbank -->


<!-- @acxbank string-substring -->
### Q14. string-substring

How long is the string returned by the following expression? What is the string?

```java
"Was it a car or a cat I saw?".substring(9, 12)
```
<!-- end @acxbank -->


<!-- @acxbank string-api-intro-2 -->
### Q15. string-api-intro-2

In the following program, called ComputeResult, what is the value of result after each numbered line executes?

```java
public class ComputeResult {
    public static void main(String[] args) {
        String original = "software";
        StringBuilder result = new StringBuilder("hi");
        int index = original.indexOf('a');

/*1*/   result.setCharAt(0, original.charAt(0));
/*2*/   result.setCharAt(1, original.charAt(original.length()-1));
/*3*/   result.insert(1, original.charAt(4));
/*4*/   result.append(original.substring(1,4));
/*5*/   result.insert(3, (original.substring(index, index+2) + " "));

        System.out.println(result);
    }
}
```
<!-- end @acxbank -->


<!-- @acxbank string-vs-char-experiments -->
### Q16. string-vs-char-experiments

Play with characters and Strings. What happens if you do the following:

1. `char c = "a";`
2. `String b = 'foo';`
3. What happens if you add, using `+`, two strings together?
4. Two chars?
5. A string and a char?
6. A char and a string?
7. Do any other mathematical operations work on strings?

<!-- end @acxbank -->



