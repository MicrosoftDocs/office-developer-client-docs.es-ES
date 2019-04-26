---
title: Método Recordset.AddNew (DAO)
TOCTitle: AddNew Method
ms:assetid: 18cb35f6-8652-fb20-2460-3d13fae39d23
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845624(v=office.15)
ms:contentKeyID: 48543483
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052883
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 79c8691fcea7cf04bac7d6cd05711730b510e215
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300647"
---
# <a name="recordsetaddnew-method-dao"></a><span data-ttu-id="99a1e-102">Método Recordset.AddNew (DAO)</span><span class="sxs-lookup"><span data-stu-id="99a1e-102">Recordset.AddNew Method (DAO)</span></span>

<span data-ttu-id="99a1e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="99a1e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="99a1e-104">Crea un nuevo registro de un objeto **[Recordset](recordset-object-dao.md)** actualizable.</span><span class="sxs-lookup"><span data-stu-id="99a1e-104">Creates a new record for an updatable **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="99a1e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99a1e-105">Syntax</span></span>

<span data-ttu-id="99a1e-106">*expression* .AddNew</span><span class="sxs-lookup"><span data-stu-id="99a1e-106">expression  . AddNew</span></span>

<span data-ttu-id="99a1e-107">*expression* Variable que representa un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="99a1e-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="99a1e-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99a1e-108">Remarks</span></span>

<span data-ttu-id="99a1e-p101">Use el método **AddNew** para crear y agregar un nuevo registro al objeto **Recordset** designado por el conjunto de registros. Este método configura los campos en sus valores predeterminados y, si no especifica ningún valor predeterminado, configura los campos en Null (valores predeterminados especificados para un objeto **Recordset** de tipo tabla).</span><span class="sxs-lookup"><span data-stu-id="99a1e-p101">Use the **AddNew** method to create and add a new record in the **Recordset** object named by recordset. This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset**).</span></span>

<span data-ttu-id="99a1e-p102">Después de modificar el nuevo registro, use el método **[Update](recordset-update-method-dao.md)** para guardar los cambios y agregar el registro a **Recordset**. No se producen cambios en la base de datos hasta que use el método **Update**.</span><span class="sxs-lookup"><span data-stu-id="99a1e-p102">After you modify the new record, use the **[Update](recordset-update-method-dao.md)** method to save the changes and add the record to the **Recordset**. No changes occur in the database until you use the **Update** method.</span></span>

> [!NOTE]
> <span data-ttu-id="99a1e-p103">Si emite un **AddNew** y ejecuta luego realiza cualquier operación para desplazarse a otro registro, pero sin usar **Update**, los cambios se perderán sin ninguna advertencia. Además, si cierra **Recordset** o termina el procedimiento que declara el objeto **Recordset** o su objeto **[Database](database-object-dao.md)**, el nuevo registro se descarta sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="99a1e-p103">If you issue an **AddNew** and then perform any operation that moves to another record, but without using **Update**, your changes are lost without warning. In addition, if you close the **Recordset** or end the procedure that declares the **Recordset** or its **[Database](database-object-dao.md)** object, the new record is discarded without warning.</span></span>

> [!NOTE]
> <span data-ttu-id="99a1e-p104">Al usar **AddNew** en un área de trabajo de Microsoft Access y el motor de base de datos tiene que crear una nueva página para albergar el registro actual, el bloqueo de página es pesimista. Si el nuevo registro se ajusta a una página existente, el bloqueo de página es optimista.</span><span class="sxs-lookup"><span data-stu-id="99a1e-p104">When you use **AddNew** in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic. If the new record fits in an existing page, page locking is optimistic.</span></span>

<span data-ttu-id="99a1e-p105">Si no se ha desplazado al último registro del objeto **Recordset**, se pueden incluir los registros agregados a las tablas base mediante otros procesos si están colocados más allá del registro actual. Sin embargo, si agrega un registro a su propio objeto **Recordset**, el registro será visible en **Recordset** y se incluirá en la tabla subyacente donde estará visible para cualquier nuevo objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="99a1e-p105">If you haven't moved to the last record of your **Recordset**, records added to base tables by other processes may be included if they are positioned beyond the current record. If you add a record to your own **Recordset**, however, the record is visible in the **Recordset** and included in the underlying table where it becomes visible to any new **Recordset** objects.</span></span>

<span data-ttu-id="99a1e-119">La posición del nuevo registro depende del tipo de **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="99a1e-119">The position of the new record depends on the type of **Recordset**:</span></span>

- <span data-ttu-id="99a1e-120">En un objeto **Recordset** de tipo Dynaset, los registros se insertan al final de **Recordset**, independientemente de las reglas de clasificación u ordenación que se aplicaban al abrir **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="99a1e-120">In a dynaset-type **Recordset** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

- <span data-ttu-id="99a1e-p106">En un objeto **Recordset** de tipo tabla cuya la propiedad **[Index](recordset-index-property-dao.md)** está configurada, los registros se devuelven a su posición correcta según el criterio de ordenación. Si no configura la propiedad **Index**, los nuevos registros se devuelven al final de **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="99a1e-p106">In a table-type **Recordset** object whose **[Index](recordset-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order. If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="99a1e-p107">El registro que estaba activo antes de usar **AddNew** sigue siendo el registro actual. Si quiere convertir el nuevo registro en el registro actual, puede configurar la propiedad **[Bookmark](recordset-bookmark-property-dao.md)** en el marcador identificado por el valor de propiedad **[LastModified](recordset-lastmodified-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="99a1e-p107">The record that was current before you used **AddNew** remains current. If you want to make the new record current, you can set the **[Bookmark](recordset-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset-lastmodified-property-dao.md)** property setting.</span></span>

> [!NOTE]
> <span data-ttu-id="99a1e-p108">Para agregar, editar o eliminar un registro, debe haber un índice único en el registro en el origen de datos subyacente. En caso contrario, se produce un error de "denegación de permiso" en la llamada a método **AddNew**, **Delete** o **Edit** en un área de trabajo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="99a1e-p108">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="99a1e-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="99a1e-127">Example</span></span>

<span data-ttu-id="99a1e-p109">En este ejemplo se usa el método **AddNew** para crear un nuevo registro con el nombre especificado. La función AddName es necesaria para que se ejecute este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="99a1e-p109">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

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
