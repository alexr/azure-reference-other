---
title: "Error 0146 | Microsoft Docs"
titleSuffix: "Azure Machine Learning Studio"
ms.date: 07/19/2016
ms.service: "machine-learning"
ms.subservice: "studio"
ms.topic: "article"


author: ericlicoding
ms.author: amlstudiodocs
manager: cgronlun
---
# Error 0146  
 When the user files are unzipped into the local directory, the combined path might be too long.  
  
 This error in Azure Machine Learning occurs when you are extracting files but some file names are too long when unzipped.  
  
## Resolution  
 Edit the file names such that combined path and file name is no longer than 248 characters.  
  
|Exception Messages|  
|------------------------|  
|Replication path is longer than 248 characters, shorten the script name or path.|  
  
## See also  
 [Module error codes](../machine-learning-module-error-codes.md)
