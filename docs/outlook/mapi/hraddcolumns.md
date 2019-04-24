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
ms.openlocfilehash: 465b685038bc3d906e468c7d7b06e9c20e1fd3c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348198"
---
# <a name="hraddcolumns"></a><span data-ttu-id="dbe12-103">HrAddColumns</span><span class="sxs-lookup"><span data-stu-id="dbe12-103">HrAddColumns</span></span>

  
  
<span data-ttu-id="dbe12-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbe12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbe12-105">Agrega o mueve columnas al principio de una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="dbe12-105">Adds or moves columns to the beginning of an existing table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dbe12-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="dbe12-106">Header file:</span></span>  <br/> |<span data-ttu-id="dbe12-107">mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="dbe12-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dbe12-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="dbe12-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dbe12-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dbe12-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dbe12-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="dbe12-110">Called by:</span></span>  <br/> |<span data-ttu-id="dbe12-111">Proveedores de servicios y aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="dbe12-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="dbe12-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="dbe12-112">Parameters</span></span>

 <span data-ttu-id="dbe12-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="dbe12-113">_lptbl_</span></span>
  
> <span data-ttu-id="dbe12-114">a Puntero a la tabla MAPI afectada.</span><span class="sxs-lookup"><span data-stu-id="dbe12-114">[in] Pointer to the MAPI table affected.</span></span>
    
 <span data-ttu-id="dbe12-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="dbe12-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="dbe12-116">a Puntero a una estructura **SPropTagArray** que contiene una matriz de etiquetas de propiedad para las propiedades que se van a agregar o mover al principio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="dbe12-116">[in] Pointer to an **SPropTagArray** structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="dbe12-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="dbe12-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="dbe12-118">a Puntero a la función **MAPIAllocateBuffer** .</span><span class="sxs-lookup"><span data-stu-id="dbe12-118">[in] Pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="dbe12-119">Se usa para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="dbe12-119">Used to allocate memory.</span></span> 
    
 <span data-ttu-id="dbe12-120">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="dbe12-120">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="dbe12-121">a Puntero a la función **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="dbe12-121">[in] Pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="dbe12-122">Se usa para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="dbe12-122">Used to free memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dbe12-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dbe12-123">Return value</span></span>

 <span data-ttu-id="dbe12-124">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="dbe12-124">**S_OK**</span></span>
  
> <span data-ttu-id="dbe12-125">La llamada se realizó correctamente y se movieron o agregaron las columnas especificadas.</span><span class="sxs-lookup"><span data-stu-id="dbe12-125">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dbe12-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dbe12-126">Remarks</span></span>

<span data-ttu-id="dbe12-127">La función **HrAddColumns** equivale a usar **HrAddColumnsEx** con _lpfnFilterColumns_ establecido en NULL.</span><span class="sxs-lookup"><span data-stu-id="dbe12-127">The **HrAddColumns** function is equivalent to using **HrAddColumnsEx** with  _lpfnFilterColumns_ set to NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dbe12-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbe12-128">See also</span></span>



[<span data-ttu-id="dbe12-129">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="dbe12-129">HrAddColumnsEx</span></span>](hraddcolumnsex.md)
  
[<span data-ttu-id="dbe12-130">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="dbe12-130">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="dbe12-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="dbe12-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="dbe12-132">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="dbe12-132">SPropTagArray</span></span>](sproptagarray.md)

