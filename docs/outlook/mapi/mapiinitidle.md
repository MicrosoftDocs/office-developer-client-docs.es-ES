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
# <a name="mapiinitidle"></a><span data-ttu-id="30c55-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="30c55-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="30c55-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30c55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30c55-105">Inicializa el motor de inactividad MAPI para la aplicación que llama.</span><span class="sxs-lookup"><span data-stu-id="30c55-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30c55-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="30c55-106">Header file:</span></span>  <br/> |<span data-ttu-id="30c55-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="30c55-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="30c55-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="30c55-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="30c55-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="30c55-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="30c55-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="30c55-110">Called by:</span></span>  <br/> |<span data-ttu-id="30c55-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="30c55-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="30c55-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30c55-112">Parameters</span></span>

 <span data-ttu-id="30c55-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="30c55-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="30c55-114">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="30c55-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="30c55-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30c55-115">Return value</span></span>

<span data-ttu-id="30c55-116">La **función MAPIInitIdle** devuelve cero si la inicialización se realiza correctamente y 1 de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="30c55-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="30c55-117">Si **se llama a MAPIInitIdle** varias veces, todas las llamadas adicionales se realiza correctamente, pero se omiten excepto para incrementar el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="30c55-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="30c55-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="30c55-118">Remarks</span></span>

<span data-ttu-id="30c55-119">Una aplicación cliente o un proveedor de servicios debe llamar a **MAPIInitIdle** antes de llamar a cualquier otra función del motor inactivo.</span><span class="sxs-lookup"><span data-stu-id="30c55-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="30c55-120">Cada llamada a **MAPIInitIdle** debe coincidir con una llamada posterior a [MAPIDeInitIdle](mapideinitidle.md)o el motor inactivo se deja en ejecución para la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="30c55-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="30c55-121">Las siguientes funciones tratan con el motor de inactividad MAPI y con rutinas inactivas basadas en el prototipo de función [FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="30c55-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="30c55-122">**Función de rutina inactiva**</span><span class="sxs-lookup"><span data-stu-id="30c55-122">**Idle routine function**</span></span>|<span data-ttu-id="30c55-123">**Uso**</span><span class="sxs-lookup"><span data-stu-id="30c55-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30c55-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="30c55-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="30c55-125">Cambia las características de una rutina inactiva registrada.</span><span class="sxs-lookup"><span data-stu-id="30c55-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="30c55-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="30c55-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="30c55-127">Quita una rutina de inactividad registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="30c55-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="30c55-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="30c55-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="30c55-129">Deshabilita o vuelve a habilitar una rutina de inactividad registrada sin quitarla del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="30c55-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="30c55-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="30c55-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="30c55-131">Agrega una rutina inactiva al sistema MAPI, con o sin habilitarla.</span><span class="sxs-lookup"><span data-stu-id="30c55-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="30c55-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="30c55-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="30c55-133">Apaga el motor de inactividad MAPI para la aplicación que llama.</span><span class="sxs-lookup"><span data-stu-id="30c55-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="30c55-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="30c55-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="30c55-135">Inicializa el motor de inactividad MAPI para la aplicación que llama.</span><span class="sxs-lookup"><span data-stu-id="30c55-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="30c55-136">Cuando todas las tareas en primer plano de la plataforma están inactivas, el motor de inactividad MAPI llama a la rutina de inactividad de prioridad más alta que está lista para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="30c55-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="30c55-137">No hay ninguna garantía de orden de llamada entre rutinas inactivas de la misma prioridad.</span><span class="sxs-lookup"><span data-stu-id="30c55-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

