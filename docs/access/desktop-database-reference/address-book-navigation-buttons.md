---
title: Botones de navegación de la libreta de direcciones
TOCTitle: Address Book navigation buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7c87acd433df4a303c1e6a15a60184cadf994c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282467"
---
# <a name="address-book-navigation-buttons"></a>Botones de navegación de la libreta de direcciones

**Se aplica a:** Access 2013, Office 2013

La aplicación libreta de direcciones muestra los botones de navegación en la parte inferior de la página web. Puede utilizar estos botones para desplazarse por los datos de la cuadrícula HTML seleccionando la primera o la última fila de datos o las filas adyacentes a la selección actual.

## <a name="navigation-sub-procedures"></a>Procedimientos (Sub) de desplazamiento

La aplicación Libreta de direcciones contiene varios procedimientos que permiten a los usuarios hacer clic en los botones **Primero**, **Siguiente**, **Anterior** y **Último** para desplazarse por los datos.

Por ejemplo, al hacer clic en **el botón Primero** se activa el procedimiento VbScript First \_ OnClick Sub. El procedimiento ejecuta un método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) que hace que la primera fila de datos pase a ser la selección actual. Al hacer **clic en** el botón Último se activa el procedimiento Last OnClick Sub, que invoca el \_ método [MoveLast,](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) lo que hace que la última fila de datos sea la selección actual. Los botones de navegación restantes funcionan de un modo similar.

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

