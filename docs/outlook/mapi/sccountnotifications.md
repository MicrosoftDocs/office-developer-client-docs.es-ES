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
ms.openlocfilehash: 923864c625cb032c3b351bb999ff7cc782eae588
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567170"
---
# <a name="sccountnotifications"></a><span data-ttu-id="db06c-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="db06c-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="db06c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db06c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db06c-105">Determina el tamaño, en bytes, de una matriz de las notificaciones de eventos y valida la memoria asociada a la matriz.</span><span class="sxs-lookup"><span data-stu-id="db06c-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db06c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="db06c-106">Header file:</span></span>  <br/> |<span data-ttu-id="db06c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="db06c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="db06c-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="db06c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="db06c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="db06c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="db06c-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="db06c-110">Called by:</span></span>  <br/> |<span data-ttu-id="db06c-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="db06c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="db06c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db06c-112">Parameters</span></span>

 <span data-ttu-id="db06c-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="db06c-113">_cntf_</span></span>
  
> <span data-ttu-id="db06c-114">[entrada] Recuento de las estructuras de [notificación](notification.md) en la matriz indicada por el parámetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="db06c-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="db06c-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="db06c-115">_rgntf_</span></span>
  
> <span data-ttu-id="db06c-116">[entrada] Puntero a la matriz de estructuras de **notificación** cuyo tamaño es que se determinará.</span><span class="sxs-lookup"><span data-stu-id="db06c-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="db06c-117">_placa de circuitos impresos_</span><span class="sxs-lookup"><span data-stu-id="db06c-117">_pcb_</span></span>
  
> <span data-ttu-id="db06c-118">[out] Puntero opcional para el tamaño, en bytes, de la matriz indicada por el parámetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="db06c-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="db06c-119">Si es NULL, **ScCountNotifications** valida la matriz de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="db06c-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="db06c-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db06c-120">Return value</span></span>

<span data-ttu-id="db06c-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="db06c-121">S_OK</span></span>
  
> <span data-ttu-id="db06c-122">Recuento de determinó correctamente.</span><span class="sxs-lookup"><span data-stu-id="db06c-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="db06c-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="db06c-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="db06c-124">Se ha producido una notificación no válida.</span><span class="sxs-lookup"><span data-stu-id="db06c-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="db06c-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db06c-125">Remarks</span></span>

<span data-ttu-id="db06c-126">Si se pasa NULL en el parámetro _pcb_ , la función **ScCountNotifications** sólo valida la matriz de notificaciones, pero no se realiza recuento; Si se pasa un valor no nulo en _placa de circuitos impresos_, **ScCountNotifications** determina el tamaño de la matriz y almacena la causa _placa de circuitos impresos_.</span><span class="sxs-lookup"><span data-stu-id="db06c-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="db06c-127">El parámetro _pcb_ debe ser lo suficientemente grande como para contener toda la matriz.</span><span class="sxs-lookup"><span data-stu-id="db06c-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

