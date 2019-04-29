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
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="dd167-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="dd167-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="dd167-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd167-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd167-105">Resuelve una clase de mensaje en su formulario dentro de un contenedor de formulario y devuelve un objeto de información de formulario para ese formulario.</span><span class="sxs-lookup"><span data-stu-id="dd167-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="dd167-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="dd167-106">Parameters</span></span>

 <span data-ttu-id="dd167-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="dd167-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="dd167-108">a Una cadena que asigna un nombre a la clase de mensaje que se está resolviendo.</span><span class="sxs-lookup"><span data-stu-id="dd167-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="dd167-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dd167-109">_ulFlags_</span></span>
  
> <span data-ttu-id="dd167-110">a Máscara de máscara de marcadores que controla cómo se resuelve la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd167-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="dd167-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="dd167-111">The following flag can be set:</span></span>
    
<span data-ttu-id="dd167-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="dd167-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="dd167-113">Solo se deben resolver las cadenas de clase de mensaje que sean una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="dd167-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="dd167-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="dd167-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="dd167-115">a Un puntero a la carpeta que contiene el mensaje que se está resolviendo.</span><span class="sxs-lookup"><span data-stu-id="dd167-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="dd167-116">El parámetro _pFolderFocus_ puede ser null.</span><span class="sxs-lookup"><span data-stu-id="dd167-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="dd167-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="dd167-117">_ppResult_</span></span>
  
> <span data-ttu-id="dd167-118">contempla Un puntero a un puntero a un objeto devuelto de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="dd167-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dd167-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd167-119">Return value</span></span>

<span data-ttu-id="dd167-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="dd167-120">S_OK</span></span> 
  
> <span data-ttu-id="dd167-121">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="dd167-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="dd167-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="dd167-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="dd167-123">La clase de mensaje pasada en el parámetro _szMsgClass_ no coincide con la clase de mensaje de ningún formulario de la biblioteca de formularios.</span><span class="sxs-lookup"><span data-stu-id="dd167-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dd167-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd167-124">Remarks</span></span>

<span data-ttu-id="dd167-125">Los visores de formularios llaman al método **IMAPIFormMgr:: ResolveMessageClass** para resolver una clase de mensaje para su formulario dentro de un contenedor de formularios.</span><span class="sxs-lookup"><span data-stu-id="dd167-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="dd167-126">El objeto de información de formulario devuelto en el parámetro _ppResult_ proporciona más acceso a las propiedades del formulario que tiene la clase de mensaje determinada.</span><span class="sxs-lookup"><span data-stu-id="dd167-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dd167-127">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="dd167-127">Notes to callers</span></span>

<span data-ttu-id="dd167-128">Para resolver una clase de mensaje en un formulario, un visor de formulario pasa el nombre de la clase de mensaje que se va a resolver `IPM.HelpDesk.Software`, como "".</span><span class="sxs-lookup"><span data-stu-id="dd167-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="dd167-129">Para forzar que la resolución sea exacta (es decir, para evitar la resolución en una clase base de la clase de mensaje cuando no está disponible un servidor de formularios que coincida exactamente), se puede pasar la marca MAPIFORM_EXACTMATCH en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="dd167-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="dd167-130">Si el parámetro _pFolderFocus_ es null, el proceso de resolución de la clase de mensaje no busca en un contenedor de carpetas.</span><span class="sxs-lookup"><span data-stu-id="dd167-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="dd167-131">El orden de los contenedores buscados depende de la implementación del proveedor de la biblioteca de formularios.</span><span class="sxs-lookup"><span data-stu-id="dd167-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="dd167-132">El proveedor de bibliotecas de formularios predeterminado busca primero en el contenedor local, luego en el contenedor de carpetas de la carpeta pasada, en el contenedor de formularios personales y, por último, en el contenedor de la organización.</span><span class="sxs-lookup"><span data-stu-id="dd167-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="dd167-133">Los nombres de clase de mensaje son siempre cadenas ANSI, nunca Unicode.</span><span class="sxs-lookup"><span data-stu-id="dd167-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="dd167-134">El identificador de clase de la clase de mensaje resuelta se devuelve como parte del objeto de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="dd167-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="dd167-135">Un visor de formularios no debe trabajar en caso de que el identificador de clase exista en la biblioteca OLE hasta que el visor de formulario haya llamado al método [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) o al método [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) .</span><span class="sxs-lookup"><span data-stu-id="dd167-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dd167-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="dd167-136">See also</span></span>



[<span data-ttu-id="dd167-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dd167-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="dd167-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="dd167-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="dd167-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="dd167-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="dd167-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dd167-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

