---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e253aa6a701d565fbc61e8a0e0a6388f7199c000
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593266"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="a6f54-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="a6f54-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="a6f54-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6f54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6f54-105">Copia o mueve uno o más mensajes.</span><span class="sxs-lookup"><span data-stu-id="a6f54-105">Copies or moves one or more messages.</span></span>
  
```cpp
HRESULT CopyMessages(
  LPENTRYLIST lpMsgList,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a6f54-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6f54-106">Parameters</span></span>

 <span data-ttu-id="a6f54-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="a6f54-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="a6f54-108">[entrada] Un puntero a una matriz de estructuras [ENTRYLIST](entrylist.md) que identifican el mensaje o mensajes para copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="a6f54-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="a6f54-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a6f54-109">_lpInterface_</span></span>
  
> <span data-ttu-id="a6f54-110">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta de destino al que apunta el parámetro _lpDestFolder_ .</span><span class="sxs-lookup"><span data-stu-id="a6f54-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="a6f54-111">Si se pasa NULL da como resultado el proveedor de servicios de devolución de la interfaz de carpeta estándar, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="a6f54-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="a6f54-112">Los clientes deben pasar NULL.</span><span class="sxs-lookup"><span data-stu-id="a6f54-112">Clients must pass NULL.</span></span> <span data-ttu-id="a6f54-113">Otros autores de llamadas pueden establecer el parámetro _lpInterface_ para IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer o IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="a6f54-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="a6f54-114">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="a6f54-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="a6f54-115">[entrada] Un puntero a la carpeta abierta para recibir los mensajes que se ha movido o copiados.</span><span class="sxs-lookup"><span data-stu-id="a6f54-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="a6f54-116">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a6f54-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="a6f54-117">[entrada] Un identificador de la ventana principal de windows o cuadros de diálogo que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="a6f54-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="a6f54-118">El parámetro _ulUIParam_ se omite a menos que el cliente establece el indicador MESSAGE_DIALOG en el parámetro _ulFlags_ y pasa NULL en el parámetro _lpProgress_ .</span><span class="sxs-lookup"><span data-stu-id="a6f54-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="a6f54-119">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="a6f54-119">_lpProgress_</span></span>
  
> <span data-ttu-id="a6f54-120">[entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="a6f54-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="a6f54-121">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI.</span><span class="sxs-lookup"><span data-stu-id="a6f54-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="a6f54-122">El parámetro _lpProgress_ se omite a menos que se establece la marca MESSAGE_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="a6f54-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="a6f54-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6f54-123">_ulFlags_</span></span>
  
> <span data-ttu-id="a6f54-124">[entrada] Una máscara de bits de indicadores que controla cómo se lleva a cabo la operación de copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="a6f54-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="a6f54-125">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="a6f54-125">The following flags can be set:</span></span>
    
<span data-ttu-id="a6f54-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="a6f54-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="a6f54-127">Informa al proveedor de almacén de mensajes para devolver inmediatamente MAPI_E_DECLINE_COPY si implementa **IMAPIFolder::CopyMessages** mediante una llamada al método [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) o [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) del objeto de la compatibilidad con.</span><span class="sxs-lookup"><span data-stu-id="a6f54-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="a6f54-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a6f54-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="a6f54-129">Muestra un indicador de progreso mientras se realiza la operación.</span><span class="sxs-lookup"><span data-stu-id="a6f54-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="a6f54-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="a6f54-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="a6f54-131">El mensaje o mensajes son va a mover en lugar de copiado.</span><span class="sxs-lookup"><span data-stu-id="a6f54-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="a6f54-132">Si no se establece MESSAGE_MOVE, se copian los mensajes.</span><span class="sxs-lookup"><span data-stu-id="a6f54-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6f54-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6f54-133">Return value</span></span>

<span data-ttu-id="a6f54-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6f54-134">S_OK</span></span> 
  
> <span data-ttu-id="a6f54-135">El mensaje o los mensajes se hayan copiado correctamente o movido.</span><span class="sxs-lookup"><span data-stu-id="a6f54-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="a6f54-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="a6f54-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="a6f54-137">El proveedor implementa este método mediante una llamada a un método del objeto de soporte, y el autor de la llamada ha pasado la marca MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="a6f54-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="a6f54-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="a6f54-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="a6f54-139">La llamada se completó correctamente, pero no todas las entradas se han movido o copiado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a6f54-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="a6f54-140">Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="a6f54-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a6f54-141">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="a6f54-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a6f54-142">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="a6f54-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6f54-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a6f54-143">Remarks</span></span>

<span data-ttu-id="a6f54-144">El método **IMAPIFolder::CopyMessages** copia o mueve los mensajes a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="a6f54-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="a6f54-145">Los mensajes que se abren con lectura y escritura permiso puede mover o copiar.</span><span class="sxs-lookup"><span data-stu-id="a6f54-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a6f54-146">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="a6f54-146">Notes to implementers</span></span>

<span data-ttu-id="a6f54-147">Si va a copiar los mensajes a otro almacén de mensajes sin utilizar el método [IMAPISupport::CopyMessages](imapisupport-copymessages.md) , primero debe llamar [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) con el conjunto de marca GENERATE_RECEIPT_ONLY.</span><span class="sxs-lookup"><span data-stu-id="a6f54-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="a6f54-148">El almacén de mensajes receptor no es responsable de la generación de informes de lectura para los mensajes que se ha movido o copiados.</span><span class="sxs-lookup"><span data-stu-id="a6f54-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="a6f54-149">Si se llama a **IMAPISupport::CopyMessages** para implementar **IMAPIFolder::CopyMessages**, no se llama a **SetReadFlags**; MAPI lo llamará.</span><span class="sxs-lookup"><span data-stu-id="a6f54-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="a6f54-150">La implementación puede mover o copiar los mensajes en cualquier orden y generación de informes de estado de lectura en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="a6f54-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="a6f54-151">Es decir, puede finalice de copiar los mensajes antes de generar cualquiera de los informes de estado de lectura o enviar los informes antes de la implementación inicia la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="a6f54-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="a6f54-152">Sin embargo, lea informes deben enviarse para que todos los mensajes que se copian, independientemente de si la copia es correcta.</span><span class="sxs-lookup"><span data-stu-id="a6f54-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="a6f54-153">Cuando la operación de copiar o mover implica más de un mensaje, realizar la operación más completo posible.</span><span class="sxs-lookup"><span data-stu-id="a6f54-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="a6f54-154">No detiene la operación de forma prematura a menos que se produzca un error que está fuera de su control, como la falta de memoria, está quedando sin espacio en disco o daños en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a6f54-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="a6f54-155">Intente mantener los identificadores de entrada a través de las operaciones de mover o copiar.</span><span class="sxs-lookup"><span data-stu-id="a6f54-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="a6f54-156">También debe conservar los identificadores de entrada, aunque no es necesario.</span><span class="sxs-lookup"><span data-stu-id="a6f54-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="a6f54-157">Enviar notificaciones al mover o copiar mensajes para que los clientes se prevenido que sus llamadas a los métodos de la de los mensajes [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pueden producir un error.</span><span class="sxs-lookup"><span data-stu-id="a6f54-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="a6f54-158">No se incluyen el estado de un mensaje en la copia o la operación de movimiento.</span><span class="sxs-lookup"><span data-stu-id="a6f54-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="a6f54-159">Mover o copiar un estado de mensaje en gran medida afecta al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a6f54-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a6f54-160">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a6f54-160">Notes to callers</span></span>

<span data-ttu-id="a6f54-161">Use **IMAPIFolder::CopyMessages** para rellenar las carpetas de resultados de búsqueda, donde los mensajes a menudo se agrupan por carpeta primaria.</span><span class="sxs-lookup"><span data-stu-id="a6f54-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="a6f54-162">Espera a que estos valores devueltos en las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="a6f54-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="a6f54-163">**Condición**</span><span class="sxs-lookup"><span data-stu-id="a6f54-163">**Condition**</span></span>|<span data-ttu-id="a6f54-164">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="a6f54-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a6f54-165">**IMAPIFolder::CopyMessages** correctamente haya copiado o movido todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="a6f54-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="a6f54-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6f54-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="a6f54-167">**IMAPIFolder::CopyMessages** no pudo copiar o mover todos los mensajes correctamente.</span><span class="sxs-lookup"><span data-stu-id="a6f54-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="a6f54-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="a6f54-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="a6f54-169">**IMAPIFolder::CopyMessages** no pudo completar.</span><span class="sxs-lookup"><span data-stu-id="a6f54-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="a6f54-170">Cualquier valor de error</span><span class="sxs-lookup"><span data-stu-id="a6f54-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="a6f54-171">Cuando **IMAPIFolder::CopyMessages** es no se puede completar, no asuma que se ha realizado ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="a6f54-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="a6f54-172">Es posible que han sido **IMAPIFolder::CopyMessages** capaz de copiar o mover mensajes de uno o varios antes de encontrar el error.</span><span class="sxs-lookup"><span data-stu-id="a6f54-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6f54-173">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a6f54-173">See also</span></span>



[<span data-ttu-id="a6f54-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a6f54-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

