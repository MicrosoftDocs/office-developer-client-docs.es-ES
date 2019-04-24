---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8b90dee3958a20994f9a60d104ae714ad95307d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335668"
---
# <a name="imapisessionshowform"></a><span data-ttu-id="4b21e-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="4b21e-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="4b21e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b21e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b21e-105">Muestra un formulario.</span><span class="sxs-lookup"><span data-stu-id="4b21e-105">Displays a form.</span></span>
  
```cpp
HRESULT ShowForm(
  ULONG_PTR ulUIParam,
  LPMDB lpMsgStore,
  LPMAPIFOLDER lpParentFolder,
  LPCIID lpInterface,
  ULONG ulMessageToken,
  LPMESSAGE lpMessageSent,
  ULONG ulFlags,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  ULONG ulAccess,
  LPSTR lpszMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="4b21e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4b21e-106">Parameters</span></span>

 <span data-ttu-id="4b21e-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4b21e-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="4b21e-108">a Identificador de la ventana primaria del formulario.</span><span class="sxs-lookup"><span data-stu-id="4b21e-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="4b21e-109">_lpMsgStore_</span><span class="sxs-lookup"><span data-stu-id="4b21e-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="4b21e-110">a Un puntero al almacén de mensajes que contiene la carpeta a la que apunta el parámetro _lpParentFolder_ .</span><span class="sxs-lookup"><span data-stu-id="4b21e-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="4b21e-111">_lpParentFolder_</span><span class="sxs-lookup"><span data-stu-id="4b21e-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="4b21e-112">a Un puntero a la carpeta en la que se creó el mensaje asociado con el parámetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="4b21e-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="4b21e-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4b21e-113">_lpInterface_</span></span>
  
> <span data-ttu-id="4b21e-114">a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso al mensaje que se muestra en el formulario.</span><span class="sxs-lookup"><span data-stu-id="4b21e-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="4b21e-115">El parámetro _lpInterface_ debe ser null o IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="4b21e-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="4b21e-116">Pasar resultados NULL en la interfaz estándar, [IMessage](imessageimapiprop.md), que se está utilizando.</span><span class="sxs-lookup"><span data-stu-id="4b21e-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="4b21e-117">_ulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="4b21e-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="4b21e-118">a Token asociado al mensaje que se va a mostrar en el formulario.</span><span class="sxs-lookup"><span data-stu-id="4b21e-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="4b21e-119">El parámetro _ulMessageToken_ debe establecerse en el contenido del parámetro _lpulMessageToken_ de la llamada anterior a [IMAPISession::P repareform](imapisession-prepareform.md).</span><span class="sxs-lookup"><span data-stu-id="4b21e-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="4b21e-120">_lpMessageSent_</span><span class="sxs-lookup"><span data-stu-id="4b21e-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="4b21e-121">a Reserve debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="4b21e-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="4b21e-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4b21e-122">_ulFlags_</span></span>
  
> <span data-ttu-id="4b21e-123">a Una máscara de máscara de marcas que controla cómo y si se guarda el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4b21e-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="4b21e-124">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="4b21e-124">The following flags can be set:</span></span>
    
<span data-ttu-id="4b21e-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="4b21e-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="4b21e-126">Nunca se ha guardado el mensaje (es decir, nunca se ha llamado al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) ).</span><span class="sxs-lookup"><span data-stu-id="4b21e-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="4b21e-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="4b21e-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="4b21e-128">El mensaje debe guardarse en su carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="4b21e-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="4b21e-129">El mensaje no se ha procesado para enviar, pero se ha publicado en la carpeta en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4b21e-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="4b21e-130">Si no se establece esta marca, el mensaje se copia en la bandeja de salida y se procesa para su envío.</span><span class="sxs-lookup"><span data-stu-id="4b21e-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="4b21e-131">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="4b21e-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="4b21e-132">a Una máscara de la máscara de los marcadores copiados de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje asociado con el token en el parámetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="4b21e-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="4b21e-133">Las marcas proporcionan información sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4b21e-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="4b21e-134">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="4b21e-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="4b21e-135">a Una máscara de la máscara de los marcadores copiados de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje asociado con el token en el parámetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="4b21e-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="4b21e-136">Estas marcas proporcionan más información sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4b21e-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="4b21e-137">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="4b21e-137">_ulAccess_</span></span>
  
> <span data-ttu-id="4b21e-138">a Marca que indica el nivel de permisos del mensaje que se muestra en el formulario.</span><span class="sxs-lookup"><span data-stu-id="4b21e-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="4b21e-139">Esta información se copia desde la propiedad **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) del mensaje asociado con el token en el parámetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="4b21e-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="4b21e-140">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="4b21e-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="4b21e-141">a Un puntero a la clase de mensaje del mensaje que se muestra en el formulario, copiado de la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) del mensaje asociado con el token en el parámetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="4b21e-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4b21e-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b21e-142">Return value</span></span>

<span data-ttu-id="4b21e-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="4b21e-143">S_OK</span></span> 
  
> <span data-ttu-id="4b21e-144">El formulario se mostró correctamente.</span><span class="sxs-lookup"><span data-stu-id="4b21e-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="4b21e-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="4b21e-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="4b21e-146">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4b21e-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4b21e-147">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b21e-147">Remarks</span></span>

<span data-ttu-id="4b21e-148">El método **IMAPISession:: ShowForm** muestra un formulario de mensaje preparado por el método **IMAPISession::P repareform** .</span><span class="sxs-lookup"><span data-stu-id="4b21e-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4b21e-149">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="4b21e-149">Notes to callers</span></span>

<span data-ttu-id="4b21e-150">Solo debe haber una referencia al mensaje pasada en el parámetro _lpMessage_ del método **PrepareForm** .</span><span class="sxs-lookup"><span data-stu-id="4b21e-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="4b21e-151">Tenga en cuenta que las implementaciones de formulario pueden devolver valores de error distintos a los documentados por MAPI.</span><span class="sxs-lookup"><span data-stu-id="4b21e-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="4b21e-152">Si puede usar estos valores de error para realizar una determinación más precisa de la condición de error, hágalo.</span><span class="sxs-lookup"><span data-stu-id="4b21e-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="4b21e-153">De lo contrario, controle estos errores tal y como lo haría con MAPI_E_CALL_FAILED.</span><span class="sxs-lookup"><span data-stu-id="4b21e-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4b21e-154">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4b21e-154">MFCMAPI reference</span></span>

<span data-ttu-id="4b21e-155">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="4b21e-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4b21e-156">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="4b21e-156">**File**</span></span>|<span data-ttu-id="4b21e-157">**Función**</span><span class="sxs-lookup"><span data-stu-id="4b21e-157">**Function**</span></span>|<span data-ttu-id="4b21e-158">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="4b21e-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4b21e-159">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="4b21e-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="4b21e-160">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="4b21e-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="4b21e-161">MFCMAPI usa el método **IMAPISession:: ShowForm** , junto con el método **PrepareForm** , para mostrar un mensaje en un formulario modal.</span><span class="sxs-lookup"><span data-stu-id="4b21e-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b21e-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b21e-162">See also</span></span>



[<span data-ttu-id="4b21e-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="4b21e-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="4b21e-164">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4b21e-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="4b21e-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="4b21e-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="4b21e-166">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4b21e-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="4b21e-167">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="4b21e-167">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

