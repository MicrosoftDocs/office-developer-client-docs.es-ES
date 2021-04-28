---
title: 'IMAPIWaitResult : IUnknown'
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: d7157f57-709d-4e53-973b-176954e2bb73
description: IMAPIWaitResult
Last modified: April 26, 2021
ms.openlocfilehash: 67a0fffdd0ab6d4989c12568f4d89808ba5adc7a
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062043"
---
# <a name="imapiwaitresult--iunknown"></a><span data-ttu-id="ff4ab-103">IMAPIWaitResult : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff4ab-103">IMAPIWaitResult : IUnknown</span></span>
  
<span data-ttu-id="ff4ab-104">**Se aplica a**: Outlook 2013 | Outlook 2016 | Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="ff4ab-104">**Applies to**: Outlook 2013 | Outlook 2016 | Outlook 2019</span></span>

<span data-ttu-id="ff4ab-105">Los consumidores de IMAPIInitMonitor usan esta interfaz para controlar dónde se produce la espera.</span><span class="sxs-lookup"><span data-stu-id="ff4ab-105">This interface is used by consumers of IMAPIInitMonitor to control where the wait happens.</span></span> <span data-ttu-id="ff4ab-106">Les permite crear el objeto en un subproceso y moverlo a otro subproceso para realizar la espera real.</span><span class="sxs-lookup"><span data-stu-id="ff4ab-106">It allows them create the object on one thread and move it another thread to perform the actual wait.</span></span>

## <a name="vtable-order"></a><span data-ttu-id="ff4ab-107">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="ff4ab-107">Vtable order</span></span>

| <span data-ttu-id="ff4ab-108">function</span><span class="sxs-lookup"><span data-stu-id="ff4ab-108">function</span></span> | <span data-ttu-id="ff4ab-109">description</span><span class="sxs-lookup"><span data-stu-id="ff4ab-109">description</span></span> |
|:-----|:-----|
|[<span data-ttu-id="ff4ab-110">HRESULT IMAPIWaitResult::End()</span><span class="sxs-lookup"><span data-stu-id="ff4ab-110">HRESULT IMAPIWaitResult::End()</span></span>](imapiwaitresult-end.md)|<span data-ttu-id="ff4ab-111">Se llama para iniciar la espera de bloqueo en el subproceso al que se llama, que no necesita ser el mismo subproceso que llamó *a IMAPIInitMonitor::BeginWait*.</span><span class="sxs-lookup"><span data-stu-id="ff4ab-111">Called to initiate the blocking wait on the thread where it is called, which does not need to be the same thread that called *IMAPIInitMonitor::BeginWait*.</span></span>|

| <span data-ttu-id="ff4ab-112">información rápida</span><span class="sxs-lookup"><span data-stu-id="ff4ab-112">quick info</span></span> | <span data-ttu-id="ff4ab-113">result</span><span class="sxs-lookup"><span data-stu-id="ff4ab-113">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="ff4ab-114">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="ff4ab-114">Inherits from:</span></span>  <br/> |<span data-ttu-id="ff4ab-115">IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff4ab-115">IUnknown</span></span>  <br/> |
|<span data-ttu-id="ff4ab-116">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ff4ab-116">Implemented by:</span></span>  <br/> |  <span data-ttu-id="ff4ab-117">OLMAPI32.DLL</span><span class="sxs-lookup"><span data-stu-id="ff4ab-117">OLMAPI32.DLL</span></span><br/> |
|<span data-ttu-id="ff4ab-118">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ff4ab-118">Called by:</span></span>  <br/> |<span data-ttu-id="ff4ab-119">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="ff4ab-119">Client applications</span></span>  <br/> |
|<span data-ttu-id="ff4ab-120">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="ff4ab-120">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ff4ab-121">IID_IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="ff4ab-121">IID_IMAPIWaitResult</span></span>  <br/> |

## <a name="see-also"></a><span data-ttu-id="ff4ab-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff4ab-122">See also</span></span>

[<span data-ttu-id="ff4ab-123">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="ff4ab-123">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="ff4ab-124">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="ff4ab-124">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="ff4ab-125">IMAPIInitMonitor : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff4ab-125">IMAPIInitMonitor : IUnknown</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="ff4ab-126">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="ff4ab-126">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)
