---
title: imapiinitmonitor-beginwait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.BeginWait
api_type:
- COM
ms.assetid: 71f565a9-651c-42b5-9102-91b728b681ae
description: IMAPIInitMonitor::BeginWait"
Last modified: April 26, 2021
ms.openlocfilehash: 43a88507cbfc23b3b842f51e69eb4bd791bcfda8
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062021"
---
# <a name="imapiinitmonitorbeginwait"></a><span data-ttu-id="00f2d-103">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="00f2d-103">IMAPIInitMonitor::BeginWait</span></span>
  
<span data-ttu-id="00f2d-104">**Se aplica a**: Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="00f2d-104">**Applies to**: Outlook 2016 | 2019</span></span>
  
<span data-ttu-id="00f2d-105">Inicie una espera para que transcurra la inicialización MAPI o el número especificado de milisegundos.</span><span class="sxs-lookup"><span data-stu-id="00f2d-105">Start a wait for MAPI initialization or the specified number of milliseconds to elapse.</span></span> <span data-ttu-id="00f2d-106">Esto devuelve una interfaz IMAPIWaitResult que debería llamar a **IMAPIWaitResult::End** para iniciar la espera.</span><span class="sxs-lookup"><span data-stu-id="00f2d-106">This returns an IMAPIWaitResult interface which should have **IMAPIWaitResult::End** called in order initiate the wait.</span></span> <span data-ttu-id="00f2d-107">Esto permite al autor de la llamada controlar qué subproceso está bloqueado mientras estamos esperando.</span><span class="sxs-lookup"><span data-stu-id="00f2d-107">This allows the caller to control which thread is blocked while we are waiting.</span></span>

```cpp
HRESULT IMAPIInitMonitor::BeginWait(DWORD timeout, IMAPIWaitResult** ppResult)
```

## <a name="parameters"></a><span data-ttu-id="00f2d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00f2d-108">Parameters</span></span>
<span data-ttu-id="00f2d-109">_tiempo de espera_</span><span class="sxs-lookup"><span data-stu-id="00f2d-109">_timeout_</span></span>
><span data-ttu-id="00f2d-110">[in] El número de milisegundos que se esperará a la inicialización MAPI, esto puede establecerse en INFINITE para esperar para siempre a que se pueda producir la inicialización.</span><span class="sxs-lookup"><span data-stu-id="00f2d-110">[in] The number of millisecond to wait for MAPI initialization, this can set to INFINITE to wait forever for the initialization to happen.</span></span>

<span data-ttu-id="00f2d-111">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="00f2d-111">_ppResult_</span></span>
><span data-ttu-id="00f2d-112">[salida] Puntero para recibir la interfaz de espera recién creada.</span><span class="sxs-lookup"><span data-stu-id="00f2d-112">[out] A pointer to recieve the newly create wait interface.</span></span>

## <a name="return-value"></a><span data-ttu-id="00f2d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00f2d-113">Return value</span></span>
<span data-ttu-id="00f2d-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="00f2d-114">S_OK</span></span>
><span data-ttu-id="00f2d-115">Se ha iniciado correctamente una operación de espera.</span><span class="sxs-lookup"><span data-stu-id="00f2d-115">A wait operation was successfully started.</span></span>

<span data-ttu-id="00f2d-116">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="00f2d-116">E_OUTOFMEMORY</span></span>
><span data-ttu-id="00f2d-117">No había suficiente memoria para crear un nuevo objeto</span><span class="sxs-lookup"><span data-stu-id="00f2d-117">There was not enough memory to create a new object</span></span>

## <a name="remarks"></a><span data-ttu-id="00f2d-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00f2d-118">Remarks</span></span>
<span data-ttu-id="00f2d-119">Esta API proporcionaba al autor de la llamada una interfaz (que es segura para subprocesos) que se puede usar para iniciar una espera de bloqueo para la inicialización mapi.</span><span class="sxs-lookup"><span data-stu-id="00f2d-119">This API provided the caller with an interface (which is thread-safe) which can be used initiate a blocking wait for MAPI initialization.</span></span> <span data-ttu-id="00f2d-120">Esto permite al consumidor degradar la mejor espera para esperar a su aplicación.</span><span class="sxs-lookup"><span data-stu-id="00f2d-120">This allows the consumer to deterime the best wait to wait for thier application.</span></span>   <span data-ttu-id="00f2d-121">El comportamiento de llamar a IMAPIWaitResult::End es idéntico a llamar a IMAPIInitMonitor::Wait.</span><span class="sxs-lookup"><span data-stu-id="00f2d-121">The behavior of calling IMAPIWaitResult::End is identical to calling IMAPIInitMonitor::Wait.</span></span>

## <a name="see-also"></a><span data-ttu-id="00f2d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="00f2d-122">See also</span></span>

[<span data-ttu-id="00f2d-123">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="00f2d-123">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="00f2d-124">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="00f2d-124">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md)

[<span data-ttu-id="00f2d-125">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="00f2d-125">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md)

[<span data-ttu-id="00f2d-126">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="00f2d-126">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)

[<span data-ttu-id="00f2d-127">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="00f2d-127">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
