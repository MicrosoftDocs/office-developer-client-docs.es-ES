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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 1fbeccd805953322b579d1490b5e74e5132aa7ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816563"
---
# <a name="changeidleroutine"></a><span data-ttu-id="dbb5d-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="dbb5d-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="dbb5d-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dbb5d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dbb5d-105">Cambia algunas o todas las características de una rutina de inactividad [FNIDLE](fnidle.md) en función de.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbb5d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="dbb5d-106">Header file:</span></span>  <br/> |<span data-ttu-id="dbb5d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="dbb5d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dbb5d-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="dbb5d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dbb5d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dbb5d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dbb5d-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="dbb5d-110">Called by:</span></span>  <br/> |<span data-ttu-id="dbb5d-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="dbb5d-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="dbb5d-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbb5d-112">Parameters</span></span>

<span data-ttu-id="dbb5d-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="dbb5d-113">_ftg_</span></span>
  
> <span data-ttu-id="dbb5d-114">[entrada] Etiqueta de función que identifica la rutina inactivo.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="dbb5d-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="dbb5d-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="dbb5d-116">[entrada] Puntero a la rutina de inactividad.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="dbb5d-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="dbb5d-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="dbb5d-118">[entrada] Puntero a un nuevo bloque de memoria que la implementación de la llamada se asigna para la rutina de inactividad.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="dbb5d-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="dbb5d-119">_priIdle_</span></span>
  
> <span data-ttu-id="dbb5d-120">[entrada] Valor que representa una nueva prioridad para la rutina de inactividad.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="dbb5d-121">Las posibles prioridades para rutinas definido por la implementación son mayor o menor que cero, pero no es cero.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="dbb5d-122">Un valor de cero está reservado para un evento de usuario como un clic del mouse o un mensaje WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="dbb5d-123">Los valores mayores que cero representan las prioridades para tareas en segundo plano que tienen una mayor prioridad a los eventos de usuario y se envían como parte del bucle de suministro de mensajes de Windows estándar.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="dbb5d-124">Los valores inferiores a cero representan las prioridades para tareas inactivas que ejecutan sólo durante el tiempo de inactividad de suministro de mensajes.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="dbb5d-125">Ejemplos de las prioridades son: 1 para el envío de primer plano, 1 para la inserción de caracteres de edición de energía y 3 para la descarga de los mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="dbb5d-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="dbb5d-126">_csecIdle_</span></span>
  
> <span data-ttu-id="dbb5d-127">[entrada] Una nueva hora, en centésimas de segundo, que se debe aplicar a la rutina de inactividad.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="dbb5d-128">El significado del valor inicial de tiempo varía en función de lo que se pasa en el parámetro _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="dbb5d-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="dbb5d-129">Puede ser:</span><span class="sxs-lookup"><span data-stu-id="dbb5d-129">It can be:</span></span> 
    
  - <span data-ttu-id="dbb5d-130">El período mínimo de omisión de usuario que debe transcurrir antes de la MAPI motor inactivo llama a la rutina de inactividad por primera vez, si se establece la marca FIROWAIT en _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="dbb5d-131">Una vez transcurrido este tiempo, el motor de inactividad puede llamar a la rutina de inactividad tantas veces como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="dbb5d-132">El intervalo mínimo entre las llamadas a la rutina de inactividad, si se establece la marca FIROINTERVAL en _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="dbb5d-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="dbb5d-133">_iroIdle_</span></span>
  
