# Prefixbox Test

## Short questions

- What is a package? How do you define a package?

Packages are similar like folders in our computer. One program usually is one package.

- What is a constructor? When is it executed?

We use constructor for consturct something, to make a new object etc.
- How do you implement inheritance in Java?

We do it with "extends" keyword after the related class.
- How do you prevent someone to inherit from a class?

Make my class private.
- What is a final variable? Where you can assign value to final variables?

If we make a variable final, later on the program can not overwrite it. 
- Specify the available access modifiers in Java and briefly explain them

The default is always public, what means you will access to in everywhere.
We have a private also, what you can use inside the class, but not in the package.
We do protected, where you can use it within the package and class and use it outside of the package but subclass only.

- Briefly explain the mechanism of exception handling


- What is the difference between an abstract class and an interface?
Interfaces are an empty shell, because they are not an classes. 

- What is the difference between Comparator and Comparable?

Comperable only a single sorting sequence what is affects the original class, but Comparator can do multiple sorting sequences and does not effect the original class. 


- How Iterable and Iterator interface works? What methods need to exist in a
class that implements them? What is their relation to for loops?

## Programming tasks

You can write your solutions in any language, you can even write pseudo code or
using only your own words.
The point is not to make a perfectly running application, the point is the way
you think!
Don't worry if you miss a semicolon or some parantheses.
You might use the Java stream API for your solutions but none of the exercises
require them

### Palindrom

Write a function which decides whether a text is palindrom(It's the same whether
you read it forwards or backwards). E.g.: abba, rotator, stats.
You might assume that the input string is not null, the length is greater than
1 and less than one million. **Strive for the low memory complexity!**

Example:

```java
public boolean isPalindrom(String input) {

}

isPalindrom("alma"); //false
isPalindrom("görög"); //true
```

### Find The Duplicate

You have an array that contains strings. Every item in the array is
unique except one which is present in the array exactly twice.
Write a function which finds the string that is present twice in the array.
You might assume that the input array is not null, the length is greater
or equal to 2 and less than one million. **Strive for the low time complexity!**

Example:

```java
public String findTheDuplicate(String[] input) {

}

String[] fruitBasket = new String[] { "apple", "banana", "coconut", "durian",
"banana", "elderberry", "fig", "grapefruit" };
findTheDuplicate(fruitBasket); //should return banana
```

### Count The Words

You have a long string that has some meaning on a real language. For example a
whole novel in a single string.
Write a function that counts the occurence of each word inside the string and
writes them to the output in the following format: `word: number of occurences`
You might assume that the input is not null and not empty. The order of the
words on the ouput does not matter.
The solution might be case insensitive, you don't have to differentiate
bwetween capital and non-capital letters.
The punctuation marks and line endings are not part of the words!

Example:

```java
public void countTheWords(String crazyLongString) {
    Array = crazylongString.split("")
    hashmap(key word, value occurrence)
for(i=0, i<stringarray.size,i++){
 hashmap.put(array[0],0)
    if (hashmap have the key what we provide then add one to the valuel; "";)
}
}

String boci = "Boci, boci tarka, se füle, se farka.";
countTheWords(boci);

//Output:
//boci:2
//tarka:1
//se:2
//füle:1
//farka:1
```

### What Is The Output

What is the output of the following Java application? Explain your solution!

```java
package com.mycompany.myproject;

public class Person {
    public String firstName;
    public String lastName;

    public Person(String firstName, String lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }  

    @Override
    public String toString() {return this.firstName + " " + this.lastName;}
}

public class Main {
    public static void main(String[] args) {
        int i = 0;
        String s = "apple";
        Person p = new Person("Jonh", "Doe");

        doSomething(i, s, p);

        System.out.println(i);
        System.out.println(s);
        System.out.println(p);
    }

    public static void doSomething(int i, String s, Person p)
    {
        i = 5;
        s += "banana";
        p.lastName = "Rambo";
    }
}

RETURN: 
5 <- we change i to 5
applebanana <- we add banana to the string s
JohnRambo < - we change the last name from Doe to Rambo


```

## SQL

- What is the PRIMARY KEY?

Primary key what you give to your database to authenticate it. 

- What is the difference between CLUSTERED INDEX and NONCLUSTERED INDEX?

- There is a table called `Employees`. Let's assume that the columns exist
and they have the right data type.
What is going to happen if we execute the script and we destroy
the database connection during the execution? What are the possible problems
that might occure?

If we destroy the connection, nothing going to happen, because we did not execute it. It will change the salaries for each person who earn under 250k and active in the company.


```sql
BEGIN TRANSACTION

UPDATE Employees
SET Salary = Salary * 1.1
WHERE
    Salary < 250000
    AND IsActiveEmployee = 1
```

## Web and HTTP

- Specify the existing HTTP request methods and describe their usage!
PUT use to send data to the server, like change password
POST is send not existing data, so forexample register
GET is to get some data from the server (usually we use this one)
DELETE is to delete data from the server

- What are the groups of HTTP response status codes? Write an example for each group!

200-299 OK response
300-399 redirection
400-499 client side error - 401
500- server side error 502 bad gateway