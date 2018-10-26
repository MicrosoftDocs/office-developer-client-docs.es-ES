---
title: IMAPIFormInfoCalcFormPropSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcFormPropSet
api_type:
- COM
ms.assetid: cc3ffb8d-9cc4-47d3-9aa9-02c3a5b7775c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7d0c044caf430c944d8912d050e4dbaba659c8b5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582500"
---
# <a name="imapiforminfocalcformpropset"></a><span data-ttu-id="af8f9-103">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="af8f9-103">IMAPIFormInfo::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="af8f9-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af8f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af8f9-105">Devuelve un puntero a todo el conjunto de propiedades que utiliza un formulario.</span><span class="sxs-lookup"><span data-stu-id="af8f9-105">Returns a pointer to the complete set of properties that a form uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="af8f9-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="af8f9-106">Parameters</span></span>

 <span data-ttu-id="af8f9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="af8f9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="af8f9-108">[entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="af8f9-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="af8f9-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="af8f9-109">The following flag can be set:</span></span>
    
<span data-ttu-id="af8f9-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="af8f9-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="af8f9-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="af8f9-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="af8f9-112">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="af8f9-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="af8f9-113">_ppFormPropArray_</span><span class="sxs-lookup"><span data-stu-id="af8f9-113">_ppFormPropArray_</span></span>
  
> <span data-ttu-id="af8f9-114">[out] Un puntero a un puntero a la estructura [SMAPIFormPropArray](smapiformproparray.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="af8f9-114">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="af8f9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af8f9-115">Return value</span></span>

<span data-ttu-id="af8f9-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="af8f9-116">S_OK</span></span> 
  
> <span data-ttu-id="af8f9-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="af8f9-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="af8f9-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="af8f9-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="af8f9-119">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="af8f9-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="af8f9-120">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="af8f9-120">MFCMAPI reference</span></span>

<span data-ttu-id="af8f9-121">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="af8f9-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="af8f9-122">**File**</span><span class="sxs-lookup"><span data-stu-id="af8f9-122">**File**</span></span>|<span data-ttu-id="af8f9-123">**Función**</span><span class="sxs-lookup"><span data-stu-id="af8f9-123">**Function**</span></span>|<span data-ttu-id="af8f9-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="af8f9-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="af8f9-125">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="af8f9-125">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="af8f9-126">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="af8f9-126">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="af8f9-127">MFCMAPI usa el método **IMAPIFormInfo::CalcFormPropSet** al escribir los resultados de la depuración de objetos de información del formulario.</span><span class="sxs-lookup"><span data-stu-id="af8f9-127">MFCMAPI uses the **IMAPIFormInfo::CalcFormPropSet** method when writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af8f9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="af8f9-128">See also</span></span>



[<span data-ttu-id="af8f9-129">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="af8f9-129">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="af8f9-130">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="af8f9-130">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="af8f9-131">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="af8f9-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

