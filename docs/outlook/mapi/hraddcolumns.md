---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ffc47e924b7a0f94db66adbffe01b2cdc619dc8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580736"
---
# <a name="hraddcolumns"></a><span data-ttu-id="558a0-103">HrAddColumns</span><span class="sxs-lookup"><span data-stu-id="558a0-103">HrAddColumns</span></span>

  
  
<span data-ttu-id="558a0-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="558a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="558a0-105">Agrega o mueve las columnas al principio de una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="558a0-105">Adds or moves columns to the beginning of an existing table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="558a0-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="558a0-106">Header file:</span></span>  <br/> |<span data-ttu-id="558a0-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="558a0-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="558a0-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="558a0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="558a0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="558a0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="558a0-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="558a0-110">Called by:</span></span>  <br/> |<span data-ttu-id="558a0-111">Las aplicaciones de cliente y los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="558a0-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="558a0-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="558a0-112">Parameters</span></span>

 <span data-ttu-id="558a0-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="558a0-113">_lptbl_</span></span>
  
> <span data-ttu-id="558a0-114">[entrada] Puntero a la tabla MAPI afectada.</span><span class="sxs-lookup"><span data-stu-id="558a0-114">[in] Pointer to the MAPI table affected.</span></span>
    
 <span data-ttu-id="558a0-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="558a0-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="558a0-116">[entrada] Puntero a una estructura de **elemento SPropTagArray** que contiene una matriz de etiquetas de propiedad para las propiedades que se agreguen o se mueve al principio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="558a0-116">[in] Pointer to an **SPropTagArray** structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="558a0-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="558a0-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="558a0-118">[entrada] Puntero a la función **MAPIAllocateBuffer** .</span><span class="sxs-lookup"><span data-stu-id="558a0-118">[in] Pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="558a0-119">Se usa para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="558a0-119">Used to allocate memory.</span></span> 
    
 <span data-ttu-id="558a0-120">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="558a0-120">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="558a0-121">[entrada] Puntero a la función **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="558a0-121">[in] Pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="558a0-122">Se usa para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="558a0-122">Used to free memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="558a0-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="558a0-123">Return value</span></span>

 <span data-ttu-id="558a0-124">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="558a0-124">**S_OK**</span></span>
  
> <span data-ttu-id="558a0-125">La llamada se ha realizado correctamente y se han movido o agregado de las columnas especificadas.</span><span class="sxs-lookup"><span data-stu-id="558a0-125">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="558a0-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="558a0-126">Remarks</span></span>

<span data-ttu-id="558a0-127">La función **HrAddColumns** es equivalente al uso de **HrAddColumnsEx** con _lpfnFilterColumns_ establecido en NULL.</span><span class="sxs-lookup"><span data-stu-id="558a0-127">The **HrAddColumns** function is equivalent to using **HrAddColumnsEx** with  _lpfnFilterColumns_ set to NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="558a0-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="558a0-128">See also</span></span>



[<span data-ttu-id="558a0-129">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="558a0-129">HrAddColumnsEx</span></span>](hraddcolumnsex.md)
  
[<span data-ttu-id="558a0-130">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="558a0-130">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="558a0-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="558a0-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="558a0-132">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="558a0-132">SPropTagArray</span></span>](sproptagarray.md)

