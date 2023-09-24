---
layout: default
title: Loggers
parent: Detailed Docs
nav_order: 18
---

# Test Automation Logs

## Java Logs

For general Java logging, use the following logger type to add log information for your code.
The following example use Slf4j logger facade. 

```java
public static final Logger logger = LoggerFactory.getLogger(ClassName.class); // Substitute  your class name.

// You can then add your log info in your code
logger.info("This is some log information");

```


To implement logger, you need to use an appender like Log4j. The following can be put into a log4j.properties file in  your resources folder.

```properties
# Root logger option
log4j.rootLogger=INFO, stdout
#log4j.rootLogger=OFF
# Direct log messages to stdout
log4j.appender.stdout=org.apache.log4j.ConsoleAppender
log4j.appender.stdout.Target=System.out
log4j.appender.stdout.layout=org.apache.log4j.PatternLayout
log4j.appender.stdout.layout.ConversionPattern=[%-4p] %c{1}: %m [%d{yyyy-MM-dd HH:mm:ss}] %n
```


## Allure Logs

To add log information to the Allure reporting, you either have to pass the log information to the Allure class using
Allure built in methods or use the Tidal Utils library logger method. While using this

```java
public static final Logger logger = new Logger(ClassName.class);

// You can then add your log info in your code
logger.info("This is some log information");
```