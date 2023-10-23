---
layout: default
title: Dropdowns
parent: Detailed Docs
nav_order: 6
---

# Dropdowns

Typical dropdown with input type as \'select\' can be interacted with using three
methods 

```java
find("locator").select(String selectText); //Visible text in the dropdown
find("locator").selectByValue(String value); //value of select elements
find("locator").select(int index); //index value of elements
```

##### select(String selectText)
{: .text-purple-000}

This method will select the drop down value with the visible text in the dropdown.

Returns: The current selected value.

##### selectByValue(String value)
{: .text-purple-000}

This method will select the drop down value with the value attribute of the dropdown elements

Returns: The current selected value.

##### select(String selectText)
{: .text-purple-000}

This method will select the drop down value with the index of the .


Returns: The current selected value.

<b>NOTE:</b> The above methods will work only with html elements of type 'select'. Many web applications may not have dropdown types as select. You might need to add extra
user interactions to select an element from those types of dropdowns. For example, click on a drop down arrow and then click on one of the values shown.
