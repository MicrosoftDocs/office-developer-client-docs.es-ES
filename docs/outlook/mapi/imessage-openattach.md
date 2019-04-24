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
ms.openlocfilehash: e0c3747b48526b715f976e7bf3c142097c85f29a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349255"
---
# <a name="imessageopenattach"></a><span data-ttu-id="4249a-103">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="4249a-103">IMessage::OpenAttach</span></span>

  
  
<span data-ttu-id="4249a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4249a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4249a-105">Abre un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="4249a-105">Opens an attachment.</span></span> 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="4249a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4249a-106">Parameters</span></span>

 <span data-ttu-id="4249a-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="4249a-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="4249a-108">a Número de índice de los datos adjuntos que se van a abrir, tal como se almacena en la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) del adjunto.</span><span class="sxs-lookup"><span data-stu-id="4249a-108">[in] Index number of the attachment to open, as stored in the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span> <span data-ttu-id="4249a-109">Este número de Índice identifica de forma exclusiva los datos adjuntos del mensaje y solo es válido en el contexto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4249a-109">This index number uniquely identifies the attachment in the message and is valid only in the context of the message.</span></span>
    
 <span data-ttu-id="4249a-110">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4249a-110">_lpInterface_</span></span>
  
> <span data-ttu-id="4249a-111">a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4249a-111">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the attachment.</span></span> <span data-ttu-id="4249a-112">Pasar los resultados NULL en la interfaz estándar de los datos adjuntos, o **IAttach**, que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="4249a-112">Passing NULL results in the attachment's standard interface, or **IAttach**, being returned.</span></span> 
    
 <span data-ttu-id="4249a-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4249a-113">_ulFlags_</span></span>
  
> <span data-ttu-id="4249a-114">a Máscara de máscara de marcadores que controla cómo se abren los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4249a-114">[in] Bitmask of flags that controls how the attachment is opened.</span></span> <span data-ttu-id="4249a-115">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="4249a-115">The following flags can be set:</span></span> 
    
<span data-ttu-id="4249a-116">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4249a-116">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="4249a-117">Solicita que los datos adjuntos se abran con los permisos de red máximos permitidos para el usuario y el acceso máximo a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="4249a-117">Requests that the attachment be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="4249a-118">Por ejemplo, si el cliente tiene permiso de lectura y escritura, los datos adjuntos deben abrirse con el permiso de lectura y escritura; Si el cliente tiene acceso de solo lectura, los datos adjuntos deben abrirse con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4249a-118">For example, if the client has read/write permission, the attachment should be opened with read/write permission; if the client has read-only access, the attachment should be opened with read-only access.</span></span> 
    
<span data-ttu-id="4249a-119">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="4249a-119">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="4249a-120">Permite que **OpenAttach** se devuelva correctamente, posiblemente antes de que los datos adjuntos estén completamente disponibles para el cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="4249a-120">Allows **OpenAttach** to return successfully, possibly before the attachment is fully available to the calling client.</span></span> <span data-ttu-id="4249a-121">Si los datos adjuntos no están disponibles, realizar una llamada posterior al mismo puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="4249a-121">If the attachment is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="4249a-122">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="4249a-122">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="4249a-123">Solicita el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4249a-123">Requests read/write permission.</span></span> <span data-ttu-id="4249a-124">De forma predeterminada, los datos adjuntos se abren con acceso de solo lectura y los clientes no deben trabajar en el supuesto de que se ha concedido el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4249a-124">By default, attachments are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="4249a-125">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="4249a-125">_lppAttach_</span></span>
  
> <span data-ttu-id="4249a-126">contempla Puntero a un puntero a los datos adjuntos abiertos.</span><span class="sxs-lookup"><span data-stu-id="4249a-126">[out] Pointer to a pointer to the open attachment.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4249a-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4249a-127">Return value</span></span>

<span data-ttu-id="4249a-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="4249a-128">S_OK</span></span> 
  
