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
ms.openlocfilehash: ec1933f80f211c7c381f9de6b15d414932b9a78e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414917"
---
# <a name="imapiformcontainercalcformpropset"></a><span data-ttu-id="97475-103">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="97475-103">IMAPIFormContainer::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="97475-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97475-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97475-105">Devuelve una matriz de las propiedades usadas por todos los formularios instalados en un contenedor de formularios.</span><span class="sxs-lookup"><span data-stu-id="97475-105">Returns an array of the properties used by all forms installed in a form container.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="97475-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97475-106">Parameters</span></span>

 <span data-ttu-id="97475-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="97475-107">_ulFlags_</span></span>
  
> <span data-ttu-id="97475-108">[entrada] Máscara de bits de marcas que controla cómo se devuelve la matriz de propiedades en el parámetro _ppResults._</span><span class="sxs-lookup"><span data-stu-id="97475-108">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="97475-109">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="97475-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="97475-110">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="97475-110">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="97475-111">La matriz devuelta contiene la intersección de las propiedades de los formularios.</span><span class="sxs-lookup"><span data-stu-id="97475-111">The returned array contains the intersection of the forms' properties.</span></span>
    
<span data-ttu-id="97475-112">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="97475-112">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="97475-113">La matriz devuelta contiene la unión de las propiedades de los formularios.</span><span class="sxs-lookup"><span data-stu-id="97475-113">The returned array contains the union of the forms' properties.</span></span>
    
<span data-ttu-id="97475-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="97475-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="97475-115">Las cadenas devueltas en la matriz están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="97475-115">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="97475-116">Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="97475-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="97475-117">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="97475-117">_ppResults_</span></span>
  
> <span data-ttu-id="97475-118">[salida] Puntero a un puntero a la estructura [SMAPIFormPropArray](smapiformproparray.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="97475-118">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> <span data-ttu-id="97475-119">Esta estructura contiene todas las propiedades usadas por los formularios instalados.</span><span class="sxs-lookup"><span data-stu-id="97475-119">This structure contains all properties used by the installed forms.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="97475-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97475-120">Return value</span></span>

<span data-ttu-id="97475-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="97475-121">S_OK</span></span> 
  
> <span data-ttu-id="97475-122">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="97475-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="97475-123">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="97475-123">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="97475-124">Se estableció MAPI_UNICODE marca y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="97475-124">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="97475-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97475-125">Remarks</span></span>

<span data-ttu-id="97475-126">Las aplicaciones cliente llaman al método **IMAPIFormContainer::CalcFormPropSet** para obtener una matriz de propiedades usadas por todos los formularios instalados en un contenedor de formularios.</span><span class="sxs-lookup"><span data-stu-id="97475-126">Client applications call the **IMAPIFormContainer::CalcFormPropSet** method to obtain an array of properties used by all forms installed in a form container.</span></span> <span data-ttu-id="97475-127">**IMAPIFormContainer::CalcFormPropSet** funciona como el método [IMAPIFormMgr::CalcFormPropSet,](imapiformmgr-calcformpropset.md) excepto que funciona en todos los formularios registrados en un contenedor determinado.</span><span class="sxs-lookup"><span data-stu-id="97475-127">**IMAPIFormContainer::CalcFormPropSet** works like the [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) method, except that it operates on every form registered in a particular container.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="97475-128">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="97475-128">Notes to implementers</span></span>

<span data-ttu-id="97475-129">Los proveedores de bibliotecas de formularios que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE se pasa.</span><span class="sxs-lookup"><span data-stu-id="97475-129">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="97475-130">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="97475-130">Notes to callers</span></span>

 <span data-ttu-id="97475-131">**IMAPIFormContainer::CalcFormPropSet** toma una intersección o una unión de los conjuntos de propiedades de los formularios, según la marca establecida en el parámetro  _ulFlags,_ y devuelve una estructura **SMAPIFormPropArray** que contiene el grupo de propiedades resultante.</span><span class="sxs-lookup"><span data-stu-id="97475-131">**IMAPIFormContainer::CalcFormPropSet** takes either an intersection or a union of the forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
<span data-ttu-id="97475-132">Si un cliente pasa la marca MAPI_UNICODE en  _ulFlags_, todas las cadenas devueltas son Unicode.</span><span class="sxs-lookup"><span data-stu-id="97475-132">If a client passes the MAPI_UNICODE flag in  _ulFlags_, all returned strings are Unicode.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="97475-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="97475-133">See also</span></span>



[<span data-ttu-id="97475-134">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="97475-134">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
  
[<span data-ttu-id="97475-135">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="97475-135">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="97475-136">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="97475-136">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

