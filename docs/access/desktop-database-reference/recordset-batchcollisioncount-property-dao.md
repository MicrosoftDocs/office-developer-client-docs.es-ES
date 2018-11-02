---
title: Propiedad Recordset.BatchCollisionCount (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 9d166463-8313-c0f5-8389-5d5ad933eb33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198240(v=office.15)
ms:contentKeyID: 48546617
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101181
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7d2100fb9803de406eca258b1d1093b343a6e88d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929660"
---
# <a name="recordsetbatchcollisioncount-property-dao"></a>Propiedad Recordset.BatchCollisionCount (DAO)


**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . BatchCollisionCount

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Observaciones

Esta propiedad indica cuántos registros encontraron conflictos o no se actualizaron por otro motivo durante el último intento de actualización del lote. El valor de esta propiedad corresponde al número de marcadores de la propiedad **[BatchCollisions](recordset-batchcollisions-property-dao.md)**.

Si se establece la propiedad **[Bookmark](recordset-object-dao.md)** del objeto **[Recordset](recordset-bookmark-property-dao.md)** de trabajo en los valores de marcador de la matriz **BatchCollisions**, puede desplazarse a cada registro que no finalizó en la operación **[Update](recordset-update-method-dao.md)** más reciente del lote.

Una vez corregidos los registros del conflicto, se puede llamar de nuevo a un método **Update** en modo de proceso por lotes. En este punto, DAO intenta llevar a cabo otra actualización del lote y la propiedad **BatchCollisions** refleja de nuevo el conjunto de registros con error en el segundo intento. Los registros que finalizaron correctamente en el intento anterior no se envían en el intento actual, ya que ahora tienen una propiedad **[RecordStatus](recordset-recordstatus-property-dao.md)** de dbRecordUnmodified. Este proceso puede continuar hasta que dejen de producirse conflictos o hasta que se abandonen las actualizaciones y se cierre el conjunto de resultados.

## <a name="example"></a>Ejemplo

En este ejemplo, se utiliza la propiedad **BatchCollisionCount** y el método **Update** para realizar una demostración de la actualización de lotes en la que los conflictos se resuelven forzando la actualización del lote.

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
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

