---
title: Propiedad Recordset.Bookmarkable (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 6323f162-75c4-7cfe-c918-0b9454560f97
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194950(v=office.15)
ms:contentKeyID: 48545257
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2bd9b91f80c9411bb7cdf4e0be9e71ab055dc72f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300626"
---
# <a name="recordsetbookmarkable-property-dao"></a>Propiedad Recordset.Bookmarkable (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve un valor que indica si un objeto **Recordset** admite marcadores, que puede configurar utilizando la propiedad **[Bookmark](recordset-bookmark-property-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . Bookmarkable

*expression* Variable que representa un objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Compruebe el valor de la propiedad **Bookmarkable** de un objeto **Recordset** antes de intentar establecer o comprobar la propiedad **Bookmark**.

Para **los objetos Recordset** basados completamente en tablas del motor de base de datos de Microsoft Access, el valor de la propiedad **Bookmarkable** es True y puede usar marcadores. Sin embargo, puede que otros productos de base de datos no admitan marcadores. Por ejemplo, no se pueden usar marcadores en un objeto **Recordset** basado en una tabla vinculada de Paradox que no tenga una clave principal.

## <a name="example"></a>Ejemplo

Este ejemplo usa las propiedades **Bookmark** y **Bookmarkable** para que el usuario pueda marcar un registro en un **Recordset** y volver a él más adelante.

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
     Dim strMessage As String 
     Dim intCommand As Integer 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenSnapshot) 
     
     With rstCategories 
     
     If .Bookmarkable = False Then 
     Debug.Print "Recordset is not Bookmarkable!" 
     Else 
     ' Populate Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show information about current record and get 
     ' user input. 
     strMessage = "Category: " & !CategoryName & _ 
     " (record " & (.AbsolutePosition + 1) & _ 
     " of " & .RecordCount & ")" & vbCr & _ 
     "Enter command:" & vbCr & _ 
     "[1 - next / 2 - previous /" & vbCr & _ 
     "3 - set bookmark / 4 - go to bookmark]" 
     intCommand = Val(InputBox(strMessage)) 
     
     Select Case intCommand 
     ' Move forward or backward, trapping for BOF 
     ' or EOF. 
     Case 1 
     .MoveNext 
     If .EOF Then .MoveLast 
     Case 2 
     .MovePrevious 
     If .BOF Then .MoveFirst 
     
     ' Store the bookmark of the current record. 
     Case 3 
     varBookmark = .Bookmark 
     
     ' Go to the record indicated by the stored 
     ' bookmark. 
     Case 4 
     If IsEmpty(varBookmark) Then 
     MsgBox "No Bookmark set!" 
     Else 
     .Bookmark = varBookmark 
     End If 
     
     Case Else 
     Exit Do 
     End Select 
     
     Loop 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