> <span data-ttu-id="dbb5d-134">[entrada] Máscara de bits de marcadores que indica nuevas opciones para llamar a la rutina de inactividad.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="dbb5d-135">Debe establecerse exactamente uno de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="dbb5d-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="dbb5d-136">FIROINTERVAL: El tiempo especificado por el parámetro _csecIdle_ es el intervalo mínimo entre las llamadas sucesivas a la rutina de inactividad.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="dbb5d-137">FIROONCEONLY: obsoleto.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="dbb5d-138">No la use.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-138">Do not use.</span></span> 
      
  - <span data-ttu-id="dbb5d-139">FIROPERBLOCK: obsoleto.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="dbb5d-140">No la use.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-140">Do not use.</span></span> 
      
  - <span data-ttu-id="dbb5d-141">FIROWAIT: El tiempo especificado por el parámetro _csecIdle_ es el período mínimo de omisión de usuario que debe transcurrir antes de que el motor de inactividad de MAPI llama a la rutina de inactividad por primera vez.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="dbb5d-142">Una vez transcurrido este tiempo, el motor de inactividad puede llamar a la rutina de inactividad tantas veces como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="dbb5d-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="dbb5d-143">_ircIdle_</span></span>
  
> <span data-ttu-id="dbb5d-144">[entrada] Máscara de bits de indicadores que se utilizan para indicar los cambios que hacer en la rutina de inactividad.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="dbb5d-145">Las siguientes marcas se pueden establecer en cualquier combinación:</span><span class="sxs-lookup"><span data-stu-id="dbb5d-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="dbb5d-146">FIRCCSEC: Un cambio en el tiempo asociado con la rutina de inactividad, es decir, un cambio indicada por el valor que se pasa en el parámetro _csecIdle_ .</span><span class="sxs-lookup"><span data-stu-id="dbb5d-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="dbb5d-147">FIRCIRO: Un cambio en las opciones para la rutina inactivo, es decir, un cambio indicado por el valor que se pasa en el parámetro _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="dbb5d-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="dbb5d-148">FIRCPFN: Un cambio en el puntero de rutina inactivo, es decir, un cambio indicado por el valor que se pasa en el parámetro _pfnIdle_ .</span><span class="sxs-lookup"><span data-stu-id="dbb5d-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="dbb5d-149">FIRCPRI: Un cambio en la prioridad de la rutina inactivo, es decir, un cambio indicado por el valor que se pasa en el parámetro _priIdle_ .</span><span class="sxs-lookup"><span data-stu-id="dbb5d-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="dbb5d-150">FIRCPV: Un cambio en el bloque de memoria de la rutina inactivo, es decir, un cambio indicado por el valor que se pasa en el parámetro _pvIdleParam_ .</span><span class="sxs-lookup"><span data-stu-id="dbb5d-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dbb5d-151">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dbb5d-151">Return value</span></span>

<span data-ttu-id="dbb5d-152">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dbb5d-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dbb5d-153">Remarks</span></span>

<span data-ttu-id="dbb5d-154">Las siguientes funciones de abordar los problemas con el motor de inactividad de MAPI y con las rutinas de inactividad según el prototipo de función [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="dbb5d-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="dbb5d-155">**Función rutina inactivo**</span><span class="sxs-lookup"><span data-stu-id="dbb5d-155">**Idle routine function**</span></span>|<span data-ttu-id="dbb5d-156">**Uso**</span><span class="sxs-lookup"><span data-stu-id="dbb5d-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dbb5d-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="dbb5d-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="dbb5d-158">Cambia las características de una rutina de inactividad registrada.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="dbb5d-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="dbb5d-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="dbb5d-160">Quita una rutina de inactividad registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="dbb5d-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="dbb5d-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="dbb5d-162">Deshabilita o habilita volver a una rutina de inactividad registrada sin quitar desde el sistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="dbb5d-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="dbb5d-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="dbb5d-164">Agrega una rutina de inactividad en el sistema MAPI, con o sin habilitarla.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="dbb5d-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="dbb5d-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="dbb5d-166">Se cierra el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="dbb5d-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="dbb5d-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="dbb5d-168">Inicializa el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="dbb5d-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como un parámetro de entrada de la etiqueta de función devuelto por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="dbb5d-170">Cuando se convierten en todas las tareas de primer plano de la plataforma de inactividad, el motor de inactividad de MAPI llama a la rutina de inactividad de prioridad más alta que esté lista para ejecutar.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="dbb5d-171">No hay ninguna garantía de orden entre las rutinas de inactividad de la misma prioridad de llamada.</span><span class="sxs-lookup"><span data-stu-id="dbb5d-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

