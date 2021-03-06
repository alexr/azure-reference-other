---
title: "Error 0082 | Microsoft Docs"
titleSuffix: "Azure Machine Learning Studio"
ms.date: 07/19/2016
ms.service: "machine-learning"
ms.subservice: "studio"
ms.topic: "reference"

author: ericlicoding
ms.author: amlstudiodocs
manager: cgronlun
---
# Error 0082  
 Exception occurs when a model cannot be successfully deserialized.  
  
 This error in Azure Machine Learning occurs when a saved machine learning model or transform cannot be loaded by a newer version of the Azure Machine Learning runtime as a result of a breaking change.  
  
## Resolution  
 The training experiment that produced the model or transform must be rerun and the model or transform must be resaved.  
  
|Exception Messages|  
|------------------------|  
|Model could not be deserialized because it is likely serialized with an older serialization format. Please retrain and re-save the model.|  
  
 > [!TIP]
 >  Need more help or troubleshooting tips for Azure Machine Learning? Try these resources:  
 >  
 >  -  [Troubleshooting guide: Create and connect to an Machine Learning workspace](https://azure.microsoft.com/documentation/articles/machine-learning-troubleshooting-creating-ml-workspace/)  
 >  -  [Azure Machine Learning Frequently Asked Questions (FAQ)](https://azure.microsoft.com/documentation/articles/machine-learning/studio/faq/)  
  
## See also  
 [Module error codes](../machine-learning-module-error-codes.md)
