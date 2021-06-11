---
title: 'IMAPIInitMonitor : IUnknown'
manager: lindalu
26ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIInitMonitor
api_type:
- COM
ms.assetid: ad71ea65-394d-4be2-a9da-cd23099bc2cc
description: IMAPIInitMonitor
Last modified: April 26, 2021
ms.openlocfilehash: dd17d50b04755d9d9c2a10a9b02cd821faf1f7ec
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062049"
---
# <a name="imapiinitmonitor--iunknown"></a><span data-ttu-id="58f9e-103">IMAPIInitMonitor : IUnknown</span><span class="sxs-lookup"><span data-stu-id="58f9e-103">IMAPIInitMonitor : IUnknown</span></span>

<span data-ttu-id="58f9e-104">**Se aplica a**: Outlook 2013 | Outlook 2016 | Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="58f9e-104">**Applies to**: Outlook 2013 | Outlook 2016 | Outlook 2019</span></span>

<span data-ttu-id="58f9e-105">Hay ocasiones en las que una aplicación que consume MAPI puede querer saber cuándo se completa la inicialización.</span><span class="sxs-lookup"><span data-stu-id="58f9e-105">There are times when an application which consumes MAPI might want to know when the initialization is completed.</span></span> <span data-ttu-id="58f9e-106">Por ejemplo, tiene varios subprocesos que podrían inicializar MAPI, o en respuesta a MAPI que se inicializa la aplicación le gustaría realizar algún trabajo, pero no quiere girar siempre la pila MAPI.</span><span class="sxs-lookup"><span data-stu-id="58f9e-106">For example, it has multiple threads which could initialize MAPI, or in response to MAPI being initialized the application would like perform some work, but does not want to always spin up the MAPI stack.</span></span> <span data-ttu-id="58f9e-107">El monitor de inicialización proporciona esta funcionalidad a través [de un objeto CreateMAPIInitializationMonitor.](createmapiinitializationmonitor.md)</span><span class="sxs-lookup"><span data-stu-id="58f9e-107">The initialization monitor provides this functionality through a [CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md) object.</span></span>

| <span data-ttu-id="58f9e-108">información rápida</span><span class="sxs-lookup"><span data-stu-id="58f9e-108">quick info</span></span> | <span data-ttu-id="58f9e-109">result</span><span class="sxs-lookup"><span data-stu-id="58f9e-109">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="58f9e-110">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="58f9e-110">Inherits from:</span></span>  <br/> |<span data-ttu-id="58f9e-111">IUnknown</span><span class="sxs-lookup"><span data-stu-id="58f9e-111">IUnknown</span></span>  <br/> |
|<span data-ttu-id="58f9e-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="58f9e-112">Implemented by:</span></span>  <br/> | <span data-ttu-id="58f9e-113">OLMAPI32.DLL</span><span class="sxs-lookup"><span data-stu-id="58f9e-113">OLMAPI32.DLL</span></span> <br/> |
|<span data-ttu-id="58f9e-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="58f9e-114">Called by:</span></span>  <br/> |<span data-ttu-id="58f9e-115">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="58f9e-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="58f9e-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="58f9e-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="58f9e-117">IID_IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="58f9e-117">IID_IMAPIInitMonitor</span></span>  <br/> |

## <a name="vtable-order"></a><span data-ttu-id="58f9e-118">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="58f9e-118">Vtable order</span></span>

| <span data-ttu-id="58f9e-119">function</span><span class="sxs-lookup"><span data-stu-id="58f9e-119">function</span></span> | <span data-ttu-id="58f9e-120">description</span><span class="sxs-lookup"><span data-stu-id="58f9e-120">description</span></span> |
|:-----|:-----|
|[<span data-ttu-id="58f9e-121">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="58f9e-121">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md) <br/> |<span data-ttu-id="58f9e-122">Devuelve el estado actual de inicialización MAPI.</span><span class="sxs-lookup"><span data-stu-id="58f9e-122">Returns the current state of MAPI initialization.</span></span>  <br/> |
|[<span data-ttu-id="58f9e-123">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="58f9e-123">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md) <br/> |<span data-ttu-id="58f9e-124">Inicia una llamada BLOCKING en este subproceso, que devolverá cuando haya transcurrido el número especificado de milisegundos o cuando se haya inicializado MAPI.</span><span class="sxs-lookup"><span data-stu-id="58f9e-124">Initiates a BLOCKING call on this thread, which will return either when the specified number of milliseconds have elapsed or MAPI has been initialized.</span></span>  <span data-ttu-id="58f9e-125">INFINITE se puede usar para una espera infinita.</span><span class="sxs-lookup"><span data-stu-id="58f9e-125">INFINITE can be used to for an infinite wait.</span></span>  <br/> |
|[<span data-ttu-id="58f9e-126">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="58f9e-126">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md) <br/> |<span data-ttu-id="58f9e-127">Inicie una espera para que transcurra la inicialización MAPI o el número especificado de milisegundos.</span><span class="sxs-lookup"><span data-stu-id="58f9e-127">Start a wait for MAPI initialization or the specified number of milliseconds to elapse.</span></span> <span data-ttu-id="58f9e-128">Esto devuelve una interfaz IMAPIWaitResult que debería tener "End" llamado para comenzar la espera.</span><span class="sxs-lookup"><span data-stu-id="58f9e-128">This return an IMAPIWaitResult interface which should have “End” called in order begin the wait.</span></span>  <span data-ttu-id="58f9e-129">Esto permite al autor de la llamada controlar qué subproceso está bloqueado mientras estamos esperando.</span><span class="sxs-lookup"><span data-stu-id="58f9e-129">This allows the caller to control which thread is blocked while we are waiting.</span></span> <br/> |
