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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e5da9ffdd3021538ec814d1367cf1b06b49cfbc6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817284"
---
# <a name="imapiforminfocalcformpropset"></a><span data-ttu-id="489bc-103">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="489bc-103">IMAPIFormInfo::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="489bc-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="489bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="489bc-105">Devuelve un puntero a todo el conjunto de propiedades que utiliza un formulario.</span><span class="sxs-lookup"><span data-stu-id="489bc-105">Returns a pointer to the complete set of properties that a form uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="489bc-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="489bc-106">Parameters</span></span>

 <span data-ttu-id="489bc-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="489bc-107">_ulFlags_</span></span>
  
> <span data-ttu-id="489bc-108">[entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="489bc-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="489bc-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="489bc-109">The following flag can be set:</span></span>
    
<span data-ttu-id="489bc-110">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="489bc-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="489bc-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="489bc-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="489bc-112">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="489bc-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="489bc-113">_ppFormPropArray_</span><span class="sxs-lookup"><span data-stu-id="489bc-113">_ppFormPropArray_</span></span>
  
> <span data-ttu-id="489bc-114">[out] Un puntero a un puntero a la estructura [SMAPIFormPropArray](smapiformproparray.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="489bc-114">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="489bc-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="489bc-115">Return value</span></span>

<span data-ttu-id="489bc-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="489bc-116">S_OK</span></span> 
  
> <span data-ttu-id="489bc-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="489bc-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="489bc-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="489bc-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="489bc-119">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="489bc-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="489bc-120">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="489bc-120">MFCMAPI reference</span></span>

<span data-ttu-id="489bc-121">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="489bc-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="489bc-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="489bc-122">**File**</span></span>|<span data-ttu-id="489bc-123">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="489bc-123">**Function**</span></span>|<span data-ttu-id="489bc-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="489bc-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="489bc-125">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="489bc-125">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="489bc-126">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="489bc-126">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="489bc-127">MFCMAPI usa el método **IMAPIFormInfo::CalcFormPropSet** al escribir los resultados de la depuración de objetos de información del formulario.</span><span class="sxs-lookup"><span data-stu-id="489bc-127">MFCMAPI uses the **IMAPIFormInfo::CalcFormPropSet** method when writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="489bc-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="489bc-128">See also</span></span>



[<span data-ttu-id="489bc-129">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="489bc-129">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="489bc-130">IMAPIFormInfo: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="489bc-130">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="489bc-131">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="489bc-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

