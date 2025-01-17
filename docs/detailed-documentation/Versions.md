---
layout: default
title: Versions
parent: Detailed Docs
nav_order: 1.1
---


# Current - Version 2.0.3

New release
{: .label .label-purple }

Maven:

```xml
        <dependency>
            <groupId>dev.tidalcode</groupId>
            <artifactId>wave</artifactId>
            <version>2.0.3</version>
        </dependency>
```

Gradle:

```yml
implementation group: 'dev.tidalcode', name: 'wave', version: '2.0.3'
```

Fix for the bug: [Attribute Verification](https://github.com/tidal-code/wave/issues/45){:target='_blank'}
### Version 2.0.2

Implemented the changes for the newest Selenium version 4.27.0
1. getAttribute() has been changed to getDomAttribute()
2. Removed WebDriverManager dependency as SeleniumManager is fully functional. 

### Version 2.0.1

1. Advanced debug mode.

2. waitFor for findAll has been limited to expected conditions.

3. RetryIf conditions can remember all sequential actions even when they repeat. 


### Version 2.0.0
Migration to new package structure [dev.tidalcode] and domain name [dev.tidalcode]


## For older versions the the group id is different. Please use the following co-ordinates

Maven:

```xml
        <dependency>
            <groupId>io.github.tidal-code</groupId>
            <artifactId>wave</artifactId>
            <version>${version}</version>
        </dependency>
```

### Version 1.3.1

Added keyboard multi interaction function.

New `FluentRquest` class for API requests.

### Version 1.3.0

Added slow run mode and debug mode. 

New upload file by drag and drop function has been added.
`find("element").uploadFileByDragAndDrop("file name");`

New page refresh function has been added.              
`find("element").doPageRefresh(MaxTime, IntervalTime);`

BugFixes:
Fixed nullpointer exception for certain user interaction scenarios.


### Version 1.2.9

Added functions to find first(), last() and skipFirst() from a collection


Bug Fixes:
Element finder scripts iframe iterator had an issue which would cause it not to find the right iframe, the element contains.
The issue has been identified and fixed.


### Version 1.2.8
Changed assertion type for test failures to reflect correct failure types in Allure reporting.

### Version 1.2.7
Internal changes only. <br>
Change in Element finder class to use CommandContext class to pass more information about element to be found.


### Version 1.2.4 to 1.2.6
Minor bug fixes and enhancements

### Version 1.2.3
Part 2 of core scripts refactoring to increase execution speed.

### Version 1.2.2
Part 1 of core scripts refactoring to increase execution speed.

### Version 1.2.1

Fixed a bug with getText, that may cause a nullpointer exception. 

### Version 1.2.0

1. Reverted from Selenium Manager to WedDriver Manager due to preformance issues. 
2. Iframe iteration is optimised to increase test execution speed. Old IframeHandler is now deprecated.

<br>

### Version 1.1.0

Added custom expectation failure message.

Example:
```java
find("#invisibleElement").expecting(toBePresent).orElseFail("The element expected to be present, but failed to fulfill the condition");
```

This would cause an assertion failure with the custom message given.


### Version 1.0.1

```Upgrade to native Selenium Manager from WebDriver Manager.```

Selenium has integrated Boni García's WebDriver manager to the core Selenium library.

### Version 1.0.0

```Initial version release.```




