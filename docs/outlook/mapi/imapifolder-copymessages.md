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
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424458"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="ad164-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="ad164-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="ad164-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad164-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad164-105">Copia o mueve uno o más mensajes.</span><span class="sxs-lookup"><span data-stu-id="ad164-105">Copies or moves one or more messages.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ad164-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ad164-106">Parameters</span></span>

 <span data-ttu-id="ad164-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="ad164-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="ad164-108">a Un puntero a una matriz de estructuras [ENTRYLIST](entrylist.md) que identifican el mensaje o los mensajes que se van a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="ad164-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="ad164-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ad164-109">_lpInterface_</span></span>
  
> <span data-ttu-id="ad164-110">a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la carpeta de destino a la que apunta el parámetro _lpDestFolder_ .</span><span class="sxs-lookup"><span data-stu-id="ad164-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="ad164-111">Pasar resultados NULL, el proveedor de servicios devuelve la interfaz de carpeta estándar, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="ad164-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="ad164-112">Los clientes deben pasar NULL.</span><span class="sxs-lookup"><span data-stu-id="ad164-112">Clients must pass NULL.</span></span> <span data-ttu-id="ad164-113">Otros llamadores pueden establecer el parámetro _lpInterface_ en IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer o IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="ad164-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="ad164-114">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="ad164-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="ad164-115">a Un puntero a la carpeta abierta para recibir los mensajes copiados o movidos.</span><span class="sxs-lookup"><span data-stu-id="ad164-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="ad164-116">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ad164-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="ad164-117">a Un controlador para la ventana primaria de los cuadros de diálogo o ventanas que este método muestra.</span><span class="sxs-lookup"><span data-stu-id="ad164-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="ad164-118">El parámetro _ulUIParam_ se omite a menos que el cliente establezca la marca MESSAGE_DIALOG en el parámetro _ULFLAGS_ y pase null en el parámetro _lpProgress_ .</span><span class="sxs-lookup"><span data-stu-id="ad164-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="ad164-119">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="ad164-119">_lpProgress_</span></span>
  
> <span data-ttu-id="ad164-120">a Un puntero a un objeto Progress que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="ad164-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="ad164-121">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI.</span><span class="sxs-lookup"><span data-stu-id="ad164-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="ad164-122">El parámetro _lpProgress_ se omite a menos que se establezca la marca MESSAGE_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="ad164-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="ad164-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ad164-123">_ulFlags_</span></span>
  
> <span data-ttu-id="ad164-124">a Una máscara de máscara de marcadores que controla cómo se realiza la operación de copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="ad164-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="ad164-125">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="ad164-125">The following flags can be set:</span></span>
    
<span data-ttu-id="ad164-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="ad164-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="ad164-127">Informa al proveedor del almacén de mensajes para que devuelva inmediatamente MAPI_E_DECLINE_COPY si implementa **IMAPIFolder:: CopyMessages** al llamar al método [IMAPISupport::D ocopyto](imapisupport-docopyto.md) o [IMAPISupport::D ocopyprops](imapisupport-docopyprops.md) del objeto support.</span><span class="sxs-lookup"><span data-stu-id="ad164-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="ad164-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ad164-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="ad164-129">Muestra un indicador de progreso mientras se lleva a cabo la operación.</span><span class="sxs-lookup"><span data-stu-id="ad164-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="ad164-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="ad164-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="ad164-131">El mensaje o los mensajes se moverán en lugar de copiarse.</span><span class="sxs-lookup"><span data-stu-id="ad164-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="ad164-132">Si no se establece MESSAGE_MOVE, se copian los mensajes.</span><span class="sxs-lookup"><span data-stu-id="ad164-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ad164-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad164-133">Return value</span></span>

<span data-ttu-id="ad164-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad164-134">S_OK</span></span> 
  
> <span data-ttu-id="ad164-135">El mensaje o los mensajes se han copiado o movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="ad164-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="ad164-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="ad164-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="ad164-137">El proveedor implementa este método llamando a un método de objeto de soporte y el autor de la llamada ha pasado la marca MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="ad164-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="ad164-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="ad164-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="ad164-139">La llamada se realizó correctamente, pero no todas las entradas se han copiado o movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="ad164-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="ad164-140">Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta.</span><span class="sxs-lookup"><span data-stu-id="ad164-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="ad164-141">Para probar esta advertencia, use la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="ad164-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="ad164-142">Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="ad164-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad164-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad164-143">Remarks</span></span>

