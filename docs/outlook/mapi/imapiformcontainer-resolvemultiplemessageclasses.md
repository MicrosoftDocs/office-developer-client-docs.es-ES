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
ms.openlocfilehash: 002dbf3e898fc0388d535e3087d17ba37d63201e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577712"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a><span data-ttu-id="6c099-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="6c099-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="6c099-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c099-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c099-105">Se resuelve un grupo de clases de mensajes en sus formularios en un contenedor de formulario y devuelve una matriz de formulario objetos de información para los formularios.</span><span class="sxs-lookup"><span data-stu-id="6c099-105">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="6c099-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c099-106">Parameters</span></span>

 <span data-ttu-id="6c099-107">_pMsgClassArray_</span><span class="sxs-lookup"><span data-stu-id="6c099-107">_pMsgClassArray_</span></span>
  
> <span data-ttu-id="6c099-108">[entrada] Un puntero a una matriz que contiene los nombres de las clases de mensaje para resolver.</span><span class="sxs-lookup"><span data-stu-id="6c099-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span> <span data-ttu-id="6c099-109">Los nombres de clase de mensaje siempre son cadenas ANSI, Unicode nunca.</span><span class="sxs-lookup"><span data-stu-id="6c099-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="6c099-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c099-110">_ulFlags_</span></span>
  
> <span data-ttu-id="6c099-111">[entrada] Una máscara de bits de indicadores que controla cómo se resuelven las clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="6c099-111">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="6c099-112">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="6c099-112">The following flag can be set:</span></span>
    
<span data-ttu-id="6c099-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="6c099-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="6c099-114">Se deben resolver sólo cadenas de clase de mensaje que son una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="6c099-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="6c099-115">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="6c099-115">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="6c099-116">[out] Un puntero a un puntero a una matriz de objetos de información del formulario.</span><span class="sxs-lookup"><span data-stu-id="6c099-116">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="6c099-117">Si una aplicación cliente pasa NULL en el parámetro _pMsgClassArray_ , el parámetro _ppfrminfoarray_ contiene objetos de información de formulario para todos los formularios en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="6c099-117">If a client application passes NULL in the  _pMsgClassArray_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6c099-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c099-118">Return value</span></span>

<span data-ttu-id="6c099-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c099-119">S_OK</span></span> 
  
> <span data-ttu-id="6c099-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="6c099-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c099-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c099-121">Remarks</span></span>

<span data-ttu-id="6c099-122">Las aplicaciones cliente de llaman al método **IMAPIFormContainer::ResolveMultipleMessageClasses** para resolver un grupo de clases de mensajes a los formularios dentro de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="6c099-122">Client applications call the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="6c099-123">La matriz de objetos de información de formulario devueltos en el parámetro _ppfrminfoarray_ aún más proporciona acceso a cada una de las propiedades de los formularios.</span><span class="sxs-lookup"><span data-stu-id="6c099-123">The array of form information objects returned in the  _ppfrminfoarray_ parameter provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6c099-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="6c099-124">Notes to callers</span></span>

<span data-ttu-id="6c099-125">Para resolver un grupo de clases de mensajes a los formularios, pase una matriz de nombres de clase de mensaje que se va a resolver.</span><span class="sxs-lookup"><span data-stu-id="6c099-125">To resolve a group of message classes to forms, pass in an array of message class names to be resolved.</span></span> <span data-ttu-id="6c099-126">Para forzar la resolución para ser exactos (es decir, para evitar la resolución a una clase de la clase de mensaje base), el indicador MAPIFORM_EXACTMATCH se puede pasar en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="6c099-126">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="6c099-127">Si una clase de mensaje no se puede resolver a un formulario, se devuelve NULL para esa clase de mensaje en la matriz de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="6c099-127">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="6c099-128">Por lo tanto, incluso si el método devuelve S_OK, no se supone que se han resueltos correctamente todas las clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="6c099-128">Therefore, even if the method returns S_OK, do not assume that all message classes have been successfully resolved.</span></span> <span data-ttu-id="6c099-129">En su lugar, compruebe los valores en la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="6c099-129">Instead, check the values in the returned array.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6c099-130">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6c099-130">MFCMAPI reference</span></span>

<span data-ttu-id="6c099-131">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="6c099-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6c099-132">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="6c099-132">**File**</span></span>|<span data-ttu-id="6c099-133">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="6c099-133">**Function**</span></span>|<span data-ttu-id="6c099-134">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="6c099-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6c099-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6c099-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="6c099-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="6c099-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span></span>  <br/> |<span data-ttu-id="6c099-137">MFCMAPI usa el método **IMAPIFormContainer::ResolveMultipleMessageClasses** para buscar un formulario que está asociado a un conjunto de clases de mensajes.</span><span class="sxs-lookup"><span data-stu-id="6c099-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to locate a form that is associated with a set of message classes.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c099-138">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6c099-138">See also</span></span>



[<span data-ttu-id="6c099-139">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="6c099-139">IMAPIFormContainer::ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md)
  
[<span data-ttu-id="6c099-140">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c099-140">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="6c099-141">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="6c099-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

