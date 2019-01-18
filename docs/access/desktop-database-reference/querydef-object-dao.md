---
title: Objeto QueryDef (DAO)
TOCTitle: QueryDef Object
ms:assetid: 0b3d901c-345d-42a2-f5f1-fb09cc562e27
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845129(v=office.15)
ms:contentKeyID: 48543169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a94d34a2dbe8043e6db637b649f59047cf3f1dda
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713558"
---
# <a name="querydef-object-dao"></a><span data-ttu-id="21ede-102">Objeto QueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="21ede-102">QueryDef object (DAO)</span></span>

<span data-ttu-id="21ede-103">**Se aplica a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="21ede-103">**Applies to:** Access 2013 | Office 2013</span></span> 

<span data-ttu-id="21ede-104">Un objeto **QueryDef** es una definición de una consulta almacenada en una base de datos del motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="21ede-104">A **QueryDef** object is a stored definition of a query in a Microsoft Access database engine database.</span></span>

## <a name="remarks"></a><span data-ttu-id="21ede-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21ede-105">Remarks</span></span>

<span data-ttu-id="21ede-p101">Puede usar el objeto **QueryDef** para definir una consulta. Por ejemplo, puede:</span><span class="sxs-lookup"><span data-stu-id="21ede-p101">You can use the **QueryDef** object to define a query. For example, you can:</span></span>

- <span data-ttu-id="21ede-108">Usar la propiedad **SQL** para configurar o devolver la definición de la consulta.</span><span class="sxs-lookup"><span data-stu-id="21ede-108">Use the **SQL** property to set or return the query definition.</span></span>

- <span data-ttu-id="21ede-109">Usar la colección **Parameters** del objeto **QueryDef** para configurar o devolver parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="21ede-109">Use the **QueryDef** object's **Parameters** collection to set or return query parameters.</span></span>

- <span data-ttu-id="21ede-110">Usar la propiedad **Type** para devolver un valor que indique si la consulta selecciona registros de una tabla existente, crea una tabla nueva, inserta registros de una tabla en otra, elimina registros o los actualiza.</span><span class="sxs-lookup"><span data-stu-id="21ede-110">Use the **Type** property to return a value indicating whether the query selects records from an existing table, makes a new table, inserts records from one table into another table, deletes records, or updates records.</span></span>

- <span data-ttu-id="21ede-111">Usar la propiedad **MaxRecords** para limitar el número de registros que devuelve una consulta.</span><span class="sxs-lookup"><span data-stu-id="21ede-111">Use the **MaxRecords** property to limit the number of records returned from a query.</span></span>

- <span data-ttu-id="21ede-p102">Usar la propiedad **ODBCTimeout** para indicar cuánto tiempo se debe esperar a que la consulta devuelva registros. La propiedad **ODBCTimeout** se aplica a cualquier consulta que tenga acceso a datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="21ede-p102">Use the **ODBCTimeout** property to indicate how long to wait before the query returns records. The **ODBCTimeout** property applies to any query that accesses ODBC data.</span></span>

- <span data-ttu-id="21ede-p103">Usar la propiedad **ReturnsRecords** para indicar que la consulta devuelve registros. La propiedad **ReturnsRecords** solo es válida en consultas SQL de paso a través.</span><span class="sxs-lookup"><span data-stu-id="21ede-p103">Use the **ReturnsRecords** property to indicate that the query returns records. The **ReturnsRecords** property is only valid on SQL pass-through queries.</span></span>

- <span data-ttu-id="21ede-116">Usar la propiedad **Connect** para crear una consulta SQL de paso a través en una base de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="21ede-116">Use the **Connect** property to make an SQL pass-through query to an ODC database.</span></span>

<span data-ttu-id="21ede-p104">También se pueden crear objetos **QueryDef** temporales. A diferencia de los objetos **QueryDef** permanentes, los objetos **QueryDef** temporales no se guardan en el disco ni se anexan a la colección **QueryDefs**. Los objetos **QueryDef** temporales son útiles para las consultas que se deben ejecutar de forma repetida en tiempo de ejecución pero que no es necesario guardar en el disco, especialmente si se crean las instrucciones SQL en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="21ede-p104">You can also create temporary **QueryDef** objects. Unlike permanent **QueryDef** objects, temporary **QueryDef** objects are not saved to disk or appended to the **QueryDefs** collection. Temporary **QueryDef** objects are useful for queries that you must run repeatedly during run time but do not not need to save to disk, particularly if you create their SQL statements during run time.</span></span>

