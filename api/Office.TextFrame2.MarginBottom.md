---
title: TextFrame2.MarginBottom property (Office)
ms.prod: office
api_name:
- Office.TextFrame2.MarginBottom
ms.assetid: c8fadba2-4e9e-4d54-b2ba-7637024ba0d6
ms.date: 01/25/2019
ms.localizationpriority: medium
---


# TextFrame2.MarginBottom property (Office)

Returns or sets the distance (in points) between the bottom of the text frame and the bottom of the inscribed rectangle of the shape that contains the text. Read/write.


## Syntax

_expression_.**MarginBottom**

_expression_ An expression that returns a **[TextFrame2](Office.TextFrame2.md)** object.


## Example

The following code adds a rectangle to a slide, adds text to the rectangle, and then sets the margins for the text frame.


```vb
Set pptSlide = ActivePresentation.Slides(1) 
With pptSlide.Shapes.AddShape(msoShapeRectangle, 0, 0, 250, 140).TextFrame2 
 .TextRange.Text = "Here is some sample text" 
 .MarginBottom = 10 
 .MarginLeft = 10 
 .MarginRight = 10 
 .MarginTop = 10 
End With
```


## See also

- [TextFrame2 object members](overview/Library-Reference/textframe2-members-office.md)



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]