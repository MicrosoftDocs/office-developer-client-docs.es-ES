---
title: Status (propiedad, Recordset ADO)
TOCTitle: Status Property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1979ad721a01ef72c08da1531a8826ec320915e5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604620"
---
# <a name="status-property-ado-recordset"></a><span data-ttu-id="92650-102">Status (propiedad, Recordset ADO)</span><span class="sxs-lookup"><span data-stu-id="92650-102">Status Property (ADO Recordset)</span></span>


<span data-ttu-id="92650-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="92650-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="92650-104">Indica el estado del registro actual con respecto a actualizaciones por lotes u otras operaciones masivas.</span><span class="sxs-lookup"><span data-stu-id="92650-104">Indicates the status of the current record with respect to batch updates or other bulk operations.</span></span>

<span data-ttu-id="92650-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="92650-105"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="92650-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92650-106">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="92650-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92650-107">Return value</span></span>
>>>>>>> <span data-ttu-id="92650-108">master</span><span class="sxs-lookup"><span data-stu-id="92650-108">master</span></span>

<span data-ttu-id="92650-109">Devuelve una suma de uno o más valores [RecordStatusEnum](recordstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="92650-109">Returns a sum of one or more [RecordStatusEnum](recordstatusenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="92650-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92650-110">Remarks</span></span>

<span data-ttu-id="92650-p101">Use la propiedad **Status** para ver los cambios pendientes en los registros modificados durante la actualización por lotes. La propiedad **Status** también se puede usar para ver el estado de registros que producen error durante operaciones masivas, por ejemplo al llamar a los métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) o [CancelBatch](cancelbatch-method-ado.md) de un objeto [Recordset](recordset-object-ado.md) o al establecer la propiedad [Filter](filter-property-ado.md) de un objeto **Recordset** en una matriz de marcadores. Con esta propiedad, es posible determinar cómo se produjo el error de un registro determinado y solucionarlo en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="92650-p101">Use the **Status** property to see what changes are pending for records modified during batch updating. You can also use the **Status** property to view the status of records that fail during bulk operations, such as when you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object to an array of bookmarks. With this property, you can determine how a given record failed and resolve it accordingly.</span></span>

