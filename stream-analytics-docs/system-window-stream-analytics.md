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
  Every event at every stage of the query in Azure Stream Analytics has a timestamp associated with it. System.Timestamp() is a system function that can be used to retrieve the event’s timestamp. Note that getting timestamp as a system property `System.Timestamp` is still supported, but using function is preferred, since use of property is depricated in compatibility mode 1.2.
  
 Below, we describe how Azure Stream Analytics assigns timestamps to events.  
  
### **Input events timestamp**  
 Timestamp of the input event can be defined by column value (or an expression) specified in the [TIMESTAMP BY](timestamp-by-azure-stream-analytics.md) clause:  
  
```SQL  
SELECT System.Timestamp() t
FROM input
TIMESTAMP BY MyTimeField 
  
```  
  
 If a TIMESTAMP BY clause is not specified for a given input, arrival time of the event is used as a timestamp. For example Enqueued time of the event will be used in case of Event Hub input.  
  
