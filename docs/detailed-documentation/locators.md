---
layout: default
title: Locators
parent: Detailed Docs
nav_order: 3
---

# Locators

The locators are supplied 
as a string prefixed with the locator types as shown in the table below.

| Type | Locator |
|:-------------     |:------------------                           | 
| id                | find(\"id:some_id\")                         |
| name              | find(\"name:some_name\")                     |
| class             | find(\"class:some_class\")                   |
| tag name          | find(\"tagName:some_tag_name\")              |
| xpath             | find(\"//xpath\")                            |
| css selector      | find(\"css: css selector")                   |
| link text         | find(\"linkText:link text")                  |
| partial link text | find(\"partialLinkText:partial link text")   |

To locate an element by its title

| Type              | Locator                     |
|:-------------     |:------------------          | 
| title             | find(\"title:title value\") |


To locate an element by its text value

| Type              | Locator                |
|:-------------     |:------------------     | 
| text              | find(\"text value\") |


## Special Xpath functions
<br>
For simple xpath expressions you can just type it in natural English.
For example `//div[name='user_name']` can be passed over to the framework like `find("div with name user_name")`

If it is a partial match you can use `find("div contains name user")`

If the property contains special characters or white spaces, you can enclose them in single quotes
`find("div contains text 'User Login'")`


## Links

For a comprehensive x-path reference, refer this [link](https://devhints.io/xpath){:target='_blank'} <br>
For CSS selectors, refer this [link](https://saucelabs.com/resources/blog/selenium-tips-css-selectors){:target='_blank'}



