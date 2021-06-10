---
title: Método Recordset2.AddNew (DAO)
TOCTitle: AddNew Method
ms:assetid: 25c7d207-185c-943b-405e-b138ffb8b3e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191874(v=office.15)
ms:contentKeyID: 48543792
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 49a69b5e8603e72faaba480ea9069d3668bd6de1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307500"
---
# <a name="recordset2addnew-method-dao"></a><span data-ttu-id="f311f-102">Método Recordset2.AddNew (DAO)</span><span class="sxs-lookup"><span data-stu-id="f311f-102">Recordset2.AddNew method (DAO)</span></span>

<span data-ttu-id="f311f-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f311f-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="f311f-104">Crea un nuevo registro para un objeto **Recordset2** actualizable.</span><span class="sxs-lookup"><span data-stu-id="f311f-104">Creates a new record for an updatable **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f311f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f311f-105">Syntax</span></span>

<span data-ttu-id="f311f-106">*expression* .AddNew</span><span class="sxs-lookup"><span data-stu-id="f311f-106">*expression* .AddNew</span></span>

<span data-ttu-id="f311f-107">*expresión* Variable que representa un **objeto Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="f311f-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f311f-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f311f-108">Remarks</span></span>

<span data-ttu-id="f311f-p101">Utilice el método **AddNew** para crear y agregar un nuevo registro al objeto **Recordset2** designado por el conjunto de registros. Este método establece los campos en sus valores predeterminados y, si no especifica ningún valor, establece los campos en Null (valores predeterminados especificados para un objeto **Recordset2** de tipo tabla).</span><span class="sxs-lookup"><span data-stu-id="f311f-p101">Use the **AddNew** method to create and add a new record in the **Recordset2** object named by recordset. This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset2**).</span></span>

<span data-ttu-id="f311f-p102">Tras modificar el nuevo registro, use el método **[Update](recordset2-update-method-dao.md)** para guardar los cambios y agregar el registro a **Recordset2**. No se producen cambios en la base de datos hasta que use el método **Update**.</span><span class="sxs-lookup"><span data-stu-id="f311f-p102">After you modify the new record, use the **[Update](recordset2-update-method-dao.md)** method to save the changes and add the record to the **Recordset2**. No changes occur in the database until you use the **Update** method.</span></span>

> [!NOTE]
> <span data-ttu-id="f311f-p103">[!NOTA] Si usa **AddNew** y ejecuta luego cualquier operación para desplazarse a otro registro pero sin usar **Update**, los cambios se pierden sin advertencia. Además, si cierra **Recordset2** o termina el procedimiento que declara el objeto **Recordset2** o su objeto **[Database](database-object-dao.md)**, el nuevo registro se descarta sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="f311f-p103">If you issue an **AddNew** and then perform any operation that moves to another record, but without using **Update**, your changes are lost without warning. In addition, if you close the **Recordset2** or end the procedure that declares the **Recordset2** or its **[Database](database-object-dao.md)** object, the new record is discarded without warning.</span></span>

> [!NOTE]
> <span data-ttu-id="f311f-p104">Al usar **AddNew** en un área de trabajo de Microsoft Access y el motor de base de datos tiene que crear una nueva página para albergar el registro actual, el bloqueo de página es pesimista. Si el nuevo registro se ajusta a una página existente, el bloqueo de página es optimista.</span><span class="sxs-lookup"><span data-stu-id="f311f-p104">When you use **AddNew** in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic. If the new record fits in an existing page, page locking is optimistic.</span></span>

<span data-ttu-id="f311f-p105">Si no se desplazó al último registro del objeto **Recordset2**, se pueden incluir los registros agregados a las tablas base por otros procesos si están colocados más allá del registro activo. Si agrega un registro a su propio objeto **Recordset2**, no obstante, el registro estará visible en **Recordset2** y se incluirá en la tabla subyacente donde estará visible para cualquier nuevo objeto **Recordset2**.</span><span class="sxs-lookup"><span data-stu-id="f311f-p105">If you haven't moved to the last record of your **Recordset2**, records added to base tables by other processes may be included if they are positioned beyond the current record. If you add a record to your own **Recordset2**, however, the record is visible in the **Recordset2** and included in the underlying table where it becomes visible to any new **Recordset2** objects.</span></span>

<span data-ttu-id="f311f-119">La posición del nuevo registro depende del tipo de **Recordset2**:</span><span class="sxs-lookup"><span data-stu-id="f311f-119">The position of the new record depends on the type of **Recordset2**:</span></span>

- <span data-ttu-id="f311f-120">En un objeto **Recordset2** de tipo dynaset, los registros se insertan al final de **Recordset**, independientemente de las reglas de clasificación u ordenación que hubiera en vigor cuando se abrió **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f311f-120">In a dynaset-type **Recordset2** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

- <span data-ttu-id="f311f-p106">En un objeto **Recordset2** de tipo tabla cuya propiedad **[Index](recordset2-index-property-dao.md)** se definió, los registros se devuelven al lugar correspondiente según el criterio de ordenación. Si no definió la propiedad **Index**, los nuevos registros se devuelven al final de **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f311f-p106">In a table-type **Recordset2** object whose **[Index](recordset2-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order. If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="f311f-p107">El registro que estaba activo antes de usar **AddNew** sigue siendo el registro actual. Si quiere convertir el nuevo registro en el registro actual, puede configurar la propiedad **[Bookmark](recordset2-bookmark-property-dao.md)** en el marcador identificado por el valor de propiedad **[LastModified](recordset2-lastmodified-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="f311f-p107">The record that was current before you used **AddNew** remains current. If you want to make the new record current, you can set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset2-lastmodified-property-dao.md)** property setting.</span></span>

> [!NOTE]
> <span data-ttu-id="f311f-p108">Para agregar, editar o eliminar un registro, debe haber un índice único en el registro en el origen de datos subyacente. En caso contrario, se produce un error de "denegación de permiso" en la llamada a método **AddNew**, **Delete** o **Edit** en un área de trabajo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f311f-p108">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="f311f-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f311f-127">Example</span></span>

<span data-ttu-id="f311f-p109">En este ejemplo se usa el método **AddNew** para crear un nuevo registro con el nombre especificado. La función AddName es necesaria para que se ejecute este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="f311f-p109">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
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
     
    Function AddName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a recordset using the data passed 
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
