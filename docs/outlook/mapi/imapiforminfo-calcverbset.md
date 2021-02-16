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
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="edbc8-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="edbc8-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="edbc8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edbc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edbc8-105">Devuelve un puntero al conjunto completo de verbos que usa un formulario.</span><span class="sxs-lookup"><span data-stu-id="edbc8-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="edbc8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edbc8-106">Parameters</span></span>

 <span data-ttu-id="edbc8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="edbc8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="edbc8-108">[entrada] Máscara de bits de marcas que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="edbc8-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="edbc8-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="edbc8-109">The following flag can be set:</span></span>
    
<span data-ttu-id="edbc8-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="edbc8-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="edbc8-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="edbc8-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="edbc8-112">Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="edbc8-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="edbc8-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="edbc8-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="edbc8-114">[salida] Puntero a un puntero a la estructura [SMAPIVerbArray](smapiverbarray.md) devuelta que contiene los verbos del formulario.</span><span class="sxs-lookup"><span data-stu-id="edbc8-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="edbc8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edbc8-115">Return value</span></span>

<span data-ttu-id="edbc8-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="edbc8-116">S_OK</span></span> 
  
> <span data-ttu-id="edbc8-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="edbc8-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="edbc8-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="edbc8-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="edbc8-119">Se estableció MAPI_UNICODE marca y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="edbc8-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="edbc8-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edbc8-120">Remarks</span></span>

<span data-ttu-id="edbc8-121">Las aplicaciones cliente llaman al método **IMAPIFormInfo::CalcVerbSet** para obtener un puntero al conjunto de verbos usado por un formulario.</span><span class="sxs-lookup"><span data-stu-id="edbc8-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="edbc8-122">En la **estructura SMAPIVerbArray** devuelta en el parámetro _ppMAPIVerbArray,_ los verbos se devuelven en orden de número de índice; el índice de cada verbo se encuentra en su **miembro lVerb.**</span><span class="sxs-lookup"><span data-stu-id="edbc8-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="edbc8-123">Las aplicaciones cliente pueden usar la matriz de verbos para crear menús dinámicamente, ocultar o mostrar botones, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="edbc8-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="edbc8-124">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="edbc8-124">MFCMAPI reference</span></span>

<span data-ttu-id="edbc8-125">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="edbc8-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="edbc8-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="edbc8-126">**File**</span></span>|<span data-ttu-id="edbc8-127">**Función**</span><span class="sxs-lookup"><span data-stu-id="edbc8-127">**Function**</span></span>|<span data-ttu-id="edbc8-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="edbc8-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="edbc8-129">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="edbc8-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="edbc8-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="edbc8-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="edbc8-131">MFCMAPI usa el **método IMAPIFormInfo::CalcVerbSet** mientras escribe resultados de depuración para objetos de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="edbc8-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="edbc8-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="edbc8-132">See also</span></span>



[<span data-ttu-id="edbc8-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="edbc8-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="edbc8-134">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="edbc8-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="edbc8-135">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="edbc8-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

