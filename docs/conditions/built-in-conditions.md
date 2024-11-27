---
layout: default
title: Built In Conditions
parent: Conditions
---

# Built In Conditions

Built in conditions are not verifications by themselves. They can be used for UI compoents verifications. 
For proper end to end test verification, use Tidal Flow assertion library. 

Examples for verifying elements of a UI:

```java
find("element").shoudBe(visible);
find("element").shoudBe(notVisible);
find("element").shouldBe(present);
find("element").shouldBe(notPresent);
find("element").shouldBe(enabled);
find("element").shouldBe(notEnabled);
```

Examples for verifying the element's Data:

```java
find("element").shouldHave(exactText("Text Value"));
find("element").shouldHave(attribute("Attribute Value"));
find("element").shouldHave(attributeAndValue("Attribute", "Value"));
find("element").shouldHave(ignoreCaseExactText("Text Value"));
find("element").shouldHave(matchingText("Text Value"));
find("element").shouldHave(textNotNull);
```

Examples for verifying a collection data set:

```java
findAll("element").shouldHave(size(int size));
findAll("element").shouldHave(sizeGreaterThan(int size));
findAll("element").shouldHave(sizeLessThan(int size));
```