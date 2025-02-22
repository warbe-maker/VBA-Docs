---
title: ToggleButton.QuickStyle property (Access)
keywords: vbaac10.chm14646
f1_keywords:
- vbaac10.chm14646
ms.prod: access
api_name:
- Access.ToggleButton.QuickStyle
ms.assetid: 6dc5a569-8758-86cd-5b2a-693081ef95c5
ms.date: 03/05/2019
ms.localizationpriority: medium
---


# ToggleButton.QuickStyle property (Access)

Gets or sets the quick style that is applied to the specified object. Read/write **Long**.


## Syntax

_expression_.**QuickStyle**

_expression_ A variable that represents a **[ToggleButton](Access.ToggleButton.md)** object.


## Remarks

The **QuickStyle** property uses one of the values listed in the following table.

|Value|Effect|
|:-----|:-----|
|0 (Default)|No Quick Style |
|1|Colored Outline - Black, Dark 1|
|2|Colored Outline - Ice Blue, Accent 1|
|3|Colored Outline - Orange, Accent 2|
|4|Colored Outline - Olive Green, Accent 3|
|5|Colored Outline - Gold, Accent 4|
|6|Colored Outline - Green, Accent 5|
|7|Colored Outline - Gray-50%, Accent 6|
|8|Colored Fill - Black, Dark 1|
|9|Colored Fill - Ice Blue, Accent 1|
|10|Colored Fill - Orange, Accent 2|
|11|Colored Fill - Olive Green, Accent 3|
|12|Colored Fill - Gold, Accent 4|
|13|Colored Fill - Green, Accent 5|
|14|Colored Fill - Gray-50%, Accent 6|
|15|Light 1 Outline, Colored Fill - Black, Dark 1|
|16|Light 1 Outline, Colored Fill - Ice Blue, Accent 1|
|17|Light 1 Outline, Colored Fill - Orange, Accent 2|
|18|Light 1 Outline, Colored Fill - Olive Green, Accent 3|
|19|Light 1 Outline, Colored Fill - Gold, Accent 4|
|10|Light 1 Outline, Colored Fill - Green, Accent 5|
|21|Light 1 Outline, Colored Fill - Gray-50%, Accent 6|
|22|Subtle Effect - Black, Dark 1|
|23|Subtle Effect - Ice Blue, Accent 1|
|24|Subtle Effect - Orange, Accent 2|
|25|Subtle Effect - Olive Green, Accent 3|
|26|Subtle Effect - Gold, Accent 4|
|27|Subtle Effect - Green, Accent 5|
|28|Subtle Effect - Gray-50%, Accent 6|
|29|Moderate Effect - Black, Dark 1|
|30|Moderate Effect - Ice Blue, Accent 1|
|31|Moderate Effect - Orange, Accent 2|
|32|Moderate Effect - Olive Green, Accent 3|
|33|Moderate Effect - Gold, Accent 4|
|34|Moderate Effect - Green, Accent 5|
|35|Moderate Effect - Gray-50%, Accent 6|
|36|Intense Effect - Black, Dark 1|
|37|Intense Effect - Ice Blue, Accent 1|
|38|Intense Effect - Orange, Accent 2|
|39|Intense Effect - Olive Green, Accent 3|
|40|Intense Effect - Gold, Accent 4|
|41|Intense Effect - Green, Accent 5|
|42|Intense Effect - Gray-50%, Accent 6|

To see the available quick styles and apply a quick style through the user interface, first open the form or report in Layout view or Design view by right-clicking the form or report in the navigation pane, and then choosing the view that you want. 

Next, choose the object to which you want to apply a quick style. Next, on the **Format** tab, in the **Control Formatting** group, choose **Quick Styles**, and then choose a quick style. 

Notice that the quick styles are indexed from left to right, and then from top to bottom. The first item, **Colored Outline - Black, Dark 1**, has the value 1. The first row contains quick styles with values from 1 to 7, the second row from 8 to 14, and so on.

This property is not surfaced in the property sheet. 



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]