> <span data-ttu-id="4249a-129">Los datos adjuntos se abrieron correctamente.</span><span class="sxs-lookup"><span data-stu-id="4249a-129">The attachment was successfully opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4249a-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4249a-130">Remarks</span></span>

<span data-ttu-id="4249a-131">El método **IMessage:: OpenAttach** abre los datos adjuntos de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4249a-131">The **IMessage::OpenAttach** method opens a message's attachment.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4249a-132">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="4249a-132">Notes to callers</span></span>

<span data-ttu-id="4249a-133">Para abrir datos adjuntos, debe tener acceso al número de datos adjuntos o a la propiedad **PR_ATTACH_NUM** .</span><span class="sxs-lookup"><span data-stu-id="4249a-133">To open an attachment, you must have access to its attachment number or **PR_ATTACH_NUM** property.</span></span> <span data-ttu-id="4249a-134">Llame a [IMessage:: GetAttachmentTable](imessage-getattachmenttable.md) para recuperar la tabla de datos adjuntos del mensaje y busque la fila que representa los datos adjuntos que se abrirán.</span><span class="sxs-lookup"><span data-stu-id="4249a-134">Call [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) to retrieve the message's attachment table and locate the row that represents the attachment to be opened.</span></span> <span data-ttu-id="4249a-135">Consulte [apertura de datos](opening-an-attachment.md) adjuntos para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4249a-135">See [Opening an Attachment](opening-an-attachment.md) for more information.</span></span> 
  
<span data-ttu-id="4249a-136">No intente abrir un archivo de datos adjuntos varias veces; los resultados no están definidos y dependen del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4249a-136">Do not try to open one attachment multiple times; the results are undefined and dependent on the message store provider.</span></span>
  
<span data-ttu-id="4249a-137">Puede solicitar que los datos adjuntos se abran en modo de lectura y escritura, en lugar del modo predeterminado de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4249a-137">You can request that the attachment be opened in read/write mode, instead of the default read-only mode.</span></span> <span data-ttu-id="4249a-138">Sin embargo, si los datos adjuntos se abrirán realmente en modo de lectura y escritura, dependerá del proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4249a-138">However, whether the attachment will actually be opened in read/write mode is up to the message store provider.</span></span> <span data-ttu-id="4249a-139">Puede intentar modificar los datos adjuntos, prepararse para controlar posibles errores o comprobar el nivel de acceso que se concedió recuperando la propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) de los datos adjuntos, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="4249a-139">You can either attempt to modify the attachment, preparing to handle possible failure, or check the level of access that was granted by retrieving the attachment's **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property, if it is available.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4249a-140">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4249a-140">MFCMAPI reference</span></span>

<span data-ttu-id="4249a-141">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="4249a-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4249a-142">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="4249a-142">**File**</span></span>|<span data-ttu-id="4249a-143">**Función**</span><span class="sxs-lookup"><span data-stu-id="4249a-143">**Function**</span></span>|<span data-ttu-id="4249a-144">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="4249a-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4249a-145">AttachmentsDlg. cpp usado para</span><span class="sxs-lookup"><span data-stu-id="4249a-145">AttachmentsDlg.cpp Used to</span></span>  <br/> |<span data-ttu-id="4249a-146">CAttachmentsDlg:: OpenItemProp</span><span class="sxs-lookup"><span data-stu-id="4249a-146">CAttachmentsDlg::OpenItemProp</span></span>  <br/> |<span data-ttu-id="4249a-147">MFCMAPI usa el método **IMessage:: OpenAttach** para abrir objetos Attachment,</span><span class="sxs-lookup"><span data-stu-id="4249a-147">MFCMAPI uses the **IMessage::OpenAttach** method to open attachment objects,</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4249a-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="4249a-148">See also</span></span>



[<span data-ttu-id="4249a-149">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4249a-149">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="4249a-150">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="4249a-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

