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
ms.openlocfilehash: b07c40882c0b9974c71eeb03123e7025b948a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432446"
---
# <a name="mapiinitidle"></a><span data-ttu-id="565e0-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="565e0-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="565e0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="565e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="565e0-105">Inicializa el motor de inactividad MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="565e0-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="565e0-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="565e0-106">Header file:</span></span>  <br/> |<span data-ttu-id="565e0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="565e0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="565e0-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="565e0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="565e0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="565e0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="565e0-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="565e0-110">Called by:</span></span>  <br/> |<span data-ttu-id="565e0-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="565e0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="565e0-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="565e0-112">Parameters</span></span>

 <span data-ttu-id="565e0-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="565e0-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="565e0-114">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="565e0-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="565e0-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="565e0-115">Return value</span></span>

<span data-ttu-id="565e0-116">La **función MAPIInitIdle** devuelve cero si la inicialización se realiza correctamente y 1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="565e0-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="565e0-117">Si **se llama a MAPIInitIdle** varias veces, todas las llamadas adicionales se realiza correctamente, pero se omiten excepto para incrementar el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="565e0-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="565e0-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="565e0-118">Remarks</span></span>

<span data-ttu-id="565e0-119">Una aplicación cliente o proveedor de servicios debe llamar **a MAPIInitIdle** antes de llamar a cualquier otra función del motor inactivo.</span><span class="sxs-lookup"><span data-stu-id="565e0-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="565e0-120">Cada llamada a **MAPIInitIdle** debe coincidir con una llamada posterior a [MAPIDeInitIdle](mapideinitidle.md)o el motor inactivo se deja en ejecución para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="565e0-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="565e0-121">Las siguientes funciones tratan con el motor de inactividad MAPI y con rutinas de inactividad basadas en el prototipo de [función FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="565e0-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="565e0-122">**Función de rutina de inactividad**</span><span class="sxs-lookup"><span data-stu-id="565e0-122">**Idle routine function**</span></span>|<span data-ttu-id="565e0-123">**Uso**</span><span class="sxs-lookup"><span data-stu-id="565e0-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="565e0-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="565e0-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="565e0-125">Cambia las características de una rutina de inactividad registrada.</span><span class="sxs-lookup"><span data-stu-id="565e0-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="565e0-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="565e0-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="565e0-127">Quita una rutina de inactividad registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="565e0-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="565e0-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="565e0-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="565e0-129">Deshabilita o vuelve a habilitar una rutina de inactividad registrada sin quitarla del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="565e0-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="565e0-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="565e0-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="565e0-131">Agrega una rutina de inactividad al sistema MAPI, con o sin habilitarlo.</span><span class="sxs-lookup"><span data-stu-id="565e0-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="565e0-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="565e0-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="565e0-133">Apaga el motor de inactividad MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="565e0-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="565e0-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="565e0-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="565e0-135">Inicializa el motor de inactividad MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="565e0-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="565e0-136">Cuando todas las tareas en primer plano de la plataforma están inactivas, el motor de inactividad MAPI llama a la rutina de inactividad de prioridad más alta que está lista para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="565e0-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="565e0-137">No hay ninguna garantía de orden de llamada entre rutinas inactivas de la misma prioridad.</span><span class="sxs-lookup"><span data-stu-id="565e0-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

