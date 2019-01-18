---
title: Propiedad Recordset.BatchCollisions (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 61f60567ac170a0ecde2d4bd46589d2308b7788f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700377"
---
# <a name="recordsetbatchcollisions-property-dao"></a><span data-ttu-id="5c5a8-102">Propiedad Recordset.BatchCollisions (DAO)</span><span class="sxs-lookup"><span data-stu-id="5c5a8-102">Recordset.BatchCollisions property (DAO)</span></span>


<span data-ttu-id="5c5a8-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c5a8-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="5c5a8-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c5a8-104">Syntax</span></span>

<span data-ttu-id="5c5a8-105">*expresión* . BatchCollisions</span><span class="sxs-lookup"><span data-stu-id="5c5a8-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="5c5a8-106">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="5c5a8-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c5a8-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c5a8-107">Remarks</span></span>

<span data-ttu-id="5c5a8-p101">Esta propiedad contiene una matriz de marcadores que hacen referencia a las filas que encontraron un conflicto durante la llamada **[Update](recordset-update-method-dao.md)** del lote que se intentó en último lugar. La propiedad **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** indica el número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5c5a8-p101">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset-update-method-dao.md)** call. The **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="5c5a8-110">Si se establece la propiedad **[Bookmark](recordset-object-dao.md)** del objeto **[Recordset](recordset-bookmark-property-dao.md)** de trabajo en los valores de marcador de la matriz **BatchCollisions**, puede desplazarse a cada registro que no finalizó la última operación de actualización en modo de proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="5c5a8-110">If you set the working **[Recordset](recordset-object-dao.md)** object's **[Bookmark](recordset-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="5c5a8-p102">Una vez corregidos los registros del conflicto, puede llamar de nuevo al método **Update** en modo de proceso por lotes. En este punto, DAO intenta llevar a cabo otra actualización del lote y la propiedad **BatchCollisions** refleja de nuevo el conjunto de registros con error en el segundo intento. Los registros que finalizaron correctamente en el intento anterior no se envían en el intento actual, ya que ahora tienen una propiedad **[RecordStatus](recordset-recordstatus-property-dao.md)** de dbRecordUnmodified. Este proceso puede continuar hasta que dejen de producirse conflictos o hasta que se abandonen las actualizaciones y se cierre el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="5c5a8-p102">After the collision records are corrected, you can call the batch mode **Update** method again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="5c5a8-115">Esta matriz se vuelve a crear cada vez que se ejecuta un método **Update** en modo de proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="5c5a8-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>