<span data-ttu-id="21ede-p105">Puede considerar un objeto **QueryDef** permanente de un área de trabajo de Microsoft Access como una instrucción SQL compilada. Si ejecuta una consulta desde un objeto **QueryDef** permanente, la consulta se ejecutará más rápidamente que si ejecuta la instrucción SQL equivalente desde el método **OpenRecordset**. Esto se debe a que el motor de base de datos de Microsoft Access no necesita compilar la consulta antes de ejecutarla.</span><span class="sxs-lookup"><span data-stu-id="21ede-p105">You can think of a permanent **QueryDef** object in a Microsoft Access workspace as a compiled SQL statement. If you execute a query from a permanent **QueryDef** object, the query will run faster than if you run the equivalent SQL statement from the **OpenRecordset** method. This is because the Microsoft Access database engine doesn't need to compile the query before executing it.</span></span>

<span data-ttu-id="21ede-p106">La forma preferida de usar el dialecto SQL nativo de un motor de base de datos externo al que se accede a través del motor de base de datos de Microsoft Access es mediante objetos **QueryDef**. Por ejemplo, puede crear una consulta de Microsoft SQL Server y almacenarla en un objeto **QueryDef**. Cuando necesite usar una consulta SQL de un motor de base de datos que no sea de Microsoft Access, deberá proporcionar una cadena de propiedad **Connect** que apunte al origen de datos externo. Las consultas con propiedades **Connect** válidas omiten el motor de base de datos de Microsoft Access y pasan la consulta directamente al servidor de base de datos externo para procesarla.</span><span class="sxs-lookup"><span data-stu-id="21ede-p106">The preferred way to use the native SQL dialect of an external database engine accessed through the Microsoft Access database engine is through **QueryDef** objects. For example, you can create a Microsoft SQL Server query and store it in a **QueryDef** object. When you need to use a non-Microsoft Access database engine SQL query, you must provide a **Connect** property string that points to the external data source. Queries with valid **Connect** properties bypass the Microsoft Access database engine and pass the query directly to the external database server for processing.</span></span>

<span data-ttu-id="21ede-127">Para crear un objeto **QueryDef** nuevo, use el método **CreateQueryDef**.</span><span class="sxs-lookup"><span data-stu-id="21ede-127">To create a new **QueryDef** object, use the **CreateQueryDef** method.</span></span> <span data-ttu-id="21ede-128">En un área de trabajo de Microsoft Access, si proporciona una cadena para el argumento name o si establece explícitamente la propiedad **Name** del nuevo objeto **QueryDef** en una cadena de longitud – cero, va a crear un **objeto QueryDef** permanente que se va a automáticamente se anexa a la colección **QueryDefs** y se guardan en el disco.</span><span class="sxs-lookup"><span data-stu-id="21ede-128">In a Microsoft Access workspace, if you supply a string for the name argument or if you explicitly set the **Name** property of the new **QueryDef** object to a non–zero-length string, you will create a permanent **QueryDef** that will automatically be appended to the **QueryDefs** collection and saved to disk.</span></span> <span data-ttu-id="21ede-129">Proporciona una cadena de longitud cero como el argumento de nombre o establecer explícitamente la propiedad **Name** en una cadena de longitud cero se producirá en un objeto **QueryDef** temporal.</span><span class="sxs-lookup"><span data-stu-id="21ede-129">Supplying a zero-length string as the name argument or explicitly setting the **Name** property to a zero-length string will result in a temporary **QueryDef** object.</span></span>

<span data-ttu-id="21ede-130">Para hacer referencia a un objeto **QueryDef** en una colección por su número ordinal o por la configuración de la propiedad **Nombre**, use cualquiera de las siguientes formas de sintaxis:</span><span class="sxs-lookup"><span data-stu-id="21ede-130">To refer to a **QueryDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="21ede-131">QueryDefs(0)</span><span class="sxs-lookup"><span data-stu-id="21ede-131">QueryDefs(0)</span></span>

<span data-ttu-id="21ede-132">QueryDefs("name")</span><span class="sxs-lookup"><span data-stu-id="21ede-132">QueryDefs("name")</span></span>

<span data-ttu-id="21ede-133">QueryDefs\! \[ nombre\]</span><span class="sxs-lookup"><span data-stu-id="21ede-133">QueryDefs\!\[ name\]</span></span>

<span data-ttu-id="21ede-134">Puede hacer referencia a objetos **QueryDef** temporales solo por las variables de objeto que les haya asignado.</span><span class="sxs-lookup"><span data-stu-id="21ede-134">You can refer to temporary **QueryDef** objects only by the object variables that you have assigned to them.</span></span>

