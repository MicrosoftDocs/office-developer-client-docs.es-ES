---
title: Objeto Index - objetos de acceso a datos (DAO)
TOCTitle: Index object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0a975017b5c5396d23817716689b37433d8f97
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708917"
---
# <a name="index-object-dao"></a><span data-ttu-id="f460b-102">Objeto Index (DAO)</span><span class="sxs-lookup"><span data-stu-id="f460b-102">Index object (DAO)</span></span>

<span data-ttu-id="f460b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f460b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f460b-p101">El objeto **Index** especifica el orden de los registros a los que se tiene acceso desde las tablas de la base de datos y si se aceptan o no los registros duplicados, lo que proporciona un acceso a los datos eficaz. Para bases de datos externas, los objetos **Index** describen los índices establecidos para tablas externas (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f460b-p101">**Index** objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data. For external databases, **Index** objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="f460b-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f460b-106">Remarks</span></span>

<span data-ttu-id="f460b-p102">El motor de base de datos de Microsoft Access usa índices cuando combina tablas y crea objetos **[Recordset](recordset-object-dao.md)**. Los índices determinan el orden en el que los objetos **Recordset** de tipo tabla devuelven registros pero no determinan el orden en el que el motor de base de datos de Microsoft Access guarda los registros en la tabla base o el orden en el que cualquier otro tipo de objeto **Recordset** devuelve los registros.</span><span class="sxs-lookup"><span data-stu-id="f460b-p102">The Microsoft Access database engine uses indexes when it joins tables and creates **[Recordset](recordset-object-dao.md)** objects. Indexes determine the order in which table-type **Recordset** objects return records, but they don't determine the order in which the Microsoft Access database engine stores records in the base table or the order in which any other type of **Recordset** object returns records.</span></span>

<span data-ttu-id="f460b-109">Con un objeto **Index**, puede:</span><span class="sxs-lookup"><span data-stu-id="f460b-109">With an **Index** object, you can:</span></span>

- <span data-ttu-id="f460b-110">Utilizar la propiedad **Required** para determinar si los objetos **[Field](field-object-dao.md)** del índice requieren valores que no sean Null y utilizar luego la propiedad **IgnoreNulls** para determinar si los valores Null tienen entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="f460b-110">Use the **Required** property to determine whether the **[Field](field-object-dao.md)** objects in the index require values that are not Null, and then use the **IgnoreNulls** property to determine whether the null values have index entries.</span></span>

- <span data-ttu-id="f460b-111">Usar las propiedades **Primary** y **Unique** para determinar el orden y la exclusividad del objeto **Index**.</span><span class="sxs-lookup"><span data-stu-id="f460b-111">Use the **Primary** and **Unique** properties to determine the ordering and uniqueness of the **Index** object.</span></span>

<span data-ttu-id="f460b-p103">El motor de base de datos de Microsoft Access mantiene todos los índices de la tabla base de forma automática. Actualiza los índices siempre que agrega, cambia o elimina registros en la tabla base. Una vez que haya creado la base de datos, utilice el método **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** periódicamente para actualizar las estadísticas del índice.</span><span class="sxs-lookup"><span data-stu-id="f460b-p103">The Microsoft Access database engine maintains all base table indexes automatically. It updates indexes whenever you add, change, or delete records from the base table. Once you create the database, use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method periodically to bring index statistics up-to-date.</span></span>

<span data-ttu-id="f460b-p104">Al tener acceso a un objeto **Recordset** de tipo tabla, especifica el orden de registros que usa la propiedad **Index** del objeto. Establezca esta propiedad en el valor de la propiedad **Name** de un objeto **Index** existente en la colección **Indexes**. Esta colección está incluida en el objeto **[TableDef](tabledef-object-dao.md)** subyacente al objeto **Recordset** que está llenando.</span><span class="sxs-lookup"><span data-stu-id="f460b-p104">When accessing a table-type **Recordset** object, you specify the order of records using the object's **Index** property. Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection. This collection is contained by the **[TableDef](tabledef-object-dao.md)** object underlying the **Recordset** object that you're populating.</span></span>

> [!NOTE]
> <span data-ttu-id="f460b-p105">[!NOTA] No es necesario crear índices para las tablas, pero en tablas grandes y sin indizar el acceso a un registro determinado o el procesamiento de combinaciones puede llevar mucho tiempo. Por el contrario, si se tienen demasiados índices se pueden ralentizar las actualizaciones de la base de datos, ya que se corrigen todos los índices de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f460b-p105">You don't have to create indexes for a table, but for large, unindexed tables, accessing a specific record or processing joins can take a long time. Conversely, having too many indexes can slow down updates to the database as each of the table indexes is amended.</span></span>

<span data-ttu-id="f460b-120">La propiedad **[Attributes](field-attributes-property-dao.md)** de cada objeto **Field** del índice determina el orden de registros devueltos y, en consecuencia, qué técnicas de acceso se utilizan para este índice.</span><span class="sxs-lookup"><span data-stu-id="f460b-120">The **[Attributes](field-attributes-property-dao.md)** property of each **Field** object in the index determines the order of records returned and consequently determines which access techniques to use for that index.</span></span>

<span data-ttu-id="f460b-p106">Cada objeto **Field** de la colección **Fields** de un objeto **Index** es un componente del índice. Para definir un nuevo objeto **Index**, establezca sus propiedades antes de anexarlo a una colección, lo que hace que el objeto **Index** esté disponible para un uso posterior.</span><span class="sxs-lookup"><span data-stu-id="f460b-p106">Each **Field** object in the **Fields** collection of an **Index** object is a component of the index. To define a new **Index** object, set its properties before you append it to a collection, making the **Index** object available for subsequent use.</span></span>

> [!NOTE]
> <span data-ttu-id="f460b-123">[!NOTA] Puede modificar el valor de la propiedad **Name** de un objeto **Index** existente sólo si el valor de la propiedad **[Updatable](connection-updatable-property-dao.md)** del objeto **TableDef** que lo contiene es **True**.</span><span class="sxs-lookup"><span data-stu-id="f460b-123">You can modify the **Name** property setting of an existing **Index** object only if the **[Updatable](connection-updatable-property-dao.md)** property setting of the containing **TableDef** object is **True**.</span></span>

<span data-ttu-id="f460b-p107">Cuando establece una clave principal para una tabla, el motor de base de datos de Microsoft Access la define automáticamente como el índice principal. Un índice principal consta de uno o varios campos que identifican de manera única todos los registros de una tabla según un orden predefinido. Como el campo del índice principal debe ser único, el motor de base de datos de Microsoft Access establece la propiedad **Unique** del objeto **Index** principal en **True**. Si el índice principal se compone de varios campos, cada campo puede contener valores duplicados, pero la combinación de valores de todos los campos indizados debe ser única. Un índice principal consta de una clave para la tabla e incluye siempre los mismos campos que la clave principal.</span><span class="sxs-lookup"><span data-stu-id="f460b-p107">When you set a primary key for a table, the Microsoft Access database engine automatically defines it as the primary index. A primary index consists of one or more fields that uniquely identify all records in a table in a predefined order. Because the primary index field must be unique, the Microsoft Access database engine automatically sets the **Unique** property of the primary **Index** object to **True**. If the primary index consists of more than one field, each field can contain duplicate values, but the combination of values from all the indexed fields must be unique. A primary index consists of a key for the table and is always made up of the same fields as the primary key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f460b-p108">[!IMPORTANTE] Asegúrese de que los datos son conformes a los atributos del nuevo índice. Si el índice requiere valores únicos, asegúrese de que no haya duplicados en los registros de datos existentes. Si hay duplicados, el motor de base de datos de Microsoft Access no puede crear el índice; se produce un error capturable cuando intenta utilizar el método Append en el nuevo índice.</span><span class="sxs-lookup"><span data-stu-id="f460b-p108">Make sure your data complies with the attributes of your new index. If your index requires unique values, make sure that there are no duplicates in existing data records. If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.</span></span>

<span data-ttu-id="f460b-p109">Al crear una relación que impone una integridad referencial, el motor de base de datos de Microsoft Access crea automáticamente un índice con la propiedad **Foreign**, establecido como clave externa en la tabla de referencia. Tras establecer una relación de tabla, el motor de base de datos de Microsoft Access impide realizar adiciones o cambios en la base de datos que infrinjan la relación. Si establece la propiedad **Attributes** del objeto **[Relation](relation-object-dao.md)** para que permita actualizaciones en cascada y eliminaciones en cascada, el motor de base de datos de Microsoft Access actualiza o elimina registros en las tablas relacionadas de forma automática.</span><span class="sxs-lookup"><span data-stu-id="f460b-p109">When you create a relationship that enforces referential integrity, the Microsoft Access database engine automatically creates an index with the **Foreign** property, set as the foreign key in the referencing table. After you've established a table relationship, the Microsoft Access database engine prevents additions or changes to the database that violate that relationship. If you set the **Attributes** property of the **[Relation](relation-object-dao.md)** object to allow cascading updates and cascading deletes, the Microsoft Access database engine updates or deletes records in related tables automatically.</span></span>

1.  <span data-ttu-id="f460b-135">Utilice el método **CreateIndex** en un objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="f460b-135">Use the **CreateIndex** method on a **TableDef** object.</span></span>

2.  <span data-ttu-id="f460b-136">Use el método **CreateField** del objeto **Index** para crear un objeto **Field** para cada campo (columna) que se va a incluir en el objeto **Index**.</span><span class="sxs-lookup"><span data-stu-id="f460b-136">Use the **CreateField** method on the **Index** object to create a **Field** object for each field (column) to be included in the **Index** object.</span></span>

3.  <span data-ttu-id="f460b-137">Establezca las propiedades de **Index** como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f460b-137">Set **Index** properties as needed.</span></span>

4.  <span data-ttu-id="f460b-138">Anexe el objeto **Field** a la colección **Fields**.</span><span class="sxs-lookup"><span data-stu-id="f460b-138">Append the **Field** object to the **Fields** collection.</span></span>

5.  <span data-ttu-id="f460b-139">Anexe el objeto **Index** a la colección **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="f460b-139">Append the **Index** object to the **Indexes** collection.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f460b-140">[!NOTA] Se omite la propiedad **Clustered** para las bases de datos que utilizan el motor de base de datos de Microsoft Access, que no admite índices agrupados.</span><span class="sxs-lookup"><span data-stu-id="f460b-140">The **Clustered** property is ignored for databases that use the Microsoft Access database engine, which doesn't support clustered indexes.</span></span>

## <a name="example"></a><span data-ttu-id="f460b-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f460b-141">Example</span></span>

<span data-ttu-id="f460b-p110">En este ejemplo se crea un nuevo objeto **Index**, se anexa a la colección **Indexes** del objeto **TableDef** de Empleados y se enumera la colección **Indexes** de **TableDef**. Por último, se enumera **Recordset**, utilizando primero el objeto **Index** principal y, luego, el nuevo objeto **Index**. Se requiere el procedimiento IndexOutput para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="f460b-p110">This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**. Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**. The IndexOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="f460b-p111">En este ejemplo se utiliza el método **CreateIndex** para crear dos nuevos objetos **Index** y anexarlos luego a la colección **Indexes** del objeto **TableDef** de Empleados. Enumera la colección **Indexes** del objeto **TableDef**, la colección **Fields** de los nuevos objetos **Index** y la colección Properties de los nuevos objetos **Index**. Se requiere la función CreateIndexOutput para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="f460b-p111">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.</span></span>

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
