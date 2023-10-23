---
layout: default
title: Multiple Elements
parent: Detailed Docs
nav_order: 12
---

# Finding Multiple Elements

You can use `findAll("element")` to identity a list of elements from the UI.
By default it will not have any wait associated with it because it is supposed to return zero or more elements.
But you can still use `waitFor(seconds)` to add a psuedo wait with details described below.

From findAll method you will get an iterable class of UIElements. You can iterate through the elements to extract
the properties or do actions on the UI.


### Adding a psuedo wait 
{: .text-red-000}


findAll() is supposed to return zero or more elements by default. So it doesn't have a default wait time. This would be
an inconvenience in many situations were you are expecting at least one element to be present. To handle this situation,
you can use the `waitFor(int time)` method to add a pseudo wait time to the process.

```java
findAll("element").waitFor(5).first();
```

## Available actions with FindAll method


```java
findAll("element").first();
findAll("element").last();
findAll("element").skipFirst(); //to skip the first element - useful to skip table headers
findAll("element").get(index); //to retrieve a UI element with nth index
findAll("element").size();
findAll("element").isPresent();
findAll("element").pause(int); //static wait
findAll("element").shouldHave(CollectionsCondition);
findAll("element").expecting(Expectation);
findAll("element").getAllText(); //list
```









