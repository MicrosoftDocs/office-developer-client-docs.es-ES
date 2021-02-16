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
# <a name="changeidleroutine"></a><span data-ttu-id="7d9f0-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="7d9f0-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="7d9f0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d9f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d9f0-105">Cambia algunas o todas las características de una rutina inactiva basada en [FNIDLE.](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="7d9f0-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d9f0-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7d9f0-106">Header file:</span></span>  <br/> |<span data-ttu-id="7d9f0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7d9f0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7d9f0-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="7d9f0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7d9f0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7d9f0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7d9f0-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="7d9f0-110">Called by:</span></span>  <br/> |<span data-ttu-id="7d9f0-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="7d9f0-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="7d9f0-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d9f0-112">Parameters</span></span>

<span data-ttu-id="7d9f0-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="7d9f0-113">_ftg_</span></span>
  
> <span data-ttu-id="7d9f0-114">[entrada] Etiqueta de función que identifica la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="7d9f0-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="7d9f0-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="7d9f0-116">[entrada] Puntero a la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="7d9f0-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="7d9f0-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="7d9f0-118">[entrada] Puntero a un nuevo bloque de memoria que la implementación de llamada asigna para la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="7d9f0-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="7d9f0-119">_priIdle_</span></span>
  
> <span data-ttu-id="7d9f0-120">[entrada] Valor que representa una nueva prioridad para la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="7d9f0-121">Las posibles prioridades de las rutinas definidas por la implementación son mayores o inferiores a cero, pero no cero.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="7d9f0-122">Se reserva un valor de cero para un evento de usuario, como un clic del mouse o un WM_PAINT mensaje.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="7d9f0-123">Los valores mayores que cero representan prioridades para las tareas en segundo plano que tienen una prioridad más alta que los eventos de usuario y se distribuyen como parte del bucle estándar de bucle de mensajes de Windows.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="7d9f0-124">Los valores inferiores a cero representan prioridades para las tareas inactivas que solo se ejecutan durante el tiempo de inactividad de la inactividad de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="7d9f0-125">Algunos ejemplos de prioridades son: 1 para el envío en primer plano, 1 para la inserción de caracteres de edición de energía y 3 para descargar nuevos mensajes.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="7d9f0-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="7d9f0-126">_csecIdle_</span></span>
  
> <span data-ttu-id="7d9f0-127">[entrada] Una nueva hora, en centésimas de segundo, que se aplica a la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="7d9f0-128">El significado del valor de hora inicial varía en función de lo que se pasa en el _parámetro iroIdle._</span><span class="sxs-lookup"><span data-stu-id="7d9f0-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="7d9f0-129">Puede ser:</span><span class="sxs-lookup"><span data-stu-id="7d9f0-129">It can be:</span></span> 
    
  - <span data-ttu-id="7d9f0-130">El período mínimo de inacción del usuario que debe transcurrir antes de que el motor de inactividad MAPI llame a la rutina inactiva por primera vez, si la marca FIROWAIT se establece en  _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="7d9f0-131">Una vez transcurrido este tiempo, el motor inactivo puede llamar a la rutina de inactividad tantas veces como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="7d9f0-132">El intervalo mínimo entre llamadas a la rutina inactiva, si la marca FIROINTERVAL está establecida en  _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="7d9f0-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="7d9f0-133">_iroIdle_</span></span>
  
> <span data-ttu-id="7d9f0-134">[entrada] Máscara de bits de marcas que indica nuevas opciones para llamar a la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="7d9f0-135">Se debe establecer exactamente una de las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="7d9f0-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="7d9f0-136">FIROINTERVAL: el tiempo especificado por el parámetro  _csecIdle_ es el intervalo mínimo entre llamadas sucesivas a la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="7d9f0-137">FIROONCEONLY: obsoleto.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="7d9f0-138">No usar.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-138">Do not use.</span></span> 
      
  - <span data-ttu-id="7d9f0-139">FIROPERBLOCK: obsoleto.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="7d9f0-140">No usar.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-140">Do not use.</span></span> 
      
  - <span data-ttu-id="7d9f0-141">FIROWAIT: el tiempo especificado por el parámetro  _csecIdle_ es el período mínimo de inacción del usuario que debe transcurrir antes de que el motor de inactividad MAPI llame a la rutina inactiva por primera vez.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="7d9f0-142">Una vez transcurrido este tiempo, el motor inactivo puede llamar a la rutina de inactividad tantas veces como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="7d9f0-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="7d9f0-143">_ircIdle_</span></span>
  
