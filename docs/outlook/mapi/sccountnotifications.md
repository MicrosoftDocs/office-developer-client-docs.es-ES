---
title: ScCountNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountNotifications
api_type:
- COM
ms.assetid: 13e80bdc-cb59-47a5-8de0-404e22f87f82
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437997"
---
# <a name="sccountnotifications"></a><span data-ttu-id="d8357-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="d8357-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="d8357-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8357-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8357-105">Determina el tamaño, en bytes, de una matriz de notificaciones de eventos y valida la memoria asociada a la matriz.</span><span class="sxs-lookup"><span data-stu-id="d8357-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8357-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d8357-106">Header file:</span></span>  <br/> |<span data-ttu-id="d8357-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="d8357-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d8357-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d8357-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d8357-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d8357-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d8357-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d8357-110">Called by:</span></span>  <br/> |<span data-ttu-id="d8357-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="d8357-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="d8357-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d8357-112">Parameters</span></span>

 <span data-ttu-id="d8357-113">_CNTF_</span><span class="sxs-lookup"><span data-stu-id="d8357-113">_cntf_</span></span>
  
> <span data-ttu-id="d8357-114">a Número de estructuras de [notificación](notification.md) en la matriz indicada por el parámetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="d8357-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="d8357-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="d8357-115">_rgntf_</span></span>
  
> <span data-ttu-id="d8357-116">a Puntero a la matriz de estructuras de **notificación** cuyo tamaño se va a determinar.</span><span class="sxs-lookup"><span data-stu-id="d8357-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="d8357-117">_impreso_</span><span class="sxs-lookup"><span data-stu-id="d8357-117">_pcb_</span></span>
  
> <span data-ttu-id="d8357-118">contempla Puntero opcional al tamaño, en bytes, de la matriz señalada por el parámetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="d8357-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="d8357-119">Si es NULL, **ScCountNotifications** valida la matriz de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d8357-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d8357-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8357-120">Return value</span></span>

<span data-ttu-id="d8357-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="d8357-121">S_OK</span></span>
  
> <span data-ttu-id="d8357-122">El reCuento se determinó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d8357-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="d8357-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d8357-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="d8357-124">Se encontró una notificación no válida.</span><span class="sxs-lookup"><span data-stu-id="d8357-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8357-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8357-125">Remarks</span></span>

<span data-ttu-id="d8357-126">Si se pasa NULL en el parámetro _PCB_ , la función **ScCountNotifications** sólo valida la matriz de notificaciones, pero no se realiza ningún recuento; Si se pasa un valor no nulo en _PCB_, **ScCountNotifications** determina el tamaño de la matriz y almacena la causa de la _PCB_.</span><span class="sxs-lookup"><span data-stu-id="d8357-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="d8357-127">El parámetro _PCB_ debe ser lo suficientemente grande como para contener toda la matriz.</span><span class="sxs-lookup"><span data-stu-id="d8357-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

