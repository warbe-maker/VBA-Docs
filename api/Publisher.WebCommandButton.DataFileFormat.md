---
title: WebCommandButton.DataFileFormat property (Publisher)
keywords: vbapb10.chm3932169
f1_keywords:
- vbapb10.chm3932169
ms.prod: publisher
api_name:
- Publisher.WebCommandButton.DataFileFormat
ms.assetid: 7594b575-b39f-3cd4-d0b9-c13c04299345
ms.date: 06/18/2019
ms.localizationpriority: medium
---


# WebCommandButton.DataFileFormat property (Publisher)

Sets or returns a **[PbSubmitDataFormatType](Publisher.PbSubmitDataFormatType.md)** constant that represents the format to use when saving web form data to a file. Read/write.


## Syntax

_expression_.**DataFileFormat**

_expression_ A variable that represents a **[WebCommandButton](Publisher.WebCommandButton.md)** object.


## Return value

PbSubmitDataFormatType


## Remarks

The **DataFileFormat** property value can be one of the **PbSubmitDataFormatType** constants declared in the Microsoft Publisher type library.


## Example

This example sets Microsoft Publisher to process web form data by saving it to a comma-delimited text file on the same web server as the form is stored. Note that `FileName` must be replaced with a valid file name for this example to work.

```vb
Sub WebDataFile() 
 With ThisDocument.Pages(1).Shapes(1).WebCommandButton 
 .DataRetrievalMethod = pbSubmitDataRetrievalSaveOnServer 
 .DataFileFormat = pbSubmitDataFormatCSV 
 .DataFileName = "FileName" 
 End With 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]