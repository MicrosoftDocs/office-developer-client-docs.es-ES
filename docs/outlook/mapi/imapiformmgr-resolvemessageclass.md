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
ms.openlocfilehash: a84698ccc132c750cbd071c05160117c40e352a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817341"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="7493d-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="7493d-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="7493d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7493d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7493d-105">Una clase de mensaje se resuelve en su formulario dentro de un contenedor de formulario y devuelve un objeto de información de formulario para ese formulario.</span><span class="sxs-lookup"><span data-stu-id="7493d-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="7493d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7493d-106">Parameters</span></span>

 <span data-ttu-id="7493d-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="7493d-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="7493d-108">[entrada] Una cadena que da nombre a la clase de mensaje que se resuelve.</span><span class="sxs-lookup"><span data-stu-id="7493d-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="7493d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7493d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="7493d-110">[entrada] Una máscara de bits de indicadores que controla cómo se resuelve la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="7493d-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="7493d-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="7493d-111">The following flag can be set:</span></span>
    
<span data-ttu-id="7493d-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="7493d-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="7493d-113">Se deben resolver sólo cadenas de clase de mensaje que son una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="7493d-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="7493d-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="7493d-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="7493d-115">[entrada] Un puntero a la carpeta que contiene el mensaje que se resuelve.</span><span class="sxs-lookup"><span data-stu-id="7493d-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="7493d-116">El parámetro _pFolderFocus_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="7493d-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="7493d-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="7493d-117">_ppResult_</span></span>
  
> <span data-ttu-id="7493d-118">[out] Un puntero a un puntero a un objeto de información de formulario devuelto.</span><span class="sxs-lookup"><span data-stu-id="7493d-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7493d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7493d-119">Return value</span></span>

<span data-ttu-id="7493d-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="7493d-120">S_OK</span></span> 
  
> <span data-ttu-id="7493d-121">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="7493d-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="7493d-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7493d-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7493d-123">La clase de mensaje que se pasa en el parámetro _szMsgClass_ no coincide con la clase de mensaje para cualquier formulario en la biblioteca de formularios.</span><span class="sxs-lookup"><span data-stu-id="7493d-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7493d-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7493d-124">Remarks</span></span>

<span data-ttu-id="7493d-125">Visores de formulario llaman al método **IMAPIFormMgr::ResolveMessageClass** para resolver una clase de mensaje para su formulario dentro de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="7493d-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="7493d-126">El objeto de información de formulario devuelto en el parámetro _ppResult_ aún más proporciona acceso a las propiedades del formulario que tiene la clase de mensaje determinado.</span><span class="sxs-lookup"><span data-stu-id="7493d-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7493d-127">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="7493d-127">Notes to callers</span></span>

<span data-ttu-id="7493d-128">Para resolver una clase de mensaje a un formulario, se pasa un visor de formulario en el nombre de la clase de mensaje para que se resuelvan, como " `IPM.HelpDesk.Software`".</span><span class="sxs-lookup"><span data-stu-id="7493d-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="7493d-129">Para forzar la resolución para ser exactos (es decir, para evitar la resolución a una clase base de la clase de mensaje cuando un formulario que coincide exactamente server no está disponible), el indicador MAPIFORM_EXACTMATCH se puede pasar en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="7493d-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="7493d-130">Si el parámetro _pFolderFocus_ es NULL, el proceso de resolución de la clase de mensaje no busca en un contenedor de carpeta.</span><span class="sxs-lookup"><span data-stu-id="7493d-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="7493d-131">El orden de los contenedores que desea buscado depende de la implementación del proveedor de la biblioteca de formulario.</span><span class="sxs-lookup"><span data-stu-id="7493d-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="7493d-132">El proveedor de biblioteca del formulario predeterminado busca en primer lugar el contenedor local y, a continuación, el contenedor de la carpeta de la carpeta en el pasado, el contenedor de formularios personal y, por último, el contenedor de la organización.</span><span class="sxs-lookup"><span data-stu-id="7493d-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="7493d-133">Los nombres de clase de mensaje siempre son cadenas ANSI, Unicode nunca.</span><span class="sxs-lookup"><span data-stu-id="7493d-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="7493d-134">Se devuelve el identificador de clase para la clase de mensaje resuelto como parte del objeto de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="7493d-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="7493d-135">Un visor de formulario no debe trabajar en la suposición de que existe el identificador de clase en la biblioteca OLE hasta después de que el Visor de formulario ha llamado al método [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) o el método [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) .</span><span class="sxs-lookup"><span data-stu-id="7493d-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7493d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="7493d-136">See also</span></span>



[<span data-ttu-id="7493d-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7493d-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="7493d-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="7493d-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="7493d-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="7493d-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="7493d-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7493d-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

