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
# <a name="mapideinitidle"></a><span data-ttu-id="584d1-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="584d1-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="584d1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="584d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="584d1-105">Cierra el motor de inactividad MAPI de la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="584d1-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="584d1-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="584d1-106">Header file:</span></span>  <br/> |<span data-ttu-id="584d1-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="584d1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="584d1-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="584d1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="584d1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="584d1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="584d1-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="584d1-110">Called by:</span></span>  <br/> |<span data-ttu-id="584d1-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="584d1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="584d1-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="584d1-112">Parameters</span></span>

<span data-ttu-id="584d1-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="584d1-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="584d1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="584d1-114">Return value</span></span>

<span data-ttu-id="584d1-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="584d1-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="584d1-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="584d1-116">Remarks</span></span>

<span data-ttu-id="584d1-117">Una aplicación cliente o un proveedor de servicios debe llamar a **MAPIDeInitIdle** cuando ya no necesite el motor inactivo, por ejemplo, cuando esté a punto de detener el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="584d1-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="584d1-118">Cada llamada a [MAPIInitIdle](mapiinitidle.md) debe coincidir con una llamada subsiguiente a **MAPIDeInitIdle**o el motor inactivo se deja en ejecución para la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="584d1-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="584d1-119">Las siguientes funciones tratan con el motor de inactividad de MAPI y con rutinas inactivas basadas en el prototipo de función [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="584d1-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="584d1-120">**Función de rutina inActiva**</span><span class="sxs-lookup"><span data-stu-id="584d1-120">**Idle routine function**</span></span>|<span data-ttu-id="584d1-121">**Usage**</span><span class="sxs-lookup"><span data-stu-id="584d1-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="584d1-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="584d1-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="584d1-123">Cambia las características de una rutina inactiva registrada.</span><span class="sxs-lookup"><span data-stu-id="584d1-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="584d1-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="584d1-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="584d1-125">Quita una rutina inactiva registrada del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="584d1-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="584d1-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="584d1-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="584d1-127">Deshabilita o vuelve a habilitar una rutina inactiva registrada sin quitarla del sistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="584d1-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="584d1-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="584d1-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="584d1-129">Agrega una rutina inactiva al sistema MAPI, con o sin habilitar.</span><span class="sxs-lookup"><span data-stu-id="584d1-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="584d1-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="584d1-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="584d1-131">Cierra el motor de inactividad MAPI de la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="584d1-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="584d1-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="584d1-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="584d1-133">Inicializa el motor de inactividad MAPI para la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="584d1-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="584d1-134">Cuando todas las tareas de primer plano de la plataforma se convierten en inactivas, el motor de inactividad de MAPI llama a la rutina inactiva de máxima prioridad que está lista para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="584d1-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="584d1-135">No hay ninguna garantía del orden de llamadas entre rutinas de inactividad de la misma prioridad.</span><span class="sxs-lookup"><span data-stu-id="584d1-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

