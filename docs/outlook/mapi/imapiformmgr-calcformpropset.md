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
ms.openlocfilehash: bf072aba27c90b7cea80c464e17fafb47524b695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436429"
---
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="d9271-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="d9271-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="d9271-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9271-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9271-105">Devuelve una matriz de las propiedades que utiliza un grupo de formularios.</span><span class="sxs-lookup"><span data-stu-id="d9271-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="d9271-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d9271-106">Parameters</span></span>

 <span data-ttu-id="d9271-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="d9271-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="d9271-108">a Un puntero a una matriz de objetos de información de formulario que identifican los formularios para los que se devuelven propiedades.</span><span class="sxs-lookup"><span data-stu-id="d9271-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="d9271-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d9271-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d9271-110">a Máscara de máscara de marcadores que controla cómo se devuelve la matriz de propiedades en el parámetro _ppResults_ .</span><span class="sxs-lookup"><span data-stu-id="d9271-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="d9271-111">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d9271-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="d9271-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="d9271-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="d9271-113">La matriz devuelta contiene la intersección de las propiedades del formulario.</span><span class="sxs-lookup"><span data-stu-id="d9271-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="d9271-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="d9271-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="d9271-115">La matriz devuelta contiene la Unión de las propiedades del formulario.</span><span class="sxs-lookup"><span data-stu-id="d9271-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="d9271-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d9271-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d9271-117">Las cadenas devueltas en la matriz tienen formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d9271-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="d9271-118">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d9271-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d9271-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="d9271-119">_ppResults_</span></span>
  
> <span data-ttu-id="d9271-120">contempla Un puntero a un puntero a la estructura [SMAPIFormPropArray](smapiformproparray.md) devuelta, que contiene las propiedades que usan los formularios.</span><span class="sxs-lookup"><span data-stu-id="d9271-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d9271-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9271-121">Return value</span></span>

<span data-ttu-id="d9271-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9271-122">S_OK</span></span> 
  
> <span data-ttu-id="d9271-123">La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="d9271-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="d9271-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d9271-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d9271-125">Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="d9271-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9271-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d9271-126">Remarks</span></span>

<span data-ttu-id="d9271-127">Los visores de formularios llaman al método **IMAPIFormMgr:: CalcFormPropSet** para obtener una matriz de las propiedades que utiliza un grupo de formularios.</span><span class="sxs-lookup"><span data-stu-id="d9271-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="d9271-128"><b0>CalcFormPropSet</b0> toma una intersección o una Unión de los conjuntos de propiedades de estos formularios, en función del indicador establecido en el parámetro <b1>ulFlags</b1> , y devuelve una estructura <b2>SMAPIFormPropArray</b2> que contiene el grupo resultante del </a1>.</span><span class="sxs-lookup"><span data-stu-id="d9271-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d9271-129">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="d9271-129">Notes to implementers</span></span>

<span data-ttu-id="d9271-130">Si un visor de formularios pasa la marca MAPI_UNICODE en el parámetro _ulFlags_ , todas las cadenas deben devolverse como cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="d9271-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="d9271-131">Los proveedores de bibliotecas de formularios que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si se pasa MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d9271-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d9271-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="d9271-132">See also</span></span>



[<span data-ttu-id="d9271-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="d9271-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="d9271-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9271-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

