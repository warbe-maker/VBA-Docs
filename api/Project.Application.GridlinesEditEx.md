---
title: Application.GridlinesEditEx method (Project)
keywords: vbapj.chm2152
f1_keywords:
- vbapj.chm2152
ms.prod: project-server
api_name:
- Project.Application.GridlinesEditEx
ms.assetid: fad3c4cc-2643-4af1-ca6b-f376b24a97bb
ms.date: 02/16/2019
ms.localizationpriority: medium
---


# Application.GridlinesEditEx method (Project)

Edits gridlines, where colors can be hexadecimal values.

## Syntax

_expression_.**GridlinesEditEx** (_Item_, _NormalType_, _NormalColor_, _Interval_, _IntervalType_, _IntervalColor_)

_expression_ An expression that returns an **[Application](Project.Application.md)** object.

## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Item_|Required|**Integer**|The gridline to edit. Can be one of the following **[PjGridline](Project.PjGridline.md)** constants:<ul><li>If the Gantt Chart is active: **pjBarRows**, **pjGanttCurrentDate**, **pjGanttPageBreaks**, **pjGanttProjectFinish**, **pjGanttProjectStart**, **pjGanttRows**, **pjGanttSheetColumns**, **pjGanttSheetRows**, **pjGanttStatusDate**, **pjGanttTitleHorizontal**, **pjGanttTitleVertical**, **pjMajorColumns**, or **pjMinorColumns**.</li><li>If the Calendar view is active: **pjCalendarDays**, **pjCalendarWeeks**, **pjTitleHorizontal**, **pjTitleVertical**, **pjDateBoxTop**, or **pjDateBoxBottom**.</li><li>If the Resource Graph is active: **pjMajorVertical**, **pjMinorVertical**, **pjHorizontal**, **pjGraphCurrentDate**, **pjGraphTitleHorizontal**, **pjGraphTitleVertical**, **pjGraphProjectStart**, **pjGraphProjectFinish**, or **pjGraphStatusDate**. </li><li>If the Task Sheet or Resource Sheet is active: **pjSheetColumns**, **pjSheetRows**, **pjSheetTitleHorizontal**, **pjSheetTitleVertical**, or **pjSheetPageBreaks**.</li><li>If the Task Usage or Resource Usage view is active: **pjUsageColumns**, **pjUsageRows**, **pjUsageSheetRows**, **pjUsageSheetColumns**, **pjUsageTitleHorizontal**, **pjUsageTitleVertical**, or **pjUsagePageBreaks**.</li></ul>|
| _NormalType_|Optional|**Integer**| The type for normal gridlines. Can be one of the following **[PjLineType](Project.PjLineType.md)** constants: **pjNoLines**, **pjContinuous**, **pjCloseDot**, **pjDot**, or **pjDash**.|
| _NormalColor_|Optional|**Long**|The color of normal gridlines. Can be a hexadecimal RGB value, where red is the last byte. For example, `&H0088FF` is orange.|
| _Interval_|Optional|**Integer**|A number from 0 to 99 that specifies the interval between gridlines.|
| _IntervalType_|Optional|**Integer**|The type for secondary gridlines. Can be one of the **[PjLineType](Project.PjLineType.md)** constants.|
| _IntervalColor_|Optional|**Long**|The color of secondary gridlines. Can be a hexadecimal RGB value, where red is the last byte.|

## Return value

**Boolean**

## Example

The following example changes the major gridlines to red.

```vb
Sub Gridlines_Edit() 
    'Activate Gantt Chart view 
    ViewApply Name:="&Gantt Chart" 
    GridlinesEditEx Item:=pjMajorColumns, NormalColor:=&HFF 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
