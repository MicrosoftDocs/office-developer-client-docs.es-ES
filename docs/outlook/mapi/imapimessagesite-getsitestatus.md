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
ms.openlocfilehash: 7d81533b13f4f44a0644215e009dc3477717e9a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817346"
---
# <a name="imapimessagesitegetsitestatus"></a><span data-ttu-id="049f6-103">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="049f6-103">IMAPIMessageSite::GetSiteStatus</span></span>

  
  
<span data-ttu-id="049f6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="049f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="049f6-105">Devuelve información de un objeto de sitio de mensaje acerca del mensaje de las capacidades del sitio para el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="049f6-105">Returns information from a message site object about the message site's capabilities for the current message.</span></span>
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="049f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="049f6-106">Parameters</span></span>

 <span data-ttu-id="049f6-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="049f6-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="049f6-108">[out] Un puntero a una máscara de bits de indicadores que proporciona información sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="049f6-108">[out] A pointer to a bitmask of flags that provides information about message status.</span></span> <span data-ttu-id="049f6-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="049f6-109">The following flags can be set:</span></span>
    
<span data-ttu-id="049f6-110">VCSTATUS_COPY</span><span class="sxs-lookup"><span data-stu-id="049f6-110">VCSTATUS_COPY</span></span> 
  
> <span data-ttu-id="049f6-111">Se puede copiar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="049f6-111">The message can be copied.</span></span> 
    
<span data-ttu-id="049f6-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="049f6-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="049f6-113">Se puede eliminar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="049f6-113">The message can be deleted.</span></span>
    
<span data-ttu-id="049f6-114">VCSTATUS_DELETE_IS_MOVE</span><span class="sxs-lookup"><span data-stu-id="049f6-114">VCSTATUS_DELETE_IS_MOVE</span></span> 
  
> <span data-ttu-id="049f6-115">Cuando se elimina, se mueve un mensaje a una carpeta de **Elementos eliminados** en su almacén de mensajes en lugar de que se quita inmediatamente de su almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="049f6-115">When deleted, a message is moved to a **Deleted Items** folder in its message store instead of being immediately removed from its message store.</span></span> 
    
<span data-ttu-id="049f6-116">VCSTATUS_MOVE</span><span class="sxs-lookup"><span data-stu-id="049f6-116">VCSTATUS_MOVE</span></span> 
  
> <span data-ttu-id="049f6-117">Se puede mover el mensaje.</span><span class="sxs-lookup"><span data-stu-id="049f6-117">The message can be moved.</span></span>
    
<span data-ttu-id="049f6-118">VCSTATUS_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="049f6-118">VCSTATUS_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="049f6-119">Se puede crear un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="049f6-119">A new message can be created.</span></span>
    
<span data-ttu-id="049f6-120">VCSTATUS_SAVE</span><span class="sxs-lookup"><span data-stu-id="049f6-120">VCSTATUS_SAVE</span></span> 
  
> <span data-ttu-id="049f6-121">Se puede guardar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="049f6-121">The message can be saved.</span></span>
    
<span data-ttu-id="049f6-122">VCSTATUS_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="049f6-122">VCSTATUS_SUBMIT</span></span> 
  
> <span data-ttu-id="049f6-123">Se puede enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="049f6-123">The message can be submitted.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="049f6-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="049f6-124">Return value</span></span>

<span data-ttu-id="049f6-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="049f6-125">S_OK</span></span> 
  
> <span data-ttu-id="049f6-126">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="049f6-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="049f6-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="049f6-127">Remarks</span></span>

