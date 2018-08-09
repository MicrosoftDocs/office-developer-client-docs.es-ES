---
title: CreateIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CreateIProp
api_type:
- COM
ms.assetid: 9bf68814-2564-433d-b762-3d2c83ca3c60
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 906dc4a24b994e079a977808c3f501aaaea9d84f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816613"
---
# <a name="createiprop"></a><span data-ttu-id="25aff-103">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="25aff-103">CreateIProp</span></span>

  
  
<span data-ttu-id="25aff-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25aff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25aff-105">Crea un objeto de datos de propiedad, es decir, un objeto [IPropData](ipropdataimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="25aff-105">Creates a property data object, that is, an [IPropData](ipropdataimapiprop.md) object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25aff-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="25aff-106">Header file:</span></span>  <br/> |<span data-ttu-id="25aff-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="25aff-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="25aff-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="25aff-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="25aff-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="25aff-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="25aff-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="25aff-110">Called by:</span></span>  <br/> |<span data-ttu-id="25aff-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="25aff-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE CreateIProp(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  LPPROPDATA FAR * lppPropData
);
```

## <a name="parameters"></a><span data-ttu-id="25aff-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25aff-112">Parameters</span></span>

 <span data-ttu-id="25aff-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="25aff-113">_lpInterface_</span></span>
  
> <span data-ttu-id="25aff-114">[entrada] Puntero a un identificador de interfaz (IID) para el objeto de datos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="25aff-114">[in] Pointer to an interface identifier (IID) for the property data object.</span></span> <span data-ttu-id="25aff-115">El identificador de interfaz válido es IID_IMAPIPropData.</span><span class="sxs-lookup"><span data-stu-id="25aff-115">The valid interface identifier is IID_IMAPIPropData.</span></span> <span data-ttu-id="25aff-116">También pasando NULL en el parámetro _lpInterface_ hace que el objeto de datos de propiedad devuelto en el parámetro _lppPropData_ a convertirse a la interfaz estándar para un objeto de datos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="25aff-116">Passing NULL in the  _lpInterface_ parameter also causes the property data object returned in the  _lppPropData_ parameter to be cast to the standard interface for a property data object.</span></span> 
    
 <span data-ttu-id="25aff-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="25aff-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="25aff-118">[entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="25aff-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="25aff-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="25aff-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="25aff-120">[entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se usará para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="25aff-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="25aff-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="25aff-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="25aff-122">[entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="25aff-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="25aff-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="25aff-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="25aff-124">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="25aff-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="25aff-125">_lppPropData_</span><span class="sxs-lookup"><span data-stu-id="25aff-125">_lppPropData_</span></span>
  
> <span data-ttu-id="25aff-126">[out] Puntero a un puntero al objeto de datos devuelto de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="25aff-126">[out] Pointer to a pointer to the returned property data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="25aff-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25aff-127">Return value</span></span>

<span data-ttu-id="25aff-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="25aff-128">S_OK</span></span> 
  
> <span data-ttu-id="25aff-129">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="25aff-129">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="25aff-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="25aff-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="25aff-131">No se admite la interfaz solicitada para este objeto.</span><span class="sxs-lookup"><span data-stu-id="25aff-131">The requested interface is not supported for this object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="25aff-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25aff-132">Remarks</span></span>

<span data-ttu-id="25aff-133">Los parámetros de entrada _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ , seleccione la [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y funciones [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="25aff-133">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="25aff-134">Una aplicación de cliente al llamar a **CreateIProp** pasa punteros a las funciones MAPI que se acaba de asignar nombre; un proveedor de servicios pasa los punteros a estas funciones reciben en su llamada de inicialización o recuperado con una llamada al método [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="25aff-134">A client application calling **CreateIProp** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  

