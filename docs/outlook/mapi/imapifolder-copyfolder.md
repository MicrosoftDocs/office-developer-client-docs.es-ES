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
ms.openlocfilehash: 134a492dbc86dd0ce6b3795d5ae40b334c14d468
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585153"
---
# <a name="imapifoldercopyfolder"></a><span data-ttu-id="2cb4c-103">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="2cb4c-103">IMAPIFolder::CopyFolder</span></span>

  
  
<span data-ttu-id="2cb4c-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2cb4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2cb4c-105">Copia o mueve una subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-105">Copies or moves a subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="2cb4c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2cb4c-106">Parameters</span></span>

 <span data-ttu-id="2cb4c-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2cb4c-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="2cb4c-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="2cb4c-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2cb4c-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="2cb4c-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="2cb4c-110">[entrada] Un puntero al identificador de entrada de la subcarpeta para copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-110">[in] A pointer to the entry identifier of the subfolder to copy or move.</span></span>
    
 <span data-ttu-id="2cb4c-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="2cb4c-111">_lpInterface_</span></span>
  
> <span data-ttu-id="2cb4c-112">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta que señala el parámetro _lpDestFolder_ .</span><span class="sxs-lookup"><span data-stu-id="2cb4c-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that the  _lpDestFolder_ parameter points to.</span></span> <span data-ttu-id="2cb4c-113">Pasando NULL hace que el proveedor de servicios devolver la interfaz de carpeta estándar, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="2cb4c-113">Passing NULL causes the service provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="2cb4c-114">Los valores válidos para _lpInterface_ son IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer y IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-114">Valid values for  _lpInterface_ include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="2cb4c-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="2cb4c-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="2cb4c-116">[entrada] Un puntero a la carpeta abierta para recibir la subcarpeta copiada o movida.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-116">[in] A pointer to the open folder to receive the copied or moved subfolder.</span></span>
    
 <span data-ttu-id="2cb4c-117">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="2cb4c-117">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="2cb4c-118">[entrada] Un puntero en el nombre de la carpeta que se ha movido o copiado en su nuevo destino.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-118">[in] A pointer to the name of the copied or moved folder in its new destination.</span></span> <span data-ttu-id="2cb4c-119">Si _lpszNewFolderName_ se establece en NULL, se usa el nombre de la subcarpeta de origen para el nombre de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-119">If  _lpszNewFolderName_ is set to NULL, the name of the source subfolder is used for the name of the destination folder.</span></span> 
    
 <span data-ttu-id="2cb4c-120">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2cb4c-120">_ulUIParam_</span></span>
  
> <span data-ttu-id="2cb4c-121">[entrada] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-121">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="2cb4c-122">El parámetro _ulUIParam_ se omite a menos que se establece la marca FOLDER_DIALOG en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="2cb4c-122">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag in the  _ulFlags_ parameter is set.</span></span> 
    
 <span data-ttu-id="2cb4c-123">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="2cb4c-123">_lpProgress_</span></span>
  
