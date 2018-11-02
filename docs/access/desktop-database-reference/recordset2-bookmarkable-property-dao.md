---
title: Propiedad Recordset2.Bookmarkable (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 9c93d04d-ca10-acf5-122a-58625ed93424
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198125(v=office.15)
ms:contentKeyID: 48546601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052888
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e87b8d41e586d9ccaf647a0721968a62a0245d11
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921799"
---
# <a name="recordset2bookmarkable-property-dao"></a>Propiedad Recordset2.Bookmarkable (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve un valor que indica si un objeto **Recordset** admite marcadores, que se pueden establecer mediante la propiedad **[Bookmark](recordset2-bookmark-property-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . Bookmarkable

*expresión* Variable que representa un objeto **Recordset2** .

## <a name="remarks"></a>Observaciones

Compruebe el valor de la propiedad **Bookmarkable** de un objeto **Recordset** antes de intentar establecer o comprobar la propiedad **Bookmark**.

Para los objetos **Recordset** basados completamente en tablas del motor de base de datos de Microsoft Access, el valor de la propiedad **Bookmarkable** es True y puede utilizar marcadores. Sin embargo, puede que otros productos de base de datos no admitan marcadores. Por ejemplo, no se pueden usar marcadores en un objeto **Recordset** basado en una tabla vinculada de Paradox que no tenga una clave principal.

## <a name="example"></a>Ejemplo

En este ejemplo se utilizan las propiedades **Bookmark** y **Bookmarkable** para que el usuario pueda marcar un registro en un conjunto de registros y volver al mismo más adelante.

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset2 
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
