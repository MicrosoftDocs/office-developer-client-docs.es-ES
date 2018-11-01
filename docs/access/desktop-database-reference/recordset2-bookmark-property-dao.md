---
title: Recordset2.Bookmark Property (DAO)
TOCTitle: Bookmark Property
ms:assetid: 7366d550-2f72-ed10-b230-eb144a6f874b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195857(v=office.15)
ms:contentKeyID: 48545637
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5336c0993230b7d380b335e6f8e7eaa1af9b306c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867828"
---
# <a name="recordset2bookmark-property-dao"></a>Recordset2.Bookmark Property (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve un marcador que identifica únicamente al registro actual en un objeto **Recordset**.

## <a name="syntax"></a>Sintaxis

*expresión* . Marcador

*expresión* Variable que representa un objeto **Recordset2** .

## <a name="remarks"></a>Comentarios

Para un objeto **Recordset** basado completamente en tablas del motor de base de datos de Microsoft Access, el valor de la propiedad **Bookmarkable** es True y puede utilizar la propiedad **Bookmark** con ese conjunto de registros. Sin embargo, puede que otros productos de la base de datos no admitan marcadores. Por ejemplo, no puede utilizar marcadores en ningún objeto **Recordset2** basado en una tabla de Paradox vinculada que no contenga una clave principal.

Cuando se crea o se abre un objeto **Recordset**, cada registro tiene ya un marcador único. Puede guardar el marcador del registro actual asignando el valor de la propiedad **Bookmark** a una variable. Para poder volver rápidamente a ese registro después de moverse a otro, establezca la propiedad **Bookmark** del objeto **Recordset** en el valor de dicha variable.

No hay límite en el número de marcadores que se pueden establecer. Para crear un marcador para un registro distinto del actual, desplácese al registro deseado y asigne el valor de la propiedad **Bookmark** a una variable de tipo **String** que identifique el registro.

Para asegurarse de que el objeto **Recordset** admita marcadores, compruebe el valor de su propiedad **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** antes de usar la propiedad **Bookmark**. Si la propiedad **Bookmarkable** es False, el objeto **Recordset** no admite marcadores y, mediante el **marcador** de propiedad da como resultado un error capturable.

Si usa el método **[Clone](recordset2-clone-method-dao.md)** para crear una copia de un objeto **Recordset**, la configuración de la propiedad **Bookmark** de los objetos **Recordset** original y duplicado es idéntica y se puede usar indistintamente. Sin embargo, no se pueden usar marcadores de distintos objetos **Recordset** indistintamente, incluso si se crearon mediante el mismo objeto o la misma instrucción SQL.

Si se establece la propiedad **Bookmark** en un valor que representa un registro eliminado, se produce un error capturable.

El valor de la propiedad **Bookmark** no es lo mismo que el número de registro.

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

<br/>

En este ejemplo se utiliza la propiedad **LastModified** para mover el puntero de registros actual a ambos registros, al que se ha modificado y al que se ha creado recientemente.

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirst As String 
     Dim strLast As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Store current data. 
     strFirst = !FirstName 
     strLast = !LastName 
     ' Change data in current record. 
     .Edit 
     !FirstName = "Julie" 
     !LastName = "Warren" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after Edit: " & _ 
     !FirstName & " " & !LastName 
     
     ' Restore original data because this is a demonstration. 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     
     ' Add new record. 
     .AddNew 
     !FirstName = "Roger" 
     !LastName = "Harui" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after AddNew: " & _ 
     !FirstName & " " & !LastName 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
