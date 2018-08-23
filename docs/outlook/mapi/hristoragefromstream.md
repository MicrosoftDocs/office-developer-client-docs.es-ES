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
ms.openlocfilehash: 39f28d5a8e9c8c7f3dfc6a8d09cf022cea08800c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563929"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="0232b-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="0232b-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="0232b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0232b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0232b-105">Capas una interfaz **IStorage** en un objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0232b-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0232b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0232b-106">Header file:</span></span>  <br/> |<span data-ttu-id="0232b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0232b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0232b-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="0232b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0232b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0232b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0232b-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="0232b-110">Called by:</span></span>  <br/> |<span data-ttu-id="0232b-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="0232b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="0232b-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0232b-112">Parameters</span></span>

 <span data-ttu-id="0232b-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="0232b-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="0232b-114">[entrada] Puntero al objeto **IUnknown** implementar **IStream**.</span><span class="sxs-lookup"><span data-stu-id="0232b-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="0232b-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0232b-115">_lpInterface_</span></span>
  
> <span data-ttu-id="0232b-116">[entrada] Puntero al identificador de interfaz (IID) para el objeto stream.</span><span class="sxs-lookup"><span data-stu-id="0232b-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="0232b-117">Cualquiera de los siguientes valores se puede pasar en el parámetro _lpInterface_ : NULL, IID_IStream o IID_ILockBytes.</span><span class="sxs-lookup"><span data-stu-id="0232b-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="0232b-118">Pasando NULL en _lpInterface_ es el mismo que pasar IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="0232b-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="0232b-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0232b-119">_ulFlags_</span></span>
  
> <span data-ttu-id="0232b-120">[entrada] Máscara de bits de indicadores que controla cómo es el objeto de almacenamiento que se creará con respecto a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0232b-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="0232b-121">El valor predeterminado es STGSTRM_RESET, que proporciona el acceso de sólo lectura del objeto de almacenamiento y lo inicia en la posición cero de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0232b-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="0232b-122">Las siguientes marcas se pueden establecer en cualquier combinación, excepto como se ha indicado:</span><span class="sxs-lookup"><span data-stu-id="0232b-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="0232b-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="0232b-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="0232b-124">Crea un nuevo objeto de almacenamiento para el objeto stream.</span><span class="sxs-lookup"><span data-stu-id="0232b-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="0232b-125">Esta marca no se puede establecer si se establece la marca STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="0232b-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="0232b-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="0232b-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="0232b-127">Inicia el almacenamiento en la posición actual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0232b-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="0232b-128">Esta marca no se puede establecer si se establece la marca STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="0232b-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="0232b-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="0232b-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="0232b-130">Permite que el proveedor de servicios de llamada escribir en el almacenamiento devuelto.</span><span class="sxs-lookup"><span data-stu-id="0232b-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="0232b-131">Esta marca no se puede establecer si se establece la marca STGSTRM_RESET.</span><span class="sxs-lookup"><span data-stu-id="0232b-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="0232b-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="0232b-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="0232b-133">Almacenamiento de información que comienza en la posición cero.</span><span class="sxs-lookup"><span data-stu-id="0232b-133">Starts storage at position zero.</span></span> <span data-ttu-id="0232b-134">Esta marca no se puede establecer si se establece cualquier otro marcador.</span><span class="sxs-lookup"><span data-stu-id="0232b-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="0232b-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="0232b-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="0232b-136">[out] Puntero a un puntero al objeto **IStorage** devuelto.</span><span class="sxs-lookup"><span data-stu-id="0232b-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0232b-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0232b-137">Return value</span></span>

<span data-ttu-id="0232b-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="0232b-138">S_OK</span></span> 
  
> <span data-ttu-id="0232b-139">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="0232b-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0232b-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0232b-140">Remarks</span></span>

<span data-ttu-id="0232b-141">Almacén de mensajes compatibilidad con proveedores la función **HrIStorageFromStream** mediante la interfaz **IStorage** para datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0232b-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="0232b-142">Los proveedores de almacén deben implementar la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0232b-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="0232b-143">**HrIStorageFromStream** proporciona la interfaz **IStorage** para el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0232b-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="0232b-144">Es posible que se pase una **ILockBytes** o una interfaz **IStream** en _lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="0232b-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

