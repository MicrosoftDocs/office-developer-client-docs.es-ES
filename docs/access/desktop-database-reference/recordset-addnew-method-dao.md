---
title: Recordset.AddNew (método) (DAO)
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
ms.openlocfilehash: b07717a209fdb0152964bcd33d228d17cecd4eec
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922352"
---
# <a name="recordsetaddnew-method-dao"></a><span data-ttu-id="3fc24-102">Recordset.AddNew (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="3fc24-102">Recordset.AddNew method (DAO)</span></span>


<span data-ttu-id="3fc24-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3fc24-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3fc24-104">Crea un nuevo registro de un objeto **[Recordset](recordset-object-dao.md)** actualizable.</span><span class="sxs-lookup"><span data-stu-id="3fc24-104">Creates a new record for an updatable **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fc24-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fc24-105">Syntax</span></span>

<span data-ttu-id="3fc24-106">*expresión* . AddNew</span><span class="sxs-lookup"><span data-stu-id="3fc24-106">*expression* .AddNew</span></span>

<span data-ttu-id="3fc24-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="3fc24-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fc24-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3fc24-108">Remarks</span></span>

<span data-ttu-id="3fc24-p101">Use el método **AddNew** para crear y agregar un nuevo registro al objeto **Recordset** designado por el conjunto de registros. Este método configura los campos en sus valores predeterminados y, si no especifica ningún valor predeterminado, configura los campos en Null (valores predeterminados especificados para un objeto **Recordset** de tipo tabla).</span><span class="sxs-lookup"><span data-stu-id="3fc24-p101">Use the **AddNew** method to create and add a new record in the **Recordset** object named by recordset. This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset**).</span></span>

<span data-ttu-id="3fc24-p102">Después de modificar el nuevo registro, use el método **[Update](recordset-update-method-dao.md)** para guardar los cambios y agregar el registro a **Recordset**. No se producen cambios en la base de datos hasta que use el método **Update**.</span><span class="sxs-lookup"><span data-stu-id="3fc24-p102">After you modify the new record, use the **[Update](recordset-update-method-dao.md)** method to save the changes and add the record to the **Recordset**. No changes occur in the database until you use the **Update** method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3fc24-p103">[!NOTA] Si emite un <STRONG>AddNew</STRONG> y ejecuta luego realiza cualquier operación para desplazarse a otro registro, pero sin usar <STRONG>Update</STRONG>, los cambios se perderán sin ninguna advertencia. Además, si cierra <STRONG>Recordset</STRONG> o termina el procedimiento que declara el objeto <STRONG>Recordset</STRONG> o su objeto <STRONG><A href="database-object-dao.md">Database</A></STRONG>, el nuevo registro se descarta sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="3fc24-p103">If you issue an <STRONG>AddNew</STRONG> and then perform any operation that moves to another record, but without using <STRONG>Update</STRONG>, your changes are lost without warning. In addition, if you close the <STRONG>Recordset</STRONG> or end the procedure that declares the <STRONG>Recordset</STRONG> or its <STRONG><A href="database-object-dao.md">Database</A></STRONG> object, the new record is discarded without warning.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="3fc24-p104">[!NOTA] Al usar <STRONG>AddNew</STRONG> en un área de trabajo de Microsoft Access y el motor de base de datos tiene que crear una nueva página para albergar el registro actual, el bloqueo de página es pesimista. Si el nuevo registro se ajusta a una página existente, el bloqueo de página es optimista.</span><span class="sxs-lookup"><span data-stu-id="3fc24-p104">When you use <STRONG>AddNew</STRONG> in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic. If the new record fits in an existing page, page locking is optimistic.</span></span></P>



<span data-ttu-id="3fc24-p105">Si no se ha desplazado al último registro del objeto **Recordset**, se pueden incluir los registros agregados a las tablas base mediante otros procesos si están colocados más allá del registro actual. Sin embargo, si agrega un registro a su propio objeto **Recordset**, el registro será visible en **Recordset** y se incluirá en la tabla subyacente donde estará visible para cualquier nuevo objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3fc24-p105">If you haven't moved to the last record of your **Recordset**, records added to base tables by other processes may be included if they are positioned beyond the current record. If you add a record to your own **Recordset**, however, the record is visible in the **Recordset** and included in the underlying table where it becomes visible to any new **Recordset** objects.</span></span>

<span data-ttu-id="3fc24-119">La posición del nuevo registro depende del tipo de **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="3fc24-119">The position of the new record depends on the type of **Recordset**:</span></span>

  - <span data-ttu-id="3fc24-120">En un objeto **Recordset** de tipo Dynaset, los registros se insertan al final de **Recordset**, independientemente de las reglas de clasificación u ordenación que se aplicaban al abrir **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3fc24-120">In a dynaset-type **Recordset** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

  - <span data-ttu-id="3fc24-p106">En un objeto **Recordset** de tipo tabla cuya la propiedad **[Index](recordset-index-property-dao.md)** está configurada, los registros se devuelven a su posición correcta según el criterio de ordenación. Si no configura la propiedad **Index**, los nuevos registros se devuelven al final de **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3fc24-p106">In a table-type **Recordset** object whose **[Index](recordset-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order. If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="3fc24-p107">El registro que estaba activo antes de usar **AddNew** sigue siendo el registro actual. Si quiere convertir el nuevo registro en el registro actual, puede configurar la propiedad **[Bookmark](recordset-bookmark-property-dao.md)** en el marcador identificado por el valor de propiedad **[LastModified](recordset-lastmodified-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="3fc24-p107">The record that was current before you used **AddNew** remains current. If you want to make the new record current, you can set the **[Bookmark](recordset-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset-lastmodified-property-dao.md)** property setting.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3fc24-p108">[!NOTA] Para agregar, editar o eliminar un registro, debe haber un índice único en el registro del origen de datos subyacente. En caso contrario, se produce un error de "denegación de permiso" en la llamada al método <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG> o <STRONG>Edit</STRONG> en un área de trabajo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3fc24-p108">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG>, or <STRONG>Edit</STRONG> method call in a Microsoft Access workspace.</span></span></P>



## <a name="example"></a><span data-ttu-id="3fc24-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3fc24-127">Example</span></span>

<span data-ttu-id="3fc24-p109">En este ejemplo se utiliza el método **AddNew** para crear un registro nuevo con el nombre especificado. Se requiere la función AddName para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="3fc24-p109">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

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
