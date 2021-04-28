---
title: CreateMAPIInitializationMonitor
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
ms.assetid: 32a9758a-395d-4526-9610-3e4eeaf78c96
description: Monitor de inicialización MAPI
Last modified: April 26, 2021
ms.openlocfilehash: da7c48a6b026ccd4cbe4cbac192a1a0760202835
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062056"
---
# <a name="createmapiinitializationmonitor"></a><span data-ttu-id="90d54-103">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="90d54-103">CreateMAPIInitializationMonitor</span></span>

<span data-ttu-id="90d54-104">**Se aplica a**: Outlook 2016 | Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="90d54-104">**Applies to**: Outlook 2016 | Outlook 2019</span></span>
  
## <a name="mapi-initialization-monitor"></a><span data-ttu-id="90d54-105">Monitor de inicialización MAPI</span><span class="sxs-lookup"><span data-stu-id="90d54-105">MAPI Initialization Monitor</span></span>

<span data-ttu-id="90d54-106">Hay ocasiones en las que una aplicación que consume MAPI puede querer saber cuándo se completa la inicialización.</span><span class="sxs-lookup"><span data-stu-id="90d54-106">There are times when an application which consumes MAPI might want to know when the initialization is completed.</span></span> <span data-ttu-id="90d54-107">Por ejemplo, tiene varios subprocesos que podrían inicializar MAPI, o en respuesta a MAPI que se inicializa la aplicación le gustaría realizar algún trabajo, pero no quiere girar siempre la pila MAPI.</span><span class="sxs-lookup"><span data-stu-id="90d54-107">For example, it have multiple threads which could initialize MAPI, or in response to MAPI being initialize the application would like perform some work, but does not want to always spin up the MAPI stack.</span></span> <span data-ttu-id="90d54-108">El monitor de inicialización proporciona esta funcionalidad a través de una función (exportada desde OLMAPI32.DLL) y un par de interfaces sencillas que se describen a continuación.</span><span class="sxs-lookup"><span data-stu-id="90d54-108">The initialization monitor provides this functionality through a function (exported from OLMAPI32.DLL) and a couple of simple interfaces described below.</span></span>

<span data-ttu-id="90d54-109">Este es el punto de entrada exportado desde OLMAPI32.DLL esto permite al autor de la llamada recuperar una interfaz para consultar el estado de inicialización actual, configurar una devolución de llamada para la finalización de inicialización o bloquear el subproceso actual hasta que se haya completado.</span><span class="sxs-lookup"><span data-stu-id="90d54-109">This is entry point exported from OLMAPI32.DLL this allows the caller to retrieve an interface to query the current initialization state, setup a callback for initialization completion or block the current thread until has completed.</span></span> <span data-ttu-id="90d54-110">El objeto devuelto de esta API es reutilizable y seguro para subprocesos y se puede invocar desde cualquier subproceso, no solo desde el subproceso que la recuperó.</span><span class="sxs-lookup"><span data-stu-id="90d54-110">The object returned from this API is reusable and thread safe and can be invoked from any thread, not just thread which retrieved it.</span></span> <span data-ttu-id="90d54-111">Además, a diferencia de otros objetos expuestos desde MAPI, este objeto es válido siempre que se cargue la DLL, se puede volver a usar en las sesiones de inicialización y se puede consumir antes o después de llamar a MAPIInitialize.</span><span class="sxs-lookup"><span data-stu-id="90d54-111">Also, unlike other objects exposed from MAPI, this object is valid as long as the DLL is loaded, it can be re-used across initialization sessions and can be consumed before or after MAPIInitialize has been called.</span></span> <span data-ttu-id="90d54-112">Devuelve éxito o error a través de un HRESULT estándar COM y asigna un parámetro de salida a una instancia de IMAPIInitMonitor.</span><span class="sxs-lookup"><span data-stu-id="90d54-112">Returns success or failure through an COM standard HRESULT, and assigns an out parameter to an instance of IMAPIInitMonitor.</span></span>

```cpp
HRESULT CreateMAPIInitializationMonitor(IMAPIInitMonitor** ppInitMonitor); 
```
#### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a><span data-ttu-id="90d54-113">HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)</span><span class="sxs-lookup"><span data-stu-id="90d54-113">HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)</span></span>

