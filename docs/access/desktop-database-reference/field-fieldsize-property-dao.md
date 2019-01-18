---
title: Propiedad Field.FieldSize (DAO)
TOCTitle: FieldSize Property
ms:assetid: c81bd5cb-6b7c-5390-2d6b-049143f2f3b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823165(v=office.15)
ms:contentKeyID: 48547645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 68a1b354b27515dd855703b9bf6344e4a9e90d7b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712795"
---
# <a name="fieldfieldsize-property-dao"></a>Propiedad Field.FieldSize (DAO)


**Se aplica a**: Access 2013, Office 2013


Devuelve el número de bytes usados en la base de datos (en lugar de en la memoria) de un objeto Memo o Long Binary **[Field](field-object-dao.md)** en la colección **[Fields](fields-collection-dao.md)** de un objeto **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . TamañoDelCampo

*expresión* Variable que representa un objeto **Field** .

## <a name="remarks"></a>Observaciones

Puede utilizar **FieldSize** con los métodos **[AppendChunk](field-appendchunk-method-dao.md)** y **[GetChunk](field-getchunk-method-dao.md)** para manipular campos grandes.

Como el tamaño de un campo Long Binary o Memo puede ser mayor de 64K, debería asignar el valor que devuelve **FieldSize** a una variable lo suficientemente grande como para almacenar una variable **Long**.

Para determinar el tamaño de un objeto **Field** distinto de los tipos Memo y Long Binary, utilice la propiedad **[Size](field-size-property-dao.md)**.

  - Si el servidor de base de datos o el controlador ODBC no admiten cursores de servidor.

  - Si está utilizando la biblioteca de cursores ODBC (es decir, la propiedad **DefaultCursorDriver** está establecida en **dbUseODBC** o en **dbUseDefault** cuando el servidor no admite cursores de servidor).

  - Si está utilizando una consulta sin cursor (es decir, la propiedad **DefaultCursorDriver** está establecida en **dbUseNoCursor**).

La propiedad **FieldSize** y las funciones VBA **Len()** o **LenB()** pueden devolver valores distintos como longitud de una misma cadena. Las cadenas se almacenan en una base de datos de Microsoft Access con formato de juego de caracteres de varios bytes (MBCS), pero expuesta a través de VBA con formato Unicode. Como resultado, la función **Len()** siempre devolverá el número de caracteres, **LenB** siempre devolverá el número de caracteres X 2 (Unicode utiliza dos bytes por cada carácter), pero **FieldSize** devolverá algún valor intermedio si la cadena contiene cualquiera de los caracteres MBCS. Por ejemplo, en una cadena que consta de tres caracteres normales y dos caracteres MBCS, **Len()** devolverá 5, **LenB()** devolverá 10 y **FieldSize** devolverá 7, la suma de 1 por cada carácter normal y 2 por cada carácter MBCS.

## <a name="example"></a>Ejemplo

En este ejemplo se utiliza la propiedad **FieldSize** para enumerar el número de bytes utilizados en los objetos Memo y Long Binary Field en dos tablas distintas.

```vb
    Sub FieldSizeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenDynaset) 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     Debug.Print _ 
     "Field sizes from records in Categories table" 
     
     With rstCategories 
     Debug.Print " CategoryName - " & _ 
     "Description (bytes) - Picture (bytes)" 
     
     ' Enumerate the Categories Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !CategoryName & " - " & _ 
     !Description.FieldSize & " - " & _ 
     !Picture.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     Debug.Print "Field sizes from records in Employees table" 
     
     With rstEmployees 
     Debug.Print " LastName - Notes (bytes) - " & _ 
     "Photo (bytes)" 
     
     ' Enumerate the Employees Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & " - " & _ 
     !Notes.FieldSize & " - " & !Photo.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

En este ejemplo se utilizan los métodos **AppendChunk** y **GetChunk** para rellenar un campo de objeto OLE con datos de otro registro, 32 K cada vez. En una aplicación real, se podría utilizar un procedimiento como éste para copiar un registro de empleado (incluida la foto del mismo) de una tabla a otra. En este ejemplo, el registro simplemente se vuelve a copiar en la misma tabla. Tenga en cuenta que todas las operaciones con fragmentos de campo se producen dentro de una sola secuencia AddNew-Update.

```vb
    Sub AppendChunkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstEmployees2 As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Open two recordsets from the Employees table. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstEmployees2 = rstEmployees.Clone 
     
     ' Add a new record to the first Recordset and copy the 
     ' data from a record in the second Recordset. 
     With rstEmployees 
     .AddNew 
     !FirstName = rstEmployees2!FirstName 
     !LastName = rstEmployees2!LastName 
     CopyLargeField rstEmployees2!Photo, !Photo 
     .Update 
     
     ' Delete new record because this is a demonstration. 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     rstEmployees2.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CopyLargeField(fldSource As Field, _ 
     fldDestination As Field) 
     
     ' Set size of chunk in bytes. 
     Const conChunkSize = 32768 
     
     Dim lngOffset As Long 
     Dim lngTotalSize As Long 
     Dim strChunk As String 
     
     ' Copy the photo from one Recordset to the other in 32K 
     ' chunks until the entire field is copied. 
     lngTotalSize = fldSource.FieldSize 
     Do While lngOffset < lngTotalSize 
     strChunk = fldSource.GetChunk(lngOffset, conChunkSize) 
     fldDestination.AppendChunk strChunk 
     lngOffset = lngOffset + conChunkSize 
     Loop 
     
    End Function
```
