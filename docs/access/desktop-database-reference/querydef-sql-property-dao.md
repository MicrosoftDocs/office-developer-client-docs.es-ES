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
ms.openlocfilehash: dfe5581e863dbb83cbb46514b247c51721698671
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483622"
---
# <a name="querydefsql-property-dao"></a>QueryDef.SQL Property (DAO)

**Se aplica a**: Access 2013 | Office 2013

Establece o devuelve la instrucción SQL que define la consulta ejecutada por un objeto **[QueryDef](querydef-object-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . SQL

*expresión* Variable que representa un objeto **QueryDef** .

## <a name="remarks"></a>Observaciones

La propiedad **SQL** contiene la instrucción SQL que determina cómo se seleccionan, agrupan y ordenan los registros cuando ejecuta la consulta. Puede usar la consulta para seleccionar los registros que se incluyen en un objeto **[Recordset](recordset-object-dao.md)**. También puede definir consultas de acción para modificar datos sin que se devuelvan registros.

La sintaxis SQL utilizada en una consulta debe seguir el dialecto SQL del motor de la consulta, que está determinado por el tipo de trabajo. En un área de trabajo de Microsoft Access, use el dialecto SQL de Microsoft Access, a no ser que cree una consulta de paso a través SQL, en cuyo caso debe usar el dialecto del servidor. En un área de trabajo de ODBCDirect, use el dialecto SQL del servidor.

Si la instrucción SQL incluye parámetros para la consulta, debe establecerlos antes de la ejecución. Mientras no se restablezcan los parámetros, se aplicarán los mismos valores de parámetros cada vez que se ejecute la consulta.

En un área de trabajo de Microsoft Access, el uso de un objeto **QueryDef** es el método preferido para realizar operaciones de paso a través SQL en orígenes de datos ODBC conectados al motor de base de datos de Microsoft Access. Al establecer la propiedad **[Connect](querydef-connect-property-dao.md)** del objeto **QueryDef** en un origen de datos ODBC, puede usar SQL sin base de datos de Microsoft Access en la consulta que se pasan al servidor externo. Por ejemplo, puede usar instrucciones TRANSACT SQL (con bases de datos de Microsoft SQL Server o de Sybase SQL Server) que, de otro modo, el motor de base de datos de Microsoft Access no procesaría.

> [!NOTE]
> Si se establece la propiedad en una cadena que se concatena con un valor no entero, y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strSQL = "PRICE &gt; " &amp; lngPrice y lngPrice = 125,50), se producirá un error cuando se Intente ejecutar el objeto **QueryDef** en una base de datos del motor de base de datos de Microsoft Access. Esto se debe a que, durante la concatenación, el número se convertirá en una cadena que utiliza el carácter decimal predeterminado del sistema, y Microsoft Access SQL sólo acepta caracteres decimales anglosajones.

## <a name="example"></a>Ejemplo

En este ejemplo se establece y se cambia la propiedad **SQL** de un objeto **QueryDef** temporal, y se comparan los resultados, para demostrar el uso de la propiedad **SQL**. Para que este procedimiento se ejecute se necesita la función SQLOutput.

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

En este ejemplo se usa el método **CopyQueryDef** para crear una copia de un objeto **QueryDef** a partir de un objeto **Recordset** existente, y se modifica la copia agregando una cláusula a la propiedad **SQL**. Cuando se crea un objeto **QueryDef** permanente, se pueden agregar espacios, puntos y coma o saltos de línea a la propiedad **SQL**; estos caracteres adicionales se deben quitar antes de anexar cláusulas nuevas a la instrucción SQL.

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

En este ejemplo se usan los métodos **CreateQueryDef** y **OpenRecordset** y la propiedad **SQL** para realizar una consulta en la tabla de títulos de la base de datos de ejemplo Pubs de Microsoft SQL Server y devolver el título y el identificador de título del libro más vendido. A continuación, se realiza una consulta en la tabla de autores y se indica al usuario que envíe una prima a cada autor en función de su porcentaje de derechos de autor (la prima total es de 1.000 dólares y cada autor debe recibir un porcentaje de ese importe).

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

En el siguiente ejemplo se muestra cómo crear una consulta de parámetro. Se crea una consulta denominada **myQuery** con dos parámetros, denominados Param1 y parámetro2. Para ello, la propiedad SQL de la consulta está configurada en una instrucción Lenguaje de consulta estructurado (SQL) que define los parámetros.

**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

En el siguiente ejemplo se muestra cómo reemplazar la instrucción de Lenguaje de consulta estructurado (SQL) en una consulta guardada.

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
