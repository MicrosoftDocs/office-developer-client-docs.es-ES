---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: db4b8d99c960deb3de3d228b2bf9549738501bcc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576284"
---
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="bfdd9-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="bfdd9-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="bfdd9-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfdd9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfdd9-105">Una clase de mensaje se resuelve en su formulario en un contenedor de formulario y devuelve un objeto de información de formulario para ese formulario.</span><span class="sxs-lookup"><span data-stu-id="bfdd9-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="bfdd9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfdd9-106">Parameters</span></span>

 <span data-ttu-id="bfdd9-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="bfdd9-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="bfdd9-108">[entrada] Una cadena que da nombre a la clase de mensaje que se resuelve.</span><span class="sxs-lookup"><span data-stu-id="bfdd9-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="bfdd9-109">Los nombres de clase de mensaje siempre son cadenas ANSI, Unicode nunca.</span><span class="sxs-lookup"><span data-stu-id="bfdd9-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="bfdd9-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bfdd9-110">_ulFlags_</span></span>
  
> <span data-ttu-id="bfdd9-111">[entrada] Una máscara de bits de indicadores que controla cómo se resuelve la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="bfdd9-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="bfdd9-112">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="bfdd9-112">The following flag can be set:</span></span>
    
<span data-ttu-id="bfdd9-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="bfdd9-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="bfdd9-114">Se deben resolver sólo cadenas de clase de mensaje que son una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="bfdd9-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="bfdd9-115">_ppforminfo_</span><span class="sxs-lookup"><span data-stu-id="bfdd9-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="bfdd9-116">[out] Un puntero a un puntero al objeto de información de formulario devuelto.</span><span class="sxs-lookup"><span data-stu-id="bfdd9-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bfdd9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfdd9-117">Return value</span></span>

<span data-ttu-id="bfdd9-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="bfdd9-118">S_OK</span></span> 
  
> <span data-ttu-id="bfdd9-119">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="bfdd9-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="bfdd9-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="bfdd9-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="bfdd9-121">La clase de mensaje que se pasa en el parámetro _szMessageClass_ no coincide con la clase de mensaje para cualquier formulario en el contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="bfdd9-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bfdd9-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bfdd9-122">Remarks</span></span>

<span data-ttu-id="bfdd9-123">Las aplicaciones cliente de llaman al método **IMAPIFormContainer::ResolveMessageClass** para resolver una clase de mensaje a un formulario dentro de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="bfdd9-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="bfdd9-124">El objeto de información de formulario devuelto en el parámetro _ppforminfo_ aún más proporciona acceso a las propiedades del formulario con la clase de mensaje determinado.</span><span class="sxs-lookup"><span data-stu-id="bfdd9-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bfdd9-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="bfdd9-125">Notes to callers</span></span>

<span data-ttu-id="bfdd9-126">Para resolver una clase de mensaje a un formulario, pase el nombre de la clase de mensaje que se va a resolver (por ejemplo, `IPM.HelpDesk.Software`).</span><span class="sxs-lookup"><span data-stu-id="bfdd9-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="bfdd9-127">Para forzar la resolución para ser exactos (es decir, para evitar la resolución a una clase de la clase de mensaje base), el indicador MAPIFORM_EXACTMATCH se puede pasar en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="bfdd9-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="bfdd9-128">Se devuelve el identificador de clase para la clase de mensaje resuelto como parte del objeto de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="bfdd9-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="bfdd9-129">No se supone que existe el identificador de clase en la biblioteca OLE hasta después de llamar a los métodos [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) o [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) .</span><span class="sxs-lookup"><span data-stu-id="bfdd9-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bfdd9-130">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bfdd9-130">MFCMAPI reference</span></span>

<span data-ttu-id="bfdd9-131">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="bfdd9-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bfdd9-132">**File**</span><span class="sxs-lookup"><span data-stu-id="bfdd9-132">**File**</span></span>|<span data-ttu-id="bfdd9-133">**Función**</span><span class="sxs-lookup"><span data-stu-id="bfdd9-133">**Function**</span></span>|<span data-ttu-id="bfdd9-134">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="bfdd9-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bfdd9-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="bfdd9-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="bfdd9-136">CFormContainerDlg::OnResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="bfdd9-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="bfdd9-137">MFCMAPI utiliza el método **IMAPIFormContainer::ResolveMessageClass** para localizar un formulario que está asociado a una clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="bfdd9-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bfdd9-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfdd9-138">See also</span></span>



[<span data-ttu-id="bfdd9-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bfdd9-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="bfdd9-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="bfdd9-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="bfdd9-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="bfdd9-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="bfdd9-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bfdd9-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

