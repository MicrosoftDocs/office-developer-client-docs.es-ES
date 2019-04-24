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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321458"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="f081c-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="f081c-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="f081c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f081c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f081c-105">Crea un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="f081c-105">Creates a new message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="f081c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f081c-106">Parameters</span></span>

 <span data-ttu-id="f081c-107">_fComposeInFolder_</span><span class="sxs-lookup"><span data-stu-id="f081c-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="f081c-108">a Indica en qué carpeta debe componerse el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f081c-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="f081c-109">Si la variable es FALSE, se omite el parámetro _pFolderFocus_ y el visor del formulario puede redactar el mensaje en cualquier carpeta.</span><span class="sxs-lookup"><span data-stu-id="f081c-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="f081c-110">Si la variable es TRUE y NULL se pasa en el parámetro _pFolderFocus_ , el mensaje se crea en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="f081c-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="f081c-111">Si la variable es TRUE y se pasa un valor no NULL en _pFolderFocus_, el mensaje se redacta en la carpeta a la que apunta _pFolderFocus_.</span><span class="sxs-lookup"><span data-stu-id="f081c-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="f081c-112">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="f081c-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="f081c-113">a Un puntero a la carpeta en la que se crea el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="f081c-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="f081c-114">_pPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="f081c-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="f081c-115">a Un puntero al objeto de formulario para el nuevo formulario.</span><span class="sxs-lookup"><span data-stu-id="f081c-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="f081c-116">_ppMessage_</span><span class="sxs-lookup"><span data-stu-id="f081c-116">_ppMessage_</span></span>
  
> <span data-ttu-id="f081c-117">contempla Un puntero a un puntero al nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="f081c-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="f081c-118">_ppMessageSite_</span><span class="sxs-lookup"><span data-stu-id="f081c-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="f081c-119">contempla Un puntero a un puntero a un objeto de sitio de mensaje para el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="f081c-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="f081c-120">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="f081c-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="f081c-121">contempla Un puntero a un puntero a un contexto de vista que es apropiado para pasar a un nuevo formulario con el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="f081c-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="f081c-122">Si el formulario implementa su propio contexto de vista, se puede pasar NULL en el parámetro _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="f081c-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f081c-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f081c-123">Return value</span></span>

<span data-ttu-id="f081c-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="f081c-124">S_OK</span></span> 
  
> <span data-ttu-id="f081c-125">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="f081c-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f081c-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f081c-126">Remarks</span></span>

<span data-ttu-id="f081c-127">Los objetos de formulario llaman al método **IMAPIMessageSite:: NewMessage** para crear un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="f081c-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="f081c-128">El formulario usa **NewMessage** para obtener un nuevo mensaje y el sitio del mensaje asociado desde su vista.</span><span class="sxs-lookup"><span data-stu-id="f081c-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="f081c-129">A continuación, puede modificar el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="f081c-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="f081c-130">También puede obtener un contexto de vista asociado pasando un valor no nulo en el parámetro _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="f081c-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="f081c-131">Este contexto de vista se puede usar directamente o se puede Agregar y pasar al nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="f081c-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="f081c-132">Si se requiere una implementación completa, pase NULL en _ppViewContext_.</span><span class="sxs-lookup"><span data-stu-id="f081c-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="f081c-133">Para obtener una lista de las interfaces relacionadas con los servidores de formularios, consulte [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="f081c-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f081c-134">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f081c-134">MFCMAPI reference</span></span>

<span data-ttu-id="f081c-135">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f081c-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f081c-136">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="f081c-136">**File**</span></span>|<span data-ttu-id="f081c-137">**Función**</span><span class="sxs-lookup"><span data-stu-id="f081c-137">**Function**</span></span>|<span data-ttu-id="f081c-138">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="f081c-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f081c-139">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="f081c-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="f081c-140">CMyMAPIFormViewer:: NewMessage</span><span class="sxs-lookup"><span data-stu-id="f081c-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="f081c-141">MFCMAPI usa el método **IMAPIMessageSite:: NewMessage** para crear un nuevo mensaje, crear una instancia de un nuevo visor de formularios y llamar a **SetPersist** para establecer el mensaje en el visor de formularios.</span><span class="sxs-lookup"><span data-stu-id="f081c-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="f081c-142">Por último, devuelve el visor del formulario como el sitio del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f081c-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f081c-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="f081c-143">See also</span></span>



[<span data-ttu-id="f081c-144">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f081c-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="f081c-145">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f081c-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="f081c-146">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="f081c-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f081c-147">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="f081c-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

