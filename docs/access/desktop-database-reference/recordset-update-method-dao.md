---
title: Recordset.Update (método) (DAO)
TOCTitle: Update Method
ms:assetid: aad4171a-da95-ed72-86b3-714615ea0ac8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821467(v=office.15)
ms:contentKeyID: 48546961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d81eaf181a87d6afc13dbf2908be307d120d349
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997024"
---
# <a name="recordsetupdate-method-dao"></a>Recordset.Update (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . Actualización (***UpdateType***, ***Force***)

*expresión* Variable que representa un objeto **Recordset** .

## <a name="parameters"></a>Parámetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>UpdateType</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Una constante <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> que indica el tipo de actualización, como se especifica en la Configuración (únicamente espacios de trabajo ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><em>Force</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p>Un valor <strong>Boolean</strong> que indica si se van a forzar los cambios en la base de datos, independientemente de que los datos subyacentes hayan sido cambiados por otro usuarios desde la llamada <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> o <strong><a href="recordset-edit-method-dao.md">Edit</a></strong>. Si es <strong>True</strong>, se fuerzan los cambios y se sobrescriben los cambios realizados por otros usuarios. Si es <strong>False</strong> (predeterminado), los cambios realizados por otro usuario mientras la actualización está pendiente, harán que la actualización falle para los cambios en conflicto. No se generan errores, pero las propiedades <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> y <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> indicarán el número de conflictos y las filas afectadas por los conflictos respectivamente (únicamente espacios de trabajo ODBCDirect).  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Utilice **Update** para guardar el registro activo y cualquier cambio realizado en él.

> [!IMPORTANT]
> [!IMPORTANTE] Los cambios en el registro activo se pierden si:
> - Utiliza el método **Edit** o **AddNew** y luego se desplaza a otro registro sin utilizar primero **Update**.
> - Utiliza **Edit** o **AddNew** y luego **Edit** o **AddNew** de nuevo sin utilizar primero **Update**.
> - Establece la propiedad **[Bookmark](recordset-bookmark-property-dao.md)** en otro registro.
> - Cierra **Recordset** sin usar primero **Update**.
> - Cancela la operación **Edit** sin utilizar **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.

Para editar un registro, utilice el método **Edit** para copiar el contenido del registro activo en el búfer de copia. Si no utiliza **Edit** primero, se produce un error cuando utiliza **Update** o intenta cambiar el valor de un campo.

En un área de trabajo de ODBCDirect, puede realizar actualizaciones por lotes, siempre que la biblioteca de cursores admita actualizaciones por lotes y el objeto **Recordset** se abra con una opción de bloqueo por lotes optimista.

En un área de trabajo de Microsoft Access, cuando el valor de la propiedad **LockEdits** del objeto **Recordset** es **True** (bloqueado de forma pesimista) en un entorno multiusuario, el registro sigue bloqueado desde que se usa **Edit** hasta que se ejecuta el método **Update** o se cancela la edición. Si el valor de la propiedad **LockEdits** es **False** (bloqueado de forma optimista), el registro se bloquea y se compara con el registro preeditado justo antes de que se actualice en la base de datos. 

Si el registro cambió desde que se usó el método **Edit**, la operación **Update** produce un error. Las bases de datos ODBC e ISAM instalable conectadas por el motor de base de datos de Microsoft Access usan siempre un bloqueo optimista. Para seguir con la operación **Update** en los cambios, use el método **Update** de nuevo. Para volver al registro cuando otro usuario lo cambia, actualice el registro activo mediante Move 0.

> [!NOTE]
> [!NOTA] Para agregar, editar o eliminar un registro, debe haber un índice único en el registro en el origen de datos subyacente. Si no hay, se genera un error "Permiso denegado" en la llamada del método **AddNew**, **Delete** o **Edit** en un espacio de trabajo de Microsoft Access, o se genera un error "Argumento no válido" en una llamada de **Update** en un espacio de trabajo de ODBCDirect.

## <a name="example"></a>Ejemplo

Este ejemplo muestra el método **Update** junto con el método **Edit**.

```vb
    Sub UpdateX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     .Edit 
     ' Store original data. 
     strOldFirst = !FirstName 
     strOldLast = !LastName 
     ' Change data in edit buffer. 
     !FirstName = "Linda" 
     !LastName = "Kobara" 
     
     ' Show contents of buffer and get user input. 
     strMessage = "Edit in progress:" & vbCr & _ 
     " Original data = " & strOldFirst & " " & _ 
     strOldLast & vbCr & " Data in buffer = " & _ 
     !FirstName & " " & !LastName & vbCr & vbCr & _ 
     "Use Update to replace the original data with " & _ 
     "the buffered data in the Recordset?" 
     
     If MsgBox(strMessage, vbYesNo) = vbYes Then 
     .Update 
     Else 
     .CancelUpdate 
     End If 
     
     ' Show the resulting data. 
     MsgBox "Data in recordset = " & !FirstName & " " & _ 
     !LastName 
     
     ' Restore original data because this is a demonstration. 
     If Not (strOldFirst = !FirstName And _ 
     strOldLast = !LastName) Then 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Este ejemplo muestra el método **Update** junto con el método **AddNew**.

```vb
    Sub UpdateX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     .AddNew 
     !FirstName = "Bill" 
     !LastName = "Sornsin" 
     
     ' Show contents of buffer and get user input. 
     strMessage = "AddNew in progress:" & vbCr & _ 
     " Data in buffer = " & !FirstName & " " & _ 
     !LastName & vbCr & vbCr & _ 
     "Use Update to save buffer to recordset?" 
     
     If MsgBox(strMessage, vbYesNoCancel) = vbYes Then 
     .Update 
     ' Go to the new record and show the resulting data. 
     .Bookmark = .LastModified 
     MsgBox "Data in recordset = " & !FirstName & _ 
     " " & !LastName 
     ' Delete new data because this is a demonstration. 
     .Delete 
     Else 
     .CancelUpdate 
     MsgBox "No new record added." 
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Este ejemplo usa la propiedad **BatchCollisionCount** y el método **Update** para mostrar la actualización por lotes donde se resuelven colisiones al forzar la actualización por lotes.

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 Dim intLoop As Integer 
 Dim strPrompt As String 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. It is also required that a table 
 ' with a primary key is used. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Modify data in local recordset. 
 Do While Not .EOF 
 .Edit 
 If !royalty <= 20 Then 
 !royalty = !royalty - 4 
 Else 
 !royalty = !royalty + 2 
 End If 
 .Update 
 .MoveNext 
 Loop 
 
 ' Attempt a batch update. 
 .Update dbUpdateBatch 
 
 ' If there are collisions, give the user the option 
 ' of forcing the changes or resolving them 
 ' individually. 
 If .BatchCollisionCount > 0 Then 
 strPrompt = "There are collisions. " & vbCr & _ 
 "Do you want the program to force " & _ 
 vbCr & "an update using the local data?" 
 If MsgBox(strPrompt, vbYesNo) = vbYes Then _ 
 .Update dbUpdateBatch, True 
 End If 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

<br/>

Este ejemplo usa el método **AddNew** para crear un registro nuevo con el nombre especificado. La función AddName es necesaria para la ejecución de este procedimiento.

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
