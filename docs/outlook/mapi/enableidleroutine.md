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
ms.openlocfilehash: c53bd63e60281e999d0d379913b3609e9472a40e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579280"
---
# <a name="enableidleroutine"></a><span data-ttu-id="589d6-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="589d6-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="589d6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="589d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="589d6-105">Habilita o deshabilita una rutina de inactividad en función de [FNIDLE](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="589d6-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="589d6-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="589d6-106">Header file:</span></span>  <br/> |<span data-ttu-id="589d6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="589d6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="589d6-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="589d6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="589d6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="589d6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="589d6-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="589d6-110">Called by:</span></span>  <br/> |<span data-ttu-id="589d6-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="589d6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="589d6-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="589d6-112">Parameters</span></span>

 <span data-ttu-id="589d6-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="589d6-113">_ftg_</span></span>
  
> <span data-ttu-id="589d6-114">[entrada] Etiqueta de función que identifica la rutina inactivo para que estén habilitadas o deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="589d6-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="589d6-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="589d6-115">_fEnable_</span></span>
  
> <span data-ttu-id="589d6-116">[entrada] Contiene TRUE si el motor de inactividad debe habilitar la rutina de inactividad o FALSE si debe deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="589d6-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="589d6-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="589d6-117">Return value</span></span>

<span data-ttu-id="589d6-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="589d6-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="589d6-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="589d6-119">Remarks</span></span>

<span data-ttu-id="589d6-120">Las siguientes funciones de abordar los problemas con el motor de inactividad de MAPI y con las rutinas de inactividad según el prototipo de función [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="589d6-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="589d6-121">**Función rutina inactivo**</span><span class="sxs-lookup"><span data-stu-id="589d6-121">**Idle routine function**</span></span>|<span data-ttu-id="589d6-122">**Uso**</span><span class="sxs-lookup"><span data-stu-id="589d6-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="589d6-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="589d6-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="589d6-124">Cambia las características de una rutina de inactividad registrada.</span><span class="sxs-lookup"><span data-stu-id="589d6-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="589d6-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="589d6-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="589d6-126">Quita una rutina de inactividad registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="589d6-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="589d6-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="589d6-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="589d6-128">Deshabilita o habilita volver a una rutina de inactividad registrada sin quitar desde el sistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="589d6-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="589d6-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="589d6-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="589d6-130">Agrega una rutina de inactividad en el sistema MAPI, con o sin habilitarla.</span><span class="sxs-lookup"><span data-stu-id="589d6-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="589d6-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="589d6-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="589d6-132">Se cierra el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="589d6-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="589d6-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="589d6-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="589d6-134">Inicializa el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="589d6-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="589d6-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como un parámetro de entrada de la etiqueta de función devuelto por **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="589d6-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="589d6-136">Cuando se convierten en todas las tareas de primer plano de la plataforma de inactividad, el motor de inactividad de MAPI llama a la rutina de inactividad de prioridad más alta que esté lista para ejecutar.</span><span class="sxs-lookup"><span data-stu-id="589d6-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="589d6-137">No hay ninguna garantía de orden entre las rutinas de inactividad de la misma prioridad de llamada.</span><span class="sxs-lookup"><span data-stu-id="589d6-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