<span data-ttu-id="049f6-128">Objetos de formulario llamar al método **IMAPIMessageSite::GetSiteStatus** para obtener las capacidades del objeto de sitio de mensaje para el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="049f6-128">Form objects call the **IMAPIMessageSite::GetSiteStatus** method to obtain the message site object's capabilities for the current message.</span></span> <span data-ttu-id="049f6-129">Los indicadores devueltos en el parámetro _lpulStatus_ proporcionan información sobre el sitio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="049f6-129">The flags returned in the  _lpulStatus_ parameter provide information about the message site.</span></span> <span data-ttu-id="049f6-130">Normalmente, un formulario habilita o deshabilita los comandos de menú, dependiendo de la información que proporcionan los indicadores acerca de las capacidades de la implementación de sitio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="049f6-130">Typically, a form enables or disables menu commands, depending on information the flags provide about the capabilities of the message site implementation.</span></span> <span data-ttu-id="049f6-131">Si se carga un nuevo mensaje en un formulario mediante el método [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) o el método [IPersistMessage::Load](ipersistmessage-load.md) , los indicadores de estado deben estar protegidos.</span><span class="sxs-lookup"><span data-stu-id="049f6-131">If a new message is loaded into a form by the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method or the [IPersistMessage::Load](ipersistmessage-load.md) method, the status flags must be checked.</span></span> <span data-ttu-id="049f6-132">Algunos objetos de sitio de mensaje, especialmente objetos de sólo lectura, no permitir los mensajes que se guarden o eliminado.</span><span class="sxs-lookup"><span data-stu-id="049f6-132">Some message site objects, especially read-only objects, do not allow messages to be saved or deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="049f6-133">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="049f6-133">Notes to implementers</span></span>

<span data-ttu-id="049f6-134">El método **IMAPIMessageSite::GetSiteStatus** puede requerir la aplicación de cliente que realice algunos cálculos para determinar qué operaciones pueden o no se puede realizar en el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="049f6-134">The **IMAPIMessageSite::GetSiteStatus** method may require the client application to do some calculation to determine what operations can or cannot be performed on the current message.</span></span> <span data-ttu-id="049f6-135">Normalmente, que implica busca en la fila de estado de proveedor de almacén de mensajes del mensaje actual o consultar el proveedor de almacenamiento para determinar las acciones que puede realizar la aplicación cliente mediante el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="049f6-135">Typically, that involves looking at the status row for the current message's message store provider, or querying the store provider to determine which actions the client application can perform by using the message store.</span></span> <span data-ttu-id="049f6-136">Por ejemplo, para determinar si se debe devolver el indicador MAPI_DELETE_IS_MOVE, compruebe la mensaje almacén de propiedad del objeto **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) para ver si hay una carpeta de **Elementos eliminados** en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="049f6-136">For example, to determine whether to return the MAPI_DELETE_IS_MOVE flag, check the message store object's **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property to see whether there is a **Deleted Items** folder in the message store.</span></span> 
  
<span data-ttu-id="049f6-137">Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="049f6-137">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="049f6-138">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="049f6-138">MFCMAPI reference</span></span>

<span data-ttu-id="049f6-139">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="049f6-139">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="049f6-140">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="049f6-140">**File**</span></span>|<span data-ttu-id="049f6-141">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="049f6-141">**Function**</span></span>|<span data-ttu-id="049f6-142">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="049f6-142">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="049f6-143">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="049f6-143">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="049f6-144">CMyMAPIFormViewer::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="049f6-144">CMyMAPIFormViewer::GetSiteStatus</span></span>  <br/> |<span data-ttu-id="049f6-145">MFCMAPI usa el método **IMAPIMessageSite::GetSiteStatus** para obtener el estado del sitio especificado.</span><span class="sxs-lookup"><span data-stu-id="049f6-145">MFCMAPI uses the **IMAPIMessageSite::GetSiteStatus** method to get the status of the specified site.</span></span> <span data-ttu-id="049f6-146">Puede devolver VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE o VCSTATUS_SUBMIT.</span><span class="sxs-lookup"><span data-stu-id="049f6-146">It can return VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE, or VCSTATUS_SUBMIT.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="049f6-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="049f6-147">See also</span></span>



[<span data-ttu-id="049f6-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="049f6-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="049f6-149">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="049f6-149">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="049f6-150">Propiedad canónica PidTagIpmWastebasketEntryId</span><span class="sxs-lookup"><span data-stu-id="049f6-150">PidTagIpmWastebasketEntryId Canonical Property</span></span>](pidtagipmwastebasketentryid-canonical-property.md)
  
[<span data-ttu-id="049f6-151">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="049f6-151">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="049f6-152">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="049f6-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="049f6-153">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="049f6-153">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

