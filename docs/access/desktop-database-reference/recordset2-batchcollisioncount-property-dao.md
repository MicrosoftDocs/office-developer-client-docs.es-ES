---
title: Propiedad Recordset2.BatchCollisionCount (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 997dfbb3-673c-8813-f51b-ab8d95093c4f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197961(v=office.15)
ms:contentKeyID: 48546514
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33650b9fdbaf7fbc9266c8c778199e1138cd5b21
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706656"
---
# <a name="recordset2batchcollisioncount-property-dao"></a>Propiedad Recordset2.BatchCollisionCount (DAO)


**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . BatchCollisionCount

*expresión* Variable que representa un objeto **Recordset2** .

## <a name="remarks"></a>Observaciones

Esta propiedad indica la cantidad de registros en los que se han producido conflictos o errores durante la actualización en el último intento de la última actualización por lotes. El valor de esta propiedad se corresponde con el número de marcadores en la propiedad **[BatchCollisions](recordset2-batchcollisions-property-dao.md)**.

Si establece la propiedad [**Bookmark**](recordset2-bookmark-property-dao.md) del objeto activo **Recordset** en los valores de marcador en la matriz **BatchCollisions**, podrá moverse a cada registro que falle para completar la última operación por lotes **[Update](recordset2-update-method-dao.md)**.

Después de corregir los registros con conflictos, se puede llamar otra vez a un método **Update** en modo por lotes. En este punto, DAO intenta otra actualización por lotes y la propiedad **BatchCollisions** refleja otra vez el error que se produjo en el conjunto de registros en el segundo intento. Cualquiera de los registros correctos en el intento anterior no se enviarán en el intento actual porque ahora tienen una propiedad **[RecordStatus](recordset2-recordstatus-property-dao.md)** de **dbRecordUnmodified**. Este proceso puede continuar tanto tiempo como conflictos se produzcan, o hasta que se abandonen las actualizaciones y se cierre el conjunto de resultados.

## <a name="example"></a>Ejemplo

En este ejemplo, se utiliza la propiedad **BatchCollisionCount** y el método **Update** para realizar una demostración de la actualización de lotes en la que los conflictos se resuelven forzando la actualización del lote.

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 Dim intLoop As Integer 
 Dim strPrompt As String 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. It is also required that a table 
 ' with a primary key is used. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Modify data in local recordset. 
 Do While Not .EOF 
 .Edit 
 If !royalty <= 20 Then 
 !royalty = !royalty - 4 
 Else 
 !royalty = !royalty + 2 
 End If 
 .Update 
 .MoveNext 
 Loop 
 
 ' Attempt a batch update. 
 .Update dbUpdateBatch 
 
 ' If there are collisions, give the user the option 
 ' of forcing the changes or resolving them 
 ' individually. 
 If .BatchCollisionCount > 0 Then 
 strPrompt = "There are collisions. " & vbCr & _ 
 "Do you want the program to force " & _ 
 vbCr & "an update using the local data?" 
 If MsgBox(strPrompt, vbYesNo) = vbYes Then _ 
 .Update dbUpdateBatch, True 
 End If 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

