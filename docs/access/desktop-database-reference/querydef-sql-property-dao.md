---
title: QueryDef.SQL Property (DAO)
TOCTitle: SQL Property
ms:assetid: 16446789-c8be-bff0-eddd-b5f6a8530128
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845522(v=office.15)
ms:contentKeyID: 48543429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053054
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a8e33f1a22e1ffd6dffbb67b8bafd5fae78f39c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881618"
---
# <a name="querydefsql-property-dao"></a><span data-ttu-id="0dff1-102">QueryDef.SQL Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="0dff1-102">QueryDef.SQL Property (DAO)</span></span>

<span data-ttu-id="0dff1-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0dff1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0dff1-104">Establece o devuelve la instrucción SQL que define la consulta ejecutada por un objeto **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="0dff1-104">Sets or returns the SQL statement that defines the query executed by a **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dff1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0dff1-105">Syntax</span></span>

<span data-ttu-id="0dff1-106">*expresión* . SQL</span><span class="sxs-lookup"><span data-stu-id="0dff1-106">*expression* .SQL</span></span>

<span data-ttu-id="0dff1-107">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="0dff1-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dff1-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dff1-108">Remarks</span></span>

<span data-ttu-id="0dff1-p101">La propiedad **SQL** contiene la instrucción SQL que determina cómo se seleccionan, agrupan y ordenan los registros cuando ejecuta la consulta. Puede usar la consulta para seleccionar los registros que se incluyen en un objeto **[Recordset](recordset-object-dao.md)**. También puede definir consultas de acción para modificar datos sin que se devuelvan registros.</span><span class="sxs-lookup"><span data-stu-id="0dff1-p101">The **SQL** property contains the SQL statement that determines how records are selected, grouped, and ordered when you execute the query. You can use the query to select records to include in a **[Recordset](recordset-object-dao.md)** object. You can also define action queries to modify data without returning records.</span></span>

<span data-ttu-id="0dff1-p102">La sintaxis SQL utilizada en una consulta debe seguir el dialecto SQL del motor de la consulta, que está determinado por el tipo de trabajo. En un área de trabajo de Microsoft Access, use el dialecto SQL de Microsoft Access, a no ser que cree una consulta de paso a través SQL, en cuyo caso debe usar el dialecto del servidor. En un área de trabajo de ODBCDirect, use el dialecto SQL del servidor.</span><span class="sxs-lookup"><span data-stu-id="0dff1-p102">The SQL syntax used in a query must conform to the SQL dialect of the query engine, which is determined by the type of workspace. In a Microsoft Access workspace, use the Microsoft Access SQL dialect, unless you create an SQL pass-through query, in which case you should use the dialect of the server.</span></span>

<span data-ttu-id="0dff1-p103">Si la instrucción SQL incluye parámetros para la consulta, debe establecerlos antes de la ejecución. Mientras no se restablezcan los parámetros, se aplicarán los mismos valores de parámetros cada vez que se ejecute la consulta.</span><span class="sxs-lookup"><span data-stu-id="0dff1-p103">If the SQL statement includes parameters for the query, you must set these before execution. Until you reset the parameters, the same parameter values are applied each time you execute the query.</span></span>

<span data-ttu-id="0dff1-116">En un área de trabajo de Microsoft Access, el uso de un objeto **QueryDef** es el método preferido para realizar operaciones de paso a través SQL en orígenes de datos ODBC conectados al motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0dff1-116">In a Microsoft Access workspace, using a **QueryDef** object is the preferred way to perform SQL pass-through operations on Microsoft Access database engine-connected ODBC data sources.</span></span> <span data-ttu-id="0dff1-117">Al establecer la propiedad **[Connect](querydef-connect-property-dao.md)** del objeto **QueryDef** en un origen de datos ODBC, puede usar SQL sin base de datos de Microsoft Access en la consulta que se pasan al servidor externo.</span><span class="sxs-lookup"><span data-stu-id="0dff1-117">By setting the **QueryDef** object's **[Connect](querydef-connect-property-dao.md)** property to an ODBC data source, you can use non–Microsoft–Access–database SQL in the query to be passed to the external server.</span></span> <span data-ttu-id="0dff1-118">Por ejemplo, puede usar instrucciones TRANSACT SQL (con bases de datos de Microsoft SQL Server o de Sybase SQL Server) que, de otro modo, el motor de base de datos de Microsoft Access no procesaría.</span><span class="sxs-lookup"><span data-stu-id="0dff1-118">For example, you can use TRANSACT SQL statements (with Microsoft SQL Server or Sybase SQL Server databases), which the Microsoft Access database engine would otherwise not process.</span></span>

