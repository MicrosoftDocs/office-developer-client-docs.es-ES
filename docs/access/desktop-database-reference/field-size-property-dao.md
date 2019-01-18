---
title: Propiedad Field.Size (DAO)
TOCTitle: Size Property
ms:assetid: 15e25201-87b6-f62f-ff18-259414a47891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845510(v=office.15)
ms:contentKeyID: 48543419
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052878
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 16ce8a9e63c18ded2738035f23e9a1baeff4cc8c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708343"
---
# <a name="fieldsize-property-dao"></a>Propiedad Field.Size (DAO)


**Se aplica a**: Access 2013, Office 2013


Establece o devuelve un valor que indica el tamaño máximo en bytes de un objeto **[Field](field-object-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . Tamaño

*expresión* Variable que representa un objeto **Field** .

## <a name="remarks"></a>Observaciones

Para un objeto no anexado todavía a la colección **[Fields](fields-collection-dao.md)**, esta propiedad es de lectura y escritura.

Para campos (que no sean campos de tipo Memo) que contienen datos de caracteres, la propiedad **Size** indica el número máximo de caracteres que el campo puede contener. Para campos numéricos, la propiedad **Size** indica el número de bytes de almacenamiento que se requieren.

El uso de la propiedad **Size** depende del objeto que contiene la colección **Fields** a la que se anexa el objeto **Field**, como se muestra en la tabla siguiente.

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
<td><p><strong>Índice</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
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


Cuando se crea un objeto **Field** con un tipo de datos distinto de Text, el valor de la propiedad **[Type](field-type-property-dao.md)** determina automáticamente el valor de la propiedad **Size**; no es necesario establecerlo. Sin embargo, para un objeto **Field** con el tipo de datos Text, se puede establecer **Size** en cualquier entero que no supere el tamaño máximo de texto (255 para bases de datos de Microsoft Access). Si no se establece el tamaño, el campo tendrá el tamaño que la base de datos permita.

Para objetos **Field** Long Binary y Memo, **Size** se establece siempre en 0. Use la propiedad **[FieldSize](field-fieldsize-property-dao.md)** del objeto **Field** para determinar el tamaño de los datos en un registro concreto. El tamaño máximo de un campo Long Binary o Memo está limitado únicamente por los recursos del sistema o por el tamaño máximo permitido por la base de datos.

## <a name="example"></a>Ejemplo

En este ejemplo se enumeran los nombres y tamaños de los objetos **Field** en la tabla Employees para demostrar el uso de la propiedad **Size**.

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field 
     Dim fldLoop As Field 
     
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
