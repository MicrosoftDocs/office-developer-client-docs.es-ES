---
title: IMAPIFormMgrResolveMultipleMessageClasses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMultipleMessageClasses
api_type:
- COM
ms.assetid: d3cc6658-e46d-42dd-b1ac-65c88cfef8ca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 515061c6c208008c4752e5ff2f23933a4c259c00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428021"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="98f31-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="98f31-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="98f31-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98f31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98f31-105">Resuelve un grupo de clases de mensajes en sus formularios dentro de un contenedor de formularios y devuelve una matriz de objetos de información de formulario para esos formularios.</span><span class="sxs-lookup"><span data-stu-id="98f31-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="98f31-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98f31-106">Parameters</span></span>

 <span data-ttu-id="98f31-107">_pMsgClasses_</span><span class="sxs-lookup"><span data-stu-id="98f31-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="98f31-108">[entrada] Puntero a una matriz que contiene los nombres de las clases de mensaje que se resolverán.</span><span class="sxs-lookup"><span data-stu-id="98f31-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="98f31-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="98f31-109">_ulFlags_</span></span>
  
> <span data-ttu-id="98f31-110">[entrada] Máscara de bits de marcas que controla cómo se resuelven las clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="98f31-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="98f31-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="98f31-111">The following flag can be set:</span></span>
    
<span data-ttu-id="98f31-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="98f31-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="98f31-113">Solo deben resolverse las cadenas de clase de mensaje que sean una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="98f31-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="98f31-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="98f31-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="98f31-115">No incluya formularios almacenados en caché.</span><span class="sxs-lookup"><span data-stu-id="98f31-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="98f31-116">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="98f31-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="98f31-117">[entrada] Puntero a la carpeta que contiene el formulario cuya clase de mensaje se está resolviendo.</span><span class="sxs-lookup"><span data-stu-id="98f31-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="98f31-118">El  _parámetro pFolderFocus_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="98f31-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="98f31-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="98f31-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="98f31-120">[salida] Puntero a un puntero a una matriz de objetos de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="98f31-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="98f31-121">Si un visor de formularios pasa NULL en el parámetro  _pMsgClasses,_ el parámetro  _ppfrminfoarray_ contiene objetos de información de formulario para todos los formularios del contenedor.</span><span class="sxs-lookup"><span data-stu-id="98f31-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="98f31-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98f31-122">Return value</span></span>

<span data-ttu-id="98f31-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="98f31-123">S_OK</span></span> 
  
> <span data-ttu-id="98f31-124">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="98f31-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98f31-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98f31-125">Remarks</span></span>

<span data-ttu-id="98f31-126">Los visores de formularios llaman al método **IMAPIFormMgr::ResolveMultipleMessageClasses** para resolver un grupo de clases de mensajes en formularios dentro de un contenedor de formularios.</span><span class="sxs-lookup"><span data-stu-id="98f31-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="98f31-127">La matriz de objetos de información de formulario devueltos  _en ppfrminfoarray_ proporciona acceso adicional a cada una de las propiedades de los formularios.</span><span class="sxs-lookup"><span data-stu-id="98f31-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="98f31-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="98f31-128">Notes to callers</span></span>

<span data-ttu-id="98f31-129">Para resolver un grupo de clases de mensajes en formularios, un visor de formularios pasa una matriz de nombres de clase de mensaje que se resolverán.</span><span class="sxs-lookup"><span data-stu-id="98f31-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="98f31-130">Para forzar que la resolución sea exacta (es decir, para evitar la resolución a una clase base de la clase de mensaje cuando no hay disponible un servidor de formulario que coincida exactamente) se puede pasar la marca MAPIFORM_EXACTMATCH en el parámetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="98f31-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="98f31-131">Los nombres de clase de mensaje son siempre cadenas ANSI, nunca Unicode.</span><span class="sxs-lookup"><span data-stu-id="98f31-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="98f31-132">Si una clase de mensaje no se puede resolver en un formulario, se devuelve NULL para esa clase de mensaje en la matriz de información del formulario.</span><span class="sxs-lookup"><span data-stu-id="98f31-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="98f31-133">Por lo tanto, incluso si el método devuelve S_OK, los visores de formularios no deben trabajar en la suposición de que todas las clases de mensajes se han resuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="98f31-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="98f31-134">En su lugar, los visores de formularios deben comprobar los valores de la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="98f31-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98f31-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98f31-135">See also</span></span>



[<span data-ttu-id="98f31-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="98f31-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="98f31-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="98f31-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