> [!NOTE]
> <span data-ttu-id="0dff1-119">Si se establece la propiedad en una cadena que se concatena con un valor no entero, y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strSQL = "PRICE &gt; " &amp; lngPrice y lngPrice = 125,50), se producirá un error cuando se Intente ejecutar el objeto **QueryDef** en una base de datos del motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0dff1-119">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when you try to execute the **QueryDef** object in a Microsoft Access database engine database.</span></span> <span data-ttu-id="0dff1-120">Esto se debe a que, durante la concatenación, el número se convertirá en una cadena que utiliza el carácter decimal predeterminado del sistema, y Microsoft Access SQL sólo acepta caracteres decimales anglosajones.</span><span class="sxs-lookup"><span data-stu-id="0dff1-120">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="0dff1-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0dff1-121">Example</span></span>

<span data-ttu-id="0dff1-p106">En este ejemplo se establece y se cambia la propiedad **SQL** de un objeto **QueryDef** temporal, y se comparan los resultados, para demostrar el uso de la propiedad **SQL**. Para que este procedimiento se ejecute se necesita la función SQLOutput.</span><span class="sxs-lookup"><span data-stu-id="0dff1-p106">This example demonstrates the **SQL** property by setting and changing the **SQL** property of a temporary **QueryDef** and comparing the results. The SQLOutput function is required for this procedure to run.</span></span>

