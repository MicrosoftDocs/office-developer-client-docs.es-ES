---
title: Propiedad Recordset2.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: 77852966-11e9-1773-6e58-53927b84c03b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196071(v=office.15)
ms:contentKeyID: 48545728
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052890
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c23de433f26b5a54b3fee5cc69f67a07b53f8a3b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309160"
---
# <a name="recordset2recordcount-property-dao"></a>Propiedad Recordset2.RecordCount (DAO)

**Se aplica a:** Access 2013, Office 2013

Devuelve el número de registros a los que se tuvo acceso en un objeto **[Recordset](recordset-object-dao.md)**, o el número total de registros en un objeto **Recordset** u objeto **[TableDef](tabledef-object-dao.md)** tipo tabla. **Long** de solo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . RecordCount

*expresión* Variable que representa un **objeto Recordset2.**

## <a name="remarks"></a>Comentarios

Use la propiedad **RecordCount** para averiguar a cuántos registros en un objeto **Recordset** o **TableDef** se obtuvo acceso. La propiedad **RecordCount** no indica cuántos registros contiene un objeto de tipo dynaset, snapshot, o forward–only **Recordset** hasta que se obtenga acceso a todos los registros. Una vez que se obtiene acceso al último registro, la propiedad **RecordCount** indica el número total de registros no eliminados en el objeto **Recordset** o **TableDef**. Para obligar el acceso al último registro, use el método **[MoveLast](recordset2-movelast-method-dao.md)** en el objeto **Recordset**. También puede usar una función **Count** de SQL para determinar el número aproximado de registros que devolverá su consulta.

> [!NOTE]
> El uso del método **MoveLast** para rellenar un **Recordset** recién abierto afecta negativamente al rendimiento. A menos que sea necesario tener un **RecordCount** preciso tan pronto como se abra un **Recordset**, es preferible esperar hasta que se rellene el **Recordset** con otras partes del código antes de comprobar la propiedad **RecordCount**.

Como su aplicación elimina registros en un objeto **Recordset** de tipo Dynaset, el valor de la propiedad **RecordCount** se reduce. Sin embargo, los registros eliminados por otros usuarios no los refleja la propiedad **RecordCount** hasta que el registro actual se coloca en un registro eliminado. Si ejecuta una transacción que afecta al valor de la propiedad **RecordCount** y posteriormente deshace la transacción, la propiedad **RecordCount** no reflejará el número real de los registros restantes.

La propiedad **RecordCount** de un objeto **Recordset** de tipo snapshot o forward–only no queda afectada por los cambios de las tablas subyacentes.

Un objeto **Recordset** o **TableDef** sin registros tiene una configuración de propiedad **RecordCount** de 0.

Al usar el método **[Requery](recordset2-requery-method-dao.md)** en un objeto **Recordset**, se restablece la propiedad **RecordCount** de la misma manera que si se volviera a ejecutar la consulta.

## <a name="example"></a>Ejemplo

Este ejemplo demuestra la propiedad **RecordCount** con tipos diferentes de **Recordsets** antes y después de que se completen.

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open table-type Recordset and show RecordCount 
     ' property. 
     Set rstEmployees = .OpenRecordset("Employees") 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open dynaset-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open snapshot-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenSnapshot) 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open forward-only-type Recordset and show 
     ' RecordCount property before populating the 
     ' Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenForwardOnly) 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after calling the 
     ' MoveNext method. 
     rstEmployees.MoveNext 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table after MoveNext" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     .Close 
     End With 
     
    End Sub
```
