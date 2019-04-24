---
title: Objeto Recordset (DAO)
TOCTitle: Recordset Object
ms:assetid: 9774232c-e6da-175b-fc7f-ed2ab7908fa0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197799(v=office.15)
ms:contentKeyID: 48546469
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 19999159f7987be87031f88d1eec87980585f369
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284521"
---
# <a name="recordset-object-dao"></a>Objeto Recordset (DAO)

**Se aplica a:** Access 2013, Office 2013

Un objeto **Recordset** representa los registros de una tabla base o los registros que son el resultado de ejecutar una consulta.

## <a name="remarks"></a>Comentarios

Los objetos **Recordset** se usan para manipular los datos de una base de datos en el nivel de registro. Al usar objetos DAO, los datos se manipulan casi por completo con objetos **Recordset**. Todos los objetos **Recordset** se construyen con registros (filas) y campos (columnas). Hay cinco tipos de objetos **Recordset**:

- Conjunto de registros de tipo tabla: la representación en código de una tabla base que puede utilizar para agregar, cambiar o eliminar registros de una sola tabla de base de datos (solo áreas de trabajo de Microsoft Access).

- Conjunto de registros de tipo conjunto de registros dinámicos: el resultado de una consulta que puede tener registros actualizables. Un objeto **Recordset** de tipo conjunto de registros dinámicos es un conjunto dinámico de registros que puede usar para agregar, cambiar o eliminar registros de una o varias tablas de base de datos subyacentes. Un objeto **Recordset** de tipo conjunto de registros dinámicos puede contener campos de una o varias tablas de una base de datos. Este tipo corresponde a un cursor de conjunto de claves ODBC.

- Conjunto de registros de tipo instantánea: una copia estática de un conjunto de registros que puede utilizar para buscar datos o generar informes. Un objeto **Recordset** de tipo instantánea puede contener campos de una o varias tablas de una base de datos, pero no se puede actualizar. Este tipo corresponde a un cursor estático ODBC.

- Conjunto de registros de tipo de solo avance: igual que el de tipo instantánea, con la excepción de que no se proporciona ningún cursor. Solo puede avanzar por los registros hacia delante. Mejora el rendimiento en las situaciones en las que solo es necesario pasar una vez por un conjunto de resultados. Este tipo corresponde a un cursor de solo avance ODBC.

- Conjunto de datos de tipo dinámico: un conjunto de resultados de una consulta a partir de una o más tablas cuyos registros puede agregar, cambiar o eliminar desde una consulta que devuelve filas. Además, los registros que agreguen, eliminen o editen otros usuarios en las tablas base también aparecerán en el **Recordset**. Este tipo corresponde a un cursor dinámico ODBC (solo áreas de trabajo de ODBCDirect).

> [!NOTE]
> Las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013. Utilice ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.

Puede elegir el tipo de objeto **Recordset** que quiere crear con el argumento tipo del método **OpenRecordset**.

En un área de trabajo de Microsoft Access, si no especifica ningún tipo, DAO tratará de crear el tipo de **Recordset** que tenga más funcionalidad disponible, empezando por tabla. Si este tipo no está disponible, DAO tratará de crear un objeto **Recordset** de tipo conjunto de registros dinámicos. Luego, de tipo instantánea y, por último, de tipo de solo avance.

En un área de trabajo de ODBCDirect, si no especifica ningún tipo, DAO tratará de crear el tipo de **Recordset** que tenga la respuesta de consulta más rápida, empezando por el tipo de solo avance. Si este tipo no está disponible, DAO tratará de crear un objeto **Recordset** de tipo instantánea. Luego, de tipo conjunto de registros dinámicos y, por último, de tipo dinámico.

Al crear un objeto **Recordset** con un objeto **[TableDef](tabledef-object-dao.md)** no vinculado en un área de trabajo de Microsoft Access, se crean objetos **Recordset** de tipo tabla. Con las tablas vinculadas y las tablas de bases de datos ODBC conectadas a un motor de base de datos de Microsoft Access, solo se pueden crear objetos **Recordset** de tipo conjunto de registros dinámicos o de tipo instantánea.

Cuando abra el objeto, se agregará automáticamente un nuevo objeto **Recordset** a la colección **Recordsets** y, cuando lo cierre, se quitará automáticamente.

> [!NOTE]
> Si usa variables para representar un objeto **Recordset** y el objeto **Database** que contiene el **Recordset**, asegúrese de que las variables tengan el mismo ámbito, o la misma duración. Por ejemplo, si declara una variable pública que representa un objeto **Recordset**, asegúrese de que la variable que representa al objeto **Database** que contiene el **Recordset** también es pública o está declarada en un procedimiento **Sub** o **Function** con la palabra clave **Static**.

