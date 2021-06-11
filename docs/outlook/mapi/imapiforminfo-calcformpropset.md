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
ms.openlocfilehash: 0b62c21348da71c1ee863f70d6e6a549a5d10003
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438074"
---
# <a name="imapiforminfocalcformpropset"></a><span data-ttu-id="2b967-103">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="2b967-103">IMAPIFormInfo::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="2b967-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b967-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b967-105">Devuelve un puntero al conjunto completo de propiedades que usa un formulario.</span><span class="sxs-lookup"><span data-stu-id="2b967-105">Returns a pointer to the complete set of properties that a form uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="2b967-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2b967-106">Parameters</span></span>

 <span data-ttu-id="2b967-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2b967-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2b967-108">[in] Máscara de bits de marcas que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="2b967-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="2b967-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="2b967-109">The following flag can be set:</span></span>
    
<span data-ttu-id="2b967-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2b967-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2b967-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="2b967-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="2b967-112">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="2b967-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="2b967-113">_ppFormPropArray_</span><span class="sxs-lookup"><span data-stu-id="2b967-113">_ppFormPropArray_</span></span>
  
> <span data-ttu-id="2b967-114">[salida] Puntero a un puntero a la estructura [SMAPIFormPropArray](smapiformproparray.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="2b967-114">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2b967-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b967-115">Return value</span></span>

<span data-ttu-id="2b967-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="2b967-116">S_OK</span></span> 
  
> <span data-ttu-id="2b967-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="2b967-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="2b967-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2b967-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2b967-119">La marca MAPI_UNICODE se estableció y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="2b967-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="2b967-120">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2b967-120">MFCMAPI reference</span></span>

<span data-ttu-id="2b967-121">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2b967-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2b967-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="2b967-122">**File**</span></span>|<span data-ttu-id="2b967-123">**Función**</span><span class="sxs-lookup"><span data-stu-id="2b967-123">**Function**</span></span>|<span data-ttu-id="2b967-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="2b967-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2b967-125">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="2b967-125">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="2b967-126">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="2b967-126">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="2b967-127">MFCMAPI usa el **método IMAPIFormInfo::CalcFormPropSet** al escribir resultados de depuración para objetos de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="2b967-127">MFCMAPI uses the **IMAPIFormInfo::CalcFormPropSet** method when writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b967-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b967-128">See also</span></span>



[<span data-ttu-id="2b967-129">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="2b967-129">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="2b967-130">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2b967-130">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="2b967-131">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="2b967-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

