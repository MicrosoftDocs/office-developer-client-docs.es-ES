---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430003"
---
# <a name="imapimessagesitecopymessage"></a><span data-ttu-id="f1ce4-103">IMAPIMessageSite::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="f1ce4-103">IMAPIMessageSite::CopyMessage</span></span>

  
  
<span data-ttu-id="f1ce4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1ce4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1ce4-105">Copia el mensaje actual en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="f1ce4-105">Copies the current message to a folder.</span></span>
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a><span data-ttu-id="f1ce4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1ce4-106">Parameters</span></span>

 <span data-ttu-id="f1ce4-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="f1ce4-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="f1ce4-108">[entrada] Puntero a la carpeta donde se va a copiar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f1ce4-108">[in] A pointer to the folder where the message is to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f1ce4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1ce4-109">Return value</span></span>

<span data-ttu-id="f1ce4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1ce4-110">S_OK</span></span> 
  
> <span data-ttu-id="f1ce4-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="f1ce4-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f1ce4-112">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f1ce4-112">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f1ce4-113">Este sitio de mensaje no admite la operación.</span><span class="sxs-lookup"><span data-stu-id="f1ce4-113">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f1ce4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1ce4-114">Remarks</span></span>

<span data-ttu-id="f1ce4-115">Los objetos de formulario llaman **al método IMAPIMessageSite::CopyMessage** para copiar el mensaje actual en una carpeta nueva.</span><span class="sxs-lookup"><span data-stu-id="f1ce4-115">Form objects call the **IMAPIMessageSite::CopyMessage** method to copy the current message to a new folder.</span></span> <span data-ttu-id="f1ce4-116">**CopyMessage** no cambia el mensaje que se muestra actualmente al usuario y no se devuelve ninguna interfaz para el mensaje recién creado al formulario.</span><span class="sxs-lookup"><span data-stu-id="f1ce4-116">**CopyMessage** does not change the message currently being displayed to the user, and no interface for the newly created message is returned to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f1ce4-117">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="f1ce4-117">Notes to implementers</span></span>

<span data-ttu-id="f1ce4-118">Una implementación típica del **método CopyMessage** realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="f1ce4-118">A typical implementation of the **CopyMessage** method performs the following tasks:</span></span> 
  
1. <span data-ttu-id="f1ce4-119">Crea un nuevo mensaje para el mensaje actual en el que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="f1ce4-119">Creates a new message for the current message to be copied to.</span></span>
    
2. <span data-ttu-id="f1ce4-120">Llama al [método IPersistMessage::Save](ipersistmessage-save.md) con un puntero al nuevo mensaje en el parámetro _pMessage_ y FALSE en el parámetro _fSameAsLoad._</span><span class="sxs-lookup"><span data-stu-id="f1ce4-120">Calls the [IPersistMessage::Save](ipersistmessage-save.md) method with a pointer to the new message in the  _pMessage_ parameter and FALSE in the  _fSameAsLoad_ parameter.</span></span> 
    
3. <span data-ttu-id="f1ce4-121">Llama al [método IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) y pasa NULL en el _parámetro pMessage._</span><span class="sxs-lookup"><span data-stu-id="f1ce4-121">Calls the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method, passing NULL in the  _pMessage_ parameter.</span></span> 
    
4. <span data-ttu-id="f1ce4-122">Llama al [método IMAPIProp::SaveChanges](imapiprop-savechanges.md) en el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="f1ce4-122">Calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the new message.</span></span> 
    
<span data-ttu-id="f1ce4-123">Para obtener una lista de interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="f1ce4-123">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f1ce4-124">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f1ce4-124">MFCMAPI reference</span></span>

<span data-ttu-id="f1ce4-125">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f1ce4-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f1ce4-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="f1ce4-126">**File**</span></span>|<span data-ttu-id="f1ce4-127">**Función**</span><span class="sxs-lookup"><span data-stu-id="f1ce4-127">**Function**</span></span>|<span data-ttu-id="f1ce4-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="f1ce4-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f1ce4-129">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="f1ce4-129">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="f1ce4-130">CMyMAPIFormViewer::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="f1ce4-130">CMyMAPIFormViewer::CopyMessage</span></span>  <br/> |<span data-ttu-id="f1ce4-131">No implementado.</span><span class="sxs-lookup"><span data-stu-id="f1ce4-131">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1ce4-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f1ce4-132">See also</span></span>



[<span data-ttu-id="f1ce4-133">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="f1ce4-133">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="f1ce4-134">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="f1ce4-134">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="f1ce4-135">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="f1ce4-135">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="f1ce4-136">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f1ce4-136">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="f1ce4-137">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="f1ce4-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f1ce4-138">Interfaces de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="f1ce4-138">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

