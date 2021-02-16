---
title: IMAPIMessageSiteGetSiteStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSiteStatus
api_type:
- COM
ms.assetid: 02718898-7857-4e43-8f46-622269f812e6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ab4a06a20c71943f9b649d8f22377f59223e9717
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430129"
---
# <a name="imapimessagesitegetsitestatus"></a><span data-ttu-id="6b1be-103">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="6b1be-103">IMAPIMessageSite::GetSiteStatus</span></span>

  
  
<span data-ttu-id="6b1be-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b1be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b1be-105">Devuelve información de un objeto de sitio de mensaje acerca de las capacidades del sitio del mensaje para el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="6b1be-105">Returns information from a message site object about the message site's capabilities for the current message.</span></span>
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="6b1be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b1be-106">Parameters</span></span>

 <span data-ttu-id="6b1be-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="6b1be-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="6b1be-108">[salida] Puntero a una máscara de bits de marcas que proporciona información sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b1be-108">[out] A pointer to a bitmask of flags that provides information about message status.</span></span> <span data-ttu-id="6b1be-109">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="6b1be-109">The following flags can be set:</span></span>
    
<span data-ttu-id="6b1be-110">VCSTATUS_COPY</span><span class="sxs-lookup"><span data-stu-id="6b1be-110">VCSTATUS_COPY</span></span> 
  
> <span data-ttu-id="6b1be-111">El mensaje se puede copiar.</span><span class="sxs-lookup"><span data-stu-id="6b1be-111">The message can be copied.</span></span> 
    
<span data-ttu-id="6b1be-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="6b1be-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="6b1be-113">El mensaje se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="6b1be-113">The message can be deleted.</span></span>
    
<span data-ttu-id="6b1be-114">VCSTATUS_DELETE_IS_MOVE</span><span class="sxs-lookup"><span data-stu-id="6b1be-114">VCSTATUS_DELETE_IS_MOVE</span></span> 
  
> <span data-ttu-id="6b1be-115">Cuando se elimina, un mensaje se mueve a una **carpeta Elementos** eliminados en su almacén de mensajes en lugar de quitarse inmediatamente de su almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="6b1be-115">When deleted, a message is moved to a **Deleted Items** folder in its message store instead of being immediately removed from its message store.</span></span> 
    
<span data-ttu-id="6b1be-116">VCSTATUS_MOVE</span><span class="sxs-lookup"><span data-stu-id="6b1be-116">VCSTATUS_MOVE</span></span> 
  
> <span data-ttu-id="6b1be-117">El mensaje se puede mover.</span><span class="sxs-lookup"><span data-stu-id="6b1be-117">The message can be moved.</span></span>
    
<span data-ttu-id="6b1be-118">VCSTATUS_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="6b1be-118">VCSTATUS_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="6b1be-119">Se puede crear un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="6b1be-119">A new message can be created.</span></span>
    
<span data-ttu-id="6b1be-120">VCSTATUS_SAVE</span><span class="sxs-lookup"><span data-stu-id="6b1be-120">VCSTATUS_SAVE</span></span> 
  
> <span data-ttu-id="6b1be-121">El mensaje se puede guardar.</span><span class="sxs-lookup"><span data-stu-id="6b1be-121">The message can be saved.</span></span>
    
<span data-ttu-id="6b1be-122">VCSTATUS_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="6b1be-122">VCSTATUS_SUBMIT</span></span> 
  
> <span data-ttu-id="6b1be-123">El mensaje se puede enviar.</span><span class="sxs-lookup"><span data-stu-id="6b1be-123">The message can be submitted.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6b1be-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b1be-124">Return value</span></span>

<span data-ttu-id="6b1be-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b1be-125">S_OK</span></span> 
  
> <span data-ttu-id="6b1be-126">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="6b1be-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b1be-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b1be-127">Remarks</span></span>

