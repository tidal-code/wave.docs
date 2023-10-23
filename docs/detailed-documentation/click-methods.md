---
layout: default
title: Click Methods
parent: Detailed Docs
nav_order: 4
---

# Click Methods

The available click methods in the framework are:

```java
find("locator").click();
find("locator").doubleClick();
find("locator").contextClick();
find("locator").actionClick();
find("locator").forceClick();
```

##### click()
{: .text-purple-000}

Involves a normal click. It handles stale element exception and element intercepted
exceptions.

##### doubleClick()
{: .text-purple-000}

Would send a double click to the element.

##### contextClick()
{: .text-purple-000}

Would send a right click (or left depending on mouse configuration), or a context click.

##### actionClick()
{: .text-purple-000}

This click  may not throw an error if it did not work properly.

##### forceClick()
{: .text-purple-000}

This click type will simulate a force click by clicking and holding on to an element for a short time.

## Javscript Click Method

This is a method using JavaScript to send a click action to an element. This may not be reliable always as it 
will not throw an exception like the other click methods when it fails. So please use this method when it is 
absolutely necessary only.

```java
clickByJS();
```




