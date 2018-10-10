---
title: Recordset.Bookmarkable Property (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 6323f162-75c4-7cfe-c918-0b9454560f97
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194950(v=office.15)
ms:contentKeyID: 48545257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 42c7b8a95eecd055e6a4581bd8d8f3a6c4693168
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485618"
---
# <a name="recordsetbookmarkable-property-dao"></a>Recordset.Bookmarkable Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

Devuelve un valor que indica si un objeto **Recordset** admite marcadores, que se pueden establecer mediante la propiedad **[Bookmark](recordset-bookmark-property-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . Bookmarkable

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Observaciones

Compruebe el valor de la propiedad **Bookmarkable** de un objeto **Recordset** antes de intentar establecer o comprobar la propiedad **Bookmark**.

Para los objetos **Recordset** basados completamente en tablas del motor de base de datos de Microsoft Access, el valor de la propiedad **Bookmarkable** es True y puede utilizar marcadores. Sin embargo, puede que otros productos de base de datos no admitan marcadores. Por ejemplo, no se pueden usar marcadores en un objeto **Recordset** basado en una tabla vinculada de Paradox que no tenga una clave principal.

## <a name="example"></a>Ejemplo

En este ejemplo, se usan las propiedades **Bookmark** y **Bookmarkable** para permitir que el usuario marque un registro de un objeto **Recordset** y vuelva a él más adelante.

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
