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
ms.openlocfilehash: 968be38e794793405aac15340a92ccd6d680498d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571699"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="a406e-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="a406e-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="a406e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a406e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a406e-105">Se resuelve un grupo de clases de mensajes en sus formularios dentro de un contenedor de formulario y devuelve una matriz de formulario objetos de información para los formularios.</span><span class="sxs-lookup"><span data-stu-id="a406e-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="a406e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a406e-106">Parameters</span></span>

 <span data-ttu-id="a406e-107">_pMsgClasses_</span><span class="sxs-lookup"><span data-stu-id="a406e-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="a406e-108">[entrada] Un puntero a una matriz que contiene los nombres de las clases de mensaje para resolver.</span><span class="sxs-lookup"><span data-stu-id="a406e-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="a406e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a406e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a406e-110">[entrada] Una máscara de bits de indicadores que controla cómo se resuelven las clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a406e-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="a406e-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="a406e-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a406e-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="a406e-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="a406e-113">Se deben resolver sólo cadenas de clase de mensaje que son una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="a406e-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="a406e-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="a406e-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="a406e-115">No incluya los formularios en caché.</span><span class="sxs-lookup"><span data-stu-id="a406e-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="a406e-116">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="a406e-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="a406e-117">[entrada] Un puntero a la carpeta que contiene el formulario se resuelve cuya clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a406e-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="a406e-118">El parámetro _pFolderFocus_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a406e-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="a406e-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="a406e-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="a406e-120">[out] Un puntero a un puntero a una matriz de objetos de información del formulario.</span><span class="sxs-lookup"><span data-stu-id="a406e-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="a406e-121">Si un visor de formulario pasa NULL en el parámetro _pMsgClasses_ , el parámetro _ppfrminfoarray_ contiene objetos de información de formulario para todos los formularios en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="a406e-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a406e-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a406e-122">Return value</span></span>

<span data-ttu-id="a406e-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="a406e-123">S_OK</span></span> 
  
> <span data-ttu-id="a406e-124">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="a406e-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a406e-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a406e-125">Remarks</span></span>

<span data-ttu-id="a406e-126">Visores de formulario llaman al método **IMAPIFormMgr::ResolveMultipleMessageClasses** para resolver un grupo de clases de mensajes a los formularios dentro de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="a406e-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="a406e-127">La matriz de objetos de información de formulario devueltos en _ppfrminfoarray_ aún más proporciona acceso a cada una de las propiedades de los formularios.</span><span class="sxs-lookup"><span data-stu-id="a406e-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a406e-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a406e-128">Notes to callers</span></span>

<span data-ttu-id="a406e-129">Para resolver un grupo de clases de mensajes a los formularios, un visor de formulario se pasa en una matriz de nombres de clase de mensaje que se va a resolver.</span><span class="sxs-lookup"><span data-stu-id="a406e-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="a406e-130">Para forzar la resolución para ser exactos (es decir, para evitar la resolución a una clase base de la clase de mensaje cuando un formulario que coincide exactamente server no está disponible) se puede pasar el indicador MAPIFORM_EXACTMATCH en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="a406e-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="a406e-131">Los nombres de clase de mensaje siempre son cadenas ANSI, Unicode nunca.</span><span class="sxs-lookup"><span data-stu-id="a406e-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="a406e-132">Si una clase de mensaje no se puede resolver a un formulario, se devuelve NULL para esa clase de mensaje en la matriz de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="a406e-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="a406e-133">Por lo tanto, incluso si el método devuelve S_OK, visores de formulario no deben trabajar en la suposición de que se han resueltos correctamente todas las clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a406e-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="a406e-134">En su lugar, los visores de formulario deben comprobar los valores de la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="a406e-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a406e-135">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a406e-135">See also</span></span>



[<span data-ttu-id="a406e-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="a406e-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="a406e-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a406e-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

