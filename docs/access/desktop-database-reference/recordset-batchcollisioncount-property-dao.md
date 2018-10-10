---
title: Recordset.BatchCollisionCount Property (DAO)
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
ms.openlocfilehash: 2c2cc3e9351eba04d1c05555b2f6b22284a8e6c0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486309"
---
# <a name="recordsetbatchcollisioncount-property-dao"></a><span data-ttu-id="d9d0b-102">Recordset.BatchCollisionCount Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="d9d0b-102">Recordset.BatchCollisionCount Property (DAO)</span></span>


<span data-ttu-id="d9d0b-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9d0b-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d0b-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9d0b-104">Syntax</span></span>

<span data-ttu-id="d9d0b-105">*expresión* . BatchCollisionCount</span><span class="sxs-lookup"><span data-stu-id="d9d0b-105">*expression* .BatchCollisionCount</span></span>

<span data-ttu-id="d9d0b-106">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d9d0b-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9d0b-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9d0b-107">Remarks</span></span>

<span data-ttu-id="d9d0b-p101">Esta propiedad indica cuántos registros encontraron conflictos o no se actualizaron por otro motivo durante el último intento de actualización del lote. El valor de esta propiedad corresponde al número de marcadores de la propiedad **[BatchCollisions](recordset-batchcollisions-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="d9d0b-p101">This property indicates how many records encountered collisions or otherwise failed to update during the last batch update attempt. The value of this property corresponds to the number of bookmarks in the **[BatchCollisions](recordset-batchcollisions-property-dao.md)** property.</span></span>

<span data-ttu-id="d9d0b-110">Si se establece la propiedad **[Bookmark](recordset-object-dao.md)** del objeto **[Recordset](recordset-bookmark-property-dao.md)** de trabajo en los valores de marcador de la matriz **BatchCollisions**, puede desplazarse a cada registro que no finalizó en la operación **[Update](recordset-update-method-dao.md)** más reciente del lote.</span><span class="sxs-lookup"><span data-stu-id="d9d0b-110">If you set the working **[Recordset](recordset-object-dao.md)** object's **[Bookmark](recordset-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch **[Update](recordset-update-method-dao.md)** operation.</span></span>

<span data-ttu-id="d9d0b-p102">Una vez corregidos los registros del conflicto, se puede llamar de nuevo a un método **Update** en modo de proceso por lotes. En este punto, DAO intenta llevar a cabo otra actualización del lote y la propiedad **BatchCollisions** refleja de nuevo el conjunto de registros con error en el segundo intento. Los registros que finalizaron correctamente en el intento anterior no se envían en el intento actual, ya que ahora tienen una propiedad **[RecordStatus](recordset-recordstatus-property-dao.md)** de dbRecordUnmodified. Este proceso puede continuar hasta que dejen de producirse conflictos o hasta que se abandonen las actualizaciones y se cierre el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="d9d0b-p102">After the collision records are corrected, a batch-mode **Update** method can be called again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, because they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

## <a name="example"></a><span data-ttu-id="d9d0b-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d9d0b-115">Example</span></span>

<span data-ttu-id="d9d0b-116">En este ejemplo, se utiliza la propiedad **BatchCollisionCount** y el método **Update** para realizar una demostración de la actualización de lotes en la que los conflictos se resuelven forzando la actualización del lote.</span><span class="sxs-lookup"><span data-stu-id="d9d0b-116">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

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

