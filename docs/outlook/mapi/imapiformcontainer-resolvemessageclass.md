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
ms.openlocfilehash: c0954d6f8b14b4088ece2ac276b045b6c163ed98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342164"
---
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="ded3a-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="ded3a-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="ded3a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ded3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ded3a-105">Resuelve una clase de mensaje en su formulario en un contenedor de formularios y devuelve un objeto de información de formulario para ese formulario.</span><span class="sxs-lookup"><span data-stu-id="ded3a-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="ded3a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ded3a-106">Parameters</span></span>

 <span data-ttu-id="ded3a-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="ded3a-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="ded3a-108">a Una cadena que asigna un nombre a la clase de mensaje que se está resolviendo.</span><span class="sxs-lookup"><span data-stu-id="ded3a-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="ded3a-109">Los nombres de clase de mensaje son siempre cadenas ANSI, nunca Unicode.</span><span class="sxs-lookup"><span data-stu-id="ded3a-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="ded3a-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ded3a-110">_ulFlags_</span></span>
  
> <span data-ttu-id="ded3a-111">a Máscara de máscara de marcadores que controla cómo se resuelve la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ded3a-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="ded3a-112">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="ded3a-112">The following flag can be set:</span></span>
    
<span data-ttu-id="ded3a-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="ded3a-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="ded3a-114">Solo se deben resolver las cadenas de clase de mensaje que sean una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="ded3a-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="ded3a-115">_ppforminfo_</span><span class="sxs-lookup"><span data-stu-id="ded3a-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="ded3a-116">contempla Un puntero a un puntero al objeto de información del formulario devuelto.</span><span class="sxs-lookup"><span data-stu-id="ded3a-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ded3a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ded3a-117">Return value</span></span>

<span data-ttu-id="ded3a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ded3a-118">S_OK</span></span> 
  
> <span data-ttu-id="ded3a-119">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="ded3a-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ded3a-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ded3a-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ded3a-121">La clase de mensaje pasada en el parámetro _szMessageClass_ no coincide con la clase de mensaje para ningún formulario del contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="ded3a-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ded3a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ded3a-122">Remarks</span></span>

<span data-ttu-id="ded3a-123">Las aplicaciones cliente llaman al método **IMAPIFormContainer:: ResolveMessageClass** para resolver una clase de mensaje en un formulario dentro de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="ded3a-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="ded3a-124">El objeto de información de formulario devuelto en el parámetro _ppforminfo_ proporciona más acceso a las propiedades del formulario con la clase de mensaje determinada.</span><span class="sxs-lookup"><span data-stu-id="ded3a-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ded3a-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ded3a-125">Notes to callers</span></span>

<span data-ttu-id="ded3a-126">Para resolver una clase de mensaje en un formulario, pase el nombre de la clase de mensaje que se va a resolver ( `IPM.HelpDesk.Software`por ejemplo,).</span><span class="sxs-lookup"><span data-stu-id="ded3a-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="ded3a-127">Para forzar que la resolución sea exacta (es decir, para evitar la resolución en una clase base de la clase de mensaje), se puede pasar la marca MAPIFORM_EXACTMATCH en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="ded3a-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="ded3a-128">El identificador de clase de la clase de mensaje resuelta se devuelve como parte del objeto de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="ded3a-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="ded3a-129">No asuma que el identificador de clase existe en la biblioteca OLE hasta después de llamar al método [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) o [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) .</span><span class="sxs-lookup"><span data-stu-id="ded3a-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ded3a-130">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ded3a-130">MFCMAPI reference</span></span>

<span data-ttu-id="ded3a-131">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ded3a-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ded3a-132">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ded3a-132">**File**</span></span>|<span data-ttu-id="ded3a-133">**Función**</span><span class="sxs-lookup"><span data-stu-id="ded3a-133">**Function**</span></span>|<span data-ttu-id="ded3a-134">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ded3a-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ded3a-135">FormContainerDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="ded3a-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="ded3a-136">CFormContainerDlg:: OnResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="ded3a-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="ded3a-137">MFCMAPI usa el método **IMAPIFormContainer:: ResolveMessageClass** para buscar un formulario que esté asociado a una clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ded3a-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ded3a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ded3a-138">See also</span></span>



[<span data-ttu-id="ded3a-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ded3a-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="ded3a-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="ded3a-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="ded3a-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="ded3a-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="ded3a-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ded3a-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

