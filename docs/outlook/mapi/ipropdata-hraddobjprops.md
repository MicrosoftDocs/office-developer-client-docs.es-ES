---
title: IPropDataHrAddObjProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: df63f08d3d453575816c4f7ab043f802023e21d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416387"
---
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="53f53-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="53f53-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="53f53-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53f53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53f53-105">Agrega una o más propiedades de tipo PT Object al objeto.</span><span class="sxs-lookup"><span data-stu-id="53f53-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="53f53-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="53f53-106">Parameters</span></span>

 <span data-ttu-id="53f53-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="53f53-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="53f53-108">a Un puntero a una matriz de etiquetas de propiedad que indica las propiedades que se van a agregar.</span><span class="sxs-lookup"><span data-stu-id="53f53-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="53f53-109">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="53f53-109">_lppProblems_</span></span>
  
> <span data-ttu-id="53f53-110">[in, out] En la entrada, un puntero válido a una estructura [SPropProblemArray](spropproblemarray.md) o null.</span><span class="sxs-lookup"><span data-stu-id="53f53-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="53f53-111">En la salida, un puntero a un puntero a una estructura que contiene información sobre las propiedades que no se han podido agregar o NULL.</span><span class="sxs-lookup"><span data-stu-id="53f53-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="53f53-112">Un puntero a una propiedad se devuelve una estructura de matriz con problemas sólo si se pasa un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="53f53-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="53f53-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53f53-113">Return value</span></span>

<span data-ttu-id="53f53-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="53f53-114">S_OK</span></span> 
  
> <span data-ttu-id="53f53-115">Las propiedades se agregaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="53f53-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="53f53-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="53f53-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="53f53-117">Se pasó un tipo de propiedad que no es PT Object en la matriz a la que apunta el parámetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="53f53-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="53f53-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="53f53-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="53f53-119">El objeto se ha establecido para no permitir el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="53f53-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="53f53-120">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="53f53-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="53f53-121">Se agregaron algunas de las propiedades, pero no todas.</span><span class="sxs-lookup"><span data-stu-id="53f53-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53f53-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53f53-122">Remarks</span></span>

<span data-ttu-id="53f53-123">El método **IPropData:: HrAddObjProps** agrega una o más propiedades de tipo PT Object al objeto.</span><span class="sxs-lookup"><span data-stu-id="53f53-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="53f53-124">**HrAddObjProps** proporciona una alternativa al método [IMAPIProp:: SetProps](imapiprop-setprops.md) para propiedades de objeto, porque las propiedades de objeto no se pueden crear llamando a **SetProps**.</span><span class="sxs-lookup"><span data-stu-id="53f53-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="53f53-125">Agregar una propiedad de objeto da como resultado la etiqueta Property que se va a incluir en la lista de etiquetas de propiedad que devuelve el método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="53f53-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="53f53-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="53f53-126">Notes to callers</span></span>

<span data-ttu-id="53f53-127">Si **HrAddObjProps** devuelve MAPI_W_PARTIAL_COMPLETION y ha establecido _lppProblems_ en un puntero válido, Compruebe la estructura de [SPropProblemArray](spropproblemarray.md) devuelta para averiguar qué propiedades no se han agregado.</span><span class="sxs-lookup"><span data-stu-id="53f53-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="53f53-128">Normalmente, el único problema que se produce es la falta de memoria.</span><span class="sxs-lookup"><span data-stu-id="53f53-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="53f53-129">Libere la estructura **SPropProblemArray** llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) cuando haya terminado con ella.</span><span class="sxs-lookup"><span data-stu-id="53f53-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="53f53-130">Para agregar una propiedad, el objeto de destino debe tener permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="53f53-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="53f53-131">Si **HrAddObjProps** devuelve MAPI_E_NO_ACCESS, no se pueden agregar propiedades al objeto porque no permite modificación.</span><span class="sxs-lookup"><span data-stu-id="53f53-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="53f53-132">Para obtener permiso de lectura y escritura en un objeto antes de llamar a **HrAddObjProps**, llame a [IPropData:: HrSetObjAccess](ipropdata-hrsetobjaccess.md) y establezca el parámetro _ulAccess_ en IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="53f53-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53f53-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="53f53-133">See also</span></span>



[<span data-ttu-id="53f53-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="53f53-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="53f53-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="53f53-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="53f53-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="53f53-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="53f53-137">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="53f53-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

