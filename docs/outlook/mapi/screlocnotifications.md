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
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415204"
---
# <a name="screlocnotifications"></a><span data-ttu-id="bed82-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="bed82-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="bed82-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bed82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bed82-105">Ajusta un puntero dentro de una matriz de notificación de eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="bed82-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bed82-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bed82-106">Header file:</span></span>  <br/> |<span data-ttu-id="bed82-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="bed82-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bed82-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="bed82-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bed82-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bed82-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bed82-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="bed82-110">Called by:</span></span>  <br/> |<span data-ttu-id="bed82-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="bed82-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="bed82-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bed82-112">Parameters</span></span>

 <span data-ttu-id="bed82-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="bed82-113">_cntf_</span></span>
  
> <span data-ttu-id="bed82-114">[entrada] Recuento de [estructuras notification](notification.md) en la matriz indicada por el _parámetro rgntf._</span><span class="sxs-lookup"><span data-stu-id="bed82-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="bed82-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="bed82-115">_rgntf_</span></span>
  
> <span data-ttu-id="bed82-116">[entrada] Puntero a la matriz de **estructuras notification** que definen las notificaciones de eventos dentro de las cuales se ajustará un puntero.</span><span class="sxs-lookup"><span data-stu-id="bed82-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="bed82-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="bed82-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="bed82-118">[entrada] Puntero a la dirección base original de la matriz indicada por el _parámetro rgntf._</span><span class="sxs-lookup"><span data-stu-id="bed82-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="bed82-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="bed82-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="bed82-120">[entrada] Ubicación en la que **ScRelocNotifications** escribe la nueva dirección base de la matriz indicada por el _parámetro rgntf._</span><span class="sxs-lookup"><span data-stu-id="bed82-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="bed82-121">_indeste_</span><span class="sxs-lookup"><span data-stu-id="bed82-121">_pcb_</span></span>
  
> <span data-ttu-id="bed82-122">[salida] Puntero al tamaño, en bytes, de la matriz indicada por el _parámetro pvBaseNew._</span><span class="sxs-lookup"><span data-stu-id="bed82-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bed82-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bed82-123">Return value</span></span>

<span data-ttu-id="bed82-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="bed82-124">S_OK</span></span>
  
> <span data-ttu-id="bed82-125">Un puntero se ha ajustado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bed82-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="bed82-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bed82-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="bed82-127">Se encontró una notificación no válida.</span><span class="sxs-lookup"><span data-stu-id="bed82-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bed82-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bed82-128">Remarks</span></span>

<span data-ttu-id="bed82-129">El  _parámetro para_ la función **ScRelocNotifications** es opcional.</span><span class="sxs-lookup"><span data-stu-id="bed82-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bed82-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bed82-130">See also</span></span>



[<span data-ttu-id="bed82-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="bed82-131">ScRelocProps</span></span>](screlocprops.md)

