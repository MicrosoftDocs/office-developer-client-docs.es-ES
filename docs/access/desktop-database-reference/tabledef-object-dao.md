---
title: Objeto TableDef (DAO)
TOCTitle: TableDef Object
ms:assetid: 715146b6-c62a-abff-28ee-e6bbe3c08adf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195790(v=office.15)
ms:contentKeyID: 48545582
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2670dadade6e934a1696251867d8ea67e8bbfc53
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927371"
---
# <a name="tabledef-object-dao"></a><span data-ttu-id="56260-102">Objeto TableDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="56260-102">TableDef object (DAO)</span></span>

<span data-ttu-id="56260-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56260-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56260-104">Un objeto **TableDef** representa la definición almacenada de una tabla base o una tabla vinculada (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="56260-104">A **TableDef** object represents the stored definition of a base table or a linked table (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="56260-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56260-105">Remarks</span></span>

<span data-ttu-id="56260-p101">La definición de una tabla se manipula con un objeto **TableDef** y sus métodos y propiedades. Por ejemplo, puede:</span><span class="sxs-lookup"><span data-stu-id="56260-p101">You manipulate a table definition using a **TableDef** object and its methods and properties. For example, you can:</span></span>

- <span data-ttu-id="56260-108">Examinar la estructura del índice y los campos de cualquier tabla local, vinculada o externa de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="56260-108">Examine the field and index structure of any local, linked, or external table in a database.</span></span>

- <span data-ttu-id="56260-109">Usar las propiedades **Connect** y **SourceTableName** para establecer o devolver información sobre las tablas vinculadas y utilizar el método **RefreshLink** para actualizar las conexiones con las tablas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="56260-109">Use the **Connect** and **SourceTableName** properties to set or return information about linked tables, and use the **RefreshLink** method to update connections to linked tables.</span></span>

- <span data-ttu-id="56260-110">Usar las propiedades **ValidationRule** y **ValidationText** para establecer o devolver las condiciones de validación.</span><span class="sxs-lookup"><span data-stu-id="56260-110">Use the **ValidationRule** and **ValidationText** properties to set or return validation conditions.</span></span>

- <span data-ttu-id="56260-111">Utilice el método **OpenRecordset** para crear una tabla –, Dynaset, dinámico, instantánea u objeto **Recordset** de tipo forward – only, según la definición de tabla.</span><span class="sxs-lookup"><span data-stu-id="56260-111">Use the **OpenRecordset** method to create a table–, dynaset–, dynamic–, snapshot–, or forward–only–type **Recordset** object, based on the table definition.</span></span>

<span data-ttu-id="56260-112">En las tablas base, la propiedad **RecordCount** contiene el número de registros de la tabla de base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="56260-112">For base tables, the **RecordCount** property contains the number of records in the specified database table.</span></span> <span data-ttu-id="56260-113">Para las tablas vinculadas, el valor de la propiedad **RecordCount** siempre es – 1.</span><span class="sxs-lookup"><span data-stu-id="56260-113">For linked tables, the **RecordCount** property setting is always –1.</span></span>

<span data-ttu-id="56260-114">Para crear un nuevo objeto **TableDef**, utilice el método **[CreateTableDef](database-createtabledef-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="56260-114">To create a new **TableDef** object, use the **[CreateTableDef](database-createtabledef-method-dao.md)** method.</span></span>

### <a name="to-add-a-field-to-a-table"></a><span data-ttu-id="56260-115">Para agregar un campo a una tabla</span><span class="sxs-lookup"><span data-stu-id="56260-115">To add a field to a table</span></span>

1.  <span data-ttu-id="56260-116">Compruebe que todos los objetos **[Recordset](recordset-object-dao.md)** que se basan en la tabla están cerrados.</span><span class="sxs-lookup"><span data-stu-id="56260-116">Make sure any **[Recordset](recordset-object-dao.md)** objects based on the table are all closed.</span></span>

2.  <span data-ttu-id="56260-117">Utilice el método **CreateField** para crear una variable de objeto **Field** y establecer sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="56260-117">Use the **CreateField** method to create a **Field** object variable and set its properties.</span></span>

3.  <span data-ttu-id="56260-118">Use el método **Append** para agregar el objeto **Field** a la colección **Fields** del objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="56260-118">Use the **Append** method to add the **Field** object to the **Fields** collection of the **TableDef** object.</span></span>

<span data-ttu-id="56260-119">Puede eliminar un objeto **Field** desde una colección **TableDefs** si no tiene ningún índice asignado, pero perderá los datos del campo.</span><span class="sxs-lookup"><span data-stu-id="56260-119">You can delete a **Field** object from a **TableDefs** collection if it doesn't have any indexes assigned to it, but you will lose the field's data.</span></span>

### <a name="to-create-a-table-that-is-ready-for-new-records-in-a-database"></a><span data-ttu-id="56260-120">Para crear una tabla lista para nuevos registros en una base de datos</span><span class="sxs-lookup"><span data-stu-id="56260-120">To create a table that is ready for new records in a database</span></span>

1.  <span data-ttu-id="56260-121">Utilice el método **CreateTableDef** para crear un objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="56260-121">Use the **CreateTableDef** method to create a **TableDef** object.</span></span>

2.  <span data-ttu-id="56260-122">Establezca sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="56260-122">Set its properties.</span></span>

3.  <span data-ttu-id="56260-123">Con cada campo de la tabla, use el método **CreateField** para crear una variable de objeto **Field** y establecer sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="56260-123">For each field in the table, use the **CreateField** method to create a **Field** object variable and set its properties.</span></span>

4.  <span data-ttu-id="56260-124">Use el método **Append** para agregar los campos a la colección **Fields** del objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="56260-124">Use the **Append** method to add the fields to the **Fields** collection of the **TableDef** object.</span></span>

5.  <span data-ttu-id="56260-125">Utilice el método **Append** para agregar el nuevo objeto **TableDef** a la colección **TableDefs** del objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="56260-125">Use the **Append** method to add the new **TableDef** object to the **TableDefs** collection of the **Database** object.</span></span>

<span data-ttu-id="56260-126">Las tablas vinculadas se conectan a la base de datos con las propiedades **SourceTableName** y **Connect** del objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="56260-126">A linked table is connected to the database by the **SourceTableName** and **Connect** properties of the **TableDef** object.</span></span>

### <a name="to-link-a-table-to-a-database"></a><span data-ttu-id="56260-127">Para vincular una tabla a una base de datos</span><span class="sxs-lookup"><span data-stu-id="56260-127">To link a table to a database</span></span>

1.  <span data-ttu-id="56260-128">Utilice el método **CreateTableDef** para crear un objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="56260-128">Use the **CreateTableDef** method to create a **TableDef** object.</span></span>

2.  <span data-ttu-id="56260-129">Establezca sus propiedades **Connect** y **SourceTableName** (y, si quiere, también la propiedad **Attributes** ).</span><span class="sxs-lookup"><span data-stu-id="56260-129">Set its **Connect** and **SourceTableName** properties (and optionally, its **Attributes** property).</span></span>

3.  <span data-ttu-id="56260-130">Use el método **Append** para agregarlo a la colección **TableDefs** de un objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="56260-130">Use the **Append** method to add it to the **TableDefs** collection of a **Database**.</span></span>

<span data-ttu-id="56260-131">Para hacer referencia a un objeto **TableDef** en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:</span><span class="sxs-lookup"><span data-stu-id="56260-131">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="56260-132">**Definiciones de tabla** (0)</span><span class="sxs-lookup"><span data-stu-id="56260-132">**TableDefs**(0)</span></span>

<span data-ttu-id="56260-133">**Definiciones de tabla** ("nombre")</span><span class="sxs-lookup"><span data-stu-id="56260-133">**TableDefs**("name")</span></span>

<span data-ttu-id="56260-134">**Definiciones de tabla**\!\[nombre\]</span><span class="sxs-lookup"><span data-stu-id="56260-134">**TableDefs**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="56260-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="56260-135">Example</span></span>

<span data-ttu-id="56260-p103">En este ejemplo, se crea un nuevo objeto **TableDef** y se anexa a la colección **TableDefs** del objeto de base de datos Northwind. Luego, se enumeran la colección **TableDefs** y la colección **Properties** del nuevo **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="56260-p103">This example creates a new **TableDef** object and appends it to the **TableDefs** collection of the Northwind Database object. It then enumerates the **TableDefs** collection and the **Properties** collection of the new **TableDef**.</span></span>

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="56260-138">En este ejemplo, se crea un nuevo objeto **TableDef** en la base de datos Northwind.</span><span class="sxs-lookup"><span data-stu-id="56260-138">This example creates a new **TableDef** object in the Northwind database.</span></span>

```vb 
Sub CreateTableDefX() 
 
   Dim dbsNorthwind As Database 
   Dim tdfNew As TableDef 
   Dim prpLoop As Property 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
   ' Create a new TableDef object. 
   Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
 
   With tdfNew 
      ' Create fields and append them to the new TableDef  
      ' object. This must be done before appending the  
      ' TableDef object to the TableDefs collection of the  
      ' Northwind database. 
      .Fields.Append .CreateField("FirstName", dbText) 
      .Fields.Append .CreateField("LastName", dbText) 
      .Fields.Append .CreateField("Phone", dbText) 
      .Fields.Append .CreateField("Notes", dbMemo) 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "before appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
      ' Append the new TableDef object to the Northwind  
      ' database. 
      dbsNorthwind.TableDefs.Append tdfNew 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "after appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
```

<br/>

<span data-ttu-id="56260-p104">En el siguiente ejemplo, se muestra cómo crear un campo calculado. El método CreateField crea un campo llamado **FullName**. Después, la propiedad Expression se configura con la expresión que calcula el valor del campo.</span><span class="sxs-lookup"><span data-stu-id="56260-p104">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="56260-142">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="56260-142">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```
