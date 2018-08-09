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
ms.openlocfilehash: dc7fa8b546783819b701604a5e489f0fd030ae86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817021"
---
# <a name="hraddcolumns"></a><span data-ttu-id="331ab-103">HrAddColumns</span><span class="sxs-lookup"><span data-stu-id="331ab-103">HrAddColumns</span></span>

  
  
<span data-ttu-id="331ab-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="331ab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="331ab-105">Agrega o mueve las columnas al principio de una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="331ab-105">Adds or moves columns to the beginning of an existing table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="331ab-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="331ab-106">Header file:</span></span>  <br/> |<span data-ttu-id="331ab-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="331ab-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="331ab-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="331ab-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="331ab-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="331ab-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="331ab-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="331ab-110">Called by:</span></span>  <br/> |<span data-ttu-id="331ab-111">Las aplicaciones de cliente y los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="331ab-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="331ab-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="331ab-112">Parameters</span></span>

 <span data-ttu-id="331ab-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="331ab-113">_lptbl_</span></span>
  
> <span data-ttu-id="331ab-114">[entrada] Puntero a la tabla MAPI afectada.</span><span class="sxs-lookup"><span data-stu-id="331ab-114">[in] Pointer to the MAPI table affected.</span></span>
    
 <span data-ttu-id="331ab-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="331ab-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="331ab-116">[entrada] Puntero a una estructura de **elemento SPropTagArray** que contiene una matriz de etiquetas de propiedad para las propiedades que se agreguen o se mueve al principio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="331ab-116">[in] Pointer to an **SPropTagArray** structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="331ab-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="331ab-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="331ab-118">[entrada] Puntero a la función **MAPIAllocateBuffer** .</span><span class="sxs-lookup"><span data-stu-id="331ab-118">[in] Pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="331ab-119">Se usa para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="331ab-119">Used to allocate memory.</span></span> 
    
 <span data-ttu-id="331ab-120">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="331ab-120">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="331ab-121">[entrada] Puntero a la función **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="331ab-121">[in] Pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="331ab-122">Se usa para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="331ab-122">Used to free memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="331ab-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="331ab-123">Return value</span></span>

 <span data-ttu-id="331ab-124">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="331ab-124">**S_OK**</span></span>
  
> <span data-ttu-id="331ab-125">La llamada se ha realizado correctamente y se han movido o agregado de las columnas especificadas.</span><span class="sxs-lookup"><span data-stu-id="331ab-125">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="331ab-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="331ab-126">Remarks</span></span>

<span data-ttu-id="331ab-127">La función **HrAddColumns** es equivalente al uso de **HrAddColumnsEx** con _lpfnFilterColumns_ establecido en NULL.</span><span class="sxs-lookup"><span data-stu-id="331ab-127">The **HrAddColumns** function is equivalent to using **HrAddColumnsEx** with  _lpfnFilterColumns_ set to NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="331ab-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="331ab-128">See also</span></span>



[<span data-ttu-id="331ab-129">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="331ab-129">HrAddColumnsEx</span></span>](hraddcolumnsex.md)
  
[<span data-ttu-id="331ab-130">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="331ab-130">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="331ab-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="331ab-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="331ab-132">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="331ab-132">SPropTagArray</span></span>](sproptagarray.md)

