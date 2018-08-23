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
ms.openlocfilehash: db3cc987b20a76116f2591485f57afae017d3e15
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567716"
---
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="91616-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="91616-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="91616-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91616-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91616-105">Devuelve un puntero a todo el conjunto de verbos que usa un formulario.</span><span class="sxs-lookup"><span data-stu-id="91616-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="91616-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="91616-106">Parameters</span></span>

 <span data-ttu-id="91616-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="91616-107">_ulFlags_</span></span>
  
> <span data-ttu-id="91616-108">[entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="91616-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="91616-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="91616-109">The following flag can be set:</span></span>
    
<span data-ttu-id="91616-110">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="91616-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="91616-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="91616-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="91616-112">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="91616-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="91616-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="91616-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="91616-114">[out] Un puntero a un puntero a la estructura [SMAPIVerbArray](smapiverbarray.md) devuelta que contiene los verbos del formulario.</span><span class="sxs-lookup"><span data-stu-id="91616-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="91616-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91616-115">Return value</span></span>

<span data-ttu-id="91616-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="91616-116">S_OK</span></span> 
  
> <span data-ttu-id="91616-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="91616-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="91616-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="91616-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="91616-119">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="91616-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="91616-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="91616-120">Remarks</span></span>

<span data-ttu-id="91616-121">Las aplicaciones cliente de llaman al método **IMAPIFormInfo::CalcVerbSet** para obtener un puntero al conjunto de verbos que utiliza un formulario.</span><span class="sxs-lookup"><span data-stu-id="91616-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="91616-122">En la estructura de **SMAPIVerbArray** devuelta en el parámetro _ppMAPIVerbArray_ , se devuelven los verbos en orden de número de índice; índice de cada verbo se encuentra en su miembro de **lVerb** .</span><span class="sxs-lookup"><span data-stu-id="91616-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="91616-123">Aplicaciones cliente pueden utilizar la matriz verbo para crear menús, ocultar o mostrar botones y así sucesivamente dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="91616-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="91616-124">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="91616-124">MFCMAPI reference</span></span>

<span data-ttu-id="91616-125">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="91616-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="91616-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="91616-126">**File**</span></span>|<span data-ttu-id="91616-127">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="91616-127">**Function**</span></span>|<span data-ttu-id="91616-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="91616-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="91616-129">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="91616-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="91616-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="91616-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="91616-131">MFCMAPI usa el método **IMAPIFormInfo::CalcVerbSet** al escribir los resultados de la depuración de objetos de información del formulario.</span><span class="sxs-lookup"><span data-stu-id="91616-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91616-132">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="91616-132">See also</span></span>



[<span data-ttu-id="91616-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="91616-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="91616-134">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="91616-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="91616-135">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="91616-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