Puede crear tantas variables de objeto **Recordset** como necesite. Varios objetos **Recordset** pueden acceder a las mismas tablas y consultas y a los mismos campos sin entrar en conflicto.

Los objetos **Recordset** de tipo conjunto de registros dinámicos, instantánea y de solo avance se almacenan en la memoria local. Si no hay suficiente espacio en la memoria local para almacenar los datos, el motor de base de datos de Microsoft Access guarda los datos adicionales en el espacio en disco de TEMP. Si este espacio se agota, se producirá un error capturable.

La colección predeterminada de un objeto **Recordset** es la colección **Fields**, y la propiedad predeterminada de un objeto **[Field](field-object-dao.md)** es la propiedad **[Value](field-value-property-dao.md)**. Aproveche estas opciones predeterminadas para simplificar el código.

Al crear un objeto **Recordset**, el objeto actual se coloca en el primer registro si hay algún registro. Si no hay ningún registro, el valor de la propiedad **RecordCount** será 0 y los valores de las propiedades **BOF** y **EOF** serán **True**.

Puede usar los métodos **MoveNext**, **MovePrevious**, **MoveFirst** y **MoveLast** para recolocar el registro actual. Los objetos **Recordset** de tipo de solo avance admiten únicamente el método **MoveNext**. Al usar los métodos Move para visitar cada registro (o “caminar” por el **Recordset**), puede usar las propiedades **BOF** y **EOF** para consultar el principio y el final del objeto **Recordset**.

Con los objetos **Recordset** de tipo conjunto de registros dinámicos y de tipo instantánea en un área de trabajo de Microsoft Access, puede usar también los métodos Find, como **FindFirst**, para buscar un determinado registro según ciertos criterios. Si no se encuentra el registro, la propiedad **NoMatch** se configurará como **True**. En el caso de los objetos **Recordset** de tipo tabla, puede examinar los registros con el método **Seek**.

La propiedad **Type** indica el tipo de objeto **Recordset** creado, y la propiedad **Updatable** indica si puede cambiar los registros del objeto.

La información sobre la estructura de una tabla base, como los nombres y los tipos de datos de cada objeto **Field** y los objetos **Index**, se almacena en un objeto **TableDef**.

Para hacer referencia a un objeto **Recordset** de una colección por su número ordinal o el valor de su propiedad **Name**, utilice cualquiera de las siguientes formas de sintaxis:

- **Recordsets**(0)

- **Recordsets**("nombre")

- **Recordsets**\!\[nombre\]

> [!NOTE]
> Puede abrir un objeto **Recordset** desde la misma base de datos o el mismo origen de datos varias veces, creando nombres duplicados en la colección **Recordsets**. Debe asignar objetos **Recordset** a variables de objeto y hacer referencia a ellos por el nombre de la variable.

## <a name="example"></a>Ejemplo

A continuación se ofrece una demostración de objetos **Recordset** y la colección **Recordsets**. En este ejemplo, se abren cuatro tipos diferentes de objetos **Recordsets**, se enumera la colección Recordsets del objeto **Database** actual y se enumera la colección **Properties** de cada objeto **Recordset**.

```vb
    Sub RecordsetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstTable As Recordset 
       Dim rstDynaset As Recordset 
       Dim rstSnapshot As Recordset 
       Dim rstForwardOnly As Recordset 
       Dim rstLoop As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
     
          ' Open one of each type of Recordset object. 
          Set rstTable = .OpenRecordset("Categories", _ 
             dbOpenTable) 
          Set rstDynaset = .OpenRecordset("Employees", _ 
             dbOpenDynaset) 
          Set rstSnapshot = .OpenRecordset("Shippers", _ 
             dbOpenSnapshot) 
          Set rstForwardOnly = .OpenRecordset _  
             ("Employees", dbOpenForwardOnly) 
     
          Debug.Print "Recordsets in Recordsets " & _ 
             "collection of dbsNorthwind" 
     
          ' Enumerate Recordsets collection. 
          For Each rstLoop In .Recordsets 
     
             With rstLoop 
                Debug.Print "  " & .Name 
     
                ' Enumerate Properties collection of each 
                ' Recordset object. Trap for any  
                ' properties whose values are invalid in  
                ' this context. 
                For Each prpLoop In .Properties 
                   On Error Resume Next 
                   If prpLoop <> "" Then Debug.Print _ 
                      "    " & prpLoop.Name & _ 
                      " = " & prpLoop 
                   On Error GoTo 0 
                Next prpLoop 
     
             End With 
     
          Next rstLoop 
     
          rstTable.Close 
          rstDynaset.Close 
          rstSnapshot.Close 
          rstForwardOnly.Close 
     
          .Close 
       End With 
     
    End Sub 
```

