---
title: ScRelocNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocNotifications
api_type:
- COM
ms.assetid: 22de5d38-7be6-48b3-90a7-bc553dcdb042
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4117558d27d64444cdac62651584fe6cfe8ff061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583970"
---
# <a name="screlocnotifications"></a><span data-ttu-id="cda64-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="cda64-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="cda64-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cda64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cda64-105">Ajusta un puntero dentro de una matriz de notificación de evento especificado.</span><span class="sxs-lookup"><span data-stu-id="cda64-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cda64-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="cda64-106">Header file:</span></span>  <br/> |<span data-ttu-id="cda64-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="cda64-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cda64-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="cda64-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cda64-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cda64-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cda64-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="cda64-110">Called by:</span></span>  <br/> |<span data-ttu-id="cda64-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="cda64-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="cda64-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cda64-112">Parameters</span></span>

 <span data-ttu-id="cda64-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="cda64-113">_cntf_</span></span>
  
> <span data-ttu-id="cda64-114">[entrada] Recuento de las estructuras de [notificación](notification.md) en la matriz indicada por el parámetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="cda64-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="cda64-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="cda64-115">_rgntf_</span></span>
  
> <span data-ttu-id="cda64-116">[entrada] Puntero a la matriz de las estructuras de **notificación** para definir las notificaciones de eventos en el que es un puntero para ajustarse.</span><span class="sxs-lookup"><span data-stu-id="cda64-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="cda64-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="cda64-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="cda64-118">[entrada] Puntero a la dirección base original de la matriz indicada por el parámetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="cda64-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="cda64-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="cda64-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="cda64-120">[entrada] La ubicación a la que **ScRelocNotifications** escribe la nueva dirección de base de la matriz indicada por el parámetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="cda64-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="cda64-121">_placa de circuitos impresos_</span><span class="sxs-lookup"><span data-stu-id="cda64-121">_pcb_</span></span>
  
> <span data-ttu-id="cda64-122">[out] Puntero al tamaño, en bytes, de la matriz indicada por el parámetro _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="cda64-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cda64-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cda64-123">Return value</span></span>

<span data-ttu-id="cda64-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="cda64-124">S_OK</span></span>
  
> <span data-ttu-id="cda64-125">Un puntero se ajusta correctamente.</span><span class="sxs-lookup"><span data-stu-id="cda64-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="cda64-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cda64-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="cda64-127">Se ha producido una notificación no válida.</span><span class="sxs-lookup"><span data-stu-id="cda64-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cda64-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cda64-128">Remarks</span></span>

<span data-ttu-id="cda64-129">El parámetro _pcb_ a la función **ScRelocNotifications** es opcional.</span><span class="sxs-lookup"><span data-stu-id="cda64-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cda64-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="cda64-130">See also</span></span>



[<span data-ttu-id="cda64-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="cda64-131">ScRelocProps</span></span>](screlocprops.md)

