---
title: Application.TextStyles32Ex method (Project)
keywords: vbapj.chm2150
f1_keywords:
- vbapj.chm2150
ms.prod: project-server
api_name:
- Project.Application.TextStyles32Ex
ms.assetid: 8e1ed2bb-dac4-42d7-616b-a67984dcffa4
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Application.TextStyles32Ex method (Project)

Sets the text styles for tasks and resources in the active view, where colors can be hexadecimal RGB values.

## Syntax

_expression_.**TextStyles32Ex** (_Item_, _Font_, _Size_, _Bold_, _Italic_, _Underline_, _Color_, _CellColor_, _Pattern_)

_expression_ An expression that returns an **[Application](Project.Application.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Item_|Optional|**Integer**|The type of text to change. Can be one of the following **[PjTextItem](Project.PjTextItem.md)** constants. See [If the Gantt Chart is active](#if-the-gantt-chart-is-active).|
| _Font_|Optional|**String**|The name of the font. The _Font_ argument is ignored if the active view is the **Network Diagram**, and Item is not **pjAll**.|
| _Size_|Optional|**Integer**|The size of the font in points. The _Size_ argument is ignored if the active view is the **Network Diagram**, and Item is not **pjAll**.|
| _Bold_|Optional|**Boolean**|**True** if the font is bold; otherwise, **False**.|
| _Italic_|Optional|**Boolean**|**True** if the font is italic; otherwise, **False**.|
| _Underline_|Optional|**Boolean**|**True** if the font is underlined; otherwise, **False**.|
| _Color_|Optional|**Long**|The color of the font. Can be a hexadecimal value for the RGB color, where red is the last byte. For example, the value `&HFF0000` is blue and `&H00FFFF` is yellow.|
| _CellColor_|Optional|**Long**|The background color of the cell. Can be a hexadecimal value for the RGB color.|
| _Pattern_|Optional|**Integer**|The background pattern of the cell. Can be one of the **[PjBackgroundPattern](Project.PjBackgroundPattern.md)** constants.|


### If the Gantt Chart is active

|Gantt Chart Active|Gantt Chart Active Continued|
|:-----|:-----|
|**pjAll**|**pjGanttMajorTimescale**|
|**pjNoncritical**|**pjGanttMinorTimescale**|
|**pjCritical**|**pjBarTextLeft**|
|**pjMilestone**|**pjBarTextRight**|
|**pjSummary**|**pjBarTextTop**|
|**pjProjectSummary**|**pjBarTextBottom**|
|**pjMarked**|**pjBarTextInside**|
|**pjTaskFilterHighlight**|**pjGanttExternalTask**|
|**pjTaskRowColumnTitles**||


### If the Task Usage view is active

|Task Usage|Task Usage Continued|
|:-----|:-----|
|**pjAll**|**pjTaskFilterHighlight**|
|**pjCritical**|**pjTaskMajorTimescale**|
|**pjMarked**|**pjTaskMinorTimescale**|
|**pjMilestone**|**pjTaskRowColumnTitles**|
|**pjNoncritical**|**pjTaskUsageAssignmentRow**|
|**pjProjectSummary**|**pjTaskUsageExternalTask**|
|**pjSummary**||


### If the Task Sheet is active

|Task Sheet 1|Task Sheet 2|
|:-----|:-----|
|**pjAll**|**pjGanttMajorTimescale**|
|**pjNoncritical**|**pjGanttMinorTimescale**|
|**pjCritical**|**pjBarTextLeft**|
|**pjMilestone**|**pjBarTextRight**|
|**pjSummary**|**pjBarTextTop**|
|**pjProjectSummary**|**pjBarTextBottom**|
|**pjMarked**|**pjBarTextInside**|
|**pjTaskFilterHighlight**|**pjGanttExternalTask**|
|**pjTaskRowColumnTitles**||

|Task Sheet 3|Task Sheet 4|
|:-----|:-----|
|**pjAll**|**pjTaskFilterHighlight**|
|**pjCritical**|**pjTaskMajorTimescale**|
|**pjMarked**|**pjTaskMinorTimescale**|
|**pjMilestone**|**pjTaskRowColumnTitles**|
|**pjNoncritical**|**pjTaskUsageAssignmentRow**|
|**pjProjectSummary**|**pjTaskUsageExternalTask**|
|**pjSummary**||

|Task Sheet 5|Task Sheet 6|
|:-----|:-----|
|**pjAll**|**pjProjectSummary**|
|**pjCritical**|**pjSummary**|
|**pjMarked**|**pjTaskSheetExternalTask**|
|**pjMilestone**|**pjTaskFilterHighlight**|
|**pjNoncritical**|**pjTaskRowColumnTitles**|



## Return value

 **Boolean**

## Remarks

Using the **TextStyles32Ex** method without specifying any arguments displays the **Text Styles** dialog box.

> [!NOTE]
> If you use any of the **PjColor** enumeration constants for the _Color_ or _CellColor_ parameters, the color will be nearly black. For example, the value of pjGreen is 9, which in the **TextStyles32Ex** method is a very dark red. To use only the sixteen colors available with **PjColor** constants, use the **[TextStylesEx](Project.Application.TextStylesEx.md)** method.

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