<br/>

En este ejemplo, se usa el método **OpenRecordset** para abrir cinco objetos **Recordset** diferentes y mostrar su contenido. El procedimiento OpenRecordsetOutput es necesario para ejecutar este procedimiento.

```vb
    Sub OpenRecordsetX() 
     
       Dim wrkAcc As Workspace 
       Dim wrkODBC As Workspace 
       Dim dbsNorthwind As Database 
       Dim conPubs As Connection 
       Dim rstTemp As Recordset 
       Dim rstTemp2 As Recordset 
     
       ' Open Microsoft Access and ODBCDirect workspaces, Microsoft  
       ' Access database, and ODBCDirect connection. 
       Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
       Set wrkODBC = CreateWorkspace("", "admin", "", dbUseODBC) 
       Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
        
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       Set conPubs = wrkODBC.OpenConnection("", , , _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
     
       ' Open five different Recordset objects and display the  
       ' contents of each. 
     
       Debug.Print "Opening forward-only-type recordset " & _ 
          "where the source is a QueryDef object..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "Ten Most Expensive Products", dbOpenForwardOnly) 
       OpenRecordsetOutput rstTemp 
     
       Debug.Print "Opening read-only dynaset-type " & _ 
          "recordset where the source is an SQL statement..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "SELECT * FROM Employees", dbOpenDynaset, dbReadOnly) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the Filter property to retrieve only certain  
       ' records with the next OpenRecordset call. 
       Debug.Print "Opening recordset from existing " & _ 
          "Recordset object to filter records..." 
       rstTemp.Filter = "LastName >= 'M'" 
       Set rstTemp2 = rstTemp.OpenRecordset() 
       OpenRecordsetOutput rstTemp2 
     
       Debug.Print "Opening dynamic-type recordset from " & _ 
          "an ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset( _ 
          "SELECT * FROM stores", dbOpenDynamic) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the StillExecuting property to determine when the  
       ' Recordset is ready for manipulation. 
       Debug.Print "Opening snapshot-type recordset based " & _ 
          "on asynchronous query to ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset("publishers", _ 
          dbOpenSnapshot, dbRunAsync) 
       Do While rstTemp.StillExecuting 
          Debug.Print "  [still executing...]" 
       Loop 
       OpenRecordsetOutput rstTemp 
     
       rstTemp.Close 
       dbsNorthwind.Close 
       conPubs.Close 
       wrkAcc.Close 
       wrkODBC.Close 
     
    End Sub 
     
    Sub OpenRecordsetOutput(rstOutput As Recordset) 
     
       ' Enumerate the specified Recordset object. 
       With rstOutput 
          Do While Not .EOF 
             Debug.Print , .Fields(0), .Fields(1) 
             .MoveNext 
          Loop 
       End With 
     
    End Sub 
```

<br/>

En este ejemplo, se abre un objeto **Recordset** de tipo dinámico y se enumeran sus registros.

```vb
    Sub dbOpenDynamicX() 
     
       Dim wrkMain As Workspace 
       Dim conMain As Connection 
       Dim qdfTemp As QueryDef 
       Dim rstTemp As Recordset 
       Dim strSQL As String 
       Dim intLoop As Integer 
     
       ' Create ODBC workspace and open connection to 
       ' SQL Server database. 
       Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
          "admin", "", dbUseODBC) 
           
       ' Note: The DSN referenced below must be configured to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server.     
       Set conMain = wrkMain.OpenConnection("Publishers", _ 
          dbDriverNoPrompt, False, _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
           
       ' Open dynamic-type recordset. 
       Set rstTemp = _ 
          conMain.OpenRecordset("authors", _ 
          dbOpenDynamic) 
     
       With rstTemp 
          Debug.Print "Dynamic-type recordset: " & .Name 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !au_lname & ", " & _ 
                !au_fname 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       conMain.Close 
       wrkMain.Close 
     
    End Sub 
```

<br/>

En este ejemplo, se abre un **Recordset** de tipo conjunto de registros dinámicos y se muestra hasta qué punto se pueden actualizar sus campos.

