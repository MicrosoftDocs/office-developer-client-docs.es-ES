---
title: ConnectComplete y Disconnect (eventos, ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ab98e270fd52d656bf722c7f666afbe22d5ea44
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926307"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="ad416-102">ConnectComplete y Disconnect (eventos, ADO)</span><span class="sxs-lookup"><span data-stu-id="ad416-102">ConnectComplete and Disconnect events (ADO)</span></span>


<span data-ttu-id="ad416-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad416-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad416-p101">Al evento **ConnectComplete** se le llama después de que un conexión se *inicia*. Al evento **Disconnect** se le llama después de que una conexión *finaliza*.</span><span class="sxs-lookup"><span data-stu-id="ad416-p101">The **ConnectComplete** event is called after a connection *starts*. The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad416-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad416-106">Syntax</span></span>

<span data-ttu-id="ad416-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="ad416-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="ad416-108">Desconectar*adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="ad416-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="ad416-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad416-109">Parameters</span></span>

  - <span data-ttu-id="ad416-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="ad416-110">*pError*</span></span>

  - <span data-ttu-id="ad416-p102">Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de *adStatus* es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ad416-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="ad416-113">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="ad416-113">*adStatus*</span></span>

  - [<span data-ttu-id="ad416-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="ad416-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="ad416-115">Cuando se llama a **ConnectComplete**, este parámetro se establece en **adStatusCancel** si un evento **WillConnect** ha solicitado la cancelación de la conexión pendiente.</span><span class="sxs-lookup"><span data-stu-id="ad416-115">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span>
    
    <span data-ttu-id="ad416-p103">Antes de que cualquiera evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores. Sin embargo, si se cierra y se vuelve a abrir el objeto [Connection](connection-object-ado.md), estos eventos vuelven a ocurrir.</span><span class="sxs-lookup"><span data-stu-id="ad416-p103">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>

  - <span data-ttu-id="ad416-118">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="ad416-118">*pConnection*</span></span>

  - <span data-ttu-id="ad416-119">Objeto **Connection** al que se aplica este evento.</span><span class="sxs-lookup"><span data-stu-id="ad416-119">The **Connection** object for which this event applies.</span></span>

