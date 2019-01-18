---
title: Objeto Relation (DAO)
TOCTitle: Relation Object
ms:assetid: 46d6dfaf-a97d-3abd-0b4b-396a41eb3be7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193195(v=office.15)
ms:contentKeyID: 48544578
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3eeaf8bf46d8673731243a1161ac578062a01f89
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716281"
---
# <a name="relation-object-dao"></a><span data-ttu-id="213c1-102">Objeto Relation (DAO)</span><span class="sxs-lookup"><span data-stu-id="213c1-102">Relation object (DAO)</span></span>


<span data-ttu-id="213c1-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="213c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="213c1-104">Un objeto **Relation** representa una relación entre campos de tablas o consultas (sólo bases de datos del motor de base de datos de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="213c1-104">A **Relation** object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="213c1-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="213c1-105">Remarks</span></span>

<span data-ttu-id="213c1-106">Puede usar el objeto **Relation** para crear nuevas relaciones y examinar las relaciones existentes en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="213c1-106">You can use the **Relation** object to create new relationships and examine existing relationships in your database.</span></span>

<span data-ttu-id="213c1-107">Mediante un objeto **Relation** y sus propiedades, se puede:</span><span class="sxs-lookup"><span data-stu-id="213c1-107">Using a **Relation** object and its properties, you can:</span></span>

  - <span data-ttu-id="213c1-108">Especificar una relación exigida entre campos de tablas base (pero no una relación que incluya una consulta o una tabla vinculada).</span><span class="sxs-lookup"><span data-stu-id="213c1-108">Specify an enforced relationship between fields in base tables (but not a relationship that involves a query or a linked table).</span></span>

  - <span data-ttu-id="213c1-109">Establecer relaciones no exigidas entre cualquier tipo de tabla o consulta, ya sea nativa o vinculada.</span><span class="sxs-lookup"><span data-stu-id="213c1-109">Establish unenforced relationships between any type of table or query— native or linked.</span></span>

  - <span data-ttu-id="213c1-110">Usar la propiedad **Name** para especificar la relación entre los campos de la tabla principal a la que se hace referencia y la tabla externa de referencia.</span><span class="sxs-lookup"><span data-stu-id="213c1-110">Use the **Name** property to refer to the relationship between the fields in the referenced primary table and the referencing foreign table.</span></span>

  - <span data-ttu-id="213c1-111">Usar la propiedad **Attributes** para determinar si la relación entre los campos de la tabla es uno a uno o uno a varios, y cómo exigir la integridad referencial.</span><span class="sxs-lookup"><span data-stu-id="213c1-111">Use the **Attributes** property to determine whether the relationship between fields in the table is one-to-one or one-to-many and how to enforce referential integrity.</span></span>

  - <span data-ttu-id="213c1-112">Usar la propiedad **Attributes** para determinar si el motor de base de datos de Microsoft Access puede realizar operaciones de actualización y eliminación en cascada en tablas principales y externas.</span><span class="sxs-lookup"><span data-stu-id="213c1-112">Use the **Attributes** property to determine whether the Microsoft Access database engine can perform cascading update and cascading delete operations on primary and foreign tables.</span></span>

  - <span data-ttu-id="213c1-113">Usar la propiedad **Attributes** para determinar si la relación entre los campos de la tabla es una combinación izquierda o una combinación derecha.</span><span class="sxs-lookup"><span data-stu-id="213c1-113">Use the **Attributes** property to determine whether the relationship between fields in the table is left join or right join.</span></span>

  - <span data-ttu-id="213c1-114">Usar la propiedad **Name** de todos los objetos **Field** de la colección **Fields** de un objeto **Relation**, para establecer o devolver los nombres de los campos de la clave principal de la tabla a la que se hace referencia o la configuración de la propiedad **ForeignName** de los objetos **Field**, para establecer o devolver los nombres de los campos de la clave externa de la tabla de referencia.</span><span class="sxs-lookup"><span data-stu-id="213c1-114">Use the **Name** property of all **Field** objects in the **Fields** collection of a **Relation** object to set or return the names of the fields in the primary key of the referenced table, or the **ForeignName** property settings of the **Field** objects to set or return the names of the fields in the foreign key of the referencing table.</span></span>

<span data-ttu-id="213c1-p101">Si se realizan cambios que infringen las relaciones establecidas para la base de datos, se produce un error capturable. Si se solicitan operaciones de actualización en cascada o eliminación en cascada, el motor de base de datos de Microsoft Access también modifica las tablas de clave principal o clave externa para exigir las relaciones que se establezcan.</span><span class="sxs-lookup"><span data-stu-id="213c1-p101">If you make changes that violate the relationships established for the database, a trappable error occurs. If you request cascading update or cascading delete operations, the Microsoft Access database engine also modifies the primary key or foreign key tables to enforce the relationships you establish.</span></span>

<span data-ttu-id="213c1-p102">Por ejemplo, la base de datos Neptuno contiene una relación entre la tabla Pedidos y la tabla Clientes. El campo IdCliente de la tabla Clientes es la clave principal y el campo IdCliente de la tabla Pedidos es la clave externa. Para que el motor de base de datos de Microsoft Access acepte un registro nuevo en la tabla Pedidos, busca en la tabla Clientes una coincidencia en el campo IdCliente de la tabla Pedidos. Si el motor de base de datos de Microsoft Access no encuentra una coincidencia, no acepta el nuevo registro y se produce un error capturable.</span><span class="sxs-lookup"><span data-stu-id="213c1-p102">For example, the Northwind database contains a relationship between an Orders table and a Customers table. The CustomerID field of the Customers table is the primary key, and the CustomerID field of the Orders table is the foreign key. For the Microsoft Access database engine to accept a new record in the Orders table, it searches the Customers table for a match on the CustomerID field of the Orders table. If the Microsoft Access database engine doesn't find a match, it doesn't accept the new record, and a trappable error occurs.</span></span>

<span data-ttu-id="213c1-p103">Cuando se exige la integridad referencial, debe existir un índice único para el campo de clave de la tabla a la que se hace referencia. El motor de base de datos de Microsoft Access crea automáticamente un índice con la propiedad **Foreign** establecida para actuar como la clave externa de la tabla de referencia.</span><span class="sxs-lookup"><span data-stu-id="213c1-p103">When you enforce referential integrity, a unique index must already exist for the key field of the referenced table. The Microsoft Access database engine automatically creates an index with the **Foreign** property set to act as the foreign key in the referencing table.</span></span>

<span data-ttu-id="213c1-p104">Para crear un nuevo objeto **Relation**, utilice el método **CreateRelation**. Para hacer referencia a un objeto **Relation** de una colección por su número ordinal o por su valor de la propiedad **Name**, utilice uno de los siguientes formatos de sintaxis:</span><span class="sxs-lookup"><span data-stu-id="213c1-p104">To create a new **Relation** object, use the **CreateRelation** method. To refer to a **Relation** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="213c1-125">**Relations**(0)</span><span class="sxs-lookup"><span data-stu-id="213c1-125">**Relations**(0)</span></span>

<span data-ttu-id="213c1-126">**Relaciones** ("nombre")</span><span class="sxs-lookup"><span data-stu-id="213c1-126">**Relations**("name")</span></span>

<span data-ttu-id="213c1-127">**Relaciones de**\!\[nombre\]</span><span class="sxs-lookup"><span data-stu-id="213c1-127">**Relations**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="213c1-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="213c1-128">Example</span></span>

<span data-ttu-id="213c1-p105">En este ejemplo se muestra cómo un objeto **Relation** existente puede controlar la entrada de datos. El procedimiento intenta agregar un registro con un CategoryID deliberadamente incorrecto, que desencadena una rutina de tratamiento de errores.</span><span class="sxs-lookup"><span data-stu-id="213c1-p105">This example shows how an existing **Relation** object can control data entry. The procedure attempts to add a record with a deliberately incorrect CategoryID; this triggers the error-handling routine.</span></span>

```vb 
    Sub RelationX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
     Dim prpLoop As Property 
     Dim fldLoop As Field 
     Dim errLoop As Error 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     ' Print a report showing all the different parts of 
     ' the relation and where each part is stored. 
     With dbsNorthwind.Relations!CategoriesProducts 
     Debug.Print "Properties of " & .Name & " Relation" 
     Debug.Print " Table = " & .Table 
     Debug.Print " ForeignTable = " & .ForeignTable 
     Debug.Print "Fields of " & .Name & " Relation" 
     With .Fields!CategoryID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     End With 
     
     ' Attempt to add a record that violates the relation. 
     With rstProducts 
     .AddNew 
     !ProductName = "Trygve's Lutefisk" 
     !CategoryID = 10 
     On Error GoTo Err_Relation 
     .Update 
     On Error GoTo 0 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
     Exit Sub 
     
    Err_Relation: 
     
     ' Notify user of any errors that result from 
     ' the invalid data. 
     If DBEngine.Errors.Count > 0 Then 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Sub 
```

<br/>

<span data-ttu-id="213c1-131">En este ejemplo se utiliza el método **CreateRelation** para crear una **Relation** entre el objeto **TableDef** de empleados y un nuevo objeto **TableDef** denominado Departments (departamentos).</span><span class="sxs-lookup"><span data-stu-id="213c1-131">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments.</span></span> <span data-ttu-id="213c1-132">También se muestra cómo crear una nueva **relación** creará también es necesario **índices** en la tabla externa (el índice DepartmentsEmployees de la tabla Employees).</span><span class="sxs-lookup"><span data-stu-id="213c1-132">It also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

```vb
    Sub CreateRelationX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim relNew As Relation 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Add new field to Employees table. 
     Set tdfEmployees = .TableDefs!Employees 
     tdfEmployees.Fields.Append _ 
     tdfEmployees.CreateField("DeptID", dbInteger, 2) 
     
     ' Create new Departments table. 
     Set tdfNew = .CreateTableDef("Departments") 
     
     With tdfNew 
     ' Create and append Field objects to Fields 
     ' collection of the new TableDef object. 
     .Fields.Append .CreateField("DeptID", dbInteger, 2) 
     .Fields.Append .CreateField("DeptName", dbText, 20) 
     
     ' Create Index object for Departments table. 
     Set idxNew = .CreateIndex("DeptIDIndex") 
     ' Create and append Field object to Fields 
     ' collection of the new Index object. 
     idxNew.Fields.Append idxNew.CreateField("DeptID") 
     ' The index in the primary table must be Unique in 
     ' order to be part of a Relation. 
     idxNew.Unique = True 
     .Indexes.Append idxNew 
     End With 
     
     .TableDefs.Append tdfNew 
     
     ' Create EmployeesDepartments Relation object, using 
     ' the names of the two tables in the relation. 
     Set relNew = .CreateRelation("EmployeesDepartments", _ 
     tdfNew.Name, tdfEmployees.Name, _ 
     dbRelationUpdateCascade) 
     
     ' Create Field object for the Fields collection of the 
     ' new Relation object. Set the Name and ForeignName 
     ' properties based on the fields to be used for the 
     ' relation. 
     relNew.Fields.Append relNew.CreateField("DeptID") 
     relNew.Fields!DeptID.ForeignName = "DeptID" 
     .Relations.Append relNew 
     
     ' Print report. 
     Debug.Print "Properties of " & relNew.Name & _ 
     " Relation" 
     Debug.Print " Table = " & relNew.Table 
     Debug.Print " ForeignTable = " & _ 
     relNew.ForeignTable 
     Debug.Print "Fields of " & relNew.Name & " Relation" 
     
     With relNew.Fields!DeptID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     
     Debug.Print "Indexes in " & tdfEmployees.Name & _ 
     " TableDef" 
     For Each idxLoop In tdfEmployees.Indexes 
     Debug.Print " " & idxLoop.Name & _ 
     ", Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     
     ' Delete new objects because this is a demonstration. 
     .Relations.Delete relNew.Name 
     .TableDefs.Delete tdfNew.Name 
     tdfEmployees.Fields.Delete "DeptID" 
     .Close 
     End With 
     
    End Sub
```
