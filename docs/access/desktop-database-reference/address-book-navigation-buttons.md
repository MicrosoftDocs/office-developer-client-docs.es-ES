---
title: Botones de desplazamiento por la Libreta de direcciones
TOCTitle: Address Book Navigation Buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d68a15873bc5030fd51e54c2219a0ffd91f080f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485483"
---
# <a name="address-book-navigation-buttons"></a>Botones de desplazamiento por la Libreta de direcciones


**Se aplica a**: Access 2013 | Office 2013

La aplicación Libreta de direcciones muestra los botones de desplazamiento en la parte inferior de la página Web. Puede utilizar estos botones para desplazarse por los datos de la cuadrícula HTML seleccionando la primera o la última fila de datos o las filas adyacentes a la selección actual.

## <a name="navigation-sub-procedures"></a>Procedimientos (Sub) de desplazamiento

La aplicación Libreta de direcciones contiene varios procedimientos que permiten a los usuarios hacer clic en los botones **Primero**, **Siguiente**, **Anterior** y **Último** para desplazarse por los datos.

Por ejemplo, al hacer clic en el **primer** botón activa la primera VBScript\_procedimiento OnClick Sub. El procedimiento ejecuta un método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) que hace que la primera fila de datos pase a ser la selección actual. Al hacer clic en el botón **último** , se activa la última\_procedimiento OnClick Sub, que invoca el método [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) , hacer que la última fila de datos de la selección actual. Los botones de navegación restantes funcionan de un modo similar.

```vb 
 
' Move to the first record in the bound Recordset. 
Sub First_OnClick 
 DC1.Recordset.MoveFirst 
End Sub 
 
' Move to the next record from the current position 
' in the bound Recordset. 
Sub Next_OnClick 
 If Not DC1.Recordset.EOF Then ' Cannot move beyond bottom record. 
 DC1.Recordset.MoveNext 
 Exit Sub 
 End If 
End Sub 
 
' Move to the previous record from the current position in the bound 
' Recordset. 
Sub Prev_OnClick 
 If Not DC1.Recordset.BOF Then ' Cannot move beyond top record. 
 DC1.Recordset.MovePrevious 
 Exit Sub 
 End If 
End Sub 
 
' Move to the last record in the bound Recordset. 
Sub Last_OnClick 
 DC1.Recordset.MoveLast 
End Sub 
```

