---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 0d3f24c41f2cfbd499d92e050c74da904dd4c377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816893"
---
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="f4593-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f4593-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="f4593-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f4593-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f4593-105">Agrega una rutina de inactividad basado en función [FNIDLE](fnidle.md) al sistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f4593-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4593-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f4593-106">Header file:</span></span>  <br/> |<span data-ttu-id="f4593-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f4593-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f4593-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="f4593-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f4593-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f4593-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f4593-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f4593-110">Called by:</span></span>  <br/> |<span data-ttu-id="f4593-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="f4593-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="f4593-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4593-112">Parameters</span></span>

<span data-ttu-id="f4593-113">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="f4593-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="f4593-114">[entrada] Un puntero a la rutina de inactividad.</span><span class="sxs-lookup"><span data-stu-id="f4593-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="f4593-115">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="f4593-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="f4593-116">[entrada] Un puntero a un bloque de memoria que el motor de inactividad debe pasar como un parámetro a la rutina inactivo cuando lo llama.</span><span class="sxs-lookup"><span data-stu-id="f4593-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="f4593-117">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="f4593-117">_priIdle_</span></span>
  
> <span data-ttu-id="f4593-118">[entrada] La prioridad inicial para la rutina de inactividad.</span><span class="sxs-lookup"><span data-stu-id="f4593-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="f4593-119">Las posibles prioridades para rutinas definido por la implementación son mayor o menor que cero, pero no es cero.</span><span class="sxs-lookup"><span data-stu-id="f4593-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="f4593-120">La prioridad cero está reservada para un evento de usuario como un clic del mouse o un mensaje WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="f4593-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="f4593-121">Las prioridades mayores que cero representan tareas en segundo plano que tienen una mayor prioridad a los eventos de usuario y se envían como parte del bucle de suministro de mensajes de Windows estándar.</span><span class="sxs-lookup"><span data-stu-id="f4593-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="f4593-122">Las prioridades menor que cero representa tareas inactivas que ejecutan sólo durante el tiempo de inactividad de suministro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4593-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="f4593-123">Ejemplos de las prioridades son los siguientes: 1 para el envío de primer plano, 2 para la inserción de caracteres de edición de energía y 3 para la descarga de los mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="f4593-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="f4593-124">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="f4593-124">_csecIdle_</span></span>
  
> <span data-ttu-id="f4593-125">[entrada] El valor de hora inicial, en centésimas de segundo, que se usará en la especificación de parámetros de rutina inactivo.</span><span class="sxs-lookup"><span data-stu-id="f4593-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="f4593-126">El significado del valor inicial de tiempo varía en función de lo que se pasa en el parámetro _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="f4593-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="f4593-127">El significado puede ser una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="f4593-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="f4593-128">El período mínimo de omisión de usuario que debe transcurrir antes de la MAPI motor inactivo llama a la rutina de inactividad por primera vez, si se establece la marca FIROWAIT en _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="f4593-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="f4593-129">Una vez transcurrido este tiempo, el motor de inactividad puede llamar a la rutina de inactividad tantas veces como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f4593-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="f4593-130">El intervalo mínimo entre las llamadas a la rutina de inactividad, si se establece la marca FIROINTERVAL en _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="f4593-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="f4593-131">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="f4593-131">_iroIdle_</span></span>
  
> <span data-ttu-id="f4593-132">[entrada] La máscara de bits de indicadores que se utilizan para establecer las opciones iniciales para la rutina de inactividad.</span><span class="sxs-lookup"><span data-stu-id="f4593-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="f4593-133">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="f4593-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="f4593-134">FIRONOADJUSTMENT</span><span class="sxs-lookup"><span data-stu-id="f4593-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="f4593-135">Utilice este indicador para especificar que no se debe ajustar el temporizador de rutina inactivo para la suspensión o reanudar.</span><span class="sxs-lookup"><span data-stu-id="f4593-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="f4593-136">El comportamiento predeterminado sin esta marca es que el tiempo de espera se excluye al calcular el tiempo transcurrido.</span><span class="sxs-lookup"><span data-stu-id="f4593-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="f4593-137">Si se pasa FIRONOADJUSTMENT el tiempo de inactividad se incluye al calcular el tiempo transcurrido.</span><span class="sxs-lookup"><span data-stu-id="f4593-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="f4593-138">FIRODISABLED</span><span class="sxs-lookup"><span data-stu-id="f4593-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="f4593-139">La rutina de inactividad debe deshabilitarse cuando registrado.</span><span class="sxs-lookup"><span data-stu-id="f4593-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="f4593-140">La acción predeterminada es permitir la rutina inactivo cuando **FtgRegisterIdleRoutine** se registra.</span><span class="sxs-lookup"><span data-stu-id="f4593-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="f4593-141">FIROINTERVAL</span><span class="sxs-lookup"><span data-stu-id="f4593-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="f4593-142">El tiempo especificado por el parámetro _csecIdle_ es el intervalo mínimo entre las llamadas sucesivas a la rutina de inactividad.</span><span class="sxs-lookup"><span data-stu-id="f4593-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="f4593-143">FIROONCEONLY</span><span class="sxs-lookup"><span data-stu-id="f4593-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="f4593-p107">Obsoleto. No usar. </span><span class="sxs-lookup"><span data-stu-id="f4593-p107">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="f4593-146">FIROPERBLOCK</span><span class="sxs-lookup"><span data-stu-id="f4593-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="f4593-p108">Obsoleto. No usar. </span><span class="sxs-lookup"><span data-stu-id="f4593-p108">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="f4593-149">FIROWAIT</span><span class="sxs-lookup"><span data-stu-id="f4593-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="f4593-150">El tiempo especificado por el parámetro _csecIdle_ es el período mínimo de omisión de usuario que debe transcurrir antes de que el motor de inactividad de MAPI llama a la rutina de inactividad por primera vez.</span><span class="sxs-lookup"><span data-stu-id="f4593-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="f4593-151">Una vez transcurrido este tiempo, el motor de inactividad puede llamar a la rutina de inactividad tantas veces como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f4593-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f4593-152">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4593-152">Return value</span></span>

