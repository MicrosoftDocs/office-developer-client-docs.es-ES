---
title: MAPIDeInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIDeInitIdle
api_type:
- COM
ms.assetid: f7b04486-bc48-4ba4-9f35-f021e06124bf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4eaeb3338c95196ff346c5098e5d06371b00bc5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818245"
---
# <a name="mapideinitidle"></a><span data-ttu-id="0ba20-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="0ba20-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="0ba20-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0ba20-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0ba20-105">Se cierra el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="0ba20-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ba20-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0ba20-106">Header file:</span></span>  <br/> |<span data-ttu-id="0ba20-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0ba20-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0ba20-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="0ba20-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0ba20-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0ba20-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0ba20-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="0ba20-110">Called by:</span></span>  <br/> |<span data-ttu-id="0ba20-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="0ba20-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="0ba20-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ba20-112">Parameters</span></span>

<span data-ttu-id="0ba20-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0ba20-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="0ba20-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ba20-114">Return value</span></span>

<span data-ttu-id="0ba20-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0ba20-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ba20-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0ba20-116">Remarks</span></span>

<span data-ttu-id="0ba20-117">Una aplicación de cliente o un proveedor de servicios debe llamar a **MAPIDeInitIdle** cuando ya no necesita el motor de inactividad, por ejemplo, cuando está a punto de detener el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="0ba20-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="0ba20-118">Todas las llamadas a [MAPIInitIdle](mapiinitidle.md) deben coincidir por una llamada a **MAPIDeInitIdle**posterior o el motor de inactividad quedo en ejecución para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="0ba20-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="0ba20-119">Las siguientes funciones de abordar los problemas con el motor de inactividad de MAPI y con las rutinas de inactividad según el prototipo de función [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="0ba20-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="0ba20-120">**Función rutina inactivo**</span><span class="sxs-lookup"><span data-stu-id="0ba20-120">**Idle routine function**</span></span>|<span data-ttu-id="0ba20-121">**Uso**</span><span class="sxs-lookup"><span data-stu-id="0ba20-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ba20-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0ba20-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="0ba20-123">Cambia las características de una rutina de inactividad registrada.</span><span class="sxs-lookup"><span data-stu-id="0ba20-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="0ba20-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0ba20-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="0ba20-125">Quita una rutina de inactividad registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="0ba20-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="0ba20-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0ba20-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="0ba20-127">Deshabilita o habilita volver a una rutina de inactividad registrada sin quitar desde el sistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0ba20-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="0ba20-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0ba20-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="0ba20-129">Agrega una rutina de inactividad en el sistema MAPI, con o sin habilitarla.</span><span class="sxs-lookup"><span data-stu-id="0ba20-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="0ba20-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="0ba20-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="0ba20-131">Se cierra el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="0ba20-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="0ba20-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="0ba20-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="0ba20-133">Inicializa el motor de inactividad de MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="0ba20-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="0ba20-134">Cuando se convierten en todas las tareas de primer plano de la plataforma de inactividad, el motor de inactividad de MAPI llama a la rutina de inactividad de prioridad más alta que esté lista para ejecutar.</span><span class="sxs-lookup"><span data-stu-id="0ba20-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="0ba20-135">No hay ninguna garantía de orden entre las rutinas de inactividad de la misma prioridad de llamada.</span><span class="sxs-lookup"><span data-stu-id="0ba20-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

