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
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426075"
---
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="2e0f1-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="2e0f1-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="2e0f1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e0f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e0f1-105">Elimina uno o más mensajes.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2e0f1-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2e0f1-106">Parameters</span></span>

 <span data-ttu-id="2e0f1-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="2e0f1-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="2e0f1-108">a Un puntero a una estructura [ENTRYLIST](entrylist.md) que contiene el número de mensajes que se va a eliminar y una matriz de estructuras [EntryID](entryid.md) que identifican los mensajes.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="2e0f1-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2e0f1-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="2e0f1-110">a Identificador de la ventana primaria del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="2e0f1-111">El parámetro _ulUIParam_ se omite a menos que se establezca la marca MESSAGE_DIALOG en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="2e0f1-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="2e0f1-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="2e0f1-112">_lpProgress_</span></span>
  
> <span data-ttu-id="2e0f1-113">a Un puntero a un objeto Progress que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="2e0f1-114">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="2e0f1-115">El parámetro _lpProgress_ se omite a menos que se establezca la marca MESSAGE_DIALOG en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="2e0f1-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="2e0f1-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2e0f1-116">_ulFlags_</span></span>
  
> <span data-ttu-id="2e0f1-117">a Una máscara de máscara de marcas que controla cómo se eliminan los mensajes.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="2e0f1-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="2e0f1-118">The following flags can be set:</span></span>
    
<span data-ttu-id="2e0f1-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="2e0f1-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="2e0f1-120">Elimina permanentemente todos los mensajes, incluidos los eliminados temporalmente.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="2e0f1-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2e0f1-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="2e0f1-122">Muestra un indicador de progreso mientras se lleva a cabo la operación.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2e0f1-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e0f1-123">Return value</span></span>

<span data-ttu-id="2e0f1-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="2e0f1-124">S_OK</span></span> 
  
> <span data-ttu-id="2e0f1-125">El mensaje o los mensajes especificados se eliminaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="2e0f1-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="2e0f1-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="2e0f1-127">La llamada se realizó correctamente, pero no todos los mensajes se eliminaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="2e0f1-128">Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="2e0f1-129">Para probar esta advertencia, use la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="2e0f1-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="2e0f1-130">Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="2e0f1-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2e0f1-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e0f1-131">Remarks</span></span>

<span data-ttu-id="2e0f1-132">El método **IMAPIFolder::D eletemessages** elimina mensajes de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="2e0f1-133">Los mensajes que no existen, que se han movido a otra ubicación, que están abiertos con permisos de lectura y escritura, o que se envían actualmente no se pueden eliminar.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2e0f1-134">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="2e0f1-134">Notes to implementers</span></span>

<span data-ttu-id="2e0f1-135">Cuando la operación de eliminación implica más de un mensaje, realice la operación lo más completamente posible para cada carpeta, incluso si uno o más de los mensajes no se pueden eliminar.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="2e0f1-136">No detenga la operación prematuramente a menos que se produzca un error que esté más allá del control, como la falta de memoria, la falta de espacio en disco o que esté dañada en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="2e0f1-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="2e0f1-137">Notes to callers</span></span>

<span data-ttu-id="2e0f1-138">Espere estos valores devueltos en las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="2e0f1-139">**Condición**</span><span class="sxs-lookup"><span data-stu-id="2e0f1-139">**Condition**</span></span>|<span data-ttu-id="2e0f1-140">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="2e0f1-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2e0f1-141">**DeleteMessages** ha eliminado correctamente todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="2e0f1-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="2e0f1-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="2e0f1-143">**DeleteMessages** no pudo eliminar correctamente todos los mensajes y subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="2e0f1-144">MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2e0f1-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="2e0f1-145">**DeleteMessages** no se pudo completar.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="2e0f1-146">Cualquier valor de error excepto MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2e0f1-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="2e0f1-147">Cuando **DeleteMessages** no pueda completarse, no dé por supuesto que no se ha realizado ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="2e0f1-148">Es posible que **DeleteMessages** haya podido eliminar uno o más mensajes antes de que se produzca el error.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="2e0f1-149">**DeleteMessages** devuelve MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND, en función de la implementación del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2e0f1-150">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2e0f1-150">MFCMAPI reference</span></span>

<span data-ttu-id="2e0f1-151">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2e0f1-152">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="2e0f1-152">**File**</span></span>|<span data-ttu-id="2e0f1-153">**Función**</span><span class="sxs-lookup"><span data-stu-id="2e0f1-153">**Function**</span></span>|<span data-ttu-id="2e0f1-154">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="2e0f1-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2e0f1-155">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="2e0f1-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="2e0f1-156">CFolderDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="2e0f1-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="2e0f1-157">MFCMAPI usa el método **IMAPIFolder::D eletemessages** para eliminar los mensajes especificados.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e0f1-158">Ver también</span><span class="sxs-lookup"><span data-stu-id="2e0f1-158">See also</span></span>



[<span data-ttu-id="2e0f1-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2e0f1-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="2e0f1-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="2e0f1-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="2e0f1-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="2e0f1-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="2e0f1-162">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="2e0f1-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="2e0f1-163">Uso de macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="2e0f1-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

