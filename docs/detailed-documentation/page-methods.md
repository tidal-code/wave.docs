---
layout: default
title: Page Methods
parent: Detailed Docs
nav_order: 13
---

# Page or Document (DOM) Related Methods


These are stand alone methods from the Page class. They have no relation to the common find("element") method 
you use in the Wave libary. That means, no waiting or page ready conditions will be applicable for these methods. 


```java
Page.refresh(); 
Page.title();
Page.currentUrl();
Page.getWindowHandles(); 
Page.getWindowHandle();
Page.getPageSource();
Page.switchToAlert();
Page.dismissAlert();
Page.acceptAlert();
Page.sendTextToAlert("text");
Page.getAlertText();
Page.getCapability("capability");
Page.getCapabilities(); //list
```









