---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9c6a6d210230fc305aef46371c22f67b3d445a81
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576585"
---
# <a name="imapiformcontainercalcformpropset"></a><span data-ttu-id="d9f6d-103">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="d9f6d-103">IMAPIFormContainer::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="d9f6d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9f6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9f6d-105">Devuelve una matriz de las propiedades de todos los formularios instalados en un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="d9f6d-105">Returns an array of the properties used by all forms installed in a form container.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="d9f6d-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="d9f6d-106">Parameters</span></span>

 <span data-ttu-id="d9f6d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d9f6d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d9f6d-108">[entrada] Una máscara de bits de indicadores que controla cómo se devuelve la matriz de propiedad en el parámetro _ppResults_ .</span><span class="sxs-lookup"><span data-stu-id="d9f6d-108">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="d9f6d-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d9f6d-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="d9f6d-110">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="d9f6d-110">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="d9f6d-111">La matriz devuelta contiene la intersección de las propiedades de los formularios.</span><span class="sxs-lookup"><span data-stu-id="d9f6d-111">The returned array contains the intersection of the forms' properties.</span></span>
    
<span data-ttu-id="d9f6d-112">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="d9f6d-112">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="d9f6d-113">La matriz devuelta contiene la unión de las propiedades de los formularios.</span><span class="sxs-lookup"><span data-stu-id="d9f6d-113">The returned array contains the union of the forms' properties.</span></span>
    
<span data-ttu-id="d9f6d-114">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d9f6d-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d9f6d-115">Las cadenas devueltas en la matriz están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d9f6d-115">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="d9f6d-116">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d9f6d-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d9f6d-117">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="d9f6d-117">_ppResults_</span></span>
  
> <span data-ttu-id="d9f6d-118">[out] Un puntero a un puntero a la estructura [SMAPIFormPropArray](smapiformproparray.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="d9f6d-118">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> <span data-ttu-id="d9f6d-119">Esta estructura contiene todas las propiedades que se utilizan en los formularios instalados.</span><span class="sxs-lookup"><span data-stu-id="d9f6d-119">This structure contains all properties used by the installed forms.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d9f6d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9f6d-120">Return value</span></span>

<span data-ttu-id="d9f6d-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9f6d-121">S_OK</span></span> 
  
> <span data-ttu-id="d9f6d-122">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="d9f6d-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d9f6d-123">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d9f6d-123">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d9f6d-124">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="d9f6d-124">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9f6d-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d9f6d-125">Remarks</span></span>

<span data-ttu-id="d9f6d-126">Las aplicaciones cliente de llaman al método **IMAPIFormContainer::CalcFormPropSet** para obtener una matriz de propiedades que se usan por todos los formularios instalados en un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="d9f6d-126">Client applications call the **IMAPIFormContainer::CalcFormPropSet** method to obtain an array of properties used by all forms installed in a form container.</span></span> <span data-ttu-id="d9f6d-127">**IMAPIFormContainer::CalcFormPropSet** funciona como el método [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) , salvo que opera en cada formulario registrado en un contenedor determinado.</span><span class="sxs-lookup"><span data-stu-id="d9f6d-127">**IMAPIFormContainer::CalcFormPropSet** works like the [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) method, except that it operates on every form registered in a particular container.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d9f6d-128">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="d9f6d-128">Notes to implementers</span></span>

<span data-ttu-id="d9f6d-129">Proveedores de biblioteca de formulario que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si se pasa MAPI_UNICODE..</span><span class="sxs-lookup"><span data-stu-id="d9f6d-129">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="d9f6d-130">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d9f6d-130">Notes to callers</span></span>

 <span data-ttu-id="d9f6d-131">**IMAPIFormContainer::CalcFormPropSet** toma una intersección o una unión de conjuntos de propiedades de los formularios, dependiendo de la marca que se define en el parámetro _ulFlags_ , y devuelve una estructura **SMAPIFormPropArray** que contiene el grupo resultante de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d9f6d-131">**IMAPIFormContainer::CalcFormPropSet** takes either an intersection or a union of the forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
<span data-ttu-id="d9f6d-132">Si un cliente pasa el indicador MAPI_UNICODE _ulFlags_, todas las cadenas devueltas son Unicode.</span><span class="sxs-lookup"><span data-stu-id="d9f6d-132">If a client passes the MAPI_UNICODE flag in  _ulFlags_, all returned strings are Unicode.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d9f6d-133">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d9f6d-133">See also</span></span>



[<span data-ttu-id="d9f6d-134">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="d9f6d-134">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
  
[<span data-ttu-id="d9f6d-135">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="d9f6d-135">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="d9f6d-136">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9f6d-136">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

