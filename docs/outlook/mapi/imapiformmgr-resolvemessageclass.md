---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e99cff77fe872018722395c53c605e4d8fabfdde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426397"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="a614f-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="a614f-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="a614f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a614f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a614f-105">Resuelve una clase de mensaje en su formulario dentro de un contenedor de formularios y devuelve un objeto de información de formulario para ese formulario.</span><span class="sxs-lookup"><span data-stu-id="a614f-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="a614f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a614f-106">Parameters</span></span>

 <span data-ttu-id="a614f-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="a614f-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="a614f-108">[entrada] Cadena que nombra la clase de mensaje que se está resolviendo.</span><span class="sxs-lookup"><span data-stu-id="a614f-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="a614f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a614f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a614f-110">[entrada] Máscara de bits de marcas que controla cómo se resuelve la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a614f-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="a614f-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="a614f-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a614f-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="a614f-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="a614f-113">Solo deben resolverse las cadenas de clase de mensaje que sean una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="a614f-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="a614f-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="a614f-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="a614f-115">[entrada] Puntero a la carpeta que contiene el mensaje que se está resolviendo.</span><span class="sxs-lookup"><span data-stu-id="a614f-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="a614f-116">El  _parámetro pFolderFocus_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a614f-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="a614f-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="a614f-117">_ppResult_</span></span>
  
> <span data-ttu-id="a614f-118">[salida] Puntero a un puntero a un objeto de información de formulario devuelto.</span><span class="sxs-lookup"><span data-stu-id="a614f-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a614f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a614f-119">Return value</span></span>

<span data-ttu-id="a614f-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="a614f-120">S_OK</span></span> 
  
> <span data-ttu-id="a614f-121">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="a614f-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a614f-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a614f-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a614f-123">La clase de mensaje pasada en  _el parámetro szMsgClass_ no coincide con la clase de mensaje de ningún formulario de la biblioteca de formularios.</span><span class="sxs-lookup"><span data-stu-id="a614f-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a614f-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a614f-124">Remarks</span></span>

<span data-ttu-id="a614f-125">Los visores de formularios llaman al método **IMAPIFormMgr::ResolveMessageClass** para resolver una clase de mensaje en su formulario dentro de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="a614f-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="a614f-126">El objeto de información del formulario devuelto en el  _parámetro ppResult_ proporciona acceso adicional a las propiedades del formulario que tiene la clase de mensaje determinada.</span><span class="sxs-lookup"><span data-stu-id="a614f-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a614f-127">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a614f-127">Notes to callers</span></span>

<span data-ttu-id="a614f-128">Para resolver una clase de mensaje en un formulario, un visor de formularios pasa el nombre de la clase de mensaje que se va a resolver, como " `IPM.HelpDesk.Software` ".</span><span class="sxs-lookup"><span data-stu-id="a614f-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="a614f-129">Para forzar que la resolución sea exacta (es decir, para evitar la resolución a una clase base de la clase de mensaje cuando no hay disponible un servidor de formulario que coincida exactamente), se puede pasar la marca MAPIFORM_EXACTMATCH en el parámetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="a614f-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="a614f-130">Si el  _parámetro pFolderFocus_ es NULL, el proceso de resolución de clase de mensaje no busca en un contenedor de carpetas.</span><span class="sxs-lookup"><span data-stu-id="a614f-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="a614f-131">El orden de los contenedores buscados depende de la implementación del proveedor de bibliotecas de formularios.</span><span class="sxs-lookup"><span data-stu-id="a614f-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="a614f-132">El proveedor de bibliotecas de formularios predeterminado busca primero el contenedor local, después el contenedor de carpetas para la carpeta pasada, el contenedor de formularios personales y, por último, el contenedor de la organización.</span><span class="sxs-lookup"><span data-stu-id="a614f-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="a614f-133">Los nombres de clase de mensaje siempre son cadenas ANSI, nunca Unicode.</span><span class="sxs-lookup"><span data-stu-id="a614f-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="a614f-134">El identificador de clase de la clase de mensaje resuelto se devuelve como parte del objeto de información del formulario.</span><span class="sxs-lookup"><span data-stu-id="a614f-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="a614f-135">Un visor de formularios no debe funcionar en la suposición de que el identificador de clase existe en la biblioteca OLE hasta después de que el visor del formulario haya llamado al método [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) o al método [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md)</span><span class="sxs-lookup"><span data-stu-id="a614f-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a614f-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a614f-136">See also</span></span>



[<span data-ttu-id="a614f-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a614f-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="a614f-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="a614f-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="a614f-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="a614f-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="a614f-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a614f-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

