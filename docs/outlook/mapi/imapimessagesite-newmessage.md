---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 133a2ae3896b9aaedb502cb77516040c53584882
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563740"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="ef49f-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="ef49f-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="ef49f-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef49f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef49f-105">Crea un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="ef49f-105">Creates a new message.</span></span>
  
```cpp
HRESULT NewMessage(
  ULONG fComposeInFolder,
  LPMAPIFOLDER pFolderFocus,
  LPPERSISTMESSAGE pPersistMessage,
  LPMESSAGE FAR * ppMessage,
  LPMAPIMESSAGESITE FAR * ppMessageSite,
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="ef49f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef49f-106">Parameters</span></span>

 <span data-ttu-id="ef49f-107">_fComposeInFolder_</span><span class="sxs-lookup"><span data-stu-id="ef49f-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="ef49f-108">[entrada] Indica en qué carpeta se debe estar compuestas por el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ef49f-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="ef49f-109">Si la variable es FALSE, se omite el parámetro _pFolderFocus_ y el Visor de formulario puede redactar el mensaje en cualquier carpeta.</span><span class="sxs-lookup"><span data-stu-id="ef49f-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="ef49f-110">Si la variable es TRUE y se pasa NULL en el parámetro _pFolderFocus_ , el mensaje se compone de la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="ef49f-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="ef49f-111">Si la variable es TRUE y se pasa un valor no nulo en _pFolderFocus_, el mensaje se compone en la carpeta indicada por _pFolderFocus_.</span><span class="sxs-lookup"><span data-stu-id="ef49f-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="ef49f-112">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="ef49f-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="ef49f-113">[entrada] Un puntero a la carpeta donde se crea el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="ef49f-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="ef49f-114">_pPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="ef49f-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="ef49f-115">[entrada] Un puntero al objeto de formulario para el nuevo formulario.</span><span class="sxs-lookup"><span data-stu-id="ef49f-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="ef49f-116">_ppMessage_</span><span class="sxs-lookup"><span data-stu-id="ef49f-116">_ppMessage_</span></span>
  
> <span data-ttu-id="ef49f-117">[out] Un puntero a un puntero al mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="ef49f-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="ef49f-118">_ppMessageSite_</span><span class="sxs-lookup"><span data-stu-id="ef49f-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="ef49f-119">[out] Un puntero a un puntero a un objeto de sitio de mensaje para el mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="ef49f-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="ef49f-120">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="ef49f-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="ef49f-121">[out] Un puntero a un puntero a un contexto de vista que es adecuado para pasar a un nuevo formulario con el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="ef49f-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="ef49f-122">Si el formulario implementa su propio contexto de vista, se puede pasar NULL en el parámetro _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="ef49f-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ef49f-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef49f-123">Return value</span></span>

<span data-ttu-id="ef49f-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef49f-124">S_OK</span></span> 
  
> <span data-ttu-id="ef49f-125">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="ef49f-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef49f-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ef49f-126">Remarks</span></span>

<span data-ttu-id="ef49f-127">Objetos de formulario llamar al método **IMAPIMessageSite::NewMessage** para crear un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="ef49f-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="ef49f-128">El formulario usa **NewMessage** para obtener un nuevo mensaje y el sitio de mensaje asociado desde su vista.</span><span class="sxs-lookup"><span data-stu-id="ef49f-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="ef49f-129">A continuación, puede modificar el mensaje de nuevo.</span><span class="sxs-lookup"><span data-stu-id="ef49f-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="ef49f-130">También puede obtener un contexto de la vista asociada al pasar un valor no nulo en el parámetro _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="ef49f-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="ef49f-131">En este contexto de vista se puede utilizar directamente, o puede ser agregado y se pasan al mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="ef49f-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="ef49f-132">Si se requiere una implementación completa, pase NULL en _ppViewContext_.</span><span class="sxs-lookup"><span data-stu-id="ef49f-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="ef49f-133">Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="ef49f-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ef49f-134">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ef49f-134">MFCMAPI reference</span></span>

<span data-ttu-id="ef49f-135">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ef49f-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ef49f-136">**File**</span><span class="sxs-lookup"><span data-stu-id="ef49f-136">**File**</span></span>|<span data-ttu-id="ef49f-137">**Función**</span><span class="sxs-lookup"><span data-stu-id="ef49f-137">**Function**</span></span>|<span data-ttu-id="ef49f-138">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ef49f-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef49f-139">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="ef49f-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="ef49f-140">CMyMAPIFormViewer::NewMessage</span><span class="sxs-lookup"><span data-stu-id="ef49f-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="ef49f-141">MFCMAPI usa el método **IMAPIMessageSite::NewMessage** para crear un nuevo mensaje, crear una instancia de un nuevo Visor de formulario y llame a **SetPersist** para establecer el mensaje en el Visor del formulario.</span><span class="sxs-lookup"><span data-stu-id="ef49f-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="ef49f-142">Por último, devuelve el Visor de formulario como el sitio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ef49f-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef49f-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef49f-143">See also</span></span>



[<span data-ttu-id="ef49f-144">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef49f-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="ef49f-145">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef49f-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="ef49f-146">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="ef49f-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="ef49f-147">Interfaces de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="ef49f-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