> <span data-ttu-id="7d9f0-144">[entrada] Máscara de bits de marcas usadas para indicar los cambios que se realizarán en la rutina inactiva.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="7d9f0-145">Las siguientes marcas se pueden establecer en cualquier combinación:</span><span class="sxs-lookup"><span data-stu-id="7d9f0-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="7d9f0-146">FIRCCSEC: un cambio en el tiempo asociado a la rutina inactiva, es decir, un cambio indicado por el valor pasado en el _parámetro csecIdle._</span><span class="sxs-lookup"><span data-stu-id="7d9f0-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="7d9f0-147">FIRCIRO: un cambio en las opciones de la rutina inactiva, es decir, un cambio indicado por el valor pasado en el parámetro _iroIdle._</span><span class="sxs-lookup"><span data-stu-id="7d9f0-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="7d9f0-148">FIRCPFN: un cambio en el puntero de rutina inactiva, es decir, un cambio indicado por el valor pasado en el parámetro _pfnIdle._</span><span class="sxs-lookup"><span data-stu-id="7d9f0-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="7d9f0-149">FIRCPRI: un cambio en la prioridad de la rutina inactiva, es decir, un cambio indicado por el valor pasado en el _parámetro priIdle._</span><span class="sxs-lookup"><span data-stu-id="7d9f0-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="7d9f0-150">FIRCPV: un cambio en el bloque de memoria de la rutina inactiva, es decir, un cambio indicado por el valor pasado en el parámetro _pvIdleParam._</span><span class="sxs-lookup"><span data-stu-id="7d9f0-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7d9f0-151">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d9f0-151">Return value</span></span>

<span data-ttu-id="7d9f0-152">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7d9f0-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7d9f0-153">Remarks</span></span>

<span data-ttu-id="7d9f0-154">Las siguientes funciones tratan con el motor de inactividad MAPI y con rutinas inactivas basadas en el prototipo de función [FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="7d9f0-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="7d9f0-155">**Función de rutina inactiva**</span><span class="sxs-lookup"><span data-stu-id="7d9f0-155">**Idle routine function**</span></span>|<span data-ttu-id="7d9f0-156">**Uso**</span><span class="sxs-lookup"><span data-stu-id="7d9f0-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7d9f0-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="7d9f0-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="7d9f0-158">Cambia las características de una rutina inactiva registrada.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="7d9f0-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="7d9f0-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="7d9f0-160">Quita una rutina de inactividad registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="7d9f0-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="7d9f0-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="7d9f0-162">Deshabilita o vuelve a habilitar una rutina de inactividad registrada sin quitarla del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="7d9f0-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="7d9f0-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="7d9f0-164">Agrega una rutina inactiva al sistema MAPI, con o sin habilitarla.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="7d9f0-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="7d9f0-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="7d9f0-166">Apaga el motor de inactividad MAPI para la aplicación que llama.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="7d9f0-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="7d9f0-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="7d9f0-168">Inicializa el motor de inactividad MAPI para la aplicación que llama.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="7d9f0-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine** y **EnableIdleRoutine** toman como parámetro de entrada la etiqueta de función devuelta por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="7d9f0-170">Cuando todas las tareas en primer plano de la plataforma están inactivas, el motor de inactividad MAPI llama a la rutina de inactividad de prioridad más alta que está lista para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="7d9f0-171">No hay ninguna garantía de orden de llamada entre rutinas inactivas de la misma prioridad.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

