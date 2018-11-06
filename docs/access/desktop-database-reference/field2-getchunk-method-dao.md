---
title: Field2.GetChunk (método) (DAO)
TOCTitle: GetChunk method
ms:assetid: 5d3a66c0-8216-d701-0a91-b79fbbc822b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194600(v=office.15)
ms:contentKeyID: 48545101
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fae8e5f0331f3c59aad482b827140ecd6366f2f1
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996436"
---
# <a name="field2getchunk-method-dao"></a>Field2.GetChunk (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

Devuelve todo o parte del contenido de un objeto **Memo** o **Long BinaryField2** en la colección **[Fields](fields-collection-dao.md)** de un objeto **[Recordset](recordset-object-dao.md)** .

## <a name="syntax"></a>Sintaxis

*expresión* . GetChunk (***desplazamiento***, ***Bytes***)

*expresión* Variable que representa un objeto **Field2** .

## <a name="parameters"></a>Parámetros

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
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Offset</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Número de bytes que se omiten antes de que se inicie la copia.</p></td>
</tr>
<tr class="even">
<td><p><em>Bytes</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Número de bytes que desea devolver.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor devuelto

Variant

## <a name="remarks"></a>Observaciones

Los bytes devueltos por **GetChunk** se asignan a una variable. Utilice **GetChunk** para devolver una parte del valor de datos total cada vez. Puede usar el método **[AppendChunk](field-appendchunk-method-dao.md)** para reorganizar las piezas.

Si offset es 0, **GetChunk** inicia la copia desde el primer byte del campo.

Si numbytes es mayor que el número de bytes en el campo, **GetChunk** devuelve el número real de bytes restantes en el campo.

> [!NOTE]
> [!NOTA] Utilice un campo **Memo** para el texto y coloque los datos binarios únicamente en campos **Long Binary** ya que, de lo contrario, se pueden obtener resultados no deseados.

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
     
    Function CopyLargeField(fldSource As Field2, _ 
     fldDestination As Field2) 
     
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
