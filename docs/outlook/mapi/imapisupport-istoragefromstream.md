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
ms.openlocfilehash: f1c27f87cb113ebe30a42211035f6f50475a1be3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588184"
---
# <a name="imapisupportistoragefromstream"></a><span data-ttu-id="46f69-103">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="46f69-103">IMAPISupport::IStorageFromStream</span></span>

  
  
<span data-ttu-id="46f69-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46f69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46f69-105">Implementa un objeto de almacenamiento para obtener acceso a una secuencia.</span><span class="sxs-lookup"><span data-stu-id="46f69-105">Implements a storage object to access a stream.</span></span>
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="46f69-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46f69-106">Parameters</span></span>

 <span data-ttu-id="46f69-107">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="46f69-107">_lpUnkIn_</span></span>
  
> <span data-ttu-id="46f69-108">[entrada] Un puntero a un objeto stream.</span><span class="sxs-lookup"><span data-stu-id="46f69-108">[in] A pointer to a stream object.</span></span>
    
 <span data-ttu-id="46f69-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="46f69-109">_lpInterface_</span></span>
  
> <span data-ttu-id="46f69-110">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la secuencia indicada por _lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="46f69-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the stream pointed to by  _lpUnkIn_.</span></span> <span data-ttu-id="46f69-111">Cualquiera de los valores siguientes son válido: IID_IStream, IID_ILockBytes, o **null**, que indica que debe usarse la interfaz [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) para tener acceso a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="46f69-111">Any of the following values are valid: IID_IStream, IID_ILockBytes, or **null**, which indicates that the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface should be used to access the stream.</span></span> 
    
 <span data-ttu-id="46f69-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="46f69-112">_ulFlags_</span></span>
  
> <span data-ttu-id="46f69-113">[entrada] Una máscara de bits de indicadores que controla cómo es el objeto de almacenamiento que se creará en relación con el objeto stream.</span><span class="sxs-lookup"><span data-stu-id="46f69-113">[in] A bitmask of flags that controls how the storage object is to be created relative to the stream object.</span></span> <span data-ttu-id="46f69-114">De forma predeterminada, se crea el almacenamiento con acceso de solo lectura y se inicia la secuencia en la posición cero en el almacenamiento de información.</span><span class="sxs-lookup"><span data-stu-id="46f69-114">By default, the storage is created with read-only access and the stream starts at position zero in the storage.</span></span> <span data-ttu-id="46f69-115">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="46f69-115">The following flags can be set:</span></span>
    
<span data-ttu-id="46f69-116">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="46f69-116">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="46f69-117">Para el objeto stream, se debe crear un nuevo objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="46f69-117">A new storage object should be created for the stream object.</span></span>
    
<span data-ttu-id="46f69-118">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="46f69-118">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="46f69-119">El objeto de almacenamiento debe comenzar en la posición actual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="46f69-119">The storage object should start at the current position of the stream.</span></span>
    
<span data-ttu-id="46f69-120">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="46f69-120">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="46f69-121">El llamador debe tener permiso de lectura y escritura para el objeto de almacenamiento devuelto.</span><span class="sxs-lookup"><span data-stu-id="46f69-121">The caller should have read/write permission to the returned storage object.</span></span>
    
<span data-ttu-id="46f69-122">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="46f69-122">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="46f69-123">El objeto de almacenamiento debe comenzar en la posición cero.</span><span class="sxs-lookup"><span data-stu-id="46f69-123">The storage object should start at position zero.</span></span>
    
 <span data-ttu-id="46f69-124">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="46f69-124">_lppStorageOut_</span></span>
  
> <span data-ttu-id="46f69-125">[out] Un puntero a un puntero al objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="46f69-125">[out] A pointer to a pointer to the storage object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="46f69-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46f69-126">Return value</span></span>

<span data-ttu-id="46f69-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="46f69-127">S_OK</span></span> 
  
> <span data-ttu-id="46f69-128">Se ha creado correctamente el objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="46f69-128">The storage object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46f69-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46f69-129">Remarks</span></span>

