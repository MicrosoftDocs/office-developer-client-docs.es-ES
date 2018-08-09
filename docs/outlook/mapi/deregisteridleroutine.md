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
ms.openlocfilehash: 85161fb87e798bbb03b267f9760870da1246e48d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816663"
---
# <a name="deregisteridleroutine"></a><span data-ttu-id="336ac-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="336ac-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="336ac-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="336ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="336ac-105">Quita un [FNIDLE](fnidle.md) basa rutina inactivo desde el sistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="336ac-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="336ac-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="336ac-106">Header file:</span></span>  <br/> |<span data-ttu-id="336ac-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="336ac-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="336ac-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="336ac-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="336ac-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="336ac-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="336ac-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="336ac-110">Called by:</span></span>  <br/> |<span data-ttu-id="336ac-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="336ac-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="336ac-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="336ac-112">Parameters</span></span>

 <span data-ttu-id="336ac-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="336ac-113">_ftg_</span></span>
  
> <span data-ttu-id="336ac-114">[entrada] Etiqueta de función que identifica la rutina inactivo que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="336ac-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="336ac-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="336ac-115">Return value</span></span>

<span data-ttu-id="336ac-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="336ac-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="336ac-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="336ac-117">Remarks</span></span>

<span data-ttu-id="336ac-118">Cualquier tarea en una aplicación de cliente o un proveedor de servicios puede anular el registro de cualquier rutina de inactividad para el que tiene un parámetro válido _ftg_ .</span><span class="sxs-lookup"><span data-stu-id="336ac-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="336ac-119">En concreto, una rutina de inactividad puede anular el registro de sí mismo.</span><span class="sxs-lookup"><span data-stu-id="336ac-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="336ac-120">Las siguientes funciones de abordar los problemas con el motor de inactividad de MAPI y con las rutinas de inactividad según el prototipo de función [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="336ac-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="336ac-121">**Función rutina inactivo**</span><span class="sxs-lookup"><span data-stu-id="336ac-121">**Idle routine function**</span></span>|<span data-ttu-id="336ac-122">**Uso**</span><span class="sxs-lookup"><span data-stu-id="336ac-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="336ac-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="336ac-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="336ac-124">Cambia las características de una rutina de inactividad registrada.</span><span class="sxs-lookup"><span data-stu-id="336ac-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="336ac-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="336ac-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="336ac-126">Quita una rutina de inactividad registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="336ac-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="336ac-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="336ac-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="336ac-128">Deshabilita o habilita volver a una rutina de inactividad registrada sin quitar desde el sistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="336ac-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="336ac-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="336ac-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="336ac-130">Agrega una rutina de inactividad en el sistema MAPI, con o sin habilitarla.</span><span class="sxs-lookup"><span data-stu-id="336ac-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="336ac-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="336ac-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="336ac-132">Se cierra el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="336ac-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="336ac-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="336ac-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="336ac-134">Inicializa el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="336ac-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="336ac-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como un parámetro de entrada de la etiqueta de función devuelto por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="336ac-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="336ac-136">Cuando se convierten en todas las tareas de primer plano de la plataforma de inactividad, el motor de inactividad de MAPI llama a la rutina de inactividad de prioridad más alta que esté lista para ejecutar.</span><span class="sxs-lookup"><span data-stu-id="336ac-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="336ac-137">No hay ninguna garantía de orden entre las rutinas de inactividad de la misma prioridad de llamada.</span><span class="sxs-lookup"><span data-stu-id="336ac-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="336ac-138">Después de la rutina de inactividad se elimina del registro, el motor de inactividad no llame nuevamente.</span><span class="sxs-lookup"><span data-stu-id="336ac-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="336ac-139">Cualquier implementación que llama a **DeregisterIdleRoutine** debe desasignar los bloques de memoria a la que se pasan punteros para el motor de inactivo a usar en su llamada original a la función **FtgRegisterIdleRoutine** .</span><span class="sxs-lookup"><span data-stu-id="336ac-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

