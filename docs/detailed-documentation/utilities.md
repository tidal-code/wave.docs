---
layout: default
title: Utilities
parent: Detailed Docs
nav_order: 19
---

# Utilities

The tidal framework provides several built in utility packages under the parent structure `import com.tidal.utils` to assist with Automation Scripting.

## Data and File Handlers
<br>

| Area of functionality | Utility Name              |
|:------------------    | :------------------       |
| csv                   | CsvData                   |
| csv                   | DataResolver              |
| data                  | GlobalData                |
| data                  | Key                       |
| data                  | TestUpdateData            |
| filehandlers          | Copy                      |
| filehandlers          | FileOutWriter             |
| filehandlers          | FilePaths                 |
| filehandlers          | FileReader                |
| filehandlers          | Finder                    |

## Exceptions
<br>

| Area of functionality | Utility Name              |
|:------------------    | :------------------       |
| exceptions            | AssertionError            |
| exceptions            | AzureOperationsException  |
| exceptions            | DataException             |
| exceptions            | DataResolverException     |
| exceptions            | DecryptorException        |
| exceptions            | PendingException          |
| exceptions            | PropertyHandlerException  |
| exceptions            | RequestClassException     |
| exceptions            | RuntimeTestException      |
| exceptions            | TimeoutException          |
| exceptions            | XMLHandlerException       |

## JSON
<br>

| Area of functionality | Utility Name              |
|:------------------    | :------------------       |
| json                  | JsonBuilder               |
| json                  | JsonReader                |
| json                  | JsonWriter                |

## JUnit
<br>

| Area of functionality | Utility Name              |
|:------------------    | :------------------       |
| junit                 | ResultParser              |
| junit                 | Template                  |

## Logs
<br>

| Area of functionality | Utility Name              |
|:------------------    | :------------------       |
| loggers               | Logger                    |
| loggers               | Log                       |
| loggers               | LoggerUtil                |

## Properties Handlers
<br>

| Area of functionality | Utility Name              |
|:------------------    | :------------------       |
| propertieshandler     | PropertiesFinder          |
| propertieshandler     | Config                    |
| propertieshandler     | PropertiesHandler         |

## Reports
<br>

| Area of functionality | Utility Name              |
|:------------------    | :------------------       |
| report                | Reporter                  |
| report                | ReportBuilder             |
| report                | ReportMatcher             |
| report                | ReportModel               |

## URLs
<br>

| Area of functionality | Utility Name              |
|:------------------    | :------------------       |
| urlbuilders           | Protocol                  |
| urlbuilders           | Url                       |

## Wait
<br>

_Instead of using the wait packages it is recommended to utilise:_ `findAll(locator).waitFor(10).isPresent();`

| Area of functionality | Utility Name              |
|:------------------    | :------------------       |
| waiter                | ThreadSleep               |
| waiter                | Wait                      |

## XML
<br>

| Area of functionality | Utility Name              |
|:------------------    | :------------------       |
| xml                   | XmlBuilder                |
| xml                   | XMLReader                 |
| xml                   | Processors                |

## General utilities
<br>

| Area of functionality | Utility Name              |
|:------------------    | :------------------       |
| counter               | TimeCounter               |
| date                  | FormattedDate             |
| encryptor             | Decryptor                 |
| pend                  | Pending                   |
| random                | Random                    |
| scenario              | ScenarioInfo              |
| utils                 | CheckString               |
| utils                 | Helper                    |


### Please review the decompiled class files for further details of the methods that are available for each package listed above