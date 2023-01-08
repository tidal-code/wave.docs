---
layout: default
title: Home
nav_order: 1
description: "Tidal is a test automation library built with Java and Selenium"
permalink: /
---

# Focus on writing good Test Automation
{: .fs-9 }

Forget about handling waits, iframes or overlay spinners. You can write concise, simple automation tests with Tidal Wave Automation Libary. No need to worry about dependency injection, object initializing, constructors etc..
{: .fs-5 .fw-350 }

[Get started now](#getting-started){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } 
<!-- [View it on GitHub](https://github.com/tidal-code/Wave){:target='_blank'}{: .btn .fs-5 .mb-4 .mb-md-0 } -->

### Need of a framework

What is the need of a framework? Typically, when you use Selenium you might have to write a lot of code to stabilise the run. Selenium is not flaky, it does exactly what it is supposed to do. In fact, we can say our web applications are flaky.
A lot of environmental factors make our applications slow. Typical web applications are made up of lots of AJAX componens which load independently to give users a seemless experience. They enable the information on the page to get updated without 
a full page refresh. For test automation libaries like Selenium, this is a challenge as they have no in-built wait times. 

If you go to [Selenium Website](https://www.selenium.dev){:target='_blank'}, you would read this: 
<br>
<br>
**Selenium automates browsers. That's it! What you do with that power is entirely up to you.**

Typically Selenium will wait for your page to be ready before it starts the interaction. But it wouldn't know if your Ajax page components are yet to load. Selenium would never know some text on your page is going to change 
after a few seconds. These are the situations where you would need to write some custom wait methods when you use raw Selenium. The frameworks which claim to do without these custom waits would some times unnecessarily slow down the test execution.

If these efforts can be reduced, the test automation engineers can focus more on designing better automation scenarios. The creative energy of the test automation engineer should focus on deriving the most efficient, faster tests rather than fixing
the flakiness of the test run. Tidal - Wave test automation library is trying to achieve this. It is designed on the assumption that, there is no wait required initially expecting the element to be present in the application. If no element is found,
it will enter the wait mode by itself. It has a default wait time of 5 seconds which can be configured to a higher or lower value if needed.



---

## Getting started

### Dependencies

Tidal Wave UI automation library is built with Java and [Selenium](https://www.selenium.dev){:target='_blank'}. It requires no additional setup other than downloading the maven dependency. 
For running tests, you can use any of your favourite test runner like Junit, TestNG etc. 

### Add the following Maven dependency to your pom.xml file

{: .pt-4 }
Tidal is hosted with [Maven Central](https://mvnrepository.com/artifact/io.github.tidal-code/wave){:target='_blank'}. For detailed version information, check the 'Versions' page under the 'Detailed Docs' section. 

```xml
        <dependency>
            <groupId>io.github.tidal-code</groupId>
            <artifactId>wave</artifactId>
            <version>1.1.0</version>
        </dependency>
```

For projects using Gradle, use
```yml
implementation group: 'io.github.tidal-code', name: 'wave', version: '1.1.0'
```

### To start the browser

If you do not need any browser options

```java
Browser.open(url); //This will start ChromeDriver as default
```

```java
# .. after the test; call the close function
Browser.close();
```

To set your own max wait time

```java
Browser.withWaitTime(Duration.ofSeconds(15));
```

To run tests in headless mode or to add any other browser options

```java
//this example is for Chrome browser 
ChromeOptions options = new ChromeOptions();
options.setHeadless(true);
Browser.withOptions(options); //add the option
```

To run with other browsers; for example

```java
Browser.type("edge");
```

```java
// combining all these options as an example for Edge browser
EdgeOptions options = new EdgeOptions();
options.setHeadless(true);

Browser.withWaitTime(Duration.ofSeconds(15))
      .type("edge")
      .withOptions(options)
      .open("https://google.co.nz");

 // your test scripts would go here... 

//finally     
Browser.close();
```

The above is the hardest part required. But we need to do it only once.
    In most scenarios you would be putting the above script in a test hook and forget about it.
    The rest is easy.

```java
find("name:q").sendKeys("Hello");
find("id:userName").sendKeys("my_username");
find("div with text 'hello world'").getText();

// to find multiple elements
findAll("linkText:User Names").get(3).click();
```

There is no extra effort needed to add waits, scripts to handle overlapping spinners, wait for background processes to finish.
Just plain simple methods which would emulate user interactions.

Call simple static methods `find()` and `findAll()` to locate your element(s). If your element is inside an iframe, don't worry; you do not need to switch to it. Tidal will find it. If you are blocked with a spinner and need to wait for it do disappear to click on an element, it will be handled. Just call the `find()` method and the rest will be done for  you.


## About the project

Tidal is maintained by [Philip Kurian](https://www.linkedin.com/in/kurianphilipk/)(author) and other community contributors

### License

Distributed by an [MIT license](https://github.com/pmarsceill/just-the-docs/tree/master/LICENSE.txt).

<!-- ### Contributing

When contributing to this repository, please first discuss the change you wish to make via issue,
email, or any other method with the owners of this repository before making a change. Read more about becoming a contributor in [our GitHub repo](https://github.com/tidal-code/Wave#readme). -->


<!-- #### Thank you to the contributors of Just the Docs!

<ul class="list-style-none">
{% for contributor in site.github.contributors %}
  <li class="d-inline-block mr-1">
     <a href="{{ contributor.html_url }}"><img src="{{ contributor.avatar_url }}" width="32" height="32" alt="{{ contributor.login }}"/></a>
  </li>
{% endfor %}
</ul> -->

<!-- ### Code of Conduct

Just the Docs is committed to fostering a welcoming community.

[View our Code of Conduct](https://github.com/pmarsceill/just-the-docs/tree/master/CODE_OF_CONDUCT.md) on our GitHub repository. -->
