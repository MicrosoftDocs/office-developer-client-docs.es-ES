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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339399"
---
# <a name="enableidleroutine"></a><span data-ttu-id="f26fd-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f26fd-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="f26fd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f26fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f26fd-105">Habilita o deshabilita una rutina de inactividad basada en [FNIDLE](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="f26fd-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f26fd-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f26fd-106">Header file:</span></span>  <br/> |<span data-ttu-id="f26fd-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="f26fd-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f26fd-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f26fd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f26fd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f26fd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f26fd-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f26fd-110">Called by:</span></span>  <br/> |<span data-ttu-id="f26fd-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="f26fd-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="f26fd-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="f26fd-112">Parameters</span></span>

 <span data-ttu-id="f26fd-113">_FTG_</span><span class="sxs-lookup"><span data-stu-id="f26fd-113">_ftg_</span></span>
  
> <span data-ttu-id="f26fd-114">a Etiqueta de función que identifica la rutina inactiva que se va a habilitar o deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="f26fd-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="f26fd-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="f26fd-115">_fEnable_</span></span>
  
> <span data-ttu-id="f26fd-116">a Contiene TRUE si el motor inactivo debe habilitar la rutina inactiva o FALSE si debe deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="f26fd-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f26fd-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f26fd-117">Return value</span></span>

<span data-ttu-id="f26fd-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f26fd-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f26fd-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f26fd-119">Remarks</span></span>

<span data-ttu-id="f26fd-120">Las siguientes funciones tratan con el motor de inactividad de MAPI y con rutinas inactivas basadas en el prototipo de función [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="f26fd-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="f26fd-121">**Función de rutina inActiva**</span><span class="sxs-lookup"><span data-stu-id="f26fd-121">**Idle routine function**</span></span>|<span data-ttu-id="f26fd-122">**Usage**</span><span class="sxs-lookup"><span data-stu-id="f26fd-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f26fd-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f26fd-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="f26fd-124">Cambia las características de una rutina inactiva registrada.</span><span class="sxs-lookup"><span data-stu-id="f26fd-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="f26fd-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f26fd-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="f26fd-126">Quita una rutina inactiva registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="f26fd-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="f26fd-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="f26fd-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="f26fd-128">Deshabilita o vuelve a habilitar una rutina inactiva registrada sin quitarla del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="f26fd-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="f26fd-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f26fd-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="f26fd-130">Agrega una rutina inactiva al sistema MAPI, con o sin habilitar.</span><span class="sxs-lookup"><span data-stu-id="f26fd-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="f26fd-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="f26fd-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="f26fd-132">Cierra el motor de inactividad MAPI de la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="f26fd-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="f26fd-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="f26fd-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="f26fd-134">Inicializa el motor de inactividad MAPI para la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="f26fd-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="f26fd-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como parámetro de entrada la etiqueta de la función devuelta por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="f26fd-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="f26fd-136">Cuando todas las tareas de primer plano de la plataforma se convierten en inactivas, el motor de inactividad de MAPI llama a la rutina inactiva de máxima prioridad que está lista para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="f26fd-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="f26fd-137">No hay ninguna garantía del orden de llamadas entre rutinas de inactividad de la misma prioridad.</span><span class="sxs-lookup"><span data-stu-id="f26fd-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

