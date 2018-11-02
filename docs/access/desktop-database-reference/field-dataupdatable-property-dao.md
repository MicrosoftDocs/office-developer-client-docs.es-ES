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
# <a name="fielddataupdatable-property-dao"></a><span data-ttu-id="30342-102">Propiedad Field.DataUpdatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="30342-102">Field.DataUpdatable property (DAO)</span></span>


<span data-ttu-id="30342-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30342-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="30342-104">Devuelve un valor que indica si los datos del campo representado por un objeto **[Field](field-object-dao.md)** se pueden actualizar.</span><span class="sxs-lookup"><span data-stu-id="30342-104">Returns a value that indicates whether the data in the field represented by a **[Field](field-object-dao.md)** object is updatable.</span></span>

## <a name="syntax"></a><span data-ttu-id="30342-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30342-105">Syntax</span></span>

<span data-ttu-id="30342-106">*expresión* . DataUpdatable</span><span class="sxs-lookup"><span data-stu-id="30342-106">*expression* .DataUpdatable</span></span>

<span data-ttu-id="30342-107">*expresión* Variable que representa un objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="30342-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="30342-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30342-108">Remarks</span></span>

<span data-ttu-id="30342-p101">Use esta propiedad para determinar si se puede cambiar el valor de la propiedad **[Value](field-value-property-dao.md)** de un objeto **Field**. Esta propiedad siempre es **False** en un objeto **Field** cuya propiedad **[Attributes](field-attributes-property-dao.md)** sea **dbAutoIncrField**.</span><span class="sxs-lookup"><span data-stu-id="30342-p101">Use this property to determine whether you can change the **[Value](field-value-property-dao.md)** property setting of a **Field** object. This property is always **False** on a **Field** object whose **[Attributes](field-attributes-property-dao.md)** property is **dbAutoIncrField**.</span></span>

<span data-ttu-id="30342-111">Puede usar la propiedad **DataUpdatable** en objetos **Field** anexados a la colección **[Fields](fields-collection-dao.md)** de objetos **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)** y **[Relation](relation-object-dao.md)**, pero no a la colección **Fields** de objetos **[Index](index-object-dao.md)** o **[TableDef](tabledef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="30342-111">You can use the **DataUpdatable** property on **Field** objects that are appended to the **[Fields](fields-collection-dao.md)** collection of **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)**, and **[Relation](relation-object-dao.md)** objects, but not the **Fields** collection of **[Index](index-object-dao.md)** or **[TableDef](tabledef-object-dao.md)** objects.</span></span>

## <a name="example"></a><span data-ttu-id="30342-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30342-112">Example</span></span>

<span data-ttu-id="30342-p102">En este ejemplo se muestra que la propiedad **DataUpdatable** usa el primer campo desde seis **Recordsets** distintos. Se requiere la función DataOutput para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="30342-p102">This example demonstrates the **DataUpdatable** property using the first field from six different **Recordsets**. The DataOutput function is required for this procedure to run.</span></span>

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

