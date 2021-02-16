---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3d9c1e88b12baf50593212a3ae3c02907ce6617b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425662"
---
# <a name="imapifoldercopyfolder"></a><span data-ttu-id="88960-103">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="88960-103">IMAPIFolder::CopyFolder</span></span>

  
  
<span data-ttu-id="88960-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88960-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88960-105">Copia o mueve una subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="88960-105">Copies or moves a subfolder.</span></span>
  
```cpp
HRESULT CopyFolder(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="88960-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88960-106">Parameters</span></span>

 <span data-ttu-id="88960-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="88960-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="88960-108">[entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="88960-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="88960-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="88960-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="88960-110">[entrada] Puntero al identificador de entrada de la subcarpeta que se debe copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="88960-110">[in] A pointer to the entry identifier of the subfolder to copy or move.</span></span>
    
 <span data-ttu-id="88960-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="88960-111">_lpInterface_</span></span>
  
> <span data-ttu-id="88960-112">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta a la que apunta el parámetro _lpDestFolder._</span><span class="sxs-lookup"><span data-stu-id="88960-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that the  _lpDestFolder_ parameter points to.</span></span> <span data-ttu-id="88960-113">Pasar NULL hace que el proveedor de servicios devuelva la interfaz de carpeta estándar, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="88960-113">Passing NULL causes the service provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="88960-114">Los valores válidos  _para lpInterface_ incluyen IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer y IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="88960-114">Valid values for  _lpInterface_ include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="88960-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="88960-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="88960-116">[entrada] Puntero a la carpeta abierta para recibir la subcarpeta copiada o movida.</span><span class="sxs-lookup"><span data-stu-id="88960-116">[in] A pointer to the open folder to receive the copied or moved subfolder.</span></span>
    
 <span data-ttu-id="88960-117">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="88960-117">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="88960-118">[entrada] Puntero al nombre de la carpeta copiada o movida en su nuevo destino.</span><span class="sxs-lookup"><span data-stu-id="88960-118">[in] A pointer to the name of the copied or moved folder in its new destination.</span></span> <span data-ttu-id="88960-119">Si  _lpszNewFolderName_ se establece en NULL, se usa el nombre de la subcarpeta de origen para el nombre de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="88960-119">If  _lpszNewFolderName_ is set to NULL, the name of the source subfolder is used for the name of the destination folder.</span></span> 
    
 <span data-ttu-id="88960-120">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="88960-120">_ulUIParam_</span></span>
  
> <span data-ttu-id="88960-121">[entrada] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="88960-121">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="88960-122">El _parámetro ulUIParam_ se omite a menos FOLDER_DIALOG marca del parámetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="88960-122">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag in the  _ulFlags_ parameter is set.</span></span> 
    
 <span data-ttu-id="88960-123">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="88960-123">_lpProgress_</span></span>
  
> <span data-ttu-id="88960-124">[entrada] Puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="88960-124">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="88960-125">Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso MAPI.</span><span class="sxs-lookup"><span data-stu-id="88960-125">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="88960-126">El  _parámetro lpProgress_ se omite a menos que FOLDER_DIALOG marca esté establecida en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="88960-126">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="88960-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="88960-127">_ulFlags_</span></span>
  
> <span data-ttu-id="88960-128">[entrada] Máscara de bits de marcas que controla la operación de copia o movimiento.</span><span class="sxs-lookup"><span data-stu-id="88960-128">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="88960-129">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="88960-129">The following flags can be set:</span></span>
    
<span data-ttu-id="88960-130">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="88960-130">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="88960-131">También se deben copiar todas las subcarpetas de la subcarpeta que se van a copiar.</span><span class="sxs-lookup"><span data-stu-id="88960-131">All of the subfolders in the subfolder to be copied should also be copied.</span></span> <span data-ttu-id="88960-132">Cuando COPY_SUBFOLDERS no se establece para una operación de copia, solo se copia la subcarpeta identificada por _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="88960-132">When COPY_SUBFOLDERS is not set for a copy operation, only the subfolder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="88960-133">Con una operación de movimiento, COPY_SUBFOLDERS comportamiento predeterminado independientemente de si se establece la marca.</span><span class="sxs-lookup"><span data-stu-id="88960-133">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="88960-134">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="88960-134">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="88960-135">Solicita la visualización de un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="88960-135">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="88960-136">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="88960-136">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="88960-137">La subcarpeta se va a mover en lugar de copiarse.</span><span class="sxs-lookup"><span data-stu-id="88960-137">The subfolder is to be moved instead of copied.</span></span> <span data-ttu-id="88960-138">Si FOLDER_MOVE no se establece, se copia la subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="88960-138">If FOLDER_MOVE is not set, the subfolder is copied.</span></span>
    
<span data-ttu-id="88960-139">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="88960-139">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="88960-140">Informa al proveedor del almacén de mensajes de que si implementa **CopyFolder** llamando al método [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) o [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) del objeto de compatibilidad, **CopyFolder** debería devolver inmediatamente MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="88960-140">Informs the message store provider that if it implements **CopyFolder** by calling its support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method, **CopyFolder** should instead immediately return MAPI_E_DECLINE_COPY.</span></span> 
    
<span data-ttu-id="88960-141">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="88960-141">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="88960-142">El nombre de la carpeta de destino está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="88960-142">The name of the destination folder is in Unicode format.</span></span> <span data-ttu-id="88960-143">Si no MAPI_UNICODE marca, el nombre de la carpeta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="88960-143">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="88960-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88960-144">Return value</span></span>

<span data-ttu-id="88960-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="88960-145">S_OK</span></span> 
  
> <span data-ttu-id="88960-146">La carpeta especificada se ha copiado o movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="88960-146">The specified folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="88960-147">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="88960-147">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="88960-148">Se estableció MAPI_UNICODE marca y el proveedor de al almacenamiento de mensajes no admite Unicode o MAPI_UNICODE no se estableció y el proveedor de al almacenamiento de mensajes solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="88960-148">Either the MAPI_UNICODE flag was set and the message store provider does not support Unicode, or MAPI_UNICODE was not set and the message store provider supports only Unicode.</span></span>
    
<span data-ttu-id="88960-149">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="88960-149">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="88960-150">El nombre de la carpeta que se va a mover o copiar es el mismo que el de una subcarpeta de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="88960-150">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="88960-151">El proveedor del almacén de mensajes requiere nombres de carpeta únicos.</span><span class="sxs-lookup"><span data-stu-id="88960-151">The message store provider requires unique folder names.</span></span>
    
<span data-ttu-id="88960-152">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="88960-152">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="88960-153">El proveedor implementa este método llamando a un método de objeto de soporte técnico y el autor de la llamada ha pasado la marca MAPI_DECLINE_OK compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="88960-153">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="88960-154">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="88960-154">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="88960-155">La carpeta de origen contiene directa o indirectamente la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="88960-155">The source folder directly or indirectly contains the destination folder.</span></span> <span data-ttu-id="88960-156">Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que la carpeta de origen y destino puede modificarse parcialmente.</span><span class="sxs-lookup"><span data-stu-id="88960-156">Significant work may have been performed before this condition was discovered, so the source and destination folder may be partially modified.</span></span> 
    
<span data-ttu-id="88960-157">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="88960-157">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="88960-158">La llamada se ha realizado correctamente, pero no todas las entradas se han copiado correctamente.</span><span class="sxs-lookup"><span data-stu-id="88960-158">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="88960-159">Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="88960-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="88960-160">Para probar esta advertencia, use la **macro HR_FAILED** datos.</span><span class="sxs-lookup"><span data-stu-id="88960-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="88960-161">Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="88960-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="88960-162">Comentarios</span><span class="sxs-lookup"><span data-stu-id="88960-162">Remarks</span></span>

<span data-ttu-id="88960-163">El **método IMAPIFolder::CopyFolder** copia o mueve una subcarpeta de una ubicación a otra.</span><span class="sxs-lookup"><span data-stu-id="88960-163">The **IMAPIFolder::CopyFolder** method copies or moves a subfolder from one location to another.</span></span> <span data-ttu-id="88960-164">La subcarpeta que se va a copiar o mover se agrega a la carpeta de destino como subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="88960-164">The subfolder being copied or moved is added to the destination folder as a subfolder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="88960-165">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="88960-165">Notes to implementers</span></span>

<span data-ttu-id="88960-166">Cuando la operación de copiar o mover implica más de una carpeta, como se indica estableciendo la marca COPY_SUBFOLDERS, realice la operación lo más completa posible para cada carpeta.</span><span class="sxs-lookup"><span data-stu-id="88960-166">When the copy or move operation involves more than one folder, as indicated by setting the COPY_SUBFOLDERS flag, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="88960-167">A veces, una de las carpetas que se va a mover o copiar no existe o ya se ha movido o copiado en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="88960-167">Sometimes one of the folders to be moved or copied does not exist or has already been moved or copied elsewhere.</span></span> <span data-ttu-id="88960-168">No detenga la operación antes de tiempo a menos que se produzca un error que esté fuera de su control, como que se queme la memoria, que se esté quedando sin espacio en disco o que el almacén de mensajes esté dañado.</span><span class="sxs-lookup"><span data-stu-id="88960-168">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="88960-169">Intente conservar todos los identificadores de entrada de mensajes en los mensajes copiados.</span><span class="sxs-lookup"><span data-stu-id="88960-169">Try to retain all message entry identifiers in the copied messages.</span></span> <span data-ttu-id="88960-170">También debe intentar conservar los identificadores de entrada, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="88960-170">You should also try to preserve entry identifiers, but it is not required.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="88960-171">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="88960-171">Notes to callers</span></span>

<span data-ttu-id="88960-172">Espere estos valores devueltos en las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="88960-172">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="88960-173">**Condition**</span><span class="sxs-lookup"><span data-stu-id="88960-173">**Condition**</span></span>|<span data-ttu-id="88960-174">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="88960-174">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="88960-175">**CopyFolder** ha copiado o movido correctamente todos los mensajes y subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="88960-175">**CopyFolder** has successfully copied or moved every message and subfolder.</span></span>  <br/> |<span data-ttu-id="88960-176">S_OK</span><span class="sxs-lookup"><span data-stu-id="88960-176">S_OK</span></span>  <br/> |
|<span data-ttu-id="88960-177">**CopyFolder** no pudo copiar o mover correctamente todos los mensajes y subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="88960-177">**CopyFolder** was unable to successfully copy or move every message and subfolder.</span></span>  <br/> |<span data-ttu-id="88960-178">MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="88960-178">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="88960-179">**CopyFolder** no se pudo completar.</span><span class="sxs-lookup"><span data-stu-id="88960-179">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="88960-180">Cualquier valor de error excepto MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="88960-180">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="88960-181">Cuando **CopyFolder** no se pueda completar, no suponga que no se ha realizado ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="88960-181">When **CopyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="88960-182">Es posible que **CopyFolder** haya podido copiar o mover uno o más mensajes y subcarpetas antes de encontrar el error.</span><span class="sxs-lookup"><span data-stu-id="88960-182">**CopyFolder** might have been able to copy or move one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="88960-183">Si se pasa un identificador de entrada para una carpeta que no existe en  _lpEntryID_, **CopyFolder** devuelve MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND, según la implementación del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="88960-183">If an entry identifier for a folder that does not exist is passed in  _lpEntryID_, **CopyFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
<span data-ttu-id="88960-184">Según el proveedor del almacén de mensajes, el identificador de entrada del mensaje original puede o no conservarse en el mensaje copiado.</span><span class="sxs-lookup"><span data-stu-id="88960-184">Depending on the message store provider, the entry identifier of the original message may or may not be preserved in the copied message.</span></span> <span data-ttu-id="88960-185">Debe conservar los identificadores de entrada siempre que sea posible, pero no es un requisito.</span><span class="sxs-lookup"><span data-stu-id="88960-185">You should preserve entry identifiers whenever possible, but it is not a requirement.</span></span> <span data-ttu-id="88960-186">Por lo general, puede depender de los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="88960-186">You can generally depend on the following scenarios:</span></span>
  
- <span data-ttu-id="88960-187">Al mover una carpeta entre dos tipos diferentes de almacenes de mensajes, se garantiza que el identificador de entrada cambie.</span><span class="sxs-lookup"><span data-stu-id="88960-187">When you move a folder between two different types of message stores, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="88960-188">Al mover una carpeta entre dos almacenes de mensajes del mismo tipo, el identificador de entrada casi siempre cambia.</span><span class="sxs-lookup"><span data-stu-id="88960-188">When you move a folder between two message stores of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="88960-189">Cuando mueve una carpeta a otra ubicación del mismo almacén de mensajes, el identificador de entrada puede o no cambiar, según el proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="88960-189">When you move a folder to another location in the same message store, the entry identifier may or may not change, depending on the message store provider.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="88960-190">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="88960-190">MFCMAPI reference</span></span>

<span data-ttu-id="88960-191">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="88960-191">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="88960-192">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="88960-192">**File**</span></span>|<span data-ttu-id="88960-193">**Función**</span><span class="sxs-lookup"><span data-stu-id="88960-193">**Function**</span></span>|<span data-ttu-id="88960-194">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="88960-194">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="88960-195">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="88960-195">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="88960-196">CMsgStoreDlg::OnPasteFolder</span><span class="sxs-lookup"><span data-stu-id="88960-196">CMsgStoreDlg::OnPasteFolder</span></span>  <br/> |<span data-ttu-id="88960-197">MFCMAPI usa el **método IMAPIFolder::CopyFolder** para copiar carpetas de una ubicación a otra.</span><span class="sxs-lookup"><span data-stu-id="88960-197">MFCMAPI uses the **IMAPIFolder::CopyFolder** method to copy folders from one location to another.</span></span> <span data-ttu-id="88960-198">MFCMAPI recuerda la carpeta de origen durante la operación de copia y, en realidad, realiza la copia durante la operación de pegado.</span><span class="sxs-lookup"><span data-stu-id="88960-198">MFCMAPI remembers the source folder during the copy operation and actually performs the copy during the paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88960-199">Consulte también</span><span class="sxs-lookup"><span data-stu-id="88960-199">See also</span></span>



[<span data-ttu-id="88960-200">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="88960-200">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="88960-201">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="88960-201">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