<span data-ttu-id="f4593-153">La función **FtgRegisterIdleRoutine** devuelve una etiqueta de función que identifica la rutina de inactividad que se ha agregado al sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="f4593-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="f4593-154">Si **FtgRegisterIdleRoutine** no se puede registrar la rutina de inactividad de la aplicación de cliente o el proveedor de servicios, por ejemplo debido a problemas de memoria, devuelve NULL.</span><span class="sxs-lookup"><span data-stu-id="f4593-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f4593-155">Notas</span><span class="sxs-lookup"><span data-stu-id="f4593-155">Remarks</span></span>

<span data-ttu-id="f4593-156">Las siguientes funciones de abordar los problemas con el motor de inactividad de MAPI y con las rutinas de inactividad según el prototipo de función [FNIDLE](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="f4593-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="f4593-157">**Función rutina inactivo**</span><span class="sxs-lookup"><span data-stu-id="f4593-157">**Idle routine function**</span></span>|<span data-ttu-id="f4593-158">**Uso**</span><span class="sxs-lookup"><span data-stu-id="f4593-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4593-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f4593-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="f4593-160">Cambia las características de una rutina de inactividad registrada.</span><span class="sxs-lookup"><span data-stu-id="f4593-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="f4593-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f4593-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="f4593-162">Quita una rutina de inactividad registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="f4593-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="f4593-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f4593-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="f4593-164">Deshabilita o habilita volver a una rutina de inactividad registrada sin quitar desde el sistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f4593-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="f4593-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="f4593-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="f4593-166">Agrega una rutina de inactividad en el sistema MAPI, con o sin habilitarla.</span><span class="sxs-lookup"><span data-stu-id="f4593-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="f4593-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="f4593-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="f4593-168">Se cierra el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="f4593-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="f4593-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="f4593-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="f4593-170">Inicializa el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="f4593-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="f4593-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como un parámetro de entrada de la etiqueta de función devuelto por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="f4593-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="f4593-172">Cuando se convierten en todas las tareas de primer plano de la plataforma de inactividad, el motor de inactividad de MAPI llama a la rutina de inactividad de prioridad más alta que esté lista para ejecutar.</span><span class="sxs-lookup"><span data-stu-id="f4593-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="f4593-173">No hay ninguna garantía de orden entre las rutinas de inactividad de la misma prioridad de llamada.</span><span class="sxs-lookup"><span data-stu-id="f4593-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="f4593-174">El siguiente es un ejemplo del uso de la marca FIRONOADJUSTMENT en el parámetro _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="f4593-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="f4593-175">Registrar una rutina de inactividad con un retraso de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="f4593-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="f4593-176">Hibernación/suspensión el equipo después de 1 minuto (4 minutos en el temporizador de la izquierda).</span><span class="sxs-lookup"><span data-stu-id="f4593-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="f4593-177">Reanudar el equipo 10 minutos más adelante.</span><span class="sxs-lookup"><span data-stu-id="f4593-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="f4593-178">El comportamiento predeterminado, sin FIRONOADJUSTMENT, es que aún tendrá que esperar más de 4 minutos para ejecutar la rutina.</span><span class="sxs-lookup"><span data-stu-id="f4593-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="f4593-179">Es decir, el temporizador se ha ajustado para permitir el ¿durante cuánto tiempo el equipo estaba en suspensión.</span><span class="sxs-lookup"><span data-stu-id="f4593-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="f4593-180">Sin embargo, si se pasa FIRONOADJUSTMENT la rutina de inactividad se ejecutará en inmediatamente debido a que han transcurrido más de 5 minutos de tiempo real.</span><span class="sxs-lookup"><span data-stu-id="f4593-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

