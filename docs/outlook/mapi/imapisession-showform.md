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
ms.openlocfilehash: d20c8e7432903ef9334f066df31694752384d034
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817464"
---
# <a name="imapisessionshowform"></a><span data-ttu-id="456be-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="456be-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="456be-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="456be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="456be-105">Muestra un formulario.</span><span class="sxs-lookup"><span data-stu-id="456be-105">Displays a form.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="456be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="456be-106">Parameters</span></span>

 <span data-ttu-id="456be-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="456be-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="456be-108">[entrada] Identificador de la ventana principal del formulario.</span><span class="sxs-lookup"><span data-stu-id="456be-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="456be-109">_lpMsgStore_</span><span class="sxs-lookup"><span data-stu-id="456be-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="456be-110">[entrada] Un puntero al almacén de mensajes que contiene la carpeta indicada por el parámetro _lpParentFolder_ .</span><span class="sxs-lookup"><span data-stu-id="456be-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="456be-111">_lpParentFolder_</span><span class="sxs-lookup"><span data-stu-id="456be-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="456be-112">[entrada] Un puntero a la carpeta en la que se creó el mensaje asociado con el parámetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="456be-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="456be-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="456be-113">_lpInterface_</span></span>
  
> <span data-ttu-id="456be-114">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al mensaje que se muestra en el formulario.</span><span class="sxs-lookup"><span data-stu-id="456be-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="456be-115">El parámetro _lpInterface_ debe ser NULL o IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="456be-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="456be-116">Si se pasa NULL da como resultado la interfaz estándar, [IMessage](imessageimapiprop.md), que se usa.</span><span class="sxs-lookup"><span data-stu-id="456be-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="456be-117">_ulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="456be-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="456be-118">[entrada] El token que está asociado con el mensaje que se mostrará en el formulario.</span><span class="sxs-lookup"><span data-stu-id="456be-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="456be-119">El parámetro _ulMessageToken_ debe establecerse en el contenido del parámetro _lpulMessageToken_ de la llamada anterior a [IMAPISession:: PrepareForm](imapisession-prepareform.md).</span><span class="sxs-lookup"><span data-stu-id="456be-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="456be-120">_lpMessageSent_</span><span class="sxs-lookup"><span data-stu-id="456be-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="456be-121">[entrada] Reservado; debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="456be-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="456be-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="456be-122">_ulFlags_</span></span>
  
> <span data-ttu-id="456be-123">[entrada] Una máscara de bits de indicadores que controla cómo y si el mensaje se guarda.</span><span class="sxs-lookup"><span data-stu-id="456be-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="456be-124">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="456be-124">The following flags can be set:</span></span>
    
<span data-ttu-id="456be-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="456be-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="456be-126">El mensaje no se ha guardado nunca (es decir, su método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) se ha llamado nunca).</span><span class="sxs-lookup"><span data-stu-id="456be-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="456be-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="456be-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="456be-128">El mensaje debe guardarse en su carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="456be-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="456be-129">El mensaje no se procesa para el envío, pero se registra en la carpeta en su lugar.</span><span class="sxs-lookup"><span data-stu-id="456be-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="456be-130">Si no se establece este indicador, el mensaje se copia en la Bandeja de salida y se procesa para el envío.</span><span class="sxs-lookup"><span data-stu-id="456be-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="456be-131">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="456be-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="456be-132">[entrada] Una máscara de bits de indicadores que se copió desde la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje asociado con el símbolo (token) en el parámetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="456be-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="456be-133">Los indicadores de proporcionan información sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="456be-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="456be-134">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="456be-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="456be-135">[entrada] Una máscara de bits de indicadores que se copió desde la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje asociado con el símbolo (token) en el parámetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="456be-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="456be-136">Estos marcadores proporcionan más información sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="456be-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="456be-137">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="456be-137">_ulAccess_</span></span>
  
> <span data-ttu-id="456be-138">[entrada] Marca que indica el nivel de permisos para el mensaje que se muestra en el formulario.</span><span class="sxs-lookup"><span data-stu-id="456be-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="456be-139">Esta información se copia desde la propiedad **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) del mensaje asociado con el símbolo (token) en el parámetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="456be-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="456be-140">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="456be-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="456be-141">[entrada] Un puntero a la clase de mensaje del mensaje que se muestra en el formulario, que se copió desde la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) del mensaje asociado con el símbolo (token) en el parámetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="456be-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="456be-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="456be-142">Return value</span></span>

<span data-ttu-id="456be-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="456be-143">S_OK</span></span> 
  
> <span data-ttu-id="456be-144">El formulario se muestra correctamente.</span><span class="sxs-lookup"><span data-stu-id="456be-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="456be-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="456be-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="456be-146">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="456be-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="456be-147">Comentarios</span><span class="sxs-lookup"><span data-stu-id="456be-147">Remarks</span></span>

<span data-ttu-id="456be-148">El método **IMAPISession:: ShowForm** muestra un formulario de mensaje que se ha preparado en el método **IMAPISession:: PrepareForm** .</span><span class="sxs-lookup"><span data-stu-id="456be-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="456be-149">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="456be-149">Notes to callers</span></span>

<span data-ttu-id="456be-150">Debe tener sólo una sola referencia para el mensaje que se pasa en el **PrepareForm** parámetro del método _lpMessage_ .</span><span class="sxs-lookup"><span data-stu-id="456be-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="456be-151">Tenga en cuenta que las implementaciones de formulario pueden devolver valores de error que no sean las documentadas por MAPI.</span><span class="sxs-lookup"><span data-stu-id="456be-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="456be-152">Si puede usar estos valores de error para realizar una determinación más precisa de la condición de error, lo haga.</span><span class="sxs-lookup"><span data-stu-id="456be-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="456be-153">De lo contrario, controlar estos errores se deben controlar MAPI_E_CALL_FAILED.</span><span class="sxs-lookup"><span data-stu-id="456be-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="456be-154">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="456be-154">MFCMAPI reference</span></span>

<span data-ttu-id="456be-155">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="456be-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="456be-156">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="456be-156">**File**</span></span>|<span data-ttu-id="456be-157">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="456be-157">**Function**</span></span>|<span data-ttu-id="456be-158">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="456be-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="456be-159">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="456be-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="456be-160">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="456be-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="456be-161">MFCMAPI usa el método **IMAPISession:: ShowForm** , junto con el método **PrepareForm** , para mostrar un mensaje en un formulario modal.</span><span class="sxs-lookup"><span data-stu-id="456be-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="456be-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="456be-162">See also</span></span>



[<span data-ttu-id="456be-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="456be-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="456be-164">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="456be-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="456be-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="456be-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="456be-166">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="456be-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="456be-167">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="456be-167">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

