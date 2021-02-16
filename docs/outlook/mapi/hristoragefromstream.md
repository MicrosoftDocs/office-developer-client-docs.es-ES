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
# <a name="hristoragefromstream"></a><span data-ttu-id="0e03d-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="0e03d-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="0e03d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e03d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e03d-105">Capas de **una interfaz IStorage** en un **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="0e03d-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e03d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0e03d-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e03d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0e03d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0e03d-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="0e03d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0e03d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0e03d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0e03d-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="0e03d-110">Called by:</span></span>  <br/> |<span data-ttu-id="0e03d-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="0e03d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="0e03d-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e03d-112">Parameters</span></span>

 <span data-ttu-id="0e03d-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="0e03d-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="0e03d-114">[entrada] Puntero al **objeto IUnknown** que implementa **IStream**.</span><span class="sxs-lookup"><span data-stu-id="0e03d-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="0e03d-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0e03d-115">_lpInterface_</span></span>
  
> <span data-ttu-id="0e03d-116">[entrada] Puntero al identificador de interfaz (IID) del objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="0e03d-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="0e03d-117">Cualquiera de los siguientes valores se puede pasar en el parámetro  _lpInterface:_ NULL, IID_IStream o IID_ILockBytes.</span><span class="sxs-lookup"><span data-stu-id="0e03d-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="0e03d-118">Pasar NULL en  _lpInterface_ es lo mismo que pasar IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="0e03d-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="0e03d-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0e03d-119">_ulFlags_</span></span>
  
> <span data-ttu-id="0e03d-120">[entrada] Máscara de bits de marcas que controla cómo se va a crear el objeto de almacenamiento en relación con la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0e03d-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="0e03d-121">El valor predeterminado es STGSTRM_RESET, que proporciona al objeto de almacenamiento acceso de solo lectura y lo inicia en la posición cero de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0e03d-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="0e03d-122">Las siguientes marcas se pueden establecer en cualquier combinación, excepto como se indica:</span><span class="sxs-lookup"><span data-stu-id="0e03d-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="0e03d-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="0e03d-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="0e03d-124">Crea un nuevo objeto de almacenamiento para el objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="0e03d-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="0e03d-125">Esta marca no se puede establecer si se STGSTRM_RESET marca.</span><span class="sxs-lookup"><span data-stu-id="0e03d-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="0e03d-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="0e03d-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="0e03d-127">Inicia el almacenamiento en la posición actual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0e03d-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="0e03d-128">Esta marca no se puede establecer si se STGSTRM_RESET marca.</span><span class="sxs-lookup"><span data-stu-id="0e03d-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="0e03d-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="0e03d-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="0e03d-130">Permite al proveedor de servicios de llamadas escribir en el almacenamiento devuelto.</span><span class="sxs-lookup"><span data-stu-id="0e03d-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="0e03d-131">Esta marca no se puede establecer si se STGSTRM_RESET marca.</span><span class="sxs-lookup"><span data-stu-id="0e03d-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="0e03d-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="0e03d-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="0e03d-133">Inicia el almacenamiento en la posición cero.</span><span class="sxs-lookup"><span data-stu-id="0e03d-133">Starts storage at position zero.</span></span> <span data-ttu-id="0e03d-134">Esta marca no se puede establecer si se establece cualquier otra marca.</span><span class="sxs-lookup"><span data-stu-id="0e03d-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="0e03d-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="0e03d-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="0e03d-136">[salida] Puntero a un puntero al objeto **IStorage** devuelto.</span><span class="sxs-lookup"><span data-stu-id="0e03d-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0e03d-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e03d-137">Return value</span></span>

<span data-ttu-id="0e03d-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e03d-138">S_OK</span></span> 
  
> <span data-ttu-id="0e03d-139">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="0e03d-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e03d-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e03d-140">Remarks</span></span>

<span data-ttu-id="0e03d-141">Los proveedores de almacenamiento de mensajes admiten la función **HrIStorageFromStream** mediante la **interfaz IStorage** para datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0e03d-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="0e03d-142">Los proveedores de la Tienda deben implementar la **interfaz IStream.**</span><span class="sxs-lookup"><span data-stu-id="0e03d-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="0e03d-143">**HrIStorageFromStream** proporciona la **interfaz IStorage** para el **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="0e03d-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="0e03d-144">Es posible pasar una interfaz **ILockBytes** o **IStream**  _en lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="0e03d-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

