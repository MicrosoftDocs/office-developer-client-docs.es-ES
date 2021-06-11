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
ms.openlocfilehash: 74bba3ea9982838f0d010bbf106c1132df1c2c25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408211"
---
# <a name="mapideinitidle"></a><span data-ttu-id="3fe6c-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="3fe6c-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="3fe6c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fe6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fe6c-105">Apaga el motor de inactividad MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3fe6c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="3fe6c-106">Header file:</span></span>  <br/> |<span data-ttu-id="3fe6c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="3fe6c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3fe6c-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="3fe6c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3fe6c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3fe6c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3fe6c-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="3fe6c-110">Called by:</span></span>  <br/> |<span data-ttu-id="3fe6c-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="3fe6c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="3fe6c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fe6c-112">Parameters</span></span>

<span data-ttu-id="3fe6c-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="3fe6c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fe6c-114">Return value</span></span>

<span data-ttu-id="3fe6c-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3fe6c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3fe6c-116">Remarks</span></span>

<span data-ttu-id="3fe6c-117">Una aplicación cliente o un proveedor de servicios debe llamar a **MAPIDeInitIdle** cuando ya no necesite el motor inactivo, por ejemplo, cuando está a punto de detener el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="3fe6c-118">Cada llamada a [MAPIInitIdle](mapiinitidle.md) debe coincidir con una llamada posterior a **MAPIDeInitIdle** o el motor inactivo se deja en ejecución para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="3fe6c-119">Las siguientes funciones tratan con el motor de inactividad MAPI y con rutinas de inactividad basadas en el prototipo de [función FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="3fe6c-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="3fe6c-120">**Función de rutina de inactividad**</span><span class="sxs-lookup"><span data-stu-id="3fe6c-120">**Idle routine function**</span></span>|<span data-ttu-id="3fe6c-121">**Uso**</span><span class="sxs-lookup"><span data-stu-id="3fe6c-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3fe6c-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3fe6c-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="3fe6c-123">Cambia las características de una rutina de inactividad registrada.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="3fe6c-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3fe6c-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="3fe6c-125">Quita una rutina de inactividad registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="3fe6c-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3fe6c-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="3fe6c-127">Deshabilita o vuelve a habilitar una rutina de inactividad registrada sin quitarla del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="3fe6c-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3fe6c-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="3fe6c-129">Agrega una rutina de inactividad al sistema MAPI, con o sin habilitarlo.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="3fe6c-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="3fe6c-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="3fe6c-131">Apaga el motor de inactividad MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="3fe6c-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="3fe6c-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="3fe6c-133">Inicializa el motor de inactividad MAPI para la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="3fe6c-134">Cuando todas las tareas en primer plano de la plataforma están inactivas, el motor de inactividad MAPI llama a la rutina de inactividad de prioridad más alta que está lista para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="3fe6c-135">No hay ninguna garantía de orden de llamada entre rutinas inactivas de la misma prioridad.</span><span class="sxs-lookup"><span data-stu-id="3fe6c-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

