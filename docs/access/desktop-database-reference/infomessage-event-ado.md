---
title: Evento InfoMessage (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 879d8e7b3733937687671a164f86dbb273cf7533
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291445"
---
# <a name="infomessage-event-ado"></a><span data-ttu-id="b1009-102">Evento InfoMessage (ADO)</span><span class="sxs-lookup"><span data-stu-id="b1009-102">InfoMessage event (ADO)</span></span>

<span data-ttu-id="b1009-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1009-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1009-104">Al evento **InfoMessage** se le llama siempre que se produce una advertencia durante una operación **ConnectionEvent**.</span><span class="sxs-lookup"><span data-stu-id="b1009-104">The **InfoMessage** event is called whenever a warning occurs during a **ConnectionEvent** operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1009-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1009-105">Syntax</span></span>

<span data-ttu-id="b1009-106">InfoMessage *pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="b1009-106">InfoMessage *pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="b1009-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1009-107">Parameters</span></span>

|<span data-ttu-id="b1009-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b1009-108">Parameter</span></span>|<span data-ttu-id="b1009-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1009-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b1009-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="b1009-110">*pError*</span></span> |<span data-ttu-id="b1009-p101">Objeto [Error](error-object-ado.md). Este parámetro contiene cualquier error devuelto. Si se devuelven varios errores, enumere la colección **Errors** para encontrarlos.</span><span class="sxs-lookup"><span data-stu-id="b1009-p101">An [Error](error-object-ado.md) object. This parameter contains any errors that are returned. If multiple errors are returned, enumerate the **Errors** collection to find them.</span></span>|
|<span data-ttu-id="b1009-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="b1009-114">*adStatus*</span></span> |<span data-ttu-id="b1009-115">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="b1009-115">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="b1009-116">Antes de que el evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b1009-116">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="b1009-117">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="b1009-117">*pConnection*</span></span> |<span data-ttu-id="b1009-p103">Objeto [Connection](connection-object-ado.md). La conexión para la que se produjo la advertencia. Por ejemplo, las advertencias pueden ocurrir al abrir un objeto **Connection** o ejecutar un objeto [Command](command-object-ado.md) sobre un objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="b1009-p103">A [Connection](connection-object-ado.md) object. The connection for which the warning occurred. For example, warnings can occur when opening a **Connection** object or executing a [Command](command-object-ado.md) on a **Connection**.</span></span>|

