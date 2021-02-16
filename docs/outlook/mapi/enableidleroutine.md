---
title: EnableIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EnableIdleRoutine
api_type:
- COM
ms.assetid: 332ea831-bdf9-4dbd-b9c7-a80f8ba11b3b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e04c872762665f4b3a22559dc2ed1504e7b8f9af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410224"
---
# <a name="enableidleroutine"></a><span data-ttu-id="dab61-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="dab61-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="dab61-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dab61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dab61-105">Habilita o deshabilita una rutina inactiva basada en [FNIDLE.](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="dab61-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dab61-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="dab61-106">Header file:</span></span>  <br/> |<span data-ttu-id="dab61-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="dab61-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dab61-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="dab61-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dab61-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dab61-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dab61-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="dab61-110">Called by:</span></span>  <br/> |<span data-ttu-id="dab61-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="dab61-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="dab61-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dab61-112">Parameters</span></span>

 <span data-ttu-id="dab61-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="dab61-113">_ftg_</span></span>
  
> <span data-ttu-id="dab61-114">[entrada] Etiqueta de función que identifica la rutina inactiva que se va a habilitar o deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="dab61-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="dab61-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="dab61-115">_fEnable_</span></span>
  
> <span data-ttu-id="dab61-116">[entrada] Contiene TRUE si el motor inactivo debe habilitar la rutina de inactividad, o FALSE si debe deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="dab61-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dab61-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dab61-117">Return value</span></span>

<span data-ttu-id="dab61-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dab61-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dab61-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dab61-119">Remarks</span></span>

<span data-ttu-id="dab61-120">Las siguientes funciones tratan con el motor de inactividad MAPI y con rutinas inactivas basadas en el prototipo de función [FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="dab61-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="dab61-121">**Función de rutina inactiva**</span><span class="sxs-lookup"><span data-stu-id="dab61-121">**Idle routine function**</span></span>|<span data-ttu-id="dab61-122">**Uso**</span><span class="sxs-lookup"><span data-stu-id="dab61-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dab61-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="dab61-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="dab61-124">Cambia las características de una rutina de inactividad registrada.</span><span class="sxs-lookup"><span data-stu-id="dab61-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="dab61-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="dab61-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="dab61-126">Quita una rutina de inactividad registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="dab61-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="dab61-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="dab61-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="dab61-128">Deshabilita o vuelve a habilitar una rutina de inactividad registrada sin quitarla del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="dab61-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="dab61-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="dab61-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="dab61-130">Agrega una rutina inactiva al sistema MAPI, con o sin habilitarla.</span><span class="sxs-lookup"><span data-stu-id="dab61-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="dab61-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="dab61-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="dab61-132">Apaga el motor de inactividad MAPI para la aplicación que llama.</span><span class="sxs-lookup"><span data-stu-id="dab61-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="dab61-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="dab61-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="dab61-134">Inicializa el motor de inactividad MAPI para la aplicación que llama.</span><span class="sxs-lookup"><span data-stu-id="dab61-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="dab61-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine** y **EnableIdleRoutine** toman como parámetro de entrada la etiqueta de función devuelta por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="dab61-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="dab61-136">Cuando todas las tareas en primer plano de la plataforma están inactivas, el motor de inactividad MAPI llama a la rutina de inactividad de prioridad más alta que está lista para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="dab61-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="dab61-137">No hay ninguna garantía de orden de llamada entre rutinas inactivas de la misma prioridad.</span><span class="sxs-lookup"><span data-stu-id="dab61-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

