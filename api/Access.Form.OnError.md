---
title: Form.OnError property (Access)
keywords: vbaac10.chm13458
f1_keywords:
- vbaac10.chm13458
ms.prod: access
api_name:
- Access.Form.OnError
ms.assetid: f89366ad-7d68-cb0f-0b17-c6b4f4eb3f3c
ms.date: 03/14/2019
ms.localizationpriority: medium
---


# Form.OnError property (Access)

Sets or returns the value of the **On Error** box in the Properties window of a form or report. Read/write **String**.


## Syntax

_expression_.**OnError**

_expression_ A variable that represents a **[Form](Access.Form.md)** object.


## Remarks

This property is helpful for programmatically changing the action that Microsoft Access takes when an event is triggered. For example, between event calls you may want to change an expression's parameters, or switch from an event procedure to an expression or macro, depending on the circumstances under which the event was triggered.

The **Error** event occurs when a run-time error is produced in Microsoft Access when a form or report has the focus. This includes Microsoft Jet database engine errors, but not run-time errors in Visual Basic.

The **OnError** value will be one of the following, depending on the selection chosen in the Choose Builder window (accessed by choosing the **Build** button next to the **On Error** box in the object's Properties window):

- If you choose Expression Builder, the value will be =_expression_, where _expression_ is the expression from the Expression Builder window.
    
- If you choose Macro Builder, the value is the name of the macro. 
    
- If you choose Code Builder, the value will be [Event Procedure]. 
    
If the **On Error** box is blank, the property value is an empty string.


## Example

The following example associates the **Error** event with the macro Error_Handler_Macro for the **Order Entry** form.

```vb
Forms("Order Entry").OnError = "Error_Handler_Macro"
```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]