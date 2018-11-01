---
title: IsolationLevel (propiedad, ADO)
TOCTitle: IsolationLevel property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76978d33fc5f82c9b1f8137b64a663e7e95f2204
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883060"
---
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="d8a9f-102">IsolationLevel (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="d8a9f-102">IsolationLevel property (ADO)</span></span>


<span data-ttu-id="d8a9f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8a9f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8a9f-104">Indica el nivel de aislamiento de un objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d8a9f-104">Indicates the level of isolation for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d8a9f-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="d8a9f-105">Settings and return values</span></span>

<span data-ttu-id="d8a9f-p101">Establece o devuelve un valor de tipo [IsolationLevelEnum](isolationlevelenum.md). El valor predeterminado es **adXactChaos**.</span><span class="sxs-lookup"><span data-stu-id="d8a9f-p101">Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value. The default is **adXactChaos**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8a9f-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8a9f-108">Remarks</span></span>

<span data-ttu-id="d8a9f-p102">Use la propiedad **IsolationLevel** para establecer el nivel de aislamiento de un objeto **Connection**. El valor no se aplica hasta la siguiente vez que se llama al método [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Si el nivel de aislamiento solicitado no está disponible, el proveedor puede devolver el siguiente mayor valor de aislamiento.</span><span class="sxs-lookup"><span data-stu-id="d8a9f-p102">Use the **IsolationLevel** property to set the isolation level of a **Connection** object. The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</span></span>

<span data-ttu-id="d8a9f-112">La propiedad **IsolationLevel** es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d8a9f-112">The **IsolationLevel** property is read/write.</span></span>

<span data-ttu-id="d8a9f-113">**Uso de servicio de datos remotos** Cuando se usa en un objeto Connection de cliente, se puede establecer la propiedad **IsolationLevel** sólo en **adXactUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="d8a9f-113">**Remote Data Service Usage**When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**.</span></span>

<span data-ttu-id="d8a9f-p103">Puesto que los usuarios están trabajando con objetos **Recordset** desconectados en una memoria caché del cliente, puede haber problemas de multiusuario. Por ejemplo, cuando dos usuarios diferentes intenten actualizar el mismo registro, el Servicio de datos remoto sólo permitirá que "gane" el usuario que actualice el registro en primer lugar. La solicitud de actualización del segundo usuario dará lugar a un error.</span><span class="sxs-lookup"><span data-stu-id="d8a9f-p103">Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues. For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win." The second user's update request will fail with an error.</span></span>

