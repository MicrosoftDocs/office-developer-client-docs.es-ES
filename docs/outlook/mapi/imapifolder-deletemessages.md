---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7845abc4f3010daf8e13d56ac4b13d0333bad07e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817245"
---
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="bb4da-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="bb4da-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="bb4da-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb4da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb4da-105">Elimina uno o más mensajes.</span><span class="sxs-lookup"><span data-stu-id="bb4da-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bb4da-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb4da-106">Parameters</span></span>

 <span data-ttu-id="bb4da-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="bb4da-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="bb4da-108">[entrada] Un puntero a una estructura [ENTRYLIST](entrylist.md) que contiene el número de mensajes para eliminar y una matriz de estructuras [ENTRYID](entryid.md) que identifique los mensajes.</span><span class="sxs-lookup"><span data-stu-id="bb4da-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="bb4da-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="bb4da-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="bb4da-110">[entrada] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="bb4da-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="bb4da-111">El parámetro _ulUIParam_ se omite a menos que se establece la marca MESSAGE_DIALOG en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="bb4da-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="bb4da-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="bb4da-112">_lpProgress_</span></span>
  
> <span data-ttu-id="bb4da-113">[entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="bb4da-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="bb4da-114">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI.</span><span class="sxs-lookup"><span data-stu-id="bb4da-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="bb4da-115">El parámetro _lpProgress_ se omite a menos que se establece la marca MESSAGE_DIALOG en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="bb4da-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="bb4da-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bb4da-116">_ulFlags_</span></span>
  
> <span data-ttu-id="bb4da-117">[entrada] Una máscara de bits de indicadores que controla cómo se eliminan los mensajes.</span><span class="sxs-lookup"><span data-stu-id="bb4da-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="bb4da-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="bb4da-118">The following flags can be set:</span></span>
    
<span data-ttu-id="bb4da-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="bb4da-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="bb4da-120">Quita de forma permanente todos los mensajes, incluidos los eliminado temporalmente.</span><span class="sxs-lookup"><span data-stu-id="bb4da-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="bb4da-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="bb4da-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="bb4da-122">Muestra un indicador de progreso mientras se realiza la operación.</span><span class="sxs-lookup"><span data-stu-id="bb4da-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bb4da-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb4da-123">Return value</span></span>

<span data-ttu-id="bb4da-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb4da-124">S_OK</span></span> 
  
> <span data-ttu-id="bb4da-125">El mensaje especificado o los mensajes se han eliminado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb4da-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="bb4da-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="bb4da-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="bb4da-127">La llamada se ha realizado correctamente, pero no todos los mensajes se han eliminado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb4da-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="bb4da-128">Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="bb4da-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="bb4da-129">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="bb4da-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="bb4da-130">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="bb4da-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb4da-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb4da-131">Remarks</span></span>

<span data-ttu-id="bb4da-132">El método **IMAPIFolder::DeleteMessages** elimina los mensajes de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="bb4da-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="bb4da-133">No se puede eliminar los mensajes que no existen, que se han movido en otra parte, que están abiertos con permiso de lectura y escritura o que se envían actualmente.</span><span class="sxs-lookup"><span data-stu-id="bb4da-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bb4da-134">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="bb4da-134">Notes to implementers</span></span>

<span data-ttu-id="bb4da-135">Cuando la operación de eliminación implica más de un mensaje, realizar la operación más completo posible para cada carpeta, incluso si no se puede eliminar uno o varios de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="bb4da-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="bb4da-136">No detiene la operación de forma prematura a menos que se produzca un error que está fuera de su control, como la falta de memoria, está quedando sin espacio en disco o daños en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bb4da-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="bb4da-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="bb4da-137">Notes to callers</span></span>

<span data-ttu-id="bb4da-138">Espera a que estos valores devueltos en las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="bb4da-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="bb4da-139">**Condición**</span><span class="sxs-lookup"><span data-stu-id="bb4da-139">**Condition**</span></span>|<span data-ttu-id="bb4da-140">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="bb4da-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb4da-141">**DeleteMessages** ha eliminado correctamente todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="bb4da-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="bb4da-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb4da-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="bb4da-143">**DeleteMessages** no pudo eliminar correctamente todos los mensajes y subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="bb4da-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="bb4da-144">MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="bb4da-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="bb4da-145">**DeleteMessages** no pudo completar.</span><span class="sxs-lookup"><span data-stu-id="bb4da-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="bb4da-146">Cualquier valor de error excepto MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="bb4da-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="bb4da-147">Cuando **DeleteMessages** es no se puede completar, no asuma que se ha realizado ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="bb4da-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="bb4da-148">Es posible que han sido **DeleteMessages** podrá eliminar uno o varios de los mensajes antes de encontrar el error.</span><span class="sxs-lookup"><span data-stu-id="bb4da-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="bb4da-149">**DeleteMessages** devuelve MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND, según la implementación del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bb4da-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bb4da-150">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bb4da-150">MFCMAPI reference</span></span>

<span data-ttu-id="bb4da-151">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="bb4da-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bb4da-152">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="bb4da-152">**File**</span></span>|<span data-ttu-id="bb4da-153">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="bb4da-153">**Function**</span></span>|<span data-ttu-id="bb4da-154">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="bb4da-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bb4da-155">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="bb4da-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="bb4da-156">CFolderDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="bb4da-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="bb4da-157">MFCMAPI usa el método **IMAPIFolder::DeleteMessages** para eliminar los mensajes especificados.</span><span class="sxs-lookup"><span data-stu-id="bb4da-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb4da-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb4da-158">See also</span></span>



[<span data-ttu-id="bb4da-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="bb4da-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="bb4da-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="bb4da-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="bb4da-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="bb4da-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="bb4da-162">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="bb4da-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="bb4da-163">Uso de macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="bb4da-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

