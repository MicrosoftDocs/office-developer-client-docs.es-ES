---
title: Propiedad Field.DataUpdatable (DAO)
TOCTitle: DataUpdatable Property
ms:assetid: 08ca57b6-2d7c-36b4-7d51-b76ac5467163
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845029(v=office.15)
ms:contentKeyID: 48543104
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052988
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ad3de8bba18b15b15311bf188822a451e74bb24d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926615"
---
# <a name="fielddataupdatable-property-dao"></a>Propiedad Field.DataUpdatable (DAO)


**Se aplica a**: Access 2013, Office 2013


Devuelve un valor que indica si los datos del campo representado por un objeto **[Field](field-object-dao.md)** se pueden actualizar.

## <a name="syntax"></a>Sintaxis

*expresión* . DataUpdatable

*expresión* Variable que representa un objeto **Field** .

## <a name="remarks"></a>Observaciones

Use esta propiedad para determinar si se puede cambiar el valor de la propiedad **[Value](field-value-property-dao.md)** de un objeto **Field**. Esta propiedad siempre es **False** en un objeto **Field** cuya propiedad **[Attributes](field-attributes-property-dao.md)** sea **dbAutoIncrField**.

Puede usar la propiedad **DataUpdatable** en objetos **Field** anexados a la colección **[Fields](fields-collection-dao.md)** de objetos **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)** y **[Relation](relation-object-dao.md)**, pero no a la colección **Fields** de objetos **[Index](index-object-dao.md)** o **[TableDef](tabledef-object-dao.md)**.

## <a name="example"></a>Ejemplo

En este ejemplo se muestra que la propiedad **DataUpdatable** usa el primer campo desde seis **Recordsets** distintos. Se requiere la función DataOutput para que pueda ejecutarse este procedimiento.

```vb 
Sub DataUpdatableX() 
 
 Dim dbsNorthwind As Database 
 Dim rstNorthwind As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Open and print report about a table-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees") 
 DataOutput rstNorthwind 
 
 ' Open and print report about a dynaset-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenDynaset) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a snapshot-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenSnapshot) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a forward-only-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenForwardOnly) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a Recordset based on 
 ' a select query. 
 Set rstNorthwind = _ 
 .OpenRecordset("Current Product List") 
 DataOutput rstNorthwind 
 
 ' Open and print report about a Recordset based on a 
 ' select query that calculates totals. 
 Set rstNorthwind = .OpenRecordset("Order Subtotals") 
 DataOutput rstNorthwind 
 
 .Close 
 End With 
 
End Sub 
 
Function DataOutput(rstTemp As Recordset) 
 
 With rstTemp 
 Debug.Print "Recordset: " & .Name & ", "; 
 Select Case .Type 
 Case dbOpenTable 
 Debug.Print "dbOpenTable" 
 Case dbOpenDynaset 
 Debug.Print "dbOpenDynaset" 
 Case dbOpenSnapshot 
 Debug.Print "dbOpenSnapshot" 
 Case dbOpenForwardOnly 
 Debug.Print "dbOpenForwardOnly" 
 End Select 
 Debug.Print " Field: " & .Fields(0).Name & ", " & _ 
 "DataUpdatable = " & .Fields(0).DataUpdatable 
 Debug.Print 
 .Close 
 End With 
 
End Function 
 
```

