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
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435925"
---
# <a name="sccopynotifications"></a><span data-ttu-id="eed3e-103">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="eed3e-103">ScCopyNotifications</span></span>

  
  
<span data-ttu-id="eed3e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eed3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eed3e-105">Copia un grupo de notificaciones de eventos en un único bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="eed3e-105">Copies a group of event notifications to a single block of memory.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eed3e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="eed3e-106">Header file:</span></span>  <br/> |<span data-ttu-id="eed3e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="eed3e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="eed3e-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="eed3e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="eed3e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="eed3e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="eed3e-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="eed3e-110">Called by:</span></span>  <br/> |<span data-ttu-id="eed3e-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="eed3e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="eed3e-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="eed3e-112">Parameters</span></span>

 <span data-ttu-id="eed3e-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="eed3e-113">_cntf_</span></span>
  
> <span data-ttu-id="eed3e-114">[in] Recuento de [estructuras NOTIFICATION](notification.md) en la matriz indicada por el _parámetro rgntf._</span><span class="sxs-lookup"><span data-stu-id="eed3e-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="eed3e-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="eed3e-115">_rgntf_</span></span>
  
> <span data-ttu-id="eed3e-116">[in] Puntero a una matriz de **estructuras NOTIFICATION** que definen las notificaciones de eventos que se van a copiar.</span><span class="sxs-lookup"><span data-stu-id="eed3e-116">[in] Pointer to an array of **NOTIFICATION** structures defining the event notifications to be copied.</span></span> 
    
 <span data-ttu-id="eed3e-117">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="eed3e-117">_pvDst_</span></span>
  
> <span data-ttu-id="eed3e-118">[salida] Puntero a las notificaciones devueltas.</span><span class="sxs-lookup"><span data-stu-id="eed3e-118">[out] Pointer to the returned notifications.</span></span> 
    
 <span data-ttu-id="eed3e-119">_pcb_</span><span class="sxs-lookup"><span data-stu-id="eed3e-119">_pcb_</span></span>
  
> <span data-ttu-id="eed3e-120">[salida] Puntero opcional a una variable donde se almacena el tamaño, en bytes, de la matriz apuntada por el parámetro _rgntf._</span><span class="sxs-lookup"><span data-stu-id="eed3e-120">[out] Optional pointer to a variable where the size, in bytes, of the array pointed to by the  _rgntf_ parameter is stored.</span></span> <span data-ttu-id="eed3e-121">Si no es NULL, el _parámetro pcb_ se establece en el número de bytes almacenados en el _parámetro pvDst._</span><span class="sxs-lookup"><span data-stu-id="eed3e-121">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eed3e-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eed3e-122">Return value</span></span>

<span data-ttu-id="eed3e-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="eed3e-123">S_OK</span></span>
  
> <span data-ttu-id="eed3e-124">Las notificaciones de eventos se copiaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="eed3e-124">Event notifications were copied successfully.</span></span>
    
<span data-ttu-id="eed3e-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="eed3e-125">E_INVALIDARG</span></span>
  
> <span data-ttu-id="eed3e-126">Se encontró una notificación no válida.</span><span class="sxs-lookup"><span data-stu-id="eed3e-126">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eed3e-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eed3e-127">Remarks</span></span>

<span data-ttu-id="eed3e-128">Si se pasa NULL en el  _parámetro pcb,_ no se realiza ninguna copia; si se pasa un valor que no es nulo en  _pcb_, la función **ScCopyNotifications** copia el tamaño de la matriz y la matriz en sí en un único bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="eed3e-128">If NULL is passed in the  _pcb_ parameter, no copying is performed; if a non-null value is passed in  _pcb_, the **ScCopyNotifications** function copies the size of the array and the array itself to a single block of memory.</span></span> <span data-ttu-id="eed3e-129">Si _pcb_ no es NULL, se establece en el número de bytes almacenados en el _parámetro pvDst._</span><span class="sxs-lookup"><span data-stu-id="eed3e-129">If  _pcb_ is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> <span data-ttu-id="eed3e-130">El  _parámetro pvDst_ debe ser lo suficientemente grande como para contener toda la matriz.</span><span class="sxs-lookup"><span data-stu-id="eed3e-130">The  _pvDst_ parameter must be large enough to contain the entire array.</span></span> 
  

