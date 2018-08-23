---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cbad4b903592f83fc7d72fde21f149c9835f2e23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575640"
---
# <a name="fnidle"></a><span data-ttu-id="9626b-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="9626b-103">FNIDLE</span></span>
 
<span data-ttu-id="9626b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9626b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9626b-105">Define una rutina de inactividad que el motor de inactividad de MAPI llama periódicamente según la prioridad.</span><span class="sxs-lookup"><span data-stu-id="9626b-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9626b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9626b-106">Header file:</span></span>  <br/> |<span data-ttu-id="9626b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9626b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9626b-108">Función definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="9626b-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="9626b-109">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="9626b-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="9626b-110">Llamado por una función definida:</span><span class="sxs-lookup"><span data-stu-id="9626b-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="9626b-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="9626b-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="9626b-112">Tipo de puntero correspondiente:</span><span class="sxs-lookup"><span data-stu-id="9626b-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="9626b-113">PFNIDLE</span><span class="sxs-lookup"><span data-stu-id="9626b-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="9626b-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9626b-114">Parameters</span></span>

 <span data-ttu-id="9626b-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="9626b-115">_lpvContext_</span></span>
  
> <span data-ttu-id="9626b-116">[entrada] Puntero a un bloque de memoria que MAPI pasadas a la rutina de inactividad cada vez que lo llama.</span><span class="sxs-lookup"><span data-stu-id="9626b-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="9626b-117">Este puntero se pasa al motor de inactividad de MAPI en el parámetro _pvIdleParam_ por [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span><span class="sxs-lookup"><span data-stu-id="9626b-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="9626b-118">Los datos en el bloque de memoria pueden proporcionar contexto para la llamada a la rutina de inactividad, como qué objeto para funcionar en, o el estado actual de una operación larga.</span><span class="sxs-lookup"><span data-stu-id="9626b-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9626b-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9626b-119">Return value</span></span>

<span data-ttu-id="9626b-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="9626b-120">FALSE</span></span> 
  
> <span data-ttu-id="9626b-121">Una rutina de inactividad con el prototipo **FNIDLE** siempre debe devolver FALSE.</span><span class="sxs-lookup"><span data-stu-id="9626b-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9626b-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9626b-122">Remarks</span></span>

<span data-ttu-id="9626b-123">La funcionalidad específica de la rutina de inactividad se determina mediante la implementación de la aplicación de cliente o un proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="9626b-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="9626b-124">El cliente o el proveedor debe limitar el tiempo de ejecución de cada estado de una rutina de inactividad.</span><span class="sxs-lookup"><span data-stu-id="9626b-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="9626b-125">Cada estado debe realizar una cantidad mínima de procesamiento, actualizar el estado actual de los datos de contexto que señala _lpvContext_y volver al motor de inactividad de MAPI.</span><span class="sxs-lookup"><span data-stu-id="9626b-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="9626b-126">El cliente o el proveedor debe llamar a la función MAPI [MAPIInitIdle](mapiinitidle.md) antes de que se puede registrar su propia rutina de inactividad con una llamada a la función [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) .</span><span class="sxs-lookup"><span data-stu-id="9626b-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="9626b-127">Las siguientes funciones de abordar los problemas con el motor de inactividad de MAPI y con las rutinas de inactividad según el prototipo de función FNIDLE:</span><span class="sxs-lookup"><span data-stu-id="9626b-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="9626b-128">**Función rutina inactivo**</span><span class="sxs-lookup"><span data-stu-id="9626b-128">**Idle routine function**</span></span>|<span data-ttu-id="9626b-129">**Uso**</span><span class="sxs-lookup"><span data-stu-id="9626b-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9626b-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9626b-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="9626b-131">Cambia las características de una rutina de inactividad registrada.</span><span class="sxs-lookup"><span data-stu-id="9626b-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="9626b-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9626b-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="9626b-133">Quita una rutina de inactividad registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="9626b-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="9626b-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9626b-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="9626b-135">Deshabilita o habilita volver a una rutina de inactividad registrada sin quitar desde el sistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="9626b-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="9626b-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9626b-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="9626b-137">Agrega una rutina de inactividad en el sistema MAPI, con o sin habilitarla.</span><span class="sxs-lookup"><span data-stu-id="9626b-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="9626b-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="9626b-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="9626b-139">Se cierra el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="9626b-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="9626b-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="9626b-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="9626b-141">Inicializa el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="9626b-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="9626b-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como un parámetro de entrada de la etiqueta de función devuelto por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="9626b-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="9626b-143">Cuando se convierten en todas las tareas de primer plano de la plataforma de inactividad, el motor de inactividad de MAPI llama a la rutina de inactividad de prioridad más alta que esté lista para ejecutar.</span><span class="sxs-lookup"><span data-stu-id="9626b-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="9626b-144">No hay ninguna garantía de orden entre las rutinas de inactividad de la misma prioridad de llamada.</span><span class="sxs-lookup"><span data-stu-id="9626b-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

