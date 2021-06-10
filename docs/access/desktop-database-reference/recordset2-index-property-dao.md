---
title: Propiedad Recordset2.Index (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 05a29ff9dbe720fe7c5539639b20e0abdc3c587b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307304"
---
# <a name="recordset2index-property-dao"></a>Propiedad Recordset2.Index (DAO)

**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que indica el nombre del objeto actual **[Index](index-object-dao.md)** en un objeto de tipo de tabla **[Recordset](recordset-object-dao.md)** (solo en áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expression* .Index

*expresión* Variable que representa un **objeto Recordset2.**

## <a name="remarks"></a>Comentarios

Los registros de tablas base no se almacenan en ningún orden concreto. Establecer la propiedad **Index** cambia el orden de los registros devueltos desde la base de datos. No afecta al orden en el que se almacenan los registros.

El objeto especificado **Index** debe estar ya definido. Si establece la propiedad **Index** en un objeto **Index** que no existe o si la propiedad **Index** no está establecida cuando se usa el método **[Seek](recordset2-seek-method-dao.md)**, se produce un error capturable.

Examine la colección **Indexes** de un objeto **TableDef** para determinar qué objetos **Index** están disponibles para objetos de tipo de tabla **Recordset** creados a partir de ese objeto **TableDef**.

Puede crear un nuevo índice para la tabla creando un nuevo objeto **Index**, estableciendo sus propiedades, anexándolo a la colección **Indexes** del objeto subyacente **TableDef** y volviendo a abrir el objeto **Recordset**.

Los registros devueltos desde un objeto de tipo de tabla **Recordset** solo pueden ordenarse por los índices definidos en el objeto subyacente **TableDef**. Para ordenar los registros en cualquier otro orden, puede abrir un objeto **Recordset** de conjunto de registros dinámicos, de instantánea o de tipo de solo avance mediante una instrucción SQL con una cláusula ORDER BY.

> [!NOTE]
> - No tiene que crear índices para las tablas. Con grandes tablas sin índice, tener acceso a un registro específico o crear un objeto **Recordset** puede llevar mucho tiempo. Por otra parte, crear demasiados índices ralentiza las operaciones de actualización, anexión y eliminación porque todos los índices se actualizan automáticamente.
> - Los registros leídos desde tablas sin índices no se devuelven en secuencias concretas.
> - La propiedad **[Attributes](field-attributes-property-dao.md)** de cada objeto **[Field](field-object-dao.md)** que hay en el objeto **Index** determina el orden de los registros y en consecuencia las técnicas de acceso que se usarán para ese índice.
> - Un índice único ayuda a optimizar la búsqueda de registros.
> - Los índices no afectan al orden físico de los índices de tablas base, solo afectan a cómo se tiene acceso a los registros mediante el objeto **Recordset** de tipo de tabla cuando se elige un índice concreto o cuando se abre **Recordset**.

## <a name="example"></a>Ejemplo

Este ejemplo usa la propiedad **Index** para establecer diferentes órdenes de registro para un tipo de tabla **Recordset**.

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset2 
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
       Dim rstProducts As Recordset2 
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