<span data-ttu-id="ad164-144">El método **IMAPIFolder:: CopyMessages** copia o mueve mensajes a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="ad164-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="ad164-145">Los mensajes que se abren con el permiso de lectura y escritura se pueden mover o copiar.</span><span class="sxs-lookup"><span data-stu-id="ad164-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ad164-146">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="ad164-146">Notes to implementers</span></span>

<span data-ttu-id="ad164-147">Si va a copiar mensajes a otro almacén de mensajes sin usar el método [IMAPISupport:: CopyMessages](imapisupport-copymessages.md) , primero debe llamar a [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) con la marca GENERATE_RECEIPT_ONLY establecida.</span><span class="sxs-lookup"><span data-stu-id="ad164-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="ad164-148">El almacén de mensajes receptor no es responsable de generar informes de lectura para los mensajes copiados o movidos.</span><span class="sxs-lookup"><span data-stu-id="ad164-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="ad164-149">Si está llamando a **IMAPISupport:: CopyMessages** para implementar **IMAPIFolder:: CopyMessages**, no llame a **SetReadFlags**; MAPI lo llamará.</span><span class="sxs-lookup"><span data-stu-id="ad164-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="ad164-150">La implementación puede mover o copiar los mensajes en cualquier orden y generar informes de estado de lectura en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="ad164-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="ad164-151">Es decir, puede terminar de copiar los mensajes antes de generar cualquiera de los informes de estado de lectura o enviar los informes antes de que la implementación inicie la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="ad164-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="ad164-152">Sin embargo, se deben enviar informes de lectura para que se copien todos los mensajes, independientemente de si la copia se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ad164-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="ad164-153">Cuando la operación de copia o movimiento implica más de un mensaje, realice la operación lo más completamente posible.</span><span class="sxs-lookup"><span data-stu-id="ad164-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="ad164-154">No detenga la operación prematuramente a menos que se produzca un error que esté más allá del control, como la falta de memoria, la falta de espacio en disco o que esté dañada en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ad164-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="ad164-155">Intente mantener los identificadores de entrada en las operaciones de movimiento o copia.</span><span class="sxs-lookup"><span data-stu-id="ad164-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="ad164-156">También debe conservar los identificadores de entrada, aunque no es necesario.</span><span class="sxs-lookup"><span data-stu-id="ad164-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="ad164-157">Enviar notificaciones cuando se mueven o se copian mensajes para que los clientes se vean prevenido de que las llamadas a los métodos ' [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de los mensajes podrían producir un error.</span><span class="sxs-lookup"><span data-stu-id="ad164-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="ad164-158">No incluya el estado de un mensaje en la operación de copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="ad164-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="ad164-159">Mover o copiar el estado de un mensaje afecta en gran medida al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="ad164-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ad164-160">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ad164-160">Notes to callers</span></span>

<span data-ttu-id="ad164-161">Use **IMAPIFolder:: CopyMessages** para rellenar las carpetas de resultados de búsqueda, donde los mensajes se suelen agrupar por carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="ad164-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="ad164-162">Espere estos valores devueltos en las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="ad164-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="ad164-163">**Condición**</span><span class="sxs-lookup"><span data-stu-id="ad164-163">**Condition**</span></span>|<span data-ttu-id="ad164-164">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="ad164-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ad164-165">**IMAPIFolder:: CopyMessages** ha copiado o movido correctamente todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="ad164-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="ad164-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad164-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="ad164-167">**IMAPIFolder:: CopyMessages** no pudo copiar o mover correctamente todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="ad164-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="ad164-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="ad164-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="ad164-169">**IMAPIFolder:: CopyMessages** no se pudo completar.</span><span class="sxs-lookup"><span data-stu-id="ad164-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="ad164-170">Cualquier valor de error</span><span class="sxs-lookup"><span data-stu-id="ad164-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="ad164-171">Cuando **IMAPIFolder:: CopyMessages** no se puede completar, no dé por supuesto que no se ha realizado ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="ad164-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="ad164-172">**IMAPIFolder:: CopyMessages** podría haber podido copiar o mover uno o más mensajes antes de que se procontrase el error.</span><span class="sxs-lookup"><span data-stu-id="ad164-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ad164-173">Ver también</span><span class="sxs-lookup"><span data-stu-id="ad164-173">See also</span></span>



[<span data-ttu-id="ad164-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ad164-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

