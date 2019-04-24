---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342185"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a><span data-ttu-id="9b1a6-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="9b1a6-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="9b1a6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b1a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b1a6-105">Resuelve un grupo de clases de mensaje en sus formularios en un contenedor de formularios y devuelve una matriz de objetos de información de formulario para esos formularios.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-105">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="9b1a6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9b1a6-106">Parameters</span></span>

 <span data-ttu-id="9b1a6-107">_pMsgClassArray_</span><span class="sxs-lookup"><span data-stu-id="9b1a6-107">_pMsgClassArray_</span></span>
  
> <span data-ttu-id="9b1a6-108">a Un puntero a una matriz que contiene los nombres de las clases de mensaje que se van a resolver.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span> <span data-ttu-id="9b1a6-109">Los nombres de clase de mensaje son siempre cadenas ANSI, nunca Unicode.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="9b1a6-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9b1a6-110">_ulFlags_</span></span>
  
> <span data-ttu-id="9b1a6-111">a Máscara de máscara de marcadores que controla cómo se resuelven las clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-111">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="9b1a6-112">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="9b1a6-112">The following flag can be set:</span></span>
    
<span data-ttu-id="9b1a6-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="9b1a6-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="9b1a6-114">Solo se deben resolver las cadenas de clase de mensaje que sean una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="9b1a6-115">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="9b1a6-115">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="9b1a6-116">contempla Un puntero a un puntero a una matriz de objetos de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-116">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="9b1a6-117">Si una aplicación cliente pasa NULL en el parámetro _pMsgClassArray_ , el parámetro _ppfrminfoarray_ contiene objetos de información de formulario para todos los formularios del contenedor.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-117">If a client application passes NULL in the  _pMsgClassArray_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9b1a6-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b1a6-118">Return value</span></span>

<span data-ttu-id="9b1a6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b1a6-119">S_OK</span></span> 
  
> <span data-ttu-id="9b1a6-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b1a6-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b1a6-121">Remarks</span></span>

<span data-ttu-id="9b1a6-122">Las aplicaciones cliente llaman al método **IMAPIFormContainer:: ResolveMultipleMessageClasses** para resolver un grupo de clases de mensaje a los formularios dentro de un contenedor de formularios.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-122">Client applications call the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="9b1a6-123">La matriz de objetos de información de formulario devuelta en el parámetro _ppfrminfoarray_ proporciona más acceso a cada una de las propiedades de los formularios.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-123">The array of form information objects returned in the  _ppfrminfoarray_ parameter provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9b1a6-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="9b1a6-124">Notes to callers</span></span>

<span data-ttu-id="9b1a6-125">Para resolver un grupo de clases de mensaje a los formularios, pase una matriz de nombres de clase de mensaje para resolver.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-125">To resolve a group of message classes to forms, pass in an array of message class names to be resolved.</span></span> <span data-ttu-id="9b1a6-126">Para forzar que la resolución sea exacta (es decir, para evitar la resolución en una clase base de la clase de mensaje), se puede pasar la marca MAPIFORM_EXACTMATCH en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="9b1a6-126">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="9b1a6-127">Si una clase de mensaje no se puede resolver en un formulario, se devuelve NULL para dicha clase de mensaje en la matriz de información del formulario.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-127">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="9b1a6-128">Por lo tanto, incluso si el método devuelve S_OK, no asuma que todas las clases de mensaje se han resuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-128">Therefore, even if the method returns S_OK, do not assume that all message classes have been successfully resolved.</span></span> <span data-ttu-id="9b1a6-129">En su lugar, compruebe los valores de la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-129">Instead, check the values in the returned array.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9b1a6-130">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9b1a6-130">MFCMAPI reference</span></span>

<span data-ttu-id="9b1a6-131">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9b1a6-132">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="9b1a6-132">**File**</span></span>|<span data-ttu-id="9b1a6-133">**Función**</span><span class="sxs-lookup"><span data-stu-id="9b1a6-133">**Function**</span></span>|<span data-ttu-id="9b1a6-134">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="9b1a6-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9b1a6-135">FormContainerDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="9b1a6-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="9b1a6-136">CFormContainerDlg:: OnResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="9b1a6-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span></span>  <br/> |<span data-ttu-id="9b1a6-137">MFCMAPI usa el método **IMAPIFormContainer:: ResolveMultipleMessageClasses** para localizar un formulario que esté asociado a un conjunto de clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9b1a6-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to locate a form that is associated with a set of message classes.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b1a6-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b1a6-138">See also</span></span>



[<span data-ttu-id="9b1a6-139">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="9b1a6-139">IMAPIFormContainer::ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md)
  
[<span data-ttu-id="9b1a6-140">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b1a6-140">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="9b1a6-141">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="9b1a6-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

