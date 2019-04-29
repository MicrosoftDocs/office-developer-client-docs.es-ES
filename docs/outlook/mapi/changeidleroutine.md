---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cfec9356a866c79b687497c3af007c046a20a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418270"
---
# <a name="changeidleroutine"></a><span data-ttu-id="139e2-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="139e2-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="139e2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="139e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="139e2-105">Cambia algunas o todas las características de una rutina inactiva basada en [FNIDLE](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="139e2-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="139e2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="139e2-106">Header file:</span></span>  <br/> |<span data-ttu-id="139e2-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="139e2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="139e2-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="139e2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="139e2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="139e2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="139e2-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="139e2-110">Called by:</span></span>  <br/> |<span data-ttu-id="139e2-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="139e2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID ChangeIdleRoutine(
  FTG ftg,
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle,
  USHORT ircIdle
);
```

## <a name="parameters"></a><span data-ttu-id="139e2-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="139e2-112">Parameters</span></span>

<span data-ttu-id="139e2-113">_FTG_</span><span class="sxs-lookup"><span data-stu-id="139e2-113">_ftg_</span></span>
  
> <span data-ttu-id="139e2-114">a Etiqueta de función que identifica la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="139e2-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="139e2-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="139e2-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="139e2-116">a Puntero a la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="139e2-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="139e2-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="139e2-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="139e2-118">a Puntero a un nuevo bloque de memoria que asigna la implementación de la llamada a la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="139e2-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="139e2-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="139e2-119">_priIdle_</span></span>
  
> <span data-ttu-id="139e2-120">a Valor que representa una nueva prioridad para la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="139e2-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="139e2-121">Las posibles prioridades de las rutinas definidas por la implementación son mayor o menor que cero, pero no cero.</span><span class="sxs-lookup"><span data-stu-id="139e2-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="139e2-122">Un valor de cero se reserva para un evento de usuario, como un clic del mouse o un mensaje WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="139e2-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="139e2-123">Los valores mayores que cero representan las prioridades de las tareas en segundo plano que tienen una prioridad mayor que los eventos de usuario y se envían como parte del bucle estándar de bombeo de mensajes de Windows.</span><span class="sxs-lookup"><span data-stu-id="139e2-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="139e2-124">Los valores inferiores a cero representan las prioridades de las tareas inactivas que solo se ejecutan durante el tiempo de inactividad del bombeo de mensajes.</span><span class="sxs-lookup"><span data-stu-id="139e2-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="139e2-125">Ejemplos de prioridades son: 1 para envío en primer plano, 1 para la inserción de caracteres de edición de energía y 3 para la descarga de mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="139e2-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="139e2-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="139e2-126">_csecIdle_</span></span>
  
> <span data-ttu-id="139e2-127">a Nueva hora, en centésimas de segundo, que se aplicará a la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="139e2-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="139e2-128">El significado del valor de hora inicial varía en función de lo que se pasa en el parámetro _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="139e2-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="139e2-129">Puede ser:</span><span class="sxs-lookup"><span data-stu-id="139e2-129">It can be:</span></span> 
    
  - <span data-ttu-id="139e2-130">Período mínimo de inacción del usuario que debe transcurrir antes de que el motor de inactividad de MAPI llame a la rutina inactiva por primera vez, si la marca FIROWAIT está establecida en _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="139e2-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="139e2-131">Una vez transCurrido este tiempo, el motor inactivo puede llamar a la rutina inactiva tantas veces como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="139e2-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="139e2-132">El intervalo mínimo entre llamadas a la rutina inactiva, si la marca FIROINTERVAL se establece en _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="139e2-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="139e2-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="139e2-133">_iroIdle_</span></span>
  
> <span data-ttu-id="139e2-134">a Máscara de máscara de marcas que indican nuevas opciones para llamar a la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="139e2-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="139e2-135">Se debe establecer exactamente uno de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="139e2-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="139e2-136">FIROINTERVAL: la hora especificada por el parámetro _csecIdle_ es el intervalo mínimo entre llamadas sucesivas a la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="139e2-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="139e2-137">FIROONCEONLY: obsoleto.</span><span class="sxs-lookup"><span data-stu-id="139e2-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="139e2-138">No usar.</span><span class="sxs-lookup"><span data-stu-id="139e2-138">Do not use.</span></span> 
      
  - <span data-ttu-id="139e2-139">FIROPERBLOCK: obsoleto.</span><span class="sxs-lookup"><span data-stu-id="139e2-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="139e2-140">No usar.</span><span class="sxs-lookup"><span data-stu-id="139e2-140">Do not use.</span></span> 
      
  - <span data-ttu-id="139e2-141">FIROWAIT: la hora especificada por el parámetro _csecIdle_ es el período mínimo de inacción del usuario que debe transcurrir antes de que el motor de inactividad de MAPI llame a la rutina inactiva por primera vez.</span><span class="sxs-lookup"><span data-stu-id="139e2-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="139e2-142">Una vez transCurrido este tiempo, el motor inactivo puede llamar a la rutina inactiva tantas veces como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="139e2-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="139e2-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="139e2-143">_ircIdle_</span></span>
  
> <span data-ttu-id="139e2-144">a Máscara de la máscara usada para indicar los cambios que se van a realizar en la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="139e2-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="139e2-145">Los siguientes indicadores se pueden establecer en cualquier combinación:</span><span class="sxs-lookup"><span data-stu-id="139e2-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="139e2-146">FIRCCSEC: un cambio en el tiempo asociado con la rutina inactiva, es decir, un cambio indicado por el valor pasado en el parámetro _csecIdle_ .</span><span class="sxs-lookup"><span data-stu-id="139e2-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="139e2-147">FIRCIRO: un cambio en las opciones de la rutina inactiva, es decir, un cambio que se indica mediante el valor pasado en el parámetro _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="139e2-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="139e2-148">FIRCPFN: un cambio en el puntero de rutina inactiva, es decir, un cambio que se indica mediante el valor pasado en el parámetro _pfnIdle_ .</span><span class="sxs-lookup"><span data-stu-id="139e2-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="139e2-149">FIRCPRI: un cambio en la prioridad de la rutina inactiva, es decir, un cambio que se indica mediante el valor pasado en el parámetro _priIdle_ .</span><span class="sxs-lookup"><span data-stu-id="139e2-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="139e2-150">FIRCPV: un cambio en el bloque de memoria de la rutina inactiva, es decir, un cambio que se indica mediante el valor pasado en el parámetro _pvIdleParam_ .</span><span class="sxs-lookup"><span data-stu-id="139e2-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="139e2-151">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="139e2-151">Return value</span></span>

<span data-ttu-id="139e2-152">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="139e2-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="139e2-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="139e2-153">Remarks</span></span>

<span data-ttu-id="139e2-154">Las siguientes funciones tratan con el motor de inactividad de MAPI y con rutinas inactivas basadas en el prototipo de función [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="139e2-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="139e2-155">**Función de rutina inActiva**</span><span class="sxs-lookup"><span data-stu-id="139e2-155">**Idle routine function**</span></span>|<span data-ttu-id="139e2-156">**Usage**</span><span class="sxs-lookup"><span data-stu-id="139e2-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="139e2-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="139e2-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="139e2-158">Cambia las características de una rutina inactiva registrada.</span><span class="sxs-lookup"><span data-stu-id="139e2-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="139e2-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="139e2-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="139e2-160">Quita una rutina inactiva registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="139e2-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="139e2-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="139e2-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="139e2-162">Deshabilita o vuelve a habilitar una rutina inactiva registrada sin quitarla del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="139e2-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="139e2-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="139e2-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="139e2-164">Agrega una rutina inactiva al sistema MAPI, con o sin habilitar.</span><span class="sxs-lookup"><span data-stu-id="139e2-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="139e2-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="139e2-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="139e2-166">Cierra el motor de inactividad MAPI de la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="139e2-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="139e2-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="139e2-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="139e2-168">Inicializa el motor de inactividad MAPI para la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="139e2-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="139e2-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como parámetro de entrada la etiqueta de la función devuelta por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="139e2-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="139e2-170">Cuando todas las tareas de primer plano de la plataforma se convierten en inactivas, el motor de inactividad de MAPI llama a la rutina inactiva de máxima prioridad que está lista para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="139e2-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="139e2-171">No hay ninguna garantía del orden de llamadas entre rutinas de inactividad de la misma prioridad.</span><span class="sxs-lookup"><span data-stu-id="139e2-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

