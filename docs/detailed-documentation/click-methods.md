---
layout: default
title: Click Methods
parent: Detailed Docs
nav_order: 4
---

# Click Methods

The following click methods are available:

```java
find("locator").click();
find("locator").doubleClick();
find("locator").contextClick();
find("locator").actionClick();
find("locator").forceClick();
```

##### click()
{: .text-purple-000}

It is encouraged to use this click method. For the click method to work, the element
should be in the correct interactable and visible state. 


##### doubleClick()
{: .text-purple-000}

To send a double click to the element.

##### contextClick()
{: .text-purple-000}

To send a right click (or left depending on mouse configuration), or a context click.

##### actionClick()
{: .text-purple-000}

actionClick would apply the click action even if the element is not in the right interactable 
state. No exception will be thrown if the click is not successful. This method would be useful when 
the normal click action wouldn't work due to overlapping elements. 

##### forceClick()
{: .text-purple-000}

This click method will simulate a force click by clicking and holding on to an element for a short time.

## Javscript Click Method

This is a method using JavaScript to send a click action to an element. This may not be reliable always as it 
will not throw an exception like the other click methods when it fails. Usage of this method is not encouraged unless 
no alternatives are available.

```java
clickByJS();
```




