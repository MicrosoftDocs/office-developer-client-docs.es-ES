---
title: Propiedad Recordset.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: aa1fed4f-ca51-918f-0a46-2b755b5f861a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821452(v=office.15)
ms:contentKeyID: 48546941
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6eec9f6be18bbf059660c804313918c480631e0b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927827"
---
# <a name="recordsetrecordcount-property-dao"></a>Propiedad Recordset.RecordCount (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve el número de registros a los que se tuvo acceso en un objeto **[Recordset](recordset-object-dao.md)**, o el número total de registros en un objeto **Recordset** u objeto **[TableDef](tabledef-object-dao.md)** tipo tabla. **Long** de solo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . RecordCount

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Comentarios

Use la propiedad **RecordCount** para saber a cuántos registros se tuvo acceso en un objeto **Recordset** o **TableDef**. La propiedad **RecordCount** no indica cuántos registros se están contenidos en un dynaset, instantánea u objeto **Recordset** de tipo forward – only hasta que todos los registros se ha tenido acceso. Una vez que se tuvo acceso al último registro, la propiedad **RecordCount** indica el número total de registros sin eliminar en el objeto **Recordset** o **TableDef**. Para obligar el acceso al último registro, use el método **[MoveLast](recordset-movelast-method-dao.md)** en el objeto **Recordset**. También puede usar una función **Count** de SQL para determinar el número aproximado de registros que devolverá su consulta.


> [!NOTE]
> <P>[!NOTA] El uso del método <STRONG>MoveLast</STRONG> para rellenar un <STRONG>Recordset</STRONG> recién abierto afecta negativamente al rendimiento. A menos que sea necesario tener un <STRONG>RecordCount</STRONG> preciso tan pronto como se abra un <STRONG>Recordset</STRONG>, es preferible esperar hasta que se rellene el <STRONG>Recordset</STRONG> con otras partes del código antes de comprobar la propiedad <STRONG>RecordCount</STRONG>.</P>



Como su aplicación elimina registros en un objeto **Recordset** de tipo Dynaset, el valor de la propiedad **RecordCount** se reduce. Sin embargo, los registros eliminados por otros usuarios no los refleja la propiedad **RecordCount** hasta que el registro actual se coloca en un registro eliminado. Si ejecuta una transacción que afecta al valor de la propiedad **RecordCount** y posteriormente deshace la transacción, la propiedad **RecordCount** no reflejará el número real de los registros restantes.

La propiedad **RecordCount** de un objeto **Recordset** de tipo snapshot o forward – only no se ve afectada por los cambios en las tablas subyacentes.

Un objeto **Recordset** o **TableDef** sin registros tiene un valor 0 para la propiedad **RecordCount**.

Al usar el método **[Requery](recordset-requery-method-dao.md)** en un objeto **Recordset**, se restablece la propiedad **RecordCount** de la misma manera que si se volviera a ejecutar la consulta.

## <a name="example"></a>Ejemplo

En este ejemplo se muestra la propiedad **RecordCount** con distintos tipos de **Recordsets** antes y después de que estos se rellenaran.

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
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
