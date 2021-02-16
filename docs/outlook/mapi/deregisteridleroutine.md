---
title: DeregisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 62231a900dbe01ebe1e848355226c0589072cd42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404564"
---
# <a name="deregisteridleroutine"></a><span data-ttu-id="2743a-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2743a-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="2743a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2743a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2743a-105">Quita una rutina inactiva basada en [FNIDLE](fnidle.md) del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="2743a-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2743a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2743a-106">Header file:</span></span>  <br/> |<span data-ttu-id="2743a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2743a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2743a-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2743a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2743a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2743a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2743a-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="2743a-110">Called by:</span></span>  <br/> |<span data-ttu-id="2743a-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="2743a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="2743a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2743a-112">Parameters</span></span>

 <span data-ttu-id="2743a-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="2743a-113">_ftg_</span></span>
  
> <span data-ttu-id="2743a-114">[entrada] Etiqueta de función que identifica la rutina inactiva que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="2743a-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2743a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2743a-115">Return value</span></span>

<span data-ttu-id="2743a-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2743a-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2743a-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2743a-117">Remarks</span></span>

<span data-ttu-id="2743a-118">Cualquier tarea de una aplicación cliente o un proveedor de servicios puede anular el registro de cualquier rutina inactiva para la que tenga un  _parámetro ftg_ válido.</span><span class="sxs-lookup"><span data-stu-id="2743a-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="2743a-119">En particular, una rutina inactiva puede anular el registro.</span><span class="sxs-lookup"><span data-stu-id="2743a-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="2743a-120">Las siguientes funciones tratan con el motor de inactividad MAPI y con rutinas inactivas basadas en el prototipo de función [FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="2743a-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="2743a-121">**Función de rutina inactiva**</span><span class="sxs-lookup"><span data-stu-id="2743a-121">**Idle routine function**</span></span>|<span data-ttu-id="2743a-122">**Uso**</span><span class="sxs-lookup"><span data-stu-id="2743a-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2743a-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2743a-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="2743a-124">Cambia las características de una rutina de inactividad registrada.</span><span class="sxs-lookup"><span data-stu-id="2743a-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="2743a-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="2743a-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="2743a-126">Quita una rutina de inactividad registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="2743a-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="2743a-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2743a-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="2743a-128">Deshabilita o vuelve a habilitar una rutina de inactividad registrada sin quitarla del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="2743a-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="2743a-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2743a-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="2743a-130">Agrega una rutina inactiva al sistema MAPI, con o sin habilitarla.</span><span class="sxs-lookup"><span data-stu-id="2743a-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="2743a-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="2743a-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="2743a-132">Apaga el motor de inactividad MAPI para la aplicación que llama.</span><span class="sxs-lookup"><span data-stu-id="2743a-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="2743a-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="2743a-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="2743a-134">Inicializa el motor de inactividad MAPI para la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="2743a-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="2743a-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine** y **EnableIdleRoutine** toman como parámetro de entrada la etiqueta de función devuelta por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="2743a-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="2743a-136">Cuando todas las tareas en primer plano de la plataforma están inactivas, el motor de inactividad MAPI llama a la rutina de inactividad de prioridad más alta que está lista para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="2743a-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="2743a-137">No hay ninguna garantía de orden de llamada entre rutinas inactivas de la misma prioridad.</span><span class="sxs-lookup"><span data-stu-id="2743a-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="2743a-138">Después de anular el registro de la rutina inactiva, el motor inactivo no la llama de nuevo.</span><span class="sxs-lookup"><span data-stu-id="2743a-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="2743a-139">Cualquier implementación que llame **a DeregisterIdleRoutine** debe desasignar los bloques de memoria a los que pasó punteros para que el motor inactivo lo use en su llamada original a la función **FtgRegisterIdleRoutine.**</span><span class="sxs-lookup"><span data-stu-id="2743a-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

