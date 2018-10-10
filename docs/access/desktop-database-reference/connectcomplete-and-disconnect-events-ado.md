---
title: s ConnectComplete y Disconnect (evento, ADO)
TOCTitle: ConnectComplete and Disconnect Events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 731879abf181f64c24b1012e45ea23435f965574
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485980"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="f181d-102">s ConnectComplete y Disconnect (evento, ADO)</span><span class="sxs-lookup"><span data-stu-id="f181d-102">ConnectComplete and Disconnect Events (ADO)</span></span>


<span data-ttu-id="f181d-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f181d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f181d-p101">Al evento **ConnectComplete** se le llama después de que un conexión se *inicia*. Al evento **Disconnect** se le llama después de que una conexión *finaliza*.</span><span class="sxs-lookup"><span data-stu-id="f181d-p101">The **ConnectComplete** event is called after a connection *starts*. The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="f181d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f181d-106">Syntax</span></span>

<span data-ttu-id="f181d-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="f181d-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="f181d-108">Desconectar*adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="f181d-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="f181d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f181d-109">Parameters</span></span>

  - <span data-ttu-id="f181d-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="f181d-110">*pError*</span></span>

  - <span data-ttu-id="f181d-p102">Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f181d-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="f181d-113">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="f181d-113">*adStatus*</span></span>

  - [<span data-ttu-id="f181d-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="f181d-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="f181d-115">Cuando se llama a **ConnectComplete**, este parámetro se establece en **adStatusCancel** si un evento **WillConnect** ha solicitado la cancelación de la conexión pendiente.</span><span class="sxs-lookup"><span data-stu-id="f181d-115">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span>
    
    <span data-ttu-id="f181d-p103">Antes de que cualquiera evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores. Sin embargo, si se cierra y se vuelve a abrir el objeto [Connection](connection-object-ado.md), estos eventos vuelven a ocurrir.</span><span class="sxs-lookup"><span data-stu-id="f181d-p103">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>

  - <span data-ttu-id="f181d-118">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="f181d-118">*pConnection*</span></span>

  - <span data-ttu-id="f181d-119">Objeto **Connection** al que se aplica este evento.</span><span class="sxs-lookup"><span data-stu-id="f181d-119">The **Connection** object for which this event applies.</span></span>

