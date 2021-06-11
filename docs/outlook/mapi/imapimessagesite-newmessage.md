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
ms.openlocfilehash: f51dd1fe533d0577996e6e1be185302f2dc972fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438774"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="41607-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="41607-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="41607-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41607-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41607-105">Crea un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="41607-105">Creates a new message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="41607-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="41607-106">Parameters</span></span>

 <span data-ttu-id="41607-107">_fComposeInFolder_</span><span class="sxs-lookup"><span data-stu-id="41607-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="41607-108">[in] Indica en qué carpeta se debe componer el mensaje.</span><span class="sxs-lookup"><span data-stu-id="41607-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="41607-109">Si la variable es FALSE, se omite el  _parámetro pFolderFocus_ y el visor de formularios puede redactar el mensaje en cualquier carpeta.</span><span class="sxs-lookup"><span data-stu-id="41607-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="41607-110">Si la variable es TRUE y NULL se pasa en el  _parámetro pFolderFocus,_ el mensaje se compone en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="41607-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="41607-111">Si la variable es TRUE y se pasa un valor que no es NULL en  _pFolderFocus_, el mensaje se compone en la carpeta señalada por  _pFolderFocus_.</span><span class="sxs-lookup"><span data-stu-id="41607-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="41607-112">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="41607-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="41607-113">[in] Puntero a la carpeta donde se crea el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="41607-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="41607-114">_pPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="41607-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="41607-115">[in] Puntero al objeto de formulario del nuevo formulario.</span><span class="sxs-lookup"><span data-stu-id="41607-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="41607-116">_ppMessage_</span><span class="sxs-lookup"><span data-stu-id="41607-116">_ppMessage_</span></span>
  
> <span data-ttu-id="41607-117">[salida] Puntero a un puntero al nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="41607-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="41607-118">_ppMessageSite_</span><span class="sxs-lookup"><span data-stu-id="41607-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="41607-119">[salida] Puntero a un puntero a un objeto de sitio de mensaje para el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="41607-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="41607-120">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="41607-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="41607-121">[salida] Puntero a un puntero a un contexto de vista adecuado para pasar a un nuevo formulario con el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="41607-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="41607-122">Si el formulario implementa su propio contexto de vista, se puede pasar NULL en el _parámetro ppViewContext._</span><span class="sxs-lookup"><span data-stu-id="41607-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="41607-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41607-123">Return value</span></span>

<span data-ttu-id="41607-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="41607-124">S_OK</span></span> 
  
> <span data-ttu-id="41607-125">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="41607-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41607-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="41607-126">Remarks</span></span>

<span data-ttu-id="41607-127">Los objetos Form llaman **al método IMAPIMessageSite::NewMessage** para crear un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="41607-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="41607-128">El formulario usa **NewMessage** para obtener un nuevo mensaje y el sitio de mensaje asociado desde su vista.</span><span class="sxs-lookup"><span data-stu-id="41607-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="41607-129">A continuación, puede modificar el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="41607-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="41607-130">También puede obtener un contexto de vista asociado pasando un valor que no sea NULL en el _parámetro ppViewContext._</span><span class="sxs-lookup"><span data-stu-id="41607-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="41607-131">Este contexto de vista se puede usar directamente o puede agregarse y pasarse al nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="41607-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="41607-132">Si se requiere una implementación completa, pase NULL en  _ppViewContext_.</span><span class="sxs-lookup"><span data-stu-id="41607-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="41607-133">Para obtener una lista de interfaces relacionadas con servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="41607-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="41607-134">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="41607-134">MFCMAPI reference</span></span>

<span data-ttu-id="41607-135">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="41607-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="41607-136">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="41607-136">**File**</span></span>|<span data-ttu-id="41607-137">**Función**</span><span class="sxs-lookup"><span data-stu-id="41607-137">**Function**</span></span>|<span data-ttu-id="41607-138">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="41607-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="41607-139">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="41607-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="41607-140">CMyMAPIFormViewer::NewMessage</span><span class="sxs-lookup"><span data-stu-id="41607-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="41607-141">MFCMAPI usa el método **IMAPIMessageSite::NewMessage** para crear un nuevo mensaje, crear una instancia de un nuevo visor de formularios y llamar a **SetPersist** para establecer el mensaje en el visor de formularios.</span><span class="sxs-lookup"><span data-stu-id="41607-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="41607-142">Por último, devuelve el visor de formularios como el sitio del mensaje.</span><span class="sxs-lookup"><span data-stu-id="41607-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41607-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="41607-143">See also</span></span>



[<span data-ttu-id="41607-144">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="41607-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="41607-145">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="41607-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="41607-146">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="41607-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="41607-147">Interfaces de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="41607-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

