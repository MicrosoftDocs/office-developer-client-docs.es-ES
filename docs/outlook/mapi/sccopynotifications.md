---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 28a802ffc43b08d3e2ec2be26dd98fa78f474d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820565"
---
# <a name="sccopynotifications"></a><span data-ttu-id="d45bf-103">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="d45bf-103">ScCopyNotifications</span></span>

  
  
<span data-ttu-id="d45bf-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d45bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d45bf-105">Copia un grupo de las notificaciones de eventos en un único bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="d45bf-105">Copies a group of event notifications to a single block of memory.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d45bf-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d45bf-106">Header file:</span></span>  <br/> |<span data-ttu-id="d45bf-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d45bf-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d45bf-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="d45bf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d45bf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d45bf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d45bf-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d45bf-110">Called by:</span></span>  <br/> |<span data-ttu-id="d45bf-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="d45bf-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="d45bf-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d45bf-112">Parameters</span></span>

 <span data-ttu-id="d45bf-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="d45bf-113">_cntf_</span></span>
  
> <span data-ttu-id="d45bf-114">[entrada] Recuento de las estructuras de [notificación](notification.md) en la matriz indicada por el parámetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="d45bf-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="d45bf-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="d45bf-115">_rgntf_</span></span>
  
> <span data-ttu-id="d45bf-116">[entrada] Puntero a una matriz de las estructuras de **notificación** para definir las notificaciones de eventos que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="d45bf-116">[in] Pointer to an array of **NOTIFICATION** structures defining the event notifications to be copied.</span></span> 
    
 <span data-ttu-id="d45bf-117">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="d45bf-117">_pvDst_</span></span>
  
> <span data-ttu-id="d45bf-118">[out] Puntero a las notificaciones devueltas.</span><span class="sxs-lookup"><span data-stu-id="d45bf-118">[out] Pointer to the returned notifications.</span></span> 
    
 <span data-ttu-id="d45bf-119">_placa de circuitos impresos_</span><span class="sxs-lookup"><span data-stu-id="d45bf-119">_pcb_</span></span>
  
> <span data-ttu-id="d45bf-120">[out] Se almacena un puntero opcional a una variable donde el tamaño, en bytes, de la matriz indicado por el parámetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="d45bf-120">[out] Optional pointer to a variable where the size, in bytes, of the array pointed to by the  _rgntf_ parameter is stored.</span></span> <span data-ttu-id="d45bf-121">Si no es NULL, el parámetro _pcb_ se establece en el número de bytes que se almacenan en el parámetro _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="d45bf-121">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d45bf-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d45bf-122">Return value</span></span>

<span data-ttu-id="d45bf-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="d45bf-123">S_OK</span></span>
  
> <span data-ttu-id="d45bf-124">Las notificaciones de eventos se copiaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="d45bf-124">Event notifications were copied successfully.</span></span>
    
<span data-ttu-id="d45bf-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d45bf-125">E_INVALIDARG</span></span>
  
> <span data-ttu-id="d45bf-126">Se ha producido una notificación no válida.</span><span class="sxs-lookup"><span data-stu-id="d45bf-126">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d45bf-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d45bf-127">Remarks</span></span>

<span data-ttu-id="d45bf-128">Si se pasa NULL en el parámetro de la _placa de circuitos impresos_ , no copiar se lleva a cabo; Si se pasa un valor no nulo en _placa de circuitos impresos_, la función **ScCopyNotifications** copia el tamaño de la matriz y la matriz de sí mismo en un único bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="d45bf-128">If NULL is passed in the  _pcb_ parameter, no copying is performed; if a non-null value is passed in  _pcb_, the **ScCopyNotifications** function copies the size of the array and the array itself to a single block of memory.</span></span> <span data-ttu-id="d45bf-129">Si la _placa de circuitos impresos_ no es NULL, se establece el número de bytes que se almacenan en el parámetro _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="d45bf-129">If  _pcb_ is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> <span data-ttu-id="d45bf-130">El parámetro _pvDst_ debe ser lo suficientemente grande como para contener toda la matriz.</span><span class="sxs-lookup"><span data-stu-id="d45bf-130">The  _pvDst_ parameter must be large enough to contain the entire array.</span></span> 
  