<span data-ttu-id="90d54-114">Este punto de entrada exportado desde OLMAPI32.DLL permite al autor de la llamada recuperar una interfaz para consultar el estado de inicialización actual, configurar una devolución de llamada para la finalización de la inicialización o bloquear el subproceso actual hasta que se haya completado.</span><span class="sxs-lookup"><span data-stu-id="90d54-114">This entry point exported from OLMAPI32.DLL allows the caller to retrieve an interface to query the current initialization state, setup a callback for initialization completion or block the current thread until has completed.</span></span> <span data-ttu-id="90d54-115">El objeto devuelto de esta API es reutilizable y seguro para subprocesos y se puede invocar desde cualquier subproceso, no solo desde el subproceso que la recuperó.</span><span class="sxs-lookup"><span data-stu-id="90d54-115">The object returned from this API is reusable and thread safe and can be invoked from any thread, not just thread which retrieved it.</span></span> <span data-ttu-id="90d54-116">Además, a diferencia de otros objetos expuestos desde MAPI, este objeto es válido siempre que se cargue la DLL, se puede volver a usar en las sesiones de inicialización y se puede consumir antes o después de llamar a MAPIInitialize.</span><span class="sxs-lookup"><span data-stu-id="90d54-116">Also, unlike other objects exposed from MAPI, this object is valid as long as the DLL is loaded, it can be re-used across initialization sessions and can be consumed before or after MAPIInitialize has been called.</span></span> <span data-ttu-id="90d54-117">Devuelve éxito o error a través de un HRESULT estándar COM y asigna un parámetro de salida a una instancia de IMAPIInitMonitor.</span><span class="sxs-lookup"><span data-stu-id="90d54-117">Returns success or failure through an COM standard HRESULT, and assigns an out parameter to an instance of IMAPIInitMonitor.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="90d54-118">Información rápida</span><span class="sxs-lookup"><span data-stu-id="90d54-118">Quick info</span></span>

| <span data-ttu-id="90d54-119">identificador</span><span class="sxs-lookup"><span data-stu-id="90d54-119">identifier</span></span> | <span data-ttu-id="90d54-120">result</span><span class="sxs-lookup"><span data-stu-id="90d54-120">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="90d54-121">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="90d54-121">Exported by:</span></span>  <br/> |<span data-ttu-id="90d54-122">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="90d54-122">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="90d54-123">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="90d54-123">Called by:</span></span>  <br/> |<span data-ttu-id="90d54-124">Cliente</span><span class="sxs-lookup"><span data-stu-id="90d54-124">Client</span></span>  <br/> |
|<span data-ttu-id="90d54-125">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="90d54-125">Implemented by:</span></span>  <br/> |<span data-ttu-id="90d54-126">Outlook</span><span class="sxs-lookup"><span data-stu-id="90d54-126">Outlook</span></span>  <br/> |

## <a name="parameters"></a><span data-ttu-id="90d54-127">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90d54-127">Parameters</span></span>
  
 <span data-ttu-id="90d54-128">_ppInitMonitor_</span><span class="sxs-lookup"><span data-stu-id="90d54-128">_ppInitMonitor_</span></span>
> <span data-ttu-id="90d54-129">[salida] Puntero para recibir la instancia recién creada del monitor de inicialización MAPI.</span><span class="sxs-lookup"><span data-stu-id="90d54-129">[out] A pointer to receive the newly created instance of the MAPI initialization monitor.</span></span>
  
## <a name="return-values"></a><span data-ttu-id="90d54-130">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="90d54-130">Return values</span></span>

<span data-ttu-id="90d54-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="90d54-131">S_OK</span></span>
> <span data-ttu-id="90d54-132">Se creó correctamente una nueva instancia del monitor de inicialización.</span><span class="sxs-lookup"><span data-stu-id="90d54-132">A new instance of the initialization monitor was created successfully.</span></span>

<span data-ttu-id="90d54-133">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="90d54-133">E_OUTOFMEMORY</span></span>
> <span data-ttu-id="90d54-134">No había suficiente memoria para crear un nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="90d54-134">There was not enough memory to crate a new object.</span></span>

## <a name="see-also"></a><span data-ttu-id="90d54-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="90d54-135">See also</span></span>
[<span data-ttu-id="90d54-136">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="90d54-136">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="90d54-137">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="90d54-137">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