```vb
    Sub SQLX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set qdfTemp = dbsNorthwind.CreateQueryDef("") 
     
       ' Open Recordset using temporary QueryDef object and  
       ' print report. 
       SQLOutput "SELECT * FROM Employees " & _ 
          "WHERE Country = 'USA' " & _ 
          "ORDER BY LastName", qdfTemp 
     
       ' Open Recordset using temporary QueryDef object and  
       ' print report. 
       SQLOutput "SELECT * FROM Employees " & _ 
          "WHERE Country = 'UK' " & _ 
          "ORDER BY LastName", qdfTemp 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Function SQLOutput(strSQL As String, qdfTemp As QueryDef) 
     
       Dim rstEmployees As Recordset 
     
       ' Set SQL property of temporary QueryDef object and open  
       ' a Recordset. 
       qdfTemp.SQL = strSQL 
       Set rstEmployees = qdfTemp.OpenRecordset 
     
       Debug.Print strSQL 
     
       With rstEmployees 
          ' Enumerate Recordset. 
          Do While Not .EOF 
             Debug.Print "  " & !FirstName & " " & _ 
                !LastName & ", " & !Country 
             .MoveNext 
          Loop 
          .Close 
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="0dff1-p107">En este ejemplo se usa el método **CopyQueryDef** para crear una copia de un objeto **QueryDef** a partir de un objeto **Recordset** existente, y se modifica la copia agregando una cláusula a la propiedad **SQL**. Cuando se crea un objeto **QueryDef** permanente, se pueden agregar espacios, puntos y coma o saltos de línea a la propiedad **SQL**; estos caracteres adicionales se deben quitar antes de anexar cláusulas nuevas a la instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="0dff1-p107">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the **SQL** property. When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the **SQL** property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
       strAdd As String) As QueryDef 
     
       Dim strSQL As String 
       Dim strRightSQL As String 
     
       Set CopyQueryNew = rstTemp.CopyQueryDef 
       With CopyQueryNew 
          ' Strip extra characters. 
          strSQL = .SQL 
          strRightSQL = Right(strSQL, 1) 
          Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
                strRightSQL = Chr(10) Or strRightSQL = vbCr 
             strSQL = Left(strSQL, Len(strSQL) - 1) 
             strRightSQL = Right(strSQL, 1) 
          Loop 
          .SQL = strSQL & strAdd 
       End With 
     
    End Function 
     
    This example shows a possible use of CopyQueryNew(). 
     
    Sub CopyQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfEmployees As QueryDef 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
       Dim strOrderBy As String 
       Dim qdfCopy As QueryDef 
       Dim rstCopy As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
          "NewQueryDef", "SELECT FirstName, LastName, " & _ 
          "BirthDate FROM Employees") 
       Set rstEmployees = qdfEmployees.OpenRecordset( _ 
          dbOpenForwardOnly) 
     
       Do While True 
          intCommand = Val(InputBox( _ 
             "Choose field on which to order a new " & _ 
             "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
             "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
             "[Cancel - exit]")) 
          Select Case intCommand 
             Case 1 
                strOrderBy = " ORDER BY FirstName" 
             Case 2 
                strOrderBy = " ORDER BY LastName" 
             Case 3 
                strOrderBy = " ORDER BY BirthDate" 
             Case Else 
                Exit Do 
          End Select 
          Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
          Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
             dbForwardOnly) 
          With rstCopy 
             Do While Not .EOF 
                Debug.Print !LastName & ", " & !FirstName & _ 
                   " - " & !BirthDate 
                .MoveNext 
             Loop 
             .Close 
          End With 
          Exit Do 
       Loop 
     
       rstEmployees.Close 
       ' Delete new QueryDef because this is a demonstration. 
       dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="0dff1-p108">En este ejemplo se usan los métodos **CreateQueryDef** y **OpenRecordset** y la propiedad **SQL** para realizar una consulta en la tabla de títulos de la base de datos de ejemplo Pubs de Microsoft SQL Server y devolver el título y el identificador de título del libro más vendido. A continuación, se realiza una consulta en la tabla de autores y se indica al usuario que envíe una prima a cada autor en función de su porcentaje de derechos de autor (la prima total es de 1.000 dólares y cada autor debe recibir un porcentaje de ese importe).</span><span class="sxs-lookup"><span data-stu-id="0dff1-p108">This example uses the **CreateQueryDef** and **OpenRecordset** methods and the **SQL** property to query the table of titles in the Microsoft SQL Server sample database Pubs and return the title and title identifier of the best-selling book. The example then queries the table of authors and instructs the user to send a bonus check to each author based on his or her royalty share (the total bonus is $1,000 and each author should receive a percentage of that amount).</span></span>

```vb
    Sub ClientServerX2() 
     
       Dim dbsCurrent As Database 
       Dim qdfBestSellers As QueryDef 
       Dim qdfBonusEarners As QueryDef 
       Dim rstTopSeller As Recordset 
       Dim rstBonusRecipients As Recordset 
       Dim strAuthorList As String 
     
       ' Open a database from which QueryDef objects can be  
       ' created. 
       Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
       ' Create a temporary QueryDef object to retrieve 
       ' data from a Microsoft SQL Server database. 
       Set qdfBestSellers = dbsCurrent.CreateQueryDef("") 
       With qdfBestSellers 
          ' Note: The DSN referenced below must be configured to  
          '       use Microsoft Windows NT Authentication Mode to  
          '       authorize user access to the Microsoft SQL Server. 
          .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
          .SQL = "SELECT title, title_id FROM titles " & _ 
             "ORDER BY ytd_sales DESC" 
          Set rstTopSeller = .OpenRecordset() 
          rstTopSeller.MoveFirst 
       End With 
     
       ' Create a temporary QueryDef to retrieve data from 
       ' a Microsoft SQL Server database based on the results from 
       ' the first query. 
       Set qdfBonusEarners = dbsCurrent.CreateQueryDef("") 
       With qdfBonusEarners 
          ' Note: The DSN referenced below must be configured to  
          '       use Microsoft Windows NT Authentication Mode to  
          '       authorize user access to the Microsoft SQL Server. 
          .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
          .SQL = "SELECT * FROM titleauthor " & _ 
             "WHERE title_id = '" & _ 
             rstTopSeller!title_id & "'" 
          Set rstBonusRecipients = .OpenRecordset() 
       End With 
     
       ' Build the output string. 
       With rstBonusRecipients 
          Do While Not .EOF 
             strAuthorList = strAuthorList & "  " & _ 
                !au_id & ":  $" & (10 * !royaltyper) & vbCr 
             .MoveNext 
          Loop 
       End With 
     
       ' Display results. 
       MsgBox "Please send a check to the following " & _ 
          "authors in the amounts shown:" & vbCr & _ 
          strAuthorList & "for outstanding sales of " & _ 
          rstTopSeller!Title & "." 
     
       rstTopSeller.Close 
       dbsCurrent.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="0dff1-128">En el siguiente ejemplo se muestra cómo crear una consulta de parámetro.</span><span class="sxs-lookup"><span data-stu-id="0dff1-128">The following example shows how to create a parameter query.</span></span> <span data-ttu-id="0dff1-129">Se crea una consulta denominada **myQuery** con dos parámetros, denominados Param1 y parámetro2.</span><span class="sxs-lookup"><span data-stu-id="0dff1-129">A query named **myQuery** is created with two parameters, named Param1 and Param2.</span></span> <span data-ttu-id="0dff1-130">Para ello, la propiedad SQL de la consulta está configurada en una instrucción Lenguaje de consulta estructurado (SQL) que define los parámetros.</span><span class="sxs-lookup"><span data-stu-id="0dff1-130">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="0dff1-131">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="0dff1-131">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateQueryWithParameters()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
        Dim strSQL As String
    
        Set dbs = CurrentDb
        Set qdf = dbs.CreateQueryDef("myQuery")
        Application.RefreshDatabaseWindow
    
        strSQL = "PARAMETERS Param1 TEXT, Param2 INT; "
        strSQL = strSQL & "SELECT * FROM [Table1] "
        strSQL = strSQL & "WHERE [Field1] = [Param1] AND [Field2] = [Param2];"
        qdf.SQL = strSQL
    
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="0dff1-132">En el siguiente ejemplo se muestra cómo reemplazar la instrucción de Lenguaje de consulta estructurado (SQL) en una consulta guardada.</span><span class="sxs-lookup"><span data-stu-id="0dff1-132">The following example shows how to replace the Structured Query Language (SQL) statement in a saved query.</span></span>

```vb
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