```vb
    Sub dbOpenDynasetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstInvoices As Recordset 
       Dim fldLoop As Field 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstInvoices = _ 
          dbsNorthwind.OpenRecordset("Invoices", dbOpenDynaset) 
     
       With rstInvoices 
          Debug.Print "Dynaset-type recordset: " & .Name 
     
          If .Updatable Then 
             Debug.Print "  Updatable fields:" 
     
             ' Enumerate Fields collection of dynaset-type 
             ' Recordset object, print only updatable 
             ' fields. 
             For Each fldLoop In .Fields 
                If fldLoop.DataUpdatable Then 
                   Debug.Print "    " & fldLoop.Name 
                End If 
             Next fldLoop 
     
          End If 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

En este ejemplo, se abre un **Recordset** de tipo de solo avance, se muestran sus características de solo lectura y se avanza por el **Recordset** con el método **MoveNext**.

```vb 
Sub dbOpenForwardOnlyX() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim fldLoop As Field 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   ' Open a forward-only-type Recordset object. Only the  
   ' MoveNext and Move methods may be used to navigate  
   ' through the recordset. 
   Set rstEmployees = _ 
      dbsNorthwind.OpenRecordset("Employees", _ 
      dbOpenForwardOnly) 
 
   With rstEmployees 
      Debug.Print "Forward-only-type recordset: " & _ 
         .Name & ", Updatable = " & .Updatable 
 
      Debug.Print "  Field - DataUpdatable" 
      ' Enumerate Fields collection, printing the Name and  
      ' DataUpdatable properties of each Field object. 
      For Each fldLoop In .Fields 
         Debug.Print "    " & _ 
            fldLoop.Name & " - " & fldLoop.DataUpdatable 
      Next fldLoop 
 
      Debug.Print "  Data" 
      ' Enumerate the recordset. 
      Do While Not .EOF 
         Debug.Print "    " & !FirstName & " " & _ 
            !LastName 
         .MoveNext 
      Loop 
 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
```

<br/>

En este ejemplo, se abre un **Recordset** de tipo instantánea y se muestran sus características de solo lectura.

```vb
    Sub dbOpenSnapshotX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          Debug.Print "Snapshot-type recordset: " & _ 
             .Name 
     
          ' Enumerate the Properties collection of the 
          ' snapshot-type Recordset object, trapping for 
          ' any properties whose values are invalid in  
          ' this context. 
          For Each prpLoop In .Properties 
             On Error Resume Next 
             Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
             On Error Goto 0 
          Next prpLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

En este ejemplo, se abre un **Recordset** de tipo tabla, se establece su propiedad **Index** y se enumeran sus registros.

```vb
    Sub dbOpenTableX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' dbOpenTable is default. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
     
       With rstEmployees 
          Debug.Print "Table-type recordset: " & .Name 
     
          ' Use predefined index. 
          .Index = "LastName" 
          Debug.Print "  Index = " & .Index 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !LastName & ", " & _ 
                !FirstName 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

El siguiente ejemplo muestra cómo usar el método Seek para encontrar un registro en una tabla vinculada.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```

<br/>

En el siguiente ejemplo, se muestra cómo abrir un Recordset basado en una consulta de parámetros.

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

En el siguiente ejemplo, se muestra cómo abrir un Recordset a partir de una tabla o una consulta.

```vb
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

En el siguiente ejemplo, se muestra cómo abrir un Recordset a partir de una instrucción del Lenguaje de consulta estructurado (SQL).

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

En el siguiente ejemplo, se muestra cómo usar los métodos FindFirst y FindNext para buscar un registro en un Recordset.

```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```

<br/>

En el siguiente ejemplo, se muestra cómo copiar los resultados de una consulta a una hoja de cálculo de un nuevo libro de Microsoft Excel.

```vb
    Public Sub CopyDataFromQuery( _
        xlApp As Excel.Application, _
        strQueryName As String)
    
        ' If the xlApp object exists
        If Not xlApp Is Nothing Then
        
            ' If the Workbook exists
            If xlApp.Workbooks.Count = 1 Then
            
                ' Create Recrodset Object from the Query
                Dim rsQuery As DAO.Recordset
                Set rsQuery = Application.CurrentDb.OpenRecordset(strQueryName)
                
                ' Get the Cells object
                Dim Cells As Object
                Set Cells = xlApp.Workbooks(1).ActiveSheet.Cells
                
                ' Copy the Data from the Query into the Sheet
                Cells.CopyFromRecordset rsQuery
                
            End If
        End If
    
    End Sub
```

