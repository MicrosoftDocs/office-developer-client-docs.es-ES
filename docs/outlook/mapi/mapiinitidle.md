---
title: MAPIInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e4f4cdd1d0ed2e03d49f471e6e91464b7973c920
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818255"
---
# <a name="mapiinitidle"></a><span data-ttu-id="25c9c-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="25c9c-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="25c9c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25c9c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25c9c-105">Inicializa el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="25c9c-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25c9c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="25c9c-106">Header file:</span></span>  <br/> |<span data-ttu-id="25c9c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="25c9c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="25c9c-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="25c9c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="25c9c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="25c9c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="25c9c-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="25c9c-110">Called by:</span></span>  <br/> |<span data-ttu-id="25c9c-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="25c9c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="25c9c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25c9c-112">Parameters</span></span>

 <span data-ttu-id="25c9c-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="25c9c-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="25c9c-114">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="25c9c-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="25c9c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25c9c-115">Return value</span></span>

<span data-ttu-id="25c9c-116">La función **MAPIInitIdle** devuelve cero si la inicialización es correcta y 1, en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="25c9c-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="25c9c-117">Si se llama a **MAPIInitIdle** varias veces, todas las llamadas adicionales se realizan con éxito, pero se omiten excepto to incrementar el recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="25c9c-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="25c9c-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25c9c-118">Remarks</span></span>

<span data-ttu-id="25c9c-119">Una aplicación de cliente o un proveedor de servicios debe llamar a **MAPIInitIdle** antes de llamar a cualquier otra función de motor inactivo.</span><span class="sxs-lookup"><span data-stu-id="25c9c-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="25c9c-120">Todas las llamadas a **MAPIInitIdle** deben coincidir por una llamada a [MAPIDeInitIdle](mapideinitidle.md)posterior o el motor de inactividad quedo en ejecución para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="25c9c-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="25c9c-121">Las siguientes funciones de abordar los problemas con el motor de inactividad de MAPI y con las rutinas de inactividad según el prototipo de función [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="25c9c-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="25c9c-122">**Función rutina inactivo**</span><span class="sxs-lookup"><span data-stu-id="25c9c-122">**Idle routine function**</span></span>|<span data-ttu-id="25c9c-123">**Uso**</span><span class="sxs-lookup"><span data-stu-id="25c9c-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25c9c-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="25c9c-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="25c9c-125">Cambia las características de una rutina de inactividad registrada.</span><span class="sxs-lookup"><span data-stu-id="25c9c-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="25c9c-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="25c9c-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="25c9c-127">Quita una rutina de inactividad registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="25c9c-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="25c9c-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="25c9c-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="25c9c-129">Deshabilita o habilita volver a una rutina de inactividad registrada sin quitar desde el sistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="25c9c-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="25c9c-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="25c9c-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="25c9c-131">Agrega una rutina de inactividad en el sistema MAPI, con o sin habilitarla.</span><span class="sxs-lookup"><span data-stu-id="25c9c-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="25c9c-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="25c9c-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="25c9c-133">Se cierra el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="25c9c-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="25c9c-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="25c9c-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="25c9c-135">Inicializa el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="25c9c-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="25c9c-136">Cuando se convierten en todas las tareas de primer plano de la plataforma de inactividad, el motor de inactividad de MAPI llama a la rutina de inactividad de prioridad más alta que esté lista para ejecutar.</span><span class="sxs-lookup"><span data-stu-id="25c9c-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="25c9c-137">No hay ninguna garantía de orden entre las rutinas de inactividad de la misma prioridad de llamada.</span><span class="sxs-lookup"><span data-stu-id="25c9c-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

