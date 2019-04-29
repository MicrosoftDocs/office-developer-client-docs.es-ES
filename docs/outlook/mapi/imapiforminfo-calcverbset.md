---
title: IMAPIFormInfoCalcVerbSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: babff746af16d51ca154d049943f6be7e9fab589
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428784"
---
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="5d7ae-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="5d7ae-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="5d7ae-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d7ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d7ae-105">Devuelve un puntero al conjunto completo de verbos que utiliza un formulario.</span><span class="sxs-lookup"><span data-stu-id="5d7ae-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="5d7ae-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5d7ae-106">Parameters</span></span>

 <span data-ttu-id="5d7ae-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5d7ae-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5d7ae-108">a Máscara de máscara de marcadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="5d7ae-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="5d7ae-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="5d7ae-109">The following flag can be set:</span></span>
    
<span data-ttu-id="5d7ae-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5d7ae-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5d7ae-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="5d7ae-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="5d7ae-112">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="5d7ae-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="5d7ae-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="5d7ae-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="5d7ae-114">contempla Un puntero a un puntero a la estructura [SMAPIVerbArray](smapiverbarray.md) devuelta que contiene los verbos del formulario.</span><span class="sxs-lookup"><span data-stu-id="5d7ae-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5d7ae-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d7ae-115">Return value</span></span>

<span data-ttu-id="5d7ae-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5d7ae-116">S_OK</span></span> 
  
> <span data-ttu-id="5d7ae-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="5d7ae-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5d7ae-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5d7ae-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5d7ae-119">Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="5d7ae-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5d7ae-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d7ae-120">Remarks</span></span>

<span data-ttu-id="5d7ae-121">Las aplicaciones cliente llaman al método **IMAPIFormInfo:: CalcVerbSet** para obtener un puntero al conjunto de verbos utilizado por un formulario.</span><span class="sxs-lookup"><span data-stu-id="5d7ae-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="5d7ae-122">En la estructura **SMAPIVerbArray** devuelta en el parámetro _ppMAPIVerbArray_ , los verbos se devuelven en orden de número de índice; el índice de cada verbo se encuentra en su miembro **lVerb** .</span><span class="sxs-lookup"><span data-stu-id="5d7ae-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="5d7ae-123">Las aplicaciones cliente pueden usar la matriz de verbo para generar dinámicamente menús, ocultar o Mostrar botones, etc.</span><span class="sxs-lookup"><span data-stu-id="5d7ae-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5d7ae-124">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5d7ae-124">MFCMAPI reference</span></span>

<span data-ttu-id="5d7ae-125">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="5d7ae-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5d7ae-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="5d7ae-126">**File**</span></span>|<span data-ttu-id="5d7ae-127">**Función**</span><span class="sxs-lookup"><span data-stu-id="5d7ae-127">**Function**</span></span>|<span data-ttu-id="5d7ae-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="5d7ae-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5d7ae-129">MFCOutput. cpp</span><span class="sxs-lookup"><span data-stu-id="5d7ae-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="5d7ae-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="5d7ae-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="5d7ae-131">MFCMAPI usa el método **IMAPIFormInfo:: CalcVerbSet** al escribir el resultado de depuración para objetos de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="5d7ae-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d7ae-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="5d7ae-132">See also</span></span>



[<span data-ttu-id="5d7ae-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="5d7ae-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="5d7ae-134">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5d7ae-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="5d7ae-135">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="5d7ae-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

