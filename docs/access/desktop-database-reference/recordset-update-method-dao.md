---
title: Recordset.Update (método) (DAO)
TOCTitle: Update Method
ms:assetid: aad4171a-da95-ed72-86b3-714615ea0ac8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821467(v=office.15)
ms:contentKeyID: 48546961
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 9f73dfc49a6ec99b726a052c588c032783010081
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721671"
---
# <a name="recordsetupdate-method-dao"></a><span data-ttu-id="1ea64-102">Recordset.Update (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="1ea64-102">Recordset.Update method (DAO)</span></span>

<span data-ttu-id="1ea64-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ea64-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="1ea64-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ea64-104">Syntax</span></span>

<span data-ttu-id="1ea64-105">*expresión* . Actualización (***UpdateType***, ***Force***)</span><span class="sxs-lookup"><span data-stu-id="1ea64-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="1ea64-106">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1ea64-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ea64-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ea64-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ea64-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="1ea64-108">Name</span></span></p></th>
<th><p><span data-ttu-id="1ea64-109">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="1ea64-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="1ea64-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1ea64-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="1ea64-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ea64-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ea64-112"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="1ea64-112"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="1ea64-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="1ea64-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="1ea64-114"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="1ea64-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="1ea64-115">Una constante <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> que indica el tipo de actualización, como se especifica en la Configuración (únicamente espacios de trabajo ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="1ea64-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea64-116"><em>Force</em></span><span class="sxs-lookup"><span data-stu-id="1ea64-116"><em>Force</em></span></span></p></td>
<td><p><span data-ttu-id="1ea64-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="1ea64-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="1ea64-118"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="1ea64-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="1ea64-p101">Un valor <strong>Boolean</strong> que indica si se van a forzar los cambios en la base de datos, independientemente de que los datos subyacentes hayan sido cambiados por otro usuarios desde la llamada <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> o <strong><a href="recordset-edit-method-dao.md">Edit</a></strong>. Si es <strong>True</strong>, se fuerzan los cambios y se sobrescriben los cambios realizados por otros usuarios. Si es <strong>False</strong> (predeterminado), los cambios realizados por otro usuario mientras la actualización está pendiente, harán que la actualización falle para los cambios en conflicto. No se generan errores, pero las propiedades <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> y <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> indicarán el número de conflictos y las filas afectadas por los conflictos respectivamente (únicamente espacios de trabajo ODBCDirect).  </span><span class="sxs-lookup"><span data-stu-id="1ea64-p101">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset-edit-method-dao.md">Edit</a></strong> call. If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten. If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict. No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1ea64-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ea64-123">Remarks</span></span>

<span data-ttu-id="1ea64-124">Utilice **Update** para guardar el registro activo y cualquier cambio realizado en él.</span><span class="sxs-lookup"><span data-stu-id="1ea64-124">Use **Update** to save the current record and any changes you've made to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ea64-125">[!IMPORTANTE] Los cambios en el registro activo se pierden si:</span><span class="sxs-lookup"><span data-stu-id="1ea64-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="1ea64-126">Utiliza el método **Edit** o **AddNew** y luego se desplaza a otro registro sin utilizar primero **Update**.</span><span class="sxs-lookup"><span data-stu-id="1ea64-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="1ea64-127">Utiliza **Edit** o **AddNew** y luego **Edit** o **AddNew** de nuevo sin utilizar primero **Update**.</span><span class="sxs-lookup"><span data-stu-id="1ea64-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="1ea64-128">Establece la propiedad **[Bookmark](recordset-bookmark-property-dao.md)** en otro registro.</span><span class="sxs-lookup"><span data-stu-id="1ea64-128">You set the **[Bookmark](recordset-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="1ea64-129">Cierra **Recordset** sin usar primero **Update**.</span><span class="sxs-lookup"><span data-stu-id="1ea64-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="1ea64-130">Cancela la operación **Edit** sin utilizar **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="1ea64-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="1ea64-p102">Para editar un registro, utilice el método **Edit** para copiar el contenido del registro activo en el búfer de copia. Si no utiliza **Edit** primero, se produce un error cuando utiliza **Update** o intenta cambiar el valor de un campo.</span><span class="sxs-lookup"><span data-stu-id="1ea64-p102">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer. If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="1ea64-133">En un área de trabajo de ODBCDirect, puede realizar actualizaciones por lotes, siempre que la biblioteca de cursores admita actualizaciones por lotes y el objeto **Recordset** se abra con una opción de bloqueo por lotes optimista.</span><span class="sxs-lookup"><span data-stu-id="1ea64-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="1ea64-134">En un área de trabajo de Microsoft Access, cuando el valor de la propiedad **LockEdits** del objeto **Recordset** es **True** (bloqueado de forma pesimista) en un entorno multiusuario, el registro sigue bloqueado desde que se usa **Edit** hasta que se ejecuta el método **Update** o se cancela la edición.</span><span class="sxs-lookup"><span data-stu-id="1ea64-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="1ea64-135">Si el valor de la propiedad **LockEdits** es **False** (bloqueado de forma optimista), el registro se bloquea y se compara con el registro preeditado justo antes de que se actualice en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1ea64-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> 

<span data-ttu-id="1ea64-136">Si el registro cambió desde que se usó el método **Edit**, la operación **Update** produce un error.</span><span class="sxs-lookup"><span data-stu-id="1ea64-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="1ea64-137">Las bases de datos ODBC e ISAM instalable conectadas por el motor de base de datos de Microsoft Access usan siempre un bloqueo optimista.</span><span class="sxs-lookup"><span data-stu-id="1ea64-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="1ea64-138">Para seguir con la operación **Update** en los cambios, use el método **Update** de nuevo.</span><span class="sxs-lookup"><span data-stu-id="1ea64-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="1ea64-139">Para volver al registro cuando otro usuario lo cambia, actualice el registro activo mediante Move 0.</span><span class="sxs-lookup"><span data-stu-id="1ea64-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>

> [!NOTE]
> <span data-ttu-id="1ea64-p105">[!NOTA] Para agregar, editar o eliminar un registro, debe haber un índice único en el registro en el origen de datos subyacente. Si no hay, se genera un error "Permiso denegado" en la llamada del método **AddNew**, **Delete** o **Edit** en un espacio de trabajo de Microsoft Access, o se genera un error "Argumento no válido" en una llamada de **Update** en un espacio de trabajo de ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="1ea64-p105">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>

## <a name="example"></a><span data-ttu-id="1ea64-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1ea64-142">Example</span></span>

<span data-ttu-id="1ea64-143">Este ejemplo muestra el método **Update** junto con el método **Edit**.</span><span class="sxs-lookup"><span data-stu-id="1ea64-143">This example demonstrates the **Update** method in conjunction with **Edit** method.</span></span>

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

<span data-ttu-id="1ea64-144">Este ejemplo muestra el método **Update** junto con el método **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="1ea64-144">This example demonstrates the **Update** method in conjunction with the **AddNew** method.</span></span>

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

<span data-ttu-id="1ea64-145">Este ejemplo usa la propiedad **BatchCollisionCount** y el método **Update** para mostrar la actualización por lotes donde se resuelven colisiones al forzar la actualización por lotes.</span><span class="sxs-lookup"><span data-stu-id="1ea64-145">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

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

<span data-ttu-id="1ea64-p106">Este ejemplo usa el método **AddNew** para crear un registro nuevo con el nombre especificado. La función AddName es necesaria para la ejecución de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="1ea64-p106">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

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
