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
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="d6a25-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="d6a25-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="d6a25-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6a25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6a25-105">Devuelve un puntero a todo el conjunto de verbos que usa un formulario.</span><span class="sxs-lookup"><span data-stu-id="d6a25-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="d6a25-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="d6a25-106">Parameters</span></span>

 <span data-ttu-id="d6a25-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6a25-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d6a25-108">[entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="d6a25-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="d6a25-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="d6a25-109">The following flag can be set:</span></span>
    
<span data-ttu-id="d6a25-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d6a25-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d6a25-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d6a25-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="d6a25-112">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d6a25-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d6a25-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="d6a25-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="d6a25-114">[out] Un puntero a un puntero a la estructura [SMAPIVerbArray](smapiverbarray.md) devuelta que contiene los verbos del formulario.</span><span class="sxs-lookup"><span data-stu-id="d6a25-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d6a25-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6a25-115">Return value</span></span>

<span data-ttu-id="d6a25-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6a25-116">S_OK</span></span> 
  
> <span data-ttu-id="d6a25-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="d6a25-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d6a25-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d6a25-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d6a25-119">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="d6a25-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d6a25-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d6a25-120">Remarks</span></span>

<span data-ttu-id="d6a25-121">Las aplicaciones cliente de llaman al método **IMAPIFormInfo::CalcVerbSet** para obtener un puntero al conjunto de verbos que utiliza un formulario.</span><span class="sxs-lookup"><span data-stu-id="d6a25-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="d6a25-122">En la estructura de **SMAPIVerbArray** devuelta en el parámetro _ppMAPIVerbArray_ , se devuelven los verbos en orden de número de índice; índice de cada verbo se encuentra en su miembro de **lVerb** .</span><span class="sxs-lookup"><span data-stu-id="d6a25-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="d6a25-123">Aplicaciones cliente pueden utilizar la matriz verbo para crear menús, ocultar o mostrar botones y así sucesivamente dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="d6a25-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d6a25-124">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d6a25-124">MFCMAPI reference</span></span>

<span data-ttu-id="d6a25-125">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d6a25-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d6a25-126">**File**</span><span class="sxs-lookup"><span data-stu-id="d6a25-126">**File**</span></span>|<span data-ttu-id="d6a25-127">**Función**</span><span class="sxs-lookup"><span data-stu-id="d6a25-127">**Function**</span></span>|<span data-ttu-id="d6a25-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="d6a25-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d6a25-129">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="d6a25-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="d6a25-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="d6a25-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="d6a25-131">MFCMAPI usa el método **IMAPIFormInfo::CalcVerbSet** al escribir los resultados de la depuración de objetos de información del formulario.</span><span class="sxs-lookup"><span data-stu-id="d6a25-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6a25-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6a25-132">See also</span></span>



[<span data-ttu-id="d6a25-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="d6a25-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="d6a25-134">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d6a25-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="d6a25-135">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="d6a25-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

