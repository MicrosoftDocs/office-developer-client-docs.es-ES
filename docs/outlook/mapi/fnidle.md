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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342248"
---
# <a name="fnidle"></a><span data-ttu-id="58ccb-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="58ccb-103">FNIDLE</span></span>
 
<span data-ttu-id="58ccb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58ccb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58ccb-105">Define una rutina inactiva que el motor de inactividad de MAPI llama periódicamente de acuerdo con la prioridad.</span><span class="sxs-lookup"><span data-stu-id="58ccb-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58ccb-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="58ccb-106">Header file:</span></span>  <br/> |<span data-ttu-id="58ccb-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="58ccb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="58ccb-108">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="58ccb-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="58ccb-109">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="58ccb-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="58ccb-110">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="58ccb-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="58ccb-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="58ccb-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="58ccb-112">Tipo de puntero correspondiente:</span><span class="sxs-lookup"><span data-stu-id="58ccb-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="58ccb-113">PFNIDLE</span><span class="sxs-lookup"><span data-stu-id="58ccb-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="58ccb-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="58ccb-114">Parameters</span></span>

 <span data-ttu-id="58ccb-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="58ccb-115">_lpvContext_</span></span>
  
> <span data-ttu-id="58ccb-116">a Puntero a un bloque de memoria que MAPI pasa a la rutina inactiva cada vez que lo llama.</span><span class="sxs-lookup"><span data-stu-id="58ccb-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="58ccb-117">Este puntero se pasa al motor de inactividad MAPI en el parámetro _pvIdleParam_ por [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span><span class="sxs-lookup"><span data-stu-id="58ccb-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="58ccb-118">Los datos en el bloque de memoria pueden proporcionar contexto para la llamada a la rutina inactiva, como el objeto en el que operar o el estado actual de una operación prolongada.</span><span class="sxs-lookup"><span data-stu-id="58ccb-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="58ccb-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58ccb-119">Return value</span></span>

<span data-ttu-id="58ccb-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="58ccb-120">FALSE</span></span> 
  
> <span data-ttu-id="58ccb-121">Una rutina inactiva con el prototipo **FNIDLE** siempre debe devolver false.</span><span class="sxs-lookup"><span data-stu-id="58ccb-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="58ccb-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58ccb-122">Remarks</span></span>

<span data-ttu-id="58ccb-123">La funcionalidad específica de la rutina inactiva está determinada por el proveedor de servicios o la aplicación cliente que se está implementando.</span><span class="sxs-lookup"><span data-stu-id="58ccb-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="58ccb-124">El cliente o el proveedor debe limitar el tiempo de ejecución de cada estado de una rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="58ccb-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="58ccb-125">Cada Estado debe realizar una cantidad mínima de procesamiento, actualizar el estado actual en los datos de contexto señalados por _lpvContext_y volver al motor de inACTIVIDAD de MAPI.</span><span class="sxs-lookup"><span data-stu-id="58ccb-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="58ccb-126">El cliente o el proveedor debe llamar a la función MAPI [MAPIInitIdle](mapiinitidle.md) antes de que pueda registrar su propia rutina inactiva con una llamada a la función [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) .</span><span class="sxs-lookup"><span data-stu-id="58ccb-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="58ccb-127">Las siguientes funciones tratan con el motor de inactividad de MAPI y con rutinas inactivas basadas en el prototipo de función FNIDLE:</span><span class="sxs-lookup"><span data-stu-id="58ccb-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="58ccb-128">**Función de rutina inActiva**</span><span class="sxs-lookup"><span data-stu-id="58ccb-128">**Idle routine function**</span></span>|<span data-ttu-id="58ccb-129">**Usage**</span><span class="sxs-lookup"><span data-stu-id="58ccb-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58ccb-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="58ccb-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="58ccb-131">Cambia las características de una rutina inactiva registrada.</span><span class="sxs-lookup"><span data-stu-id="58ccb-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="58ccb-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="58ccb-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="58ccb-133">Quita una rutina inactiva registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="58ccb-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="58ccb-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="58ccb-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="58ccb-135">Deshabilita o vuelve a habilitar una rutina inactiva registrada sin quitarla del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="58ccb-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="58ccb-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="58ccb-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="58ccb-137">Agrega una rutina inactiva al sistema MAPI, con o sin habilitar.</span><span class="sxs-lookup"><span data-stu-id="58ccb-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="58ccb-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="58ccb-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="58ccb-139">Cierra el motor de inactividad MAPI de la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="58ccb-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="58ccb-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="58ccb-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="58ccb-141">Inicializa el motor de inactividad MAPI para la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="58ccb-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="58ccb-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como parámetro de entrada la etiqueta de la función devuelta por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="58ccb-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="58ccb-143">Cuando todas las tareas de primer plano de la plataforma se convierten en inactivas, el motor de inactividad de MAPI llama a la rutina inactiva de máxima prioridad que está lista para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="58ccb-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="58ccb-144">No hay ninguna garantía del orden de llamadas entre rutinas de inactividad de la misma prioridad.</span><span class="sxs-lookup"><span data-stu-id="58ccb-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

