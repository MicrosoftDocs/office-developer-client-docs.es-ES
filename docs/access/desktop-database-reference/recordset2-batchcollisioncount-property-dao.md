---
title: Propiedad Recordset2. BatchCollisionCount (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 997dfbb3-673c-8813-f51b-ab8d95093c4f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197961(v=office.15)
ms:contentKeyID: 48546514
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33650b9fdbaf7fbc9266c8c778199e1138cd5b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307486"
---
# <a name="recordset2batchcollisioncount-property-dao"></a><span data-ttu-id="30ff8-102">Propiedad Recordset2. BatchCollisionCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="30ff8-102">Recordset2.BatchCollisionCount property (DAO)</span></span>


<span data-ttu-id="30ff8-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30ff8-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="30ff8-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30ff8-104">Syntax</span></span>

<span data-ttu-id="30ff8-105">*expresión* . BatchCollisionCount</span><span class="sxs-lookup"><span data-stu-id="30ff8-105">*expression* .BatchCollisionCount</span></span>

<span data-ttu-id="30ff8-106">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="30ff8-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="30ff8-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="30ff8-107">Remarks</span></span>

<span data-ttu-id="30ff8-p101">Esta propiedad indica la cantidad de registros en los que se han producido conflictos o errores durante la actualización en el último intento de la última actualización por lotes. El valor de esta propiedad se corresponde con el número de marcadores en la propiedad **[BatchCollisions](recordset2-batchcollisions-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="30ff8-p101">This property indicates how many records encountered collisions or otherwise failed to update during the last batch update attempt. The value of this property corresponds to the number of bookmarks in the **[BatchCollisions](recordset2-batchcollisions-property-dao.md)** property.</span></span>

<span data-ttu-id="30ff8-110">Si establece la propiedad [**Bookmark**](recordset2-bookmark-property-dao.md) del objeto activo **Recordset** en los valores de marcador en la matriz **BatchCollisions**, podrá moverse a cada registro que falle para completar la última operación por lotes **[Update](recordset2-update-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="30ff8-110">If you set the working **Recordset** object's **[Bookmark](recordset2-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch **[Update](recordset2-update-method-dao.md)** operation.</span></span>

<span data-ttu-id="30ff8-p102">Después de corregir los registros con conflictos, se puede llamar otra vez a un método **Update** en modo por lotes. En este punto, DAO intenta otra actualización por lotes y la propiedad **BatchCollisions** refleja otra vez el error que se produjo en el conjunto de registros en el segundo intento. Cualquiera de los registros correctos en el intento anterior no se enviarán en el intento actual porque ahora tienen una propiedad **[RecordStatus](recordset2-recordstatus-property-dao.md)** de **dbRecordUnmodified**. Este proceso puede continuar tanto tiempo como conflictos se produzcan, o hasta que se abandonen las actualizaciones y se cierre el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="30ff8-p102">After the collision records are corrected, a batch-mode **Update** method can be called again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, because they now have a **[RecordStatus](recordset2-recordstatus-property-dao.md)** property of **dbRecordUnmodified**. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

## <a name="example"></a><span data-ttu-id="30ff8-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30ff8-115">Example</span></span>

<span data-ttu-id="30ff8-116">En este ejemplo se utiliza la propiedad **BatchCollisionCount** y el método **Update** para demostrar una actualización por lotes en donde cualquier conflicto se resuelve al obligar la actualización por lotes.</span><span class="sxs-lookup"><span data-stu-id="30ff8-116">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

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

