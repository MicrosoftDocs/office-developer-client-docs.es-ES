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
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412383"
---
# <a name="fnidle"></a><span data-ttu-id="838a9-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="838a9-103">FNIDLE</span></span>
 
<span data-ttu-id="838a9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="838a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="838a9-105">Define una rutina inactiva a la que el motor de inactividad MAPI llama periódicamente según la prioridad.</span><span class="sxs-lookup"><span data-stu-id="838a9-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="838a9-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="838a9-106">Header file:</span></span>  <br/> |<span data-ttu-id="838a9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="838a9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="838a9-108">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="838a9-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="838a9-109">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="838a9-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="838a9-110">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="838a9-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="838a9-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="838a9-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="838a9-112">Tipo de puntero correspondiente:</span><span class="sxs-lookup"><span data-stu-id="838a9-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="838a9-113">PFNIDLE</span><span class="sxs-lookup"><span data-stu-id="838a9-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="838a9-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="838a9-114">Parameters</span></span>

 <span data-ttu-id="838a9-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="838a9-115">_lpvContext_</span></span>
  
> <span data-ttu-id="838a9-116">[entrada] Puntero a un bloque de memoria que MAPI pasa a la rutina inactiva cada vez que lo llama.</span><span class="sxs-lookup"><span data-stu-id="838a9-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="838a9-117">Este puntero se pasa al motor inactivo MAPI en el parámetro  _pvIdleParam_ [mediante FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span><span class="sxs-lookup"><span data-stu-id="838a9-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="838a9-118">Los datos del bloque de memoria pueden proporcionar contexto para la llamada a la rutina inactiva, como el objeto en el que se va a operar o el estado actual de una operación larga.</span><span class="sxs-lookup"><span data-stu-id="838a9-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="838a9-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="838a9-119">Return value</span></span>

<span data-ttu-id="838a9-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="838a9-120">FALSE</span></span> 
  
> <span data-ttu-id="838a9-121">Una rutina inactiva con el **prototipo FNIDLE** siempre debe devolver FALSE.</span><span class="sxs-lookup"><span data-stu-id="838a9-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="838a9-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="838a9-122">Remarks</span></span>

<span data-ttu-id="838a9-123">La funcionalidad específica de la rutina inactiva la determina la aplicación cliente o el proveedor de servicios de implementación.</span><span class="sxs-lookup"><span data-stu-id="838a9-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="838a9-124">El cliente o proveedor debe limitar el tiempo de ejecución de cada estado de una rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="838a9-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="838a9-125">Cada estado debe realizar una cantidad mínima de procesamiento, actualizar el estado actual en los datos de contexto a los que apunta  _lpvContext_ y volver al motor inactivo MAPI.</span><span class="sxs-lookup"><span data-stu-id="838a9-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="838a9-126">El cliente o proveedor debe llamar a la función [MAPI MAPIInitIdle](mapiinitidle.md) para poder registrar su propia rutina inactiva con una llamada a la función [FtgRegisterIdleRoutine.](ftgregisteridleroutine.md)</span><span class="sxs-lookup"><span data-stu-id="838a9-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="838a9-127">Las siguientes funciones tratan con el motor de inactividad MAPI y con rutinas inactivas basadas en el prototipo de función FNIDLE:</span><span class="sxs-lookup"><span data-stu-id="838a9-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="838a9-128">**Función de rutina inactiva**</span><span class="sxs-lookup"><span data-stu-id="838a9-128">**Idle routine function**</span></span>|<span data-ttu-id="838a9-129">**Uso**</span><span class="sxs-lookup"><span data-stu-id="838a9-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="838a9-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="838a9-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="838a9-131">Cambia las características de una rutina de inactividad registrada.</span><span class="sxs-lookup"><span data-stu-id="838a9-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="838a9-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="838a9-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="838a9-133">Quita una rutina de inactividad registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="838a9-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="838a9-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="838a9-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="838a9-135">Deshabilita o vuelve a habilitar una rutina de inactividad registrada sin quitarla del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="838a9-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="838a9-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="838a9-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="838a9-137">Agrega una rutina inactiva al sistema MAPI, con o sin habilitarla.</span><span class="sxs-lookup"><span data-stu-id="838a9-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="838a9-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="838a9-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="838a9-139">Cierra el motor de inactividad MAPI para la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="838a9-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="838a9-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="838a9-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="838a9-141">Inicializa el motor de inactividad MAPI para la aplicación que llama.</span><span class="sxs-lookup"><span data-stu-id="838a9-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="838a9-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine** y **EnableIdleRoutine** toman como parámetro de entrada la etiqueta de función devuelta por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="838a9-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="838a9-143">Cuando todas las tareas en primer plano de la plataforma están inactivas, el motor de inactividad MAPI llama a la rutina de inactividad de prioridad más alta que está lista para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="838a9-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="838a9-144">No hay ninguna garantía de orden de llamada entre rutinas inactivas de la misma prioridad.</span><span class="sxs-lookup"><span data-stu-id="838a9-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

