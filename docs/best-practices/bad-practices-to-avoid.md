---
layout: default
title: Other Practices to Avoid
parent: Best Practices
nav_order: 3
---

# Bad Practices to Avoid

## Unnecessary use of try-catch function

In test automation code the use of try-catch function is discouraged. Test automation code is not production code 
and you don't have to handle the error and present it in a nicer way. 

Also using try catch to check the presence of an element is a bad practice which would unnecessarily slow down your execution time. 

For example:

```java
try{
    find("element").click();
} catch (Exception e){
    //ignore or do something else.
}
```

If you are using the above method to avoid a failure when trying to click on an element that may or may not be present in the DOM, you would be wasting your time by waiting for that element. Also it adds unnecessary code into your test automation scripts. Remember, more code, more maintenance. 

The best way to achieve the above is to first check the presence of the element and then do your next action.

For example:

```java
 if(findAll("element").isPresent()){
    find("element").click();
 }
```

Try-catch can be used to handle checked exceptions if you would like to handle the exceptions and do something about it. It also would avoid exception propogation to the calling methods. 

For example:

```java
try{
    File file = new File("path");
} catch(FileNotFoundException e) { //Here we are capturing a specific exception.
    //do something.
    or 
    throw new RuntimeException("File not found from path: " + "path");
}
```

## Complex Code

It is preferable to use simple code rather than using a complex advanced Java function instead. The more simple the code, the more maintainable it would be. Test automation code should be simple and maintainable by everyone with basic skills in the programming language.  

Some times that may require us to do a bit of compromise. For example, using an extra if-else condition is easier than bringing in a design pattern class to achieve the same result, it is worth using the if-else even though it would look ugly and violate the coding standards. 