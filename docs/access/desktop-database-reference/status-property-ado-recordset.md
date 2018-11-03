---
title: Status (propiedad, Recordset de ADO)
TOCTitle: Status property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 396188dcd959b229f7f7a58ccafb76b00508aa49
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944238"
---
# <a name="status-property-ado-recordset"></a><span data-ttu-id="caa0b-102">Status (propiedad, Recordset de ADO)</span><span class="sxs-lookup"><span data-stu-id="caa0b-102">Status property (ADO Recordset)</span></span>


<span data-ttu-id="caa0b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="caa0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="caa0b-104">Indica el estado del registro actual con respecto a actualizaciones por lotes u otras operaciones masivas.</span><span class="sxs-lookup"><span data-stu-id="caa0b-104">Indicates the status of the current record with respect to batch updates or other bulk operations.</span></span>

## <a name="return-value"></a><span data-ttu-id="caa0b-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="caa0b-105">Return value</span></span>

<span data-ttu-id="caa0b-106">Devuelve una suma de uno o más valores [RecordStatusEnum](recordstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="caa0b-106">Returns a sum of one or more [RecordStatusEnum](recordstatusenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="caa0b-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="caa0b-107">Remarks</span></span>

<span data-ttu-id="caa0b-p101">Use la propiedad **Status** para ver los cambios pendientes en los registros modificados durante la actualización por lotes. La propiedad **Status** también se puede usar para ver el estado de registros que producen error durante operaciones masivas, por ejemplo al llamar a los métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) o [CancelBatch](cancelbatch-method-ado.md) de un objeto [Recordset](recordset-object-ado.md) o al establecer la propiedad [Filter](filter-property-ado.md) de un objeto **Recordset** en una matriz de marcadores. Con esta propiedad, es posible determinar cómo se produjo el error de un registro determinado y solucionarlo en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="caa0b-p101">Use the **Status** property to see what changes are pending for records modified during batch updating. You can also use the **Status** property to view the status of records that fail during bulk operations, such as when you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object to an array of bookmarks. With this property, you can determine how a given record failed and resolve it accordingly.</span></span>

