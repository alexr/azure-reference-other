---
title: "System.Window()  (Stream Analytics) | Microsoft Docs"
description: "System.Window() is a system function that can be used to retrieve window properties."
applies_to: 
  - "Azure"
services: stream-analytics
author: mamccrea
manager: kfile

ms.service: stream-analytics
ms.topic: reference
ms.assetid: 5636701f-8977-42bf-a864-227652bdf2e5
caps.latest.revision: 15
ms.workload: data-services
ms.date: 01/30/2019
ms.author: mamccrea
---
# System.Window()  (Stream Analytics)
  Every event in the result of an aggregate query in Azure Stream Analytics belongs to a window of events over which the aggregate was computed. System.Window() provides access to the properties of the window. System.Window() can only be used with HOPPINGWINDOW when multiple durations are specified. Currently only Duration is available.

## Syntax  
  
```SQL
System.Window().Duration(timeunit)

```

## Arguments  
 **timeunit**  
  
 Is the unit of time for the *duration* result. The following table lists all valid *timeunit* arguments.
  
|Timeunit|Abbreviations|  
|--------------|-------------------|  
|day|dd, d|  
|hour|hh|  
|minute|mi, n|  
|second|ss, s|  
|millisecond|ms|  
|microsecond|mcs|  

 **resturned value**
 
 Is a float representing window's duration in the specified time units.
 
## Example

```SQL
SELECT
    System.Window().Duration(second) AS windowInSeconds,
    System.Window().Duration(minute) AS WindowInMinutes,
    COUNT(*) AS count
FROM input
GROUP BY id, HOPPINGWINDOW(Duration(minute, 5), Duration(second, 30), Hop(second, 10))
```
The value of `WindowInSeconds` will be one of 30.0 or 300.0 and the value of the `WindowInMinutes` will be correspondingly either 0.5 or 5.0 depending on which window the resulting event will belong.
