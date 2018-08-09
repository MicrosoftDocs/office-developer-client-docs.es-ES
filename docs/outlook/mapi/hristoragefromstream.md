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
ms.openlocfilehash: bd2d0a662585e8aba91250786f88dd310fe37e32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817064"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="0fcd7-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="0fcd7-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="0fcd7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0fcd7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0fcd7-105">Capas una interfaz **IStorage** en un objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0fcd7-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0fcd7-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0fcd7-106">Header file:</span></span>  <br/> |<span data-ttu-id="0fcd7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0fcd7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0fcd7-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="0fcd7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0fcd7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0fcd7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0fcd7-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="0fcd7-110">Called by:</span></span>  <br/> |<span data-ttu-id="0fcd7-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="0fcd7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="0fcd7-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fcd7-112">Parameters</span></span>

 <span data-ttu-id="0fcd7-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="0fcd7-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="0fcd7-114">[entrada] Puntero al objeto **IUnknown** implementar **IStream**.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="0fcd7-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0fcd7-115">_lpInterface_</span></span>
  
> <span data-ttu-id="0fcd7-116">[entrada] Puntero al identificador de interfaz (IID) para el objeto stream.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="0fcd7-117">Cualquiera de los siguientes valores se puede pasar en el parámetro _lpInterface_ : NULL, IID_IStream o IID_ILockBytes.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="0fcd7-118">Pasando NULL en _lpInterface_ es el mismo que pasar IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="0fcd7-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0fcd7-119">_ulFlags_</span></span>
  
> <span data-ttu-id="0fcd7-120">[entrada] Máscara de bits de indicadores que controla cómo es el objeto de almacenamiento que se creará con respecto a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="0fcd7-121">El valor predeterminado es STGSTRM_RESET, que proporciona el acceso de sólo lectura del objeto de almacenamiento y lo inicia en la posición cero de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="0fcd7-122">Las siguientes marcas se pueden establecer en cualquier combinación, excepto como se ha indicado:</span><span class="sxs-lookup"><span data-stu-id="0fcd7-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="0fcd7-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="0fcd7-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="0fcd7-124">Crea un nuevo objeto de almacenamiento para el objeto stream.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="0fcd7-125">Esta marca no se puede establecer si se establece la marca STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="0fcd7-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="0fcd7-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="0fcd7-127">Inicia el almacenamiento en la posición actual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="0fcd7-128">Esta marca no se puede establecer si se establece la marca STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="0fcd7-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="0fcd7-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="0fcd7-130">Permite que el proveedor de servicios de llamada escribir en el almacenamiento devuelto.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="0fcd7-131">Esta marca no se puede establecer si se establece la marca STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="0fcd7-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="0fcd7-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="0fcd7-133">Almacenamiento de información que comienza en la posición cero.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-133">Starts storage at position zero.</span></span> <span data-ttu-id="0fcd7-134">Esta marca no se puede establecer si se establece cualquier otro marcador.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="0fcd7-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="0fcd7-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="0fcd7-136">[out] Puntero a un puntero al objeto **IStorage** devuelto.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0fcd7-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0fcd7-137">Return value</span></span>

<span data-ttu-id="0fcd7-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="0fcd7-138">S_OK</span></span> 
  
> <span data-ttu-id="0fcd7-139">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0fcd7-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0fcd7-140">Remarks</span></span>

<span data-ttu-id="0fcd7-141">Almacén de mensajes compatibilidad con proveedores la función **HrIStorageFromStream** mediante la interfaz **IStorage** para datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="0fcd7-142">Los proveedores de almacén deben implementar la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0fcd7-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="0fcd7-143">**HrIStorageFromStream** proporciona la interfaz **IStorage** para el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0fcd7-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="0fcd7-144">Es posible que se pase una **ILockBytes** o una interfaz **IStream** en _lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="0fcd7-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

