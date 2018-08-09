---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c702e4063bf5e5a06a9e476a02172a780c7e326a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817646"
---
# <a name="imessageopenattach"></a><span data-ttu-id="61b27-103">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="61b27-103">IMessage::OpenAttach</span></span>

  
  
<span data-ttu-id="61b27-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61b27-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61b27-105">Se abre un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="61b27-105">Opens an attachment.</span></span> 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="61b27-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61b27-106">Parameters</span></span>

 <span data-ttu-id="61b27-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="61b27-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="61b27-108">[entrada] Número de índice de los datos adjuntos para abrir, tal como se almacena en la propiedad de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="61b27-108">[in] Index number of the attachment to open, as stored in the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span> <span data-ttu-id="61b27-109">Este número de índice identifica los datos adjuntos en el mensaje y sólo es válido en el contexto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="61b27-109">This index number uniquely identifies the attachment in the message and is valid only in the context of the message.</span></span>
    
 <span data-ttu-id="61b27-110">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="61b27-110">_lpInterface_</span></span>
  
> <span data-ttu-id="61b27-111">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="61b27-111">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the attachment.</span></span> <span data-ttu-id="61b27-112">Si se pasa NULL da como resultado una interfaz estándar de los datos adjuntos o **IAttach**, que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="61b27-112">Passing NULL results in the attachment's standard interface, or **IAttach**, being returned.</span></span> 
    
 <span data-ttu-id="61b27-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="61b27-113">_ulFlags_</span></span>
  
> <span data-ttu-id="61b27-114">[entrada] Máscara de bits de indicadores que controla cómo se abren los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="61b27-114">[in] Bitmask of flags that controls how the attachment is opened.</span></span> <span data-ttu-id="61b27-115">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="61b27-115">The following flags can be set:</span></span> 
    
<span data-ttu-id="61b27-116">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="61b27-116">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="61b27-117">Solicita que los datos adjuntos se abran con los permisos de red máximo permitidos para el acceso de usuarios y el número máximo de clientes aplicación.</span><span class="sxs-lookup"><span data-stu-id="61b27-117">Requests that the attachment be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="61b27-118">Por ejemplo, si el cliente no tiene permiso de lectura y escritura, se deben abrir los datos adjuntos con permisos de lectura y escritura; Si el cliente no tiene acceso de solo lectura, los datos adjuntos se deben abrir con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="61b27-118">For example, if the client has read/write permission, the attachment should be opened with read/write permission; if the client has read-only access, the attachment should be opened with read-only access.</span></span> 
    
<span data-ttu-id="61b27-119">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="61b27-119">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="61b27-120">Permite **OpenAttach** a correctamente, devolver, posiblemente, antes de que los datos adjuntos son completamente disponibles para el cliente de la llamada.</span><span class="sxs-lookup"><span data-stu-id="61b27-120">Allows **OpenAttach** to return successfully, possibly before the attachment is fully available to the calling client.</span></span> <span data-ttu-id="61b27-121">Si los datos adjuntos no está disponible, realizar una llamada posterior a él puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="61b27-121">If the attachment is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="61b27-122">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="61b27-122">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="61b27-123">Las solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="61b27-123">Requests read/write permission.</span></span> <span data-ttu-id="61b27-124">De forma predeterminada, los datos adjuntos se abren con acceso de solo lectura y los clientes no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="61b27-124">By default, attachments are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="61b27-125">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="61b27-125">_lppAttach_</span></span>
  
> <span data-ttu-id="61b27-126">[out] Puntero a un puntero a los datos adjuntos abiertos.</span><span class="sxs-lookup"><span data-stu-id="61b27-126">[out] Pointer to a pointer to the open attachment.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="61b27-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61b27-127">Return value</span></span>

<span data-ttu-id="61b27-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="61b27-128">S_OK</span></span> 
  
> <span data-ttu-id="61b27-129">Los datos adjuntos se abren correctamente.</span><span class="sxs-lookup"><span data-stu-id="61b27-129">The attachment was successfully opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="61b27-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61b27-130">Remarks</span></span>

<span data-ttu-id="61b27-131">El método **IMessage::OpenAttach** abre datos adjuntos de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="61b27-131">The **IMessage::OpenAttach** method opens a message's attachment.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="61b27-132">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="61b27-132">Notes to callers</span></span>

<span data-ttu-id="61b27-133">Para abrir un archivo adjunto, debe tener acceso a su número de datos adjuntos o la propiedad **PR_ATTACH_NUM** .</span><span class="sxs-lookup"><span data-stu-id="61b27-133">To open an attachment, you must have access to its attachment number or **PR_ATTACH_NUM** property.</span></span> <span data-ttu-id="61b27-134">Llame a [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) para recuperar la tabla de datos adjuntos del mensaje y busque la fila que representa los datos adjuntos que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="61b27-134">Call [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) to retrieve the message's attachment table and locate the row that represents the attachment to be opened.</span></span> <span data-ttu-id="61b27-135">Para obtener más información, vea [Abrir un archivo adjunto](opening-an-attachment.md) .</span><span class="sxs-lookup"><span data-stu-id="61b27-135">See [Opening an Attachment](opening-an-attachment.md) for more information.</span></span> 
  
<span data-ttu-id="61b27-136">No intente abrir un archivo adjunto varias veces; los resultados son dependientes en el proveedor de almacén de mensajes y no definido.</span><span class="sxs-lookup"><span data-stu-id="61b27-136">Do not try to open one attachment multiple times; the results are undefined and dependent on the message store provider.</span></span>
  
<span data-ttu-id="61b27-137">Puede solicitar que los datos adjuntos se pueden abrir en modo de lectura y escritura, en lugar del modo de sólo lectura de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="61b27-137">You can request that the attachment be opened in read/write mode, instead of the default read-only mode.</span></span> <span data-ttu-id="61b27-138">Sin embargo, si los datos adjuntos en realidad se abrirán en modo de lectura y escritura es responsabilidad del proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="61b27-138">However, whether the attachment will actually be opened in read/write mode is up to the message store provider.</span></span> <span data-ttu-id="61b27-139">Puede intentar modificar los datos adjuntos, preparación para controlar posibles errores o comprobar el nivel de acceso que se ha concedido, se recupera la propiedad de **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) de los datos adjuntos, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="61b27-139">You can either attempt to modify the attachment, preparing to handle possible failure, or check the level of access that was granted by retrieving the attachment's **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property, if it is available.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="61b27-140">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="61b27-140">MFCMAPI reference</span></span>

<span data-ttu-id="61b27-141">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="61b27-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="61b27-142">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="61b27-142">**File**</span></span>|<span data-ttu-id="61b27-143">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="61b27-143">**Function**</span></span>|<span data-ttu-id="61b27-144">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="61b27-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="61b27-145">AttachmentsDlg.cpp usado para</span><span class="sxs-lookup"><span data-stu-id="61b27-145">AttachmentsDlg.cpp Used to</span></span>  <br/> |<span data-ttu-id="61b27-146">CAttachmentsDlg::OpenItemProp</span><span class="sxs-lookup"><span data-stu-id="61b27-146">CAttachmentsDlg::OpenItemProp</span></span>  <br/> |<span data-ttu-id="61b27-147">MFCMAPI usa el método **IMessage::OpenAttach** para abrir los objetos de datos adjuntos,</span><span class="sxs-lookup"><span data-stu-id="61b27-147">MFCMAPI uses the **IMessage::OpenAttach** method to open attachment objects,</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61b27-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="61b27-148">See also</span></span>



[<span data-ttu-id="61b27-149">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="61b27-149">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="61b27-150">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="61b27-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