<span data-ttu-id="6b1be-128">Los objetos de formulario llaman **al método IMAPIMessageSite::GetSiteStatus** para obtener las capacidades del objeto de sitio de mensaje para el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="6b1be-128">Form objects call the **IMAPIMessageSite::GetSiteStatus** method to obtain the message site object's capabilities for the current message.</span></span> <span data-ttu-id="6b1be-129">Las marcas devueltas en el  _parámetro lpulStatus_ proporcionan información sobre el sitio del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b1be-129">The flags returned in the  _lpulStatus_ parameter provide information about the message site.</span></span> <span data-ttu-id="6b1be-130">Normalmente, un formulario habilita o deshabilita los comandos de menú, en función de la información que proporcionan las marcas sobre las capacidades de la implementación del sitio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="6b1be-130">Typically, a form enables or disables menu commands, depending on information the flags provide about the capabilities of the message site implementation.</span></span> <span data-ttu-id="6b1be-131">Si el método [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) o el método [IPersistMessage::Load](ipersistmessage-load.md) cargan un nuevo mensaje en un formulario, deben comprobarse las marcas de estado.</span><span class="sxs-lookup"><span data-stu-id="6b1be-131">If a new message is loaded into a form by the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method or the [IPersistMessage::Load](ipersistmessage-load.md) method, the status flags must be checked.</span></span> <span data-ttu-id="6b1be-132">Algunos objetos de sitio de mensajes, especialmente los objetos de solo lectura, no permiten que los mensajes se guarden o eliminen.</span><span class="sxs-lookup"><span data-stu-id="6b1be-132">Some message site objects, especially read-only objects, do not allow messages to be saved or deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6b1be-133">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="6b1be-133">Notes to implementers</span></span>

<span data-ttu-id="6b1be-134">El **método IMAPIMessageSite::GetSiteStatus** puede requerir que la aplicación cliente realice algún cálculo para determinar qué operaciones se pueden o no realizar en el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="6b1be-134">The **IMAPIMessageSite::GetSiteStatus** method may require the client application to do some calculation to determine what operations can or cannot be performed on the current message.</span></span> <span data-ttu-id="6b1be-135">Normalmente, esto implica consultar la fila de estado del proveedor de al almacenamiento de mensajes del mensaje actual o consultar al proveedor de almacenamiento para determinar qué acciones puede realizar la aplicación cliente mediante el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="6b1be-135">Typically, that involves looking at the status row for the current message's message store provider, or querying the store provider to determine which actions the client application can perform by using the message store.</span></span> <span data-ttu-id="6b1be-136">Por ejemplo, para determinar si se va a devolver la marca MAPI_DELETE_IS_MOVE, compruebe la propiedad **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) del objeto del almacén de mensajes para ver si hay una carpeta Elementos eliminados en el almacén de mensajes. </span><span class="sxs-lookup"><span data-stu-id="6b1be-136">For example, to determine whether to return the MAPI_DELETE_IS_MOVE flag, check the message store object's **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property to see whether there is a **Deleted Items** folder in the message store.</span></span> 
  
<span data-ttu-id="6b1be-137">Para obtener una lista de interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="6b1be-137">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6b1be-138">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6b1be-138">MFCMAPI reference</span></span>

<span data-ttu-id="6b1be-139">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="6b1be-139">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6b1be-140">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="6b1be-140">**File**</span></span>|<span data-ttu-id="6b1be-141">**Función**</span><span class="sxs-lookup"><span data-stu-id="6b1be-141">**Function**</span></span>|<span data-ttu-id="6b1be-142">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="6b1be-142">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b1be-143">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="6b1be-143">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="6b1be-144">CMyMAPIFormViewer::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="6b1be-144">CMyMAPIFormViewer::GetSiteStatus</span></span>  <br/> |<span data-ttu-id="6b1be-145">MFCMAPI usa el **método IMAPIMessageSite::GetSiteStatus** para obtener el estado del sitio especificado.</span><span class="sxs-lookup"><span data-stu-id="6b1be-145">MFCMAPI uses the **IMAPIMessageSite::GetSiteStatus** method to get the status of the specified site.</span></span> <span data-ttu-id="6b1be-146">Puede devolver VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE o VCSTATUS_SUBMIT.</span><span class="sxs-lookup"><span data-stu-id="6b1be-146">It can return VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE, or VCSTATUS_SUBMIT.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b1be-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6b1be-147">See also</span></span>



[<span data-ttu-id="6b1be-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="6b1be-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="6b1be-149">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="6b1be-149">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="6b1be-150">Propiedad canónica PidTagIpmWastebasketEntryId</span><span class="sxs-lookup"><span data-stu-id="6b1be-150">PidTagIpmWastebasketEntryId Canonical Property</span></span>](pidtagipmwastebasketentryid-canonical-property.md)
  
[<span data-ttu-id="6b1be-151">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b1be-151">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="6b1be-152">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="6b1be-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="6b1be-153">Interfaces de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="6b1be-153">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

