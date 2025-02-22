---
title: Label.ThemeFontIndex property (Access)
keywords: vbaac10.chm14610
f1_keywords:
- vbaac10.chm14610
ms.prod: access
api_name:
- Access.Label.ThemeFontIndex
ms.assetid: 56e24b5e-18c4-193a-95ec-dcfc5b8ff477
ms.date: 03/02/2019
ms.localizationpriority: medium
---


# Label.ThemeFontIndex property (Access)

Gets or sets the font index that represents a font in the applied theme associated with the **FontName** property of the specified object. Read/write **Long**.


## Syntax

_expression_.**ThemeFontIndex**

_expression_ A variable that represents a **[Label](Access.Label.md)** object.


## Remarks

The **ThemeFontIndex** property uses one of the values listed in the following table.

|Value|Description|
|:-----|:-----|
|0|Header font|
|1 (Default)|Detail font|

If no theme is applied, the **ThemeFontIndex** property contains -1.

This property is not surfaced in the property sheet.



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]