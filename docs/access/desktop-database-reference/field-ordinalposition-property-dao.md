---
title: Propiedad Field.OrdinalPosition (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 07f2344e-2a72-33d8-be47-b37d76ecca47
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845002(v=office.15)
ms:contentKeyID: 48543088
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d45f0362831d91b83b3a2449affbbfb5ac2b4e51
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701882"
---
# <a name="fieldordinalposition-property-dao"></a>Propiedad Field.OrdinalPosition (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve la posición relativa de un objeto **[Field](field-object-dao.md)** en una colección **[Fields](fields-collection-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . OrdinalPosition

*expresión* Variable que representa un objeto **Field** .

## <a name="remarks"></a>Observaciones

Para un objeto que todavía no está anexado a la colección **Fields**, esta propiedad es de lectura y escritura.

El valor predeterminado es 0.

La disponibilidad de la propiedad **OrdinalPosition** depende del objeto que contiene la colección **Fields**, como se muestra en la siguiente tabla.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Si la colección Fields pertenece a un</p></th>
<th><p>
Entonces OrdinalPosition</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>							Objeto <strong>Index</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="even">
<td><p>							Objeto <strong>QueryDef</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="odd">
<td><p>							Objeto <strong>Recordset</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="even">
<td><p>							Objeto <strong>Relation</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="odd">
<td><p>							Objeto <strong>TableDef</strong></p></td>
<td><p>Es de lectura y escritura.</p></td>
</tr>
</tbody>
</table>


Generalmente, la posición ordinal de un objeto anexado a una colección depende del orden en el que se anexe el objeto. El primer objeto anexado estará en la primera posición (0), el segundo estará en la segunda posición (1) y así sucesivamente. El último objeto anexado estará en la posición ordinal recuento – 1, donde recuento es el número de objetos en la colección tal y como aparece especificado en el valor de la propiedad **[Count](containers-count-property-dao.md)**.

Puede utilizar la propiedad **OrdinalPosition** para especificar una posición ordinal para los nuevos objetos **Field** que difiera del orden en el que ha anexado esos objetos a una colección. Esto le permite especificar un orden de campo para sus tablas, consultas y conjuntos de registros cuando los utiliza en una aplicación. Por ejemplo, el orden en el que los campos se devuelven en una instrucción SELECT \* consulta viene determinada por los valores de propiedad **OrdinalPosition** actuales.

Puede restablecer permanentemente el orden en el que los campos se devuelven en los conjuntos de registros estableciendo la propiedad **OrdinalPosition** en cualquier entero positivo.

Dos o más objetos **Field** en la misma colección pueden tener el mismo valor que la propiedad **OrdinalPosition**, en cuyo caso se ordenarán alfabéticamente. Por ejemplo, si tiene un campo denominado Edad establecido en 4 y establece un segundo campo denominado Peso en 4, Peso se devuelve después de Edad.

Puede especificar un número que sea mayor que el número de campos menos 1. El campo se devolverá siguiendo un orden respecto al número más grande. Por ejemplo, si establece una propiedad de campo **OrdinalPosition** en 20 (y sólo hay 5 campos) y ha establecido la propiedad **OrdinalPosition** para dos campos más en 10 y en 30, respectivamente, el campo establecido en 20 se devolverá entre los campos establecidos en 10 y en 30.

> [!NOTE]
> [!NOTA] Incluso si la colección **Fields** de un [TableDef](tabledef-object-dao.md) no se actualizó, el orden del campo en un [Recordset](recordset-object-dao.md) abierto desde **TableDef** reflejará los datos de **OrdinalPosition** del objeto **TableDef**. Un tipo de tabla **Recordset** tendrá los mismos datos **OrdinalPosition** que la tabla base, pero cualquier otro tipo de **Recordset** tendrá nuevos datos **OrdinalPosition** (comenzando por 0) que sigue el orden determinado por los datos de **OrdinalPosition** del objeto **TableDef**.

## <a name="example"></a>Ejemplo

En este ejemplo se cambian los valores de la propiedad **OrdinalPosition** para Employees **TableDef** de forma que se controla el orden de **Field** en un resultado **Recordset**. Al establecer la **OrdinalPosition** de todos los **Fields** en 1, cualquier **Recordset** resultante ordenará los **Fields** alfabéticamente. Observe que los valores **OrdinalPosition** en **Recordset** no coinciden con los valores de **TableDef**, pero sólo reflejan el resultado final de los cambios de **TableDef**.

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     
     With tdfEmployees 
     ' Display and store original OrdinalPosition data. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldTemp In .Fields 
     fldTemp.OrdinalPosition = 1 
     Next fldTemp 
     
     ' Open new Recordset object to show how the 
     ' OrdinalPosition data has affected the record order. 
     Debug.Print _ 
     "OrdinalPosition data from resulting Recordset." 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT * FROM Employees") 
     For Each fldTemp In rstEmployees.Fields 
     Debug.Print , fldTemp.OrdinalPosition, fldTemp.Name 
     Next fldTemp 
     rstEmployees.Close 
     
     ' Restore original OrdinalPosition data because this is 
     ' a demonstration. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
