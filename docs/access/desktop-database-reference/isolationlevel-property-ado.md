---
title: IsolationLevel (propiedad, ADO)
TOCTitle: IsolationLevel property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4eb46fa97b831030617916d03557b5bf9af9606d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291152"
---
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="d51c4-102">IsolationLevel (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="d51c4-102">IsolationLevel property (ADO)</span></span>


<span data-ttu-id="d51c4-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d51c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d51c4-104">Indica el nivel de aislamiento de un objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d51c4-104">Indicates the level of isolation for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d51c4-105">Valores de configuración y devueltos</span><span class="sxs-lookup"><span data-stu-id="d51c4-105">Settings and return values</span></span>

<span data-ttu-id="d51c4-106">Establece o devuelve un valor de tipo [IsolationLevelEnum](isolationlevelenum.md).</span><span class="sxs-lookup"><span data-stu-id="d51c4-106">Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value.</span></span> <span data-ttu-id="d51c4-107">El valor predeterminado es **adXactChaos**.</span><span class="sxs-lookup"><span data-stu-id="d51c4-107">The default is **adXactChaos**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d51c4-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d51c4-108">Remarks</span></span>

<span data-ttu-id="d51c4-p102">Use la propiedad **IsolationLevel** para establecer el nivel de aislamiento de un objeto **Connection**. El valor no se aplica hasta la siguiente vez que se llama al método [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Si el nivel de aislamiento solicitado no está disponible, el proveedor puede devolver el siguiente mayor valor de aislamiento.</span><span class="sxs-lookup"><span data-stu-id="d51c4-p102">Use the **IsolationLevel** property to set the isolation level of a **Connection** object. The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</span></span>

<span data-ttu-id="d51c4-112">La propiedad **IsolationLevel** es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d51c4-112">The **IsolationLevel** property is read/write.</span></span>

<span data-ttu-id="d51c4-113">**Uso del servicio de datos remotos** Cuando se usa en un objeto Connection del cliente, la propiedad **IsolationLevel** sólo se puede establecer en **adXactUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="d51c4-113">**Remote Data Service Usage**When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**.</span></span>

<span data-ttu-id="d51c4-p103">Puesto que los usuarios están trabajando con objetos **Recordset** desconectados en una memoria caché del cliente, puede haber problemas de multiusuario. Por ejemplo, cuando dos usuarios diferentes intenten actualizar el mismo registro, el Servicio de datos remoto sólo permitirá que "gane" el usuario que actualice el registro en primer lugar. La solicitud de actualización del segundo usuario dará lugar a un error.</span><span class="sxs-lookup"><span data-stu-id="d51c4-p103">Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues. For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win." The second user's update request will fail with an error.</span></span>

