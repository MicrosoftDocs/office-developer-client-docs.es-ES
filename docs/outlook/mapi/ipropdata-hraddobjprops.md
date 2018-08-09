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
ms.openlocfilehash: 985b763ade9670c064c6c338953debf7beaa2783
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817902"
---
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="36268-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="36268-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="36268-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="36268-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="36268-105">Agrega una o más propiedades de tipo pt Object para el objeto.</span><span class="sxs-lookup"><span data-stu-id="36268-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="36268-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="36268-106">Parameters</span></span>

 <span data-ttu-id="36268-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="36268-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="36268-108">[entrada] Un puntero a una matriz de etiquetas de propiedad que indican las propiedades para agregar.</span><span class="sxs-lookup"><span data-stu-id="36268-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="36268-109">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="36268-109">_lppProblems_</span></span>
  
> <span data-ttu-id="36268-110">[entrada, salida] En la entrada, un puntero a una estructura [SPropProblemArray](spropproblemarray.md) , válido o NULL.</span><span class="sxs-lookup"><span data-stu-id="36268-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="36268-111">En resultado, un puntero a un puntero a una estructura que contiene información acerca de las propiedades que no se pudo agregar o NULL.</span><span class="sxs-lookup"><span data-stu-id="36268-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="36268-112">Se devuelve un puntero a una estructura de matriz de propiedad problema sólo si se pasa un puntero válido en.</span><span class="sxs-lookup"><span data-stu-id="36268-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="36268-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36268-113">Return value</span></span>

<span data-ttu-id="36268-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="36268-114">S_OK</span></span> 
  
> <span data-ttu-id="36268-115">Las propiedades se han agregado correctamente.</span><span class="sxs-lookup"><span data-stu-id="36268-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="36268-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="36268-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="36268-117">Una propiedad de tipo que se pasó pt Object en la matriz que señala el parámetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="36268-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="36268-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="36268-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="36268-119">El objeto se estableció para no permitir el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="36268-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="36268-120">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="36268-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="36268-121">Algunos, pero no todos, de las propiedades que se han agregado.</span><span class="sxs-lookup"><span data-stu-id="36268-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36268-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="36268-122">Remarks</span></span>

<span data-ttu-id="36268-123">El método **IPropData::HrAddObjProps** agrega una o más propiedades de tipo pt Object para el objeto.</span><span class="sxs-lookup"><span data-stu-id="36268-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="36268-124">**HrAddObjProps** proporciona una alternativa al método [IMAPIProp::SetProps](imapiprop-setprops.md) para las propiedades del objeto, debido a que las propiedades del objeto no se puede crear llamando **SetProps**.</span><span class="sxs-lookup"><span data-stu-id="36268-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="36268-125">Adición de resultado de una propiedad de objeto en la etiqueta de propiedad que se encuentran en la lista de etiquetas de propiedad que devuelve el método [IMAPIProp::GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="36268-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="36268-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="36268-126">Notes to callers</span></span>

<span data-ttu-id="36268-127">Si **HrAddObjProps** devuelve MAPI_W_PARTIAL_COMPLETION y ha establecido _lppProblems_ a un puntero válido, compruebe la estructura [SPropProblemArray](spropproblemarray.md) devuelta para averiguar qué propiedades no se han agregado.</span><span class="sxs-lookup"><span data-stu-id="36268-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="36268-128">Normalmente, el único problema que se produce es la falta de memoria.</span><span class="sxs-lookup"><span data-stu-id="36268-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="36268-129">Libere la estructura **SPropProblemArray** mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) cuando haya terminado con él.</span><span class="sxs-lookup"><span data-stu-id="36268-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="36268-130">Para agregar una propiedad, el objeto de destino debe tener permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="36268-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="36268-131">Si **HrAddObjProps** devuelve MAPI_E_NO_ACCESS, no se puede agregar propiedades al objeto debido a que no permite la modificación.</span><span class="sxs-lookup"><span data-stu-id="36268-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="36268-132">Para obtener permiso de lectura y escritura a un objeto antes de llamar a **HrAddObjProps**, llame [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) y establezca el parámetro _ulAccess_ en IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="36268-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="36268-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="36268-133">See also</span></span>



[<span data-ttu-id="36268-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="36268-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="36268-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="36268-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="36268-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="36268-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="36268-137">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="36268-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

