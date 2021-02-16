---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7200e7d226eb148fef094ab8540990644d2d4c99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316595"
---
# <a name="imapisupportistoragefromstream"></a><span data-ttu-id="fd5ed-103">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="fd5ed-103">IMAPISupport::IStorageFromStream</span></span>

  
  
<span data-ttu-id="fd5ed-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd5ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd5ed-105">Implementa un objeto de almacenamiento para tener acceso a una secuencia.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-105">Implements a storage object to access a stream.</span></span>
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="fd5ed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd5ed-106">Parameters</span></span>

 <span data-ttu-id="fd5ed-107">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="fd5ed-107">_lpUnkIn_</span></span>
  
> <span data-ttu-id="fd5ed-108">[entrada] Puntero a un objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-108">[in] A pointer to a stream object.</span></span>
    
 <span data-ttu-id="fd5ed-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="fd5ed-109">_lpInterface_</span></span>
  
> <span data-ttu-id="fd5ed-110">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la secuencia a la que apunta  _lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the stream pointed to by  _lpUnkIn_.</span></span> <span data-ttu-id="fd5ed-111">Cualquiera de los siguientes valores son válidos: IID_IStream, IID_ILockBytes o **null**, lo que indica que se debe usar la interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para obtener acceso a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-111">Any of the following values are valid: IID_IStream, IID_ILockBytes, or **null**, which indicates that the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface should be used to access the stream.</span></span> 
    
 <span data-ttu-id="fd5ed-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fd5ed-112">_ulFlags_</span></span>
  
> <span data-ttu-id="fd5ed-113">[entrada] Máscara de bits de marcas que controla cómo se va a crear el objeto de almacenamiento en relación con el objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-113">[in] A bitmask of flags that controls how the storage object is to be created relative to the stream object.</span></span> <span data-ttu-id="fd5ed-114">De forma predeterminada, el almacenamiento se crea con acceso de solo lectura y la secuencia comienza en la posición cero del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-114">By default, the storage is created with read-only access and the stream starts at position zero in the storage.</span></span> <span data-ttu-id="fd5ed-115">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="fd5ed-115">The following flags can be set:</span></span>
    
<span data-ttu-id="fd5ed-116">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="fd5ed-116">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="fd5ed-117">Se debe crear un nuevo objeto de almacenamiento para el objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-117">A new storage object should be created for the stream object.</span></span>
    
<span data-ttu-id="fd5ed-118">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="fd5ed-118">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="fd5ed-119">El objeto de almacenamiento debe comenzar en la posición actual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-119">The storage object should start at the current position of the stream.</span></span>
    
<span data-ttu-id="fd5ed-120">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="fd5ed-120">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="fd5ed-121">El autor de la llamada debe tener permiso de lectura y escritura para el objeto de almacenamiento devuelto.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-121">The caller should have read/write permission to the returned storage object.</span></span>
    
<span data-ttu-id="fd5ed-122">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="fd5ed-122">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="fd5ed-123">El objeto de almacenamiento debe comenzar en la posición cero.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-123">The storage object should start at position zero.</span></span>
    
 <span data-ttu-id="fd5ed-124">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="fd5ed-124">_lppStorageOut_</span></span>
  
> <span data-ttu-id="fd5ed-125">[salida] Puntero a un puntero al objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-125">[out] A pointer to a pointer to the storage object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fd5ed-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd5ed-126">Return value</span></span>

<span data-ttu-id="fd5ed-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd5ed-127">S_OK</span></span> 
  
> <span data-ttu-id="fd5ed-128">El objeto de almacenamiento se creó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-128">The storage object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd5ed-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fd5ed-129">Remarks</span></span>

<span data-ttu-id="fd5ed-130">El **método IMAPISupport::IStorageFromStream** se implementa para todos los objetos de compatibilidad del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-130">The **IMAPISupport::IStorageFromStream** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="fd5ed-131">Los proveedores de servicios **llaman a IStorageFromStream** para crear un objeto de almacenamiento que se usará para abrir propiedades concretas.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-131">Service providers call **IStorageFromStream** to create a storage object to use for opening particular properties.</span></span> <span data-ttu-id="fd5ed-132">Los proveedores de servicios que tienen su propia implementación de [la interfaz IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) no necesitan llamar a **IStorageFromStream**.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-132">Service providers that have their own implementation of the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface do not need to call **IStorageFromStream**.</span></span> 
  
<span data-ttu-id="fd5ed-133">El objeto de almacenamiento creado por **IStorageFromStream** llama al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) de la secuencia para incrementar su recuento de referencias y, a continuación, disminuye el recuento cuando se libera el almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-133">The storage object created by **IStorageFromStream** calls the stream's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment its reference count and then decrements the count when the storage is released.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fd5ed-134">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="fd5ed-134">Notes to callers</span></span>

<span data-ttu-id="fd5ed-135">Cuando se llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de uno de los objetos para abrir una propiedad con la interfaz **IStorage,** realice las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="fd5ed-135">When the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method of one of your objects is called to open a property with the **IStorage** interface, perform the following tasks:</span></span> 
  
1. <span data-ttu-id="fd5ed-136">Abra un objeto de secuencia con permiso de lectura y escritura para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-136">Open a stream object with read/write permission for the property.</span></span>
    
2. <span data-ttu-id="fd5ed-137">Marca internamente la secuencia de propiedades como un objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-137">Internally mark the property stream as a storage object.</span></span>
    
3. <span data-ttu-id="fd5ed-138">Llama **a IStorageFromStream** para generar un objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-138">Call **IStorageFromStream** to generate a storage object.</span></span> 
    
4. <span data-ttu-id="fd5ed-139">Devuelve un puntero a este objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-139">Return a pointer to this storage object.</span></span>
    
<span data-ttu-id="fd5ed-140">Si implementa interfaces adicionales que usan el objeto de almacenamiento, cree un objeto que ajuste el objeto de almacenamiento e implemente un método [IUnknown::QueryInterface de nivel](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) superior.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-140">If you implement additional interfaces that use the storage object, create an object that wraps the storage object and implement a higher level [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method.</span></span> 
  
<span data-ttu-id="fd5ed-141">No permitir que se abra una propiedad con la **interfaz IStream** si se creó con **IStorage**.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-141">Do not allow a property to be opened with the **IStream** interface if it was created with **IStorage**.</span></span> <span data-ttu-id="fd5ed-142">Por el contrario, no permita que se abra una propiedad con la interfaz **IStorage** si se creó con **IStream**.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-142">Conversely, do not allow a property to be opened with the **IStorage** interface if it was created with **IStream**.</span></span> 
  
<span data-ttu-id="fd5ed-143">Con una excepción, es aceptable usar la interfaz **IStreamDocfile** para transmitir un objeto de almacenamiento de un contenedor a otro, pero el identificador de interfaz IID_IStreamDocfile debe pasarse en el parámetro _lpInterface_ del método **OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="fd5ed-143">With one exception, it is acceptable to use the **IStreamDocfile** interface to stream a storage object from one container to another, but the IID_IStreamDocfile interface identifier must be passed in the **OpenProperty** method's  _lpInterface_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fd5ed-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fd5ed-144">See also</span></span>



[<span data-ttu-id="fd5ed-145">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="fd5ed-145">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="fd5ed-146">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fd5ed-146">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