<span data-ttu-id="21ede-135">**Vínculo proporcionado por** la Comunidad [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="21ede-135">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="21ede-136">UtterAccess es el principal foro de ayuda y wiki de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="21ede-136">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="21ede-137">Consultas: documentar SQL en Word</span><span class="sxs-lookup"><span data-stu-id="21ede-137">Queries: Document SQL to Word</span></span>](https://www.utteraccess.com/wiki/index.php/queries:_document_sql_to_word)

## <a name="example"></a><span data-ttu-id="21ede-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21ede-138">Example</span></span>

<span data-ttu-id="21ede-p109">En este ejemplo se crea un nuevo objeto **QueryDef** y se anexa a la colección **QueryDefs** del objeto **Base de datos** de Northwind. Luego se enumera la colección **QueryDefs** y la colección **Propiedades** del nuevo **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="21ede-p109">This example creates a new **QueryDef** object and appends it to the **QueryDefs** collection of the Northwind **Database** object. It then enumerates the **QueryDefs** collection and the **Properties** collection of the new **QueryDef**.</span></span>

```vb
    Sub QueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfNew As QueryDef 
       Dim qdfLoop As QueryDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new QueryDef object. Because it has a  
       ' name, it is automatically appended to the  
       ' QueryDefs collection. 
       Set qdfNew = dbsNorthwind.CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
     
       With dbsNorthwind 
          Debug.Print .QueryDefs.Count & _ 
             " QueryDefs in " & .Name 
     
          ' Enumerate QueryDefs collection. 
          For Each qdfLoop In .QueryDefs 
             Debug.Print "  " & qdfLoop.Name 
          Next qdfLoop 
     
          With qdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new  
             ' QueryDef object. 
             For Each prpLoop In .Properties 
                On Error Resume Next 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
                On Error Goto 0 
             Next prpLoop 
          End With 
     
          ' Delete new QueryDef because this is a  
          ' demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="21ede-p110">En este ejemplo se usa el método **CreateQueryDef** para crear y ejecutar un **QueryDef** temporal y otro permanente. La función GetrstTemp es necesaria para que se ejecute este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="21ede-p110">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**. The GetrstTemp function is required for this procedure to run.</span></span>

```vb
    Sub CreateQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim qdfNew As QueryDef 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
          ' Create temporary QueryDef. 
          Set qdfTemp = .CreateQueryDef("", _ 
             "SELECT * FROM Employees") 
          ' Open Recordset and print report. 
          GetrstTemp qdfTemp 
          ' Create permanent QueryDef. 
          Set qdfNew = .CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
          ' Open Recordset and print report. 
          GetrstTemp qdfNew 
          ' Delete new QueryDef because this is a demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
     
    Function GetrstTemp(qdfTemp As QueryDef) 
     
       Dim rstTemp As Recordset 
     
       With qdfTemp 
          Debug.Print .Name 
          Debug.Print "  " & .SQL 
          ' Open Recordset from QueryDef. 
          Set rstTemp = .OpenRecordset(dbOpenSnapshot) 
     
          With rstTemp 
             ' Populate Recordset and print number of records. 
             .MoveLast 
             Debug.Print "  Number of records = " & _ 
                .RecordCount 
             Debug.Print 
             .Close 
          End With 
     
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="21ede-143">En el siguiente ejemplo se muestra cómo reemplazar la instrucción de Lenguaje de consulta estructurado (SQL) en una consulta guardada.</span><span class="sxs-lookup"><span data-stu-id="21ede-143">The following example shows how to replace the Structured Query Language (SQL) statement in a saved query.</span></span>

<span data-ttu-id="21ede-144">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="21ede-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    ‘To change the Where clause in a saved query  
    Dim qdf as QueryDef
    Dim db as Database
    Set db = CurrentDB
    Set qdf = db.QueryDefs("YourQueryName")
    qdf.SQL = ReplaceWhereClause(qdf.SQL, strYourNewWhereClause)
    set qdf = Nothing
    set db = Nothing
    
    Public Function ReplaceWhereClause(strSQL As Variant, strNewWHERE As Variant)
    On Error GoTo Error_Handler
    
    ‘This subroutine accepts a valid SQL string and Where clause, and
    ‘returns the same SQL statement with the original Where clause (if any)
    ‘replaced by the passed in Where clause.
    ‘
    ‘INPUT:
    ‘ strSQL valid SQL string to change
    ‘OUTPUT:
    ‘ strNewWHERE New WHERE clause to insert into SQL statement
    ‘
        Dim strSELECT As String, strWhere As String
        Dim strOrderBy As String, strGROUPBY As String, strHAVING As String
    
        Call ParseSQL(strSQL, strSELECT, strWhere, strOrderBy, _
            strGROUPBY, strHAVING)
    
        ReplaceWhereClause = strSELECT &""& strNewWHERE &""_
            & strGROUPBY &""& strHAVING &""& strOrderBy
    
        Exit_Procedure:
            Exit Function
    
        Error_Handler:
            MsgBox (Err.Number & ": " & Err.Description)
            Resume Exit_Procedure
    
    End Function
```

