---
title: IMAPIFormMgrCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CalcFormPropSet
api_type:
- COM
ms.assetid: ab302bfd-5cff-49b4-b0d2-308ae5af478d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5380b6541e609c17a9005c3390c6d5db06155306
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567247"
---
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="bb144-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="bb144-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="bb144-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb144-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb144-105">Devuelve una matriz de las propiedades que utiliza un grupo de formularios.</span><span class="sxs-lookup"><span data-stu-id="bb144-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="bb144-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb144-106">Parameters</span></span>

 <span data-ttu-id="bb144-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="bb144-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="bb144-108">[entrada] Un puntero a una matriz de objetos de información de formulario que identifican los formularios que se va a devolver propiedades.</span><span class="sxs-lookup"><span data-stu-id="bb144-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="bb144-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bb144-109">_ulFlags_</span></span>
  
> <span data-ttu-id="bb144-110">[entrada] Una máscara de bits de indicadores que controla cómo se devuelve la matriz de propiedad en el parámetro _ppResults_ .</span><span class="sxs-lookup"><span data-stu-id="bb144-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="bb144-111">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="bb144-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="bb144-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="bb144-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="bb144-113">La matriz devuelta contiene la intersección de las propiedades del formulario.</span><span class="sxs-lookup"><span data-stu-id="bb144-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="bb144-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="bb144-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="bb144-115">La matriz devuelta contiene la unión de las propiedades del formulario.</span><span class="sxs-lookup"><span data-stu-id="bb144-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="bb144-116">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="bb144-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bb144-117">Las cadenas devueltas en la matriz están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="bb144-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="bb144-118">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="bb144-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="bb144-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="bb144-119">_ppResults_</span></span>
  
> <span data-ttu-id="bb144-120">[out] Un puntero a un puntero a la estructura [SMAPIFormPropArray](smapiformproparray.md) devuelta, que contiene las propiedades que usan los formularios.</span><span class="sxs-lookup"><span data-stu-id="bb144-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bb144-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb144-121">Return value</span></span>

<span data-ttu-id="bb144-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb144-122">S_OK</span></span> 
  
> <span data-ttu-id="bb144-123">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="bb144-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="bb144-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="bb144-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="bb144-125">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="bb144-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb144-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb144-126">Remarks</span></span>

<span data-ttu-id="bb144-127">Visores de formulario llamar al método **IMAPIFormMgr::CalcFormPropSet** para obtener una matriz de las propiedades que utiliza un grupo de formularios.</span><span class="sxs-lookup"><span data-stu-id="bb144-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="bb144-128">**CalcFormPropSet** toma puede ser una intersección o una unión de propiedad estos formularios establece, según el indicador establecido en el parámetro _ulFlags_ y se devuelve una estructura **SMAPIFormPropArray** que contiene el grupo resultante de Propiedades.</span><span class="sxs-lookup"><span data-stu-id="bb144-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bb144-129">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="bb144-129">Notes to implementers</span></span>

<span data-ttu-id="bb144-130">Si un visor de formulario, pasa el indicador MAPI_UNICODE el parámetro _ulFlags_ , se deberían devolver todas las cadenas como cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="bb144-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="bb144-131">Proveedores de biblioteca de formulario que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si se pasa MAPI_UNICODE..</span><span class="sxs-lookup"><span data-stu-id="bb144-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bb144-132">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="bb144-132">See also</span></span>



[<span data-ttu-id="bb144-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="bb144-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="bb144-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb144-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

