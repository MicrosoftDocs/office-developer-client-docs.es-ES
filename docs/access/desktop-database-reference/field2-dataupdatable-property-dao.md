---
title: Propiedad Field2. DataUpdatable (DAO)
TOCTitle: DataUpdatable Property
ms:assetid: e6619c4e-26b1-777b-f0de-78fed3dbc890
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835966(v=office.15)
ms:contentKeyID: 48548377
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 88a57ff2daeaaaab202daad55f01eebc6bdf86dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292842"
---
# <a name="field2dataupdatable-property-dao"></a>Propiedad Field2. DataUpdatable (DAO)


**Se aplica a:** Access 2013, Office 2013


Devuelve un valor que indica si se pueden actualizar los datos en el campo representado por un objeto **Field2**.

## <a name="syntax"></a>Sintaxis

*expresión* . DataUpdatable

*expresión* Variable que representa un objeto **Field2** .

## <a name="remarks"></a>Comentarios

Utilice esta propiedad para determinar si puede cambiar el valor de la propiedad **[Value](field-value-property-dao.md)** de un objeto **Field2**. Esta propiedad es siempre **False** en un objeto **Field2** cuya propiedad **[Attributes](field-attributes-property-dao.md)** es **dbAutoIncrField**.

Puede usar la propiedad **DataUpdatable** en objetos **Field2** anexados a la colección **[Fields](fields-collection-dao.md)** de los objetos **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)** y **[Relation](relation-object-dao.md)**, pero no a la colección **Fields** de los objetos **[Index](index-object-dao.md)** o **[TableDef](tabledef-object-dao.md)**.

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

