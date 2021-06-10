---
title: Recordset2.BatchCollisions (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 07d6c25f-baf5-f7d6-d225-0447e0f78fe6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844993(v=office.15)
ms:contentKeyID: 48543085
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101180
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ea75da06c0db4eeb4e846bacfddc9f125c03fc84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307493"
---
# <a name="recordset2batchcollisions-property-dao"></a><span data-ttu-id="059f5-102">Recordset2.BatchCollisions (DAO)</span><span class="sxs-lookup"><span data-stu-id="059f5-102">Recordset2.BatchCollisions property (DAO)</span></span>


<span data-ttu-id="059f5-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="059f5-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="059f5-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="059f5-104">Syntax</span></span>

<span data-ttu-id="059f5-105">*expresión* . BatchCollisions</span><span class="sxs-lookup"><span data-stu-id="059f5-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="059f5-106">*expresión* Variable que representa un **objeto Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="059f5-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="059f5-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="059f5-107">Remarks</span></span>

<span data-ttu-id="059f5-p101">Esta propiedad contiene una matriz de marcadores para las filas en las que se produce un conflicto durante el último intento de llamada de actualización por lotes **[Update](recordset2-update-method-dao.md)**. La propiedad **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** indica el número de elementos en la matriz.</span><span class="sxs-lookup"><span data-stu-id="059f5-p101">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset2-update-method-dao.md)** call. The **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="059f5-110">Si establece la propiedad activa [**Bookmark**](recordset2-bookmark-property-dao.md) del objeto **Recordset** en los valores de marcador en la matriz **BatchCollisions**, podrá desplazarse a cada uno de los registros que no completaron la última operación Update en modo de actualización por lotes.</span><span class="sxs-lookup"><span data-stu-id="059f5-110">If you set the working **Recordset** object's **[Bookmark](recordset2-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="059f5-p102">Después de corregir los registros con conflictos, puede volver a llamar al método **Update** en modo de actualización por lotes. En este punto, DAO intenta otra actualización por lotes y la propiedad **BatchCollisions** refleja otra vez el error que se produjo en el conjunto de registros en el segundo intento. Cualquiera de los registros correctos en el intento anterior no se enviarán en el intento actual puesto que ahora tienen una propiedad **[RecordStatus](recordset2-recordstatus-property-dao.md)** de dbRecordUnmodified. Este proceso puede continuar tanto tiempo como conflictos se produzcan, o hasta que se abandonen las actualizaciones y se cierre el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="059f5-p102">After the collision records are corrected, you can call the batch mode **Update** method again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset2-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="059f5-115">Esta matriz se vuelve a crear cada vez que se ejecute un método **Update** en modo de actualización por lotes.</span><span class="sxs-lookup"><span data-stu-id="059f5-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>

