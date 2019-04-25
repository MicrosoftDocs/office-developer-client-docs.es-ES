---
title: Propiedad Recordset.Index (DAO)
TOCTitle: Index Property
ms:assetid: 54626de0-eb51-31f2-bf24-e29cbfbbaa02
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194103(v=office.15)
ms:contentKeyID: 48544895
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052906
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: f475635424cfb9ed8ddab4025d6a944bdedd39fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300528"
---
# <a name="recordsetindex-property-dao"></a>Propiedad Recordset.Index (DAO)

**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que indica el nombre del objeto actual **[Index](index-object-dao.md)** en un objeto de tipo de tabla **[Recordset](recordset-object-dao.md)** (solo en áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expression* .Index

*expression* Variable que representa un objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Los registros de tablas base no se almacenan en ningún orden concreto. Establecer la propiedad **Index** cambia el orden de los registros devueltos desde la base de datos. No afecta al orden en el que se almacenan los registros.

El objeto especificado **Index** debe estar ya definido. Si establece la propiedad **Index** en un objeto **Index** que no existe o si la propiedad **Index** no está establecida cuando se usa el método **[Seek](recordset-seek-method-dao.md)**, se produce un error capturable.

Examine la colección **Indexes** de un objeto **TableDef** para determinar qué objetos **Index** están disponibles para objetos de tipo de tabla **Recordset** creados a partir de ese objeto **TableDef**.

Puede crear un nuevo índice para la tabla creando un nuevo objeto **Index**, estableciendo sus propiedades, anexándolo a la colección **Indexes** del objeto subyacente **TableDef** y volviendo a abrir el objeto **Recordset**.

Los registros devueltos desde un objeto de tipo de tabla **Recordset** solo pueden ordenarse por los índices definidos en el objeto subyacente **TableDef**. Para ordenar los registros en cualquier otro orden, puede abrir un objeto **Recordset** de conjunto de registros dinámicos, de instantánea o de tipo de solo avance mediante una instrucción SQL con una cláusula ORDER BY.


> [!NOTE]
> - No tiene que crear índices para las tablas. Con grandes tablas sin índice, tener acceso a un registro específico o crear un objeto **Recordset** puede llevar mucho tiempo. Por otra parte, crear demasiados índices ralentiza las operaciones de actualización, anexión y eliminación porque todos los índices se actualizan automáticamente.
> - Los registros leídos desde tablas sin índices no se devuelven en secuencias concretas.
> - La propiedad **[Attributes](field-attributes-property-dao.md)** de cada objeto **[Field](field-object-dao.md)** que hay en el objeto **Index** determina el orden de los registros y en consecuencia las técnicas de acceso que se usarán para ese índice.
> - Un índice único ayuda a optimizar la búsqueda de registros.
> - Los índices no afectan al orden físico de una tabla base, solo afectan a cómo se obtiene acceso a los registros por el objeto de tipo de tabla **Recordset** cuando se elige un índice concreto o cuando **Recordset** se abre.


## <a name="example"></a>Ejemplo

Este ejemplo usa la propiedad **Index** para establecer diferentes órdenes de registro para un tipo de tabla **Recordset**.

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset 
       Dim idxLoop As Index 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
       Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
       With rstEmployees 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In tdfEmployees.Indexes 
             .Index = idxLoop.Name 
             Debug.Print "Index = " & .Index 
             Debug.Print "  EmployeeID - PostalCode - Name" 
             .MoveFirst 
     
             ' Enumerate Recordset to show the order of records. 
             Do While Not .EOF 
                Debug.Print "    " & !EmployeeID & " - " & _ 
                   !PostalCode & " - " & !FirstName & " " & _ 
                   !LastName 
                .MoveNext 
             Loop 
     
          Next idxLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Este ejemplo demuestra el método **Seek** al permitir al usuario buscar un producto según un número de ID.

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
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
