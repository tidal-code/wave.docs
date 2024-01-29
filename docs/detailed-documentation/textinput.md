---
layout: default
title: Text Input
parent: Detailed Docs
nav_order: 5
---

# Text Input Methods

The following text input methods are avaialable with the Tidal libray:

```java
find("locator").sendKeys(String text);
find("locator").setText(String text);
find("locator").setInnerHtml(String text);
find("locator").clearAndType(String text);
```

##### sendKeys(text)
{: .text-purple-000}

Normal text input method to send text data to a UI text input field. 

##### setText(text)
{: .text-purple-000}

This method would revisit the value input and if not correct, it will clear and 
try again until it succeeds or a timeout is reached. This method is slower than the sendKeys() method. 

With setText method, you don't need to use a separate clear() method.

**<span class='text-red-000'>Caution:</span>**
<br>Do not try to input passwords or keyboard 'key inputs' using this method. The setText method will fail to read the
value or evaluate it. This will eventually throw an exception when the timeout exceeds.


##### setInnerHtml(text)
{: .text-purple-000}

This method would set the text value as an inner HTML value. This is not a proper text input method as it relies on modifying the HTML directly. So it may have unforeseen consequences. 


##### clearAndType(text):
{: .text-purple-000}


This method will try to clear the input field and send the text to the input field. 


## Javscript Text Input Method

This is a method using JavaScript to send a text value to an element. This may not be reliable always as it 
will not throw an exception. Again the method is quite fast and the UI application may not recognise the value. So use the method with caution and bear in mind that it is not always reliable.

```java
setValue(String text);
```