> <span data-ttu-id="2cb4c-124">[entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-124">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="2cb4c-125">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-125">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="2cb4c-126">El parámetro _lpProgress_ se omite a menos que se establece la marca FOLDER_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-126">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="2cb4c-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2cb4c-127">_ulFlags_</span></span>
  
> <span data-ttu-id="2cb4c-128">[entrada] Una máscara de bits de indicadores que controla la operación de copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-128">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="2cb4c-129">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="2cb4c-129">The following flags can be set:</span></span>
    
<span data-ttu-id="2cb4c-130">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="2cb4c-130">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="2cb4c-131">También se deben copiar todas las subcarpetas en la subcarpeta que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-131">All of the subfolders in the subfolder to be copied should also be copied.</span></span> <span data-ttu-id="2cb4c-132">Cuando COPY_SUBFOLDERS no está establecido para una operación de copia, se copia sólo la subcarpeta identificada por _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="2cb4c-132">When COPY_SUBFOLDERS is not set for a copy operation, only the subfolder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="2cb4c-133">Con una operación de movimiento, el comportamiento COPY_SUBFOLDERS es el valor predeterminado, independientemente de si se establece la marca.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-133">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="2cb4c-134">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2cb4c-134">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="2cb4c-135">Solicita la visualización de un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-135">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="2cb4c-136">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="2cb4c-136">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="2cb4c-137">La subcarpeta es va a mover en lugar de copiado.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-137">The subfolder is to be moved instead of copied.</span></span> <span data-ttu-id="2cb4c-138">Si no se establece FOLDER_MOVE, se copia la subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-138">If FOLDER_MOVE is not set, the subfolder is copied.</span></span>
    
<span data-ttu-id="2cb4c-139">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="2cb4c-139">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="2cb4c-140">El proveedor de almacenamiento de mensaje le informa de que si implementa **CopyFolder** mediante una llamada al método [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) o [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) del objeto de su soporte técnico, **CopyFolder** debe devolver en su lugar inmediatamente MAPI_E_ DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-140">Informs the message store provider that if it implements **CopyFolder** by calling its support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method, **CopyFolder** should instead immediately return MAPI_E_DECLINE_COPY.</span></span> 
    
<span data-ttu-id="2cb4c-141">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2cb4c-141">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2cb4c-142">El nombre de la carpeta de destino está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-142">The name of the destination folder is in Unicode format.</span></span> <span data-ttu-id="2cb4c-143">Si no está establecido el indicador MAPI_UNICODE., el nombre de la carpeta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-143">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2cb4c-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2cb4c-144">Return value</span></span>

<span data-ttu-id="2cb4c-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="2cb4c-145">S_OK</span></span> 
  
> <span data-ttu-id="2cb4c-146">La carpeta especificada se ha copiado o movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-146">The specified folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="2cb4c-147">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2cb4c-147">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2cb4c-148">Se ha establecido el indicador MAPI_UNICODE y el proveedor de almacén de mensajes no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y el proveedor de almacenamiento de mensaje admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-148">Either the MAPI_UNICODE flag was set and the message store provider does not support Unicode, or MAPI_UNICODE was not set and the message store provider supports only Unicode.</span></span>
    
<span data-ttu-id="2cb4c-149">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="2cb4c-149">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="2cb4c-150">El nombre de la carpeta que se va a mover o copiar es el mismo que el de una subcarpeta en la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-150">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="2cb4c-151">El proveedor de almacén de mensajes requiere nombres de carpeta única.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-151">The message store provider requires unique folder names.</span></span>
    
<span data-ttu-id="2cb4c-152">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="2cb4c-152">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="2cb4c-153">El proveedor implementa este método mediante una llamada a un método del objeto de soporte, y el autor de la llamada ha pasado la marca MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-153">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="2cb4c-154">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="2cb4c-154">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="2cb4c-155">La carpeta de origen, directa o indirectamente contiene la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-155">The source folder directly or indirectly contains the destination folder.</span></span> <span data-ttu-id="2cb4c-156">Trabajo significativo es posible que se han realizado antes de que se ha detectado esta condición, por lo que se puede modificar parcialmente la carpeta de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-156">Significant work may have been performed before this condition was discovered, so the source and destination folder may be partially modified.</span></span> 
    
<span data-ttu-id="2cb4c-157">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="2cb4c-157">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="2cb4c-158">La llamada se ha realizado correctamente, pero no todas las entradas se copiaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-158">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="2cb4c-159">Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="2cb4c-160">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="2cb4c-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="2cb4c-161">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="2cb4c-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2cb4c-162">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2cb4c-162">Remarks</span></span>

<span data-ttu-id="2cb4c-163">El método **IMAPIFolder::CopyFolder** copia o mueve una subcarpeta de una ubicación a otra.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-163">The **IMAPIFolder::CopyFolder** method copies or moves a subfolder from one location to another.</span></span> <span data-ttu-id="2cb4c-164">La subcarpeta se copien o muevan se agrega a la carpeta de destino como una subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-164">The subfolder being copied or moved is added to the destination folder as a subfolder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2cb4c-165">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="2cb4c-165">Notes to implementers</span></span>

<span data-ttu-id="2cb4c-166">Cuando la operación de copiar o mover implica más de una carpeta, como se indica mediante la configuración de la marca COPY_SUBFOLDERS, realizar la operación más completo posible para cada carpeta.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-166">When the copy or move operation involves more than one folder, as indicated by setting the COPY_SUBFOLDERS flag, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="2cb4c-167">En ocasiones, una de las carpetas que se va a mover o copiar no existe o ya se ha movido o copiado en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-167">Sometimes one of the folders to be moved or copied does not exist or has already been moved or copied elsewhere.</span></span> <span data-ttu-id="2cb4c-168">No detiene la operación de forma prematura a menos que se produzca un error que está fuera de su control, como la falta de memoria, está quedando sin espacio en disco o daños en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-168">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="2cb4c-169">Intente conservar todos los identificadores de entrada del mensaje en los mensajes copiados.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-169">Try to retain all message entry identifiers in the copied messages.</span></span> <span data-ttu-id="2cb4c-170">También debe intentar conservar los identificadores de entrada, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-170">You should also try to preserve entry identifiers, but it is not required.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2cb4c-171">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="2cb4c-171">Notes to callers</span></span>

<span data-ttu-id="2cb4c-172">Espera a que estos valores devueltos en las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-172">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="2cb4c-173">**Condición**</span><span class="sxs-lookup"><span data-stu-id="2cb4c-173">**Condition**</span></span>|<span data-ttu-id="2cb4c-174">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="2cb4c-174">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2cb4c-175">**CopyFolder** correctamente haya copiado o movido todos los mensajes y subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-175">**CopyFolder** has successfully copied or moved every message and subfolder.</span></span>  <br/> |<span data-ttu-id="2cb4c-176">S_OK</span><span class="sxs-lookup"><span data-stu-id="2cb4c-176">S_OK</span></span>  <br/> |
|<span data-ttu-id="2cb4c-177">**CopyFolder** no pudo copiar o mover todos los mensajes y subcarpeta correctamente.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-177">**CopyFolder** was unable to successfully copy or move every message and subfolder.</span></span>  <br/> |<span data-ttu-id="2cb4c-178">MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2cb4c-178">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="2cb4c-179">**CopyFolder** no pudo completar.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-179">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="2cb4c-180">Cualquier valor de error excepto MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2cb4c-180">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="2cb4c-181">Cuando no se puede completar **CopyFolder** , no asuma que se ha realizado ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-181">When **CopyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="2cb4c-182">Es posible que han sido **CopyFolder** capaz de copiar o mover uno o varios de los mensajes y subcarpetas antes de encontrar el error.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-182">**CopyFolder** might have been able to copy or move one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="2cb4c-183">Si se pasa un identificador de entrada para una carpeta que no existe en _lpEntryID_, **CopyFolder** devuelve MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND, según la implementación del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-183">If an entry identifier for a folder that does not exist is passed in  _lpEntryID_, **CopyFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
<span data-ttu-id="2cb4c-184">Dependiendo del proveedor de almacén de mensajes, el identificador de entrada del mensaje original puede o no es posible que se conserva en el mensaje copiado.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-184">Depending on the message store provider, the entry identifier of the original message may or may not be preserved in the copied message.</span></span> <span data-ttu-id="2cb4c-185">Debe conservar los identificadores de entrada siempre que sea posible, pero no es un requisito.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-185">You should preserve entry identifiers whenever possible, but it is not a requirement.</span></span> <span data-ttu-id="2cb4c-186">Por lo general puede confiar en los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="2cb4c-186">You can generally depend on the following scenarios:</span></span>
  
- <span data-ttu-id="2cb4c-187">Al mover una carpeta entre dos tipos diferentes de los almacenes de mensajes, se garantiza que el identificador de entrada cambia.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-187">When you move a folder between two different types of message stores, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="2cb4c-188">Al mover una carpeta entre dos almacenes de mensajes del mismo tipo, casi siempre se cambia el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-188">When you move a folder between two message stores of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="2cb4c-189">Cuando se mueve una carpeta a otra ubicación en el mismo almacén de mensajes, el identificador de entrada puede o puede que no cambie, según el mensaje de proveedor de almacén.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-189">When you move a folder to another location in the same message store, the entry identifier may or may not change, depending on the message store provider.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="2cb4c-190">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2cb4c-190">MFCMAPI reference</span></span>

<span data-ttu-id="2cb4c-191">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-191">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2cb4c-192">**File**</span><span class="sxs-lookup"><span data-stu-id="2cb4c-192">**File**</span></span>|<span data-ttu-id="2cb4c-193">**Función**</span><span class="sxs-lookup"><span data-stu-id="2cb4c-193">**Function**</span></span>|<span data-ttu-id="2cb4c-194">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="2cb4c-194">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2cb4c-195">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2cb4c-195">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="2cb4c-196">CMsgStoreDlg::OnPasteFolder</span><span class="sxs-lookup"><span data-stu-id="2cb4c-196">CMsgStoreDlg::OnPasteFolder</span></span>  <br/> |<span data-ttu-id="2cb4c-197">MFCMAPI usa el método **IMAPIFolder::CopyFolder** para copiar las carpetas desde una ubicación a otra.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-197">MFCMAPI uses the **IMAPIFolder::CopyFolder** method to copy folders from one location to another.</span></span> <span data-ttu-id="2cb4c-198">MFCMAPI recuerda la carpeta de origen durante la operación de copia y realmente realiza la copia durante la operación de pegado.</span><span class="sxs-lookup"><span data-stu-id="2cb4c-198">MFCMAPI remembers the source folder during the copy operation and actually performs the copy during the paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2cb4c-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cb4c-199">See also</span></span>



[<span data-ttu-id="2cb4c-200">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="2cb4c-200">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="2cb4c-201">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="2cb4c-201">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

