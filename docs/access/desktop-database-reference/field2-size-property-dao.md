---
title: Field2.Size Property (DAO)
TOCTitle: Size Property
ms:assetid: e252759a-cea9-25cb-667d-80b422fbf97e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835700(v=office.15)
ms:contentKeyID: 48548282
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3783ed413d57eb3bb9a41fa1880485aa5d3ad281
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882451"
---
# <a name="field2size-property-dao"></a>Field2.Size Property (DAO)


**Se aplica a**: Access 2013, Office 2013


Establece o devuelve un valor que indica el tamaño máximo, en bytes, de un objeto **Field2**.

## <a name="syntax"></a>Sintaxis

*expresión* . Tamaño

*expresión* Variable que representa un objeto **Field2** .

## <a name="remarks"></a>Observaciones

Para un objeto no anexado todavía a la colección **[Fields](fields-collection-dao.md)**, esta propiedad es de lectura y escritura.

Para aquellos campos (distintos de los campos tipo Memo) que contienen datos sobre caracteres, la propiedad **Size** indica el número máximo de caracteres que admite ese campo. Para los campos numéricos, la propiedad **Size** indica cuántos bytes de almacenamiento son necesarios.

El uso de la propiedad **Size** depende del objeto que contenga la colección **Fields** para el que está anexado el objeto **Field2**, como se muestra en la siguiente tabla.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto anexado a</p></th>
<th><p>Uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="even">
<td><p><strong>Objeto QueryDef</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="even">
<td><p><strong>Relación</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
</tbody>
</table>


Cuando se crea un objeto **Field2** con un tipo de datos distinto de Texto, el valor de la propiedad **Type** determina automáticamente el valor de la propiedad **Size** y no es necesario establecer este valor. Sin embargo, para un objeto **Field2** con el tipo de datos Texto, se puede establecer **Size** en cualquier entero hasta el tamaño máximo del texto (255 para las bases de datos del motor de base de datos de Microsoft Access). Si no se establece el tamaño, el campo será tan grande como lo permita la base de datos.

Para Long Binary y Memo de los objetos **Field2**, **Size** está establecido siempre en 0. Utilice la propiedad **FieldSize** del objeto **Field2** para determinar el tamaño de los datos en un registro específico. El tamaño máximo de un campo Long Binary o Memo está limitado sólo por los recursos de su sistema o por el tamaño máximo permitido por la base de datos.

## <a name="example"></a>Ejemplo

En este ejemplo se muestra la propiedad **Size** mediante la enumeración de los nombres y tamaños de los objetos **Field2** en la tabla Empleados.

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field2 
     Dim fldLoop As Field2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     With tdfEmployees 
     
     ' Create and append a new Field object to the 
     ' Employees table. 
     Set fldNew = .CreateField("FaxPhone") 
     fldNew.Type = dbText 
     fldNew.Size = 20 
     .Fields.Append fldNew 
     
     Debug.Print "TableDef: " & .Name 
     Debug.Print " Field.Name - Field.Type - Field.Size" 
     
     ' Enumerate Fields collection; print field names, 
     ' types, and sizes. 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name & " - " & _ 
     fldLoop.Type & " - " & fldLoop.Size 
     Next fldLoop 
     
     ' Delete new field because this is a demonstration. 
     .Fields.Delete fldNew.Name 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
