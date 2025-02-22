---
title: Application.ProjectBeforePrint2 event (Project)
ms.prod: project-server
api_name:
- Project.Application.ProjectBeforePrint2
ms.assetid: 93e243b7-d765-e3d9-d061-dd98407010d1
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Application.ProjectBeforePrint2 event (Project)

Occurs before a project is printed. Uses the **EventInfo** object parameter.


## Syntax

_expression_. `ProjectBeforePrint2`( `_pj_`, `_Info_` )

_expression_ A variable that represents an **[Application](Project.Application.md)** object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _pj_|Required|**Project**|The project to be printed.|
| _Info_|Required|**EventInfo**|EventInfo.Cancel is **False** when the event occurs. If the event procedure sets this argument to **True**, the project will not be printed.|

## Return value

**Nothing**


## Remarks

Project events don't occur when the project is embedded in another document or application.

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]