<span data-ttu-id="46f69-130">El método **IMAPISupport::IStorageFromStream** se implementa para todos los objetos de soporte técnico de proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="46f69-130">The **IMAPISupport::IStorageFromStream** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="46f69-131">Proveedores de servicios de llamar a **IStorageFromStream** para crear un objeto de almacenamiento que se usará para abrir propiedades concretas.</span><span class="sxs-lookup"><span data-stu-id="46f69-131">Service providers call **IStorageFromStream** to create a storage object to use for opening particular properties.</span></span> <span data-ttu-id="46f69-132">Proveedores de servicios que tienen su propia implementación de la interfaz [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) no es necesario llamar a **IStorageFromStream**.</span><span class="sxs-lookup"><span data-stu-id="46f69-132">Service providers that have their own implementation of the [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) interface do not need to call **IStorageFromStream**.</span></span> 
  
<span data-ttu-id="46f69-133">El objeto de almacenamiento creado por **IStorageFromStream** llama al método [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) de la secuencia para incrementar su recuento de referencia y, a continuación, se disminuye el recuento cuando se libera el almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="46f69-133">The storage object created by **IStorageFromStream** calls the stream's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) method to increment its reference count and then decrements the count when the storage is released.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="46f69-134">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="46f69-134">Notes to callers</span></span>

<span data-ttu-id="46f69-135">Cuando se llama al método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de uno de los objetos para abrir una propiedad con la interfaz **IStorage** , realice las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="46f69-135">When the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method of one of your objects is called to open a property with the **IStorage** interface, perform the following tasks:</span></span> 
  
1. <span data-ttu-id="46f69-136">Abrir un objeto stream con el permiso de lectura y escritura para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="46f69-136">Open a stream object with read/write permission for the property.</span></span>
    
2. <span data-ttu-id="46f69-137">Internamente, marque la secuencia de la propiedad como un objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="46f69-137">Internally mark the property stream as a storage object.</span></span>
    
3. <span data-ttu-id="46f69-138">Llame a **IStorageFromStream** para generar un objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="46f69-138">Call **IStorageFromStream** to generate a storage object.</span></span> 
    
4. <span data-ttu-id="46f69-139">Devolver un puntero a este objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="46f69-139">Return a pointer to this storage object.</span></span>
    
<span data-ttu-id="46f69-140">Si implementa interfaces adicionales que utilizan el objeto de almacenamiento, cree un objeto que encapsula el objeto de almacenamiento e implementar un método [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="46f69-140">If you implement additional interfaces that use the storage object, create an object that wraps the storage object and implement a higher level [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) method.</span></span> 
  
<span data-ttu-id="46f69-141">No permitir una propiedad para abrirse con la interfaz **IStream** si se creó con **IStorage**.</span><span class="sxs-lookup"><span data-stu-id="46f69-141">Do not allow a property to be opened with the **IStream** interface if it was created with **IStorage**.</span></span> <span data-ttu-id="46f69-142">Por el contrario, no permitir una propiedad para abrirse con la interfaz **IStorage** si se creó con **IStream**.</span><span class="sxs-lookup"><span data-stu-id="46f69-142">Conversely, do not allow a property to be opened with the **IStorage** interface if it was created with **IStream**.</span></span> 
  
<span data-ttu-id="46f69-143">Con una excepción, es aceptable para usar la interfaz de **IStreamDocfile** para un objeto de almacenamiento de un contenedor a otro en secuencia, pero se debe pasar el identificador de interfaz IID_IStreamDocfile en el método de **OpenProperty** _lpInterface _parámetro.</span><span class="sxs-lookup"><span data-stu-id="46f69-143">With one exception, it is acceptable to use the **IStreamDocfile** interface to stream a storage object from one container to another, but the IID_IStreamDocfile interface identifier must be passed in the **OpenProperty** method's  _lpInterface_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46f69-144">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="46f69-144">See also</span></span>



[<span data-ttu-id="46f69-145">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="46f69-145">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="46f69-146">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="46f69-146">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

