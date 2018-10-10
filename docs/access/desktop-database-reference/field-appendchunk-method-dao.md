---
title: Field.AppendChunk Method (DAO)
TOCTitle: AppendChunk Method
ms:assetid: f98c6862-fecf-06cb-a7c0-42b0d3150a06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837014(v=office.15)
ms:contentKeyID: 48548819
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2ba2009bb9b8ccbde52c3b521c0551bf803fdb1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486236"
---
# <a name="fieldappendchunk-method-dao"></a>Field.AppendChunk Method (DAO)

**Se aplica a**: Access 2013 | Office 2013

Agrega datos de una expresión de cadena a un objeto **[Field](field-object-dao.md)** de Memo o binario largo en un objeto **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . AppendChunk (***Val***)

*expresión* Variable que representa un objeto **Field** .

### <a name="parameters"></a>Parámetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Necesario/Opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Val</p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Expresión o variable Variant (subtipo cadena) que contiene los datos que desea agregar al objeto <strong>Field</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Puede utilizar los métodos **AppendChunk** y **[GetChunk](field-getchunk-method-dao.md)** para tener acceso a subconjuntos de datos en un campo Memo o Binario largo.

Puede utilizar también estos métodos para conservar espacio de cadena cuando trabaje con campos Memo o Binario largo. En algunas operaciones (como copiar) se utilizan cadenas temporales. Si el espacio de cadena es limitado, quizás necesite trabajar con fragmentos de un campo en lugar de con todo el campo.

Si no hay ningún registro actual cuando utiliza **AppendChunk**, se produce un error.

> [!NOTE]
> La operación **AppendChunk** inicial (después de una llamada a **[Edit](recordset-edit-method-dao.md)** o **[AddNew](recordset-addnew-method-dao.md)** ) sólo colocará los datos en el campo sobrescribiendo los existentes. Las siguientes llamadas a **AppendChunk** en la misma sesión **Edit** o **AddNew** agregarán entonces los datos a los datos existentes.

## <a name="example"></a>Ejemplo

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
