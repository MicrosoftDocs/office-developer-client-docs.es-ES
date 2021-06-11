---
title: HrIStorageFromStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrIStorageFromStream
api_type:
- HeaderDef
ms.assetid: 1cdc95b8-a156-4600-9e20-caaa02680e87
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1362b1131d937ef240aa1962db8c1b5116786c67
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416835"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="ddaac-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="ddaac-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="ddaac-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddaac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddaac-105">Capas de **una interfaz IStorage** en un **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="ddaac-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddaac-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ddaac-106">Header file:</span></span>  <br/> |<span data-ttu-id="ddaac-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ddaac-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ddaac-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ddaac-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ddaac-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ddaac-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ddaac-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ddaac-110">Called by:</span></span>  <br/> |<span data-ttu-id="ddaac-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="ddaac-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="ddaac-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="ddaac-112">Parameters</span></span>

 <span data-ttu-id="ddaac-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="ddaac-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="ddaac-114">[in] Puntero al **objeto IUnknown** que implementa **IStream**.</span><span class="sxs-lookup"><span data-stu-id="ddaac-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="ddaac-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ddaac-115">_lpInterface_</span></span>
  
> <span data-ttu-id="ddaac-116">[in] Puntero al identificador de interfaz (IID) del objeto stream.</span><span class="sxs-lookup"><span data-stu-id="ddaac-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="ddaac-117">Cualquiera de los siguientes valores se puede pasar en el parámetro  _lpInterface:_ NULL, IID_IStream o IID_ILockBytes.</span><span class="sxs-lookup"><span data-stu-id="ddaac-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="ddaac-118">Pasar NULL en  _lpInterface_ es lo mismo que pasar IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="ddaac-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="ddaac-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ddaac-119">_ulFlags_</span></span>
  
> <span data-ttu-id="ddaac-120">[in] Máscara de bits de marcas que controla cómo se va a crear el objeto de almacenamiento con relación a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="ddaac-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="ddaac-121">El valor predeterminado es STGSTRM_RESET, que proporciona al objeto de almacenamiento acceso de solo lectura e inicia en la posición cero de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="ddaac-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="ddaac-122">Las siguientes marcas se pueden establecer en cualquier combinación, excepto como se indica:</span><span class="sxs-lookup"><span data-stu-id="ddaac-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="ddaac-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="ddaac-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="ddaac-124">Crea un nuevo objeto de almacenamiento para el objeto stream.</span><span class="sxs-lookup"><span data-stu-id="ddaac-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="ddaac-125">Esta marca no se puede establecer si STGSTRM_RESET marca está establecida.</span><span class="sxs-lookup"><span data-stu-id="ddaac-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="ddaac-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="ddaac-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="ddaac-127">Inicia el almacenamiento en la posición actual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="ddaac-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="ddaac-128">Esta marca no se puede establecer si STGSTRM_RESET marca está establecida.</span><span class="sxs-lookup"><span data-stu-id="ddaac-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="ddaac-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="ddaac-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="ddaac-130">Permite al proveedor de servicios de llamadas escribir en el almacenamiento devuelto.</span><span class="sxs-lookup"><span data-stu-id="ddaac-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="ddaac-131">Esta marca no se puede establecer si STGSTRM_RESET marca está establecida.</span><span class="sxs-lookup"><span data-stu-id="ddaac-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="ddaac-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="ddaac-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="ddaac-133">Inicia el almacenamiento en la posición cero.</span><span class="sxs-lookup"><span data-stu-id="ddaac-133">Starts storage at position zero.</span></span> <span data-ttu-id="ddaac-134">Esta marca no se puede establecer si se establece otra marca.</span><span class="sxs-lookup"><span data-stu-id="ddaac-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="ddaac-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="ddaac-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="ddaac-136">[salida] Puntero a un puntero al objeto **IStorage** devuelto.</span><span class="sxs-lookup"><span data-stu-id="ddaac-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ddaac-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ddaac-137">Return value</span></span>

<span data-ttu-id="ddaac-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="ddaac-138">S_OK</span></span> 
  
> <span data-ttu-id="ddaac-139">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="ddaac-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ddaac-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ddaac-140">Remarks</span></span>

<span data-ttu-id="ddaac-141">Los proveedores de almacén de mensajes **admiten la función HrIStorageFromStream** mediante la **interfaz IStorage** para datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ddaac-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="ddaac-142">Los proveedores de almacenamiento deben implementar la **interfaz IStream.**</span><span class="sxs-lookup"><span data-stu-id="ddaac-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="ddaac-143">**HrIStorageFromStream proporciona** la **interfaz IStorage** para el **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="ddaac-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="ddaac-144">Es posible pasar un **ILockBytes** o una **interfaz IStream** en  _lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="ddaac-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

