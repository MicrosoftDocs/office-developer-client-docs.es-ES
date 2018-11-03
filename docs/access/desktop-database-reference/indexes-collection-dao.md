---
title: Colección Indexes (DAO)
TOCTitle: Indexes Collection
ms:assetid: 26450e85-c79d-b12a-d760-dfc89c37f36c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191889(v=office.15)
ms:contentKeyID: 48543802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21609d6299caf6de5e2fe0b777796033b69d9f87
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946695"
---
# <a name="indexes-collection-dao"></a><span data-ttu-id="438b4-102">Colección Indexes (DAO)</span><span class="sxs-lookup"><span data-stu-id="438b4-102">Indexes collection (DAO)</span></span>

<span data-ttu-id="438b4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="438b4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="438b4-104">Una colección **Indexes** contiene todos los objetos **Index** almacenados de un objeto **TableDef** (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="438b4-104">An **Indexes** collection contains all the stored **Index** objects of a **TableDef** object (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="438b4-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="438b4-105">Remarks</span></span>

<span data-ttu-id="438b4-p101">Cuando obtenga acceso a un objeto Recordset de tipo de tabla, use la propiedad **Index** del objeto para especificar el orden de los registros. Establezca esta propiedad en el valor de la propiedad **Name** de un objeto **Index** existente en la colección **Indexes** del objeto **[TableDef](tabledef-object-dao.md)** subyacente al objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="438b4-p101">When you access a table-type Recordset object, use the object's **Index** property to specify the order of records. Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection of the **[TableDef](tabledef-object-dao.md)** object underlying the **[Recordset](recordset-object-dao.md)** object.</span></span>


> [!NOTE]
> <span data-ttu-id="438b4-108">[!NOTA] Sólo puede utilizar el método **Append** o **Delete** en una colección **Indexes** si el valor de la propiedad **[Updatable](connection-updatable-property-dao.md)** del objeto **TableDef** integrante es **True**.</span><span class="sxs-lookup"><span data-stu-id="438b4-108">You can use the **Append** or **Delete** method on an **Indexes** collection only if the **[Updatable](connection-updatable-property-dao.md)** property setting of the containing **TableDef** object is **True**.</span></span>

<span data-ttu-id="438b4-109">Una vez creado un nuevo objeto **Index**, debe utilizar el método **Append** para agregarlo a la colección **Indexes** del objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="438b4-109">After you create a new **Index** object, you should use the **Append** method to add it to the **TableDef** object's **Indexes** collection.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="438b4-p102">[!IMPORTANTE] Asegúrese de que los datos son compatibles con los atributos del nuevo índice. Si el índice requiere valores únicos, compruebe que no hay duplicados en los registros de datos existentes. Si hay duplicados, el motor de base de datos de Microsoft Access no puede crear el índice; se producirá un error capturable al intentar utilizar el método Append en el nuevo índice.</span><span class="sxs-lookup"><span data-stu-id="438b4-p102">Make sure your data complies with the attributes of your new index. If your index requires unique values, make sure that there are no duplicates in existing data records. If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.</span></span>



## <a name="example"></a><span data-ttu-id="438b4-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="438b4-113">Example</span></span>

<span data-ttu-id="438b4-p103">En este ejemplo se crea un nuevo objeto **Index**, se anexa a la colección **Indexes** del objeto **TableDef** de Empleados y se enumera la colección **Indexes** de **TableDef**. Por último, se enumera **Recordset**, utilizando primero el objeto **Index** principal y, luego, el nuevo objeto **Index**. Se requiere el procedimiento IndexOutput para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="438b4-p103">This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**. Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**. The IndexOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub IndexObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create new index, create and append Field 
     ' objects to its Fields collection. 
     Set idxNew = .CreateIndex("NewIndex") 
     
     With idxNew 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     
     ' Add new Index object to the Indexes collection 
     ' of the Employees table collection. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection of Employees 
     ' table. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Print report using old and new indexes. 
     IndexOutput rstEmployees, "PrimaryKey" 
     IndexOutput rstEmployees, idxNew.Name 
     rstEmployees.Close 
     
     ' Delete new Index because this is a 
     ' demonstration. 
     .Indexes.Delete idxNew.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub IndexOutput(rstTemp As Recordset, _ 
     strIndex As String) 
     ' Report function for FieldX. 
     
     With rstTemp 
     ' Set the index. 
     .Index = strIndex 
     .MoveFirst 
     Debug.Print "Recordset = " & .Name & _ 
     ", Index = " & .Index 
     Debug.Print " EmployeeID - Country - Name" 
     
     ' Enumerate the recordset using the specified 
     ' index. 
     Do While Not .EOF 
     Debug.Print " " & !EmployeeID & " - " & _ 
     !Country & " - " & !LastName & ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="438b4-p104">En este ejemplo se utiliza el método **CreateIndex** para crear dos nuevos objetos **Index** y anexarlos luego a la colección **Indexes** del objeto **TableDef** de Empleados. Enumera la colección **Indexes** del objeto **TableDef**, la colección **Fields** de los nuevos objetos **Index** y la colección Properties de los nuevos objetos **Index**. Se requiere la función CreateIndexOutput para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="438b4-p104">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.</span></span>

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
