---
title: IMAPISupportCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6ffbf74496d4b61357a0fb473b82deedf39ee576
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570677"
---
# <a name="imapisupportcopyfolder"></a><span data-ttu-id="bf780-103">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="bf780-103">IMAPISupport::CopyFolder</span></span>

  
  
<span data-ttu-id="bf780-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf780-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf780-105">Copia o mueve una carpeta de su carpeta primaria actual a otra carpeta primaria.</span><span class="sxs-lookup"><span data-stu-id="bf780-105">Copies or moves a folder from its current parent folder to another parent folder.</span></span>
  
```cpp
HRESULT CopyFolder(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
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

## <a name="parameters"></a><span data-ttu-id="bf780-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf780-106">Parameters</span></span>

 <span data-ttu-id="bf780-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="bf780-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="bf780-108">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta principal de la carpeta que desea copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="bf780-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the parent folder of the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="bf780-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="bf780-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="bf780-110">[entrada] Un puntero a la carpeta principal de la carpeta que desea copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="bf780-110">[in] A pointer to the parent folder of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="bf780-111">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="bf780-111">_cbEntryID_</span></span>
  
> <span data-ttu-id="bf780-112">[entrada] El número de bytes en el identificador de entrada que señala _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="bf780-112">[in] The byte count in the entry identifier pointed to by  _lpEntryID_.</span></span>
    
 <span data-ttu-id="bf780-113">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="bf780-113">_lpEntryID_</span></span>
  
> <span data-ttu-id="bf780-114">[entrada] Un puntero al identificador de entrada de la carpeta que desea copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="bf780-114">[in] A pointer to the entry identifier of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="bf780-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="bf780-115">_lpInterface_</span></span>
  
> <span data-ttu-id="bf780-116">[entrada] Reservado; debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="bf780-116">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="bf780-117">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="bf780-117">_lpDestFolder_</span></span>
  
> <span data-ttu-id="bf780-118">[entrada] Un puntero a la carpeta que va a recibir la carpeta para ser copiado o movido.</span><span class="sxs-lookup"><span data-stu-id="bf780-118">[in] A pointer to the folder that is to receive the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="bf780-119">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="bf780-119">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="bf780-120">[entrada] Un puntero en el nombre de la carpeta que se ha movido o copiado; de lo contrario, NULL, que indica que la carpeta que se ha movido o copiada debe tener el mismo nombre que la carpeta de origen (es decir, la carpeta indicada por _lpEntryID_).</span><span class="sxs-lookup"><span data-stu-id="bf780-120">[in] A pointer to the name of the copied or moved folder; otherwise, NULL, which indicates that the copied or moved folder should have the same name as the source folder (the folder pointed to by  _lpEntryID_).</span></span>
    
 <span data-ttu-id="bf780-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="bf780-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="bf780-122">[entrada] Identificador de la ventana para el cuadro de diálogo de indicador de progreso y ventanas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="bf780-122">[in] A handle of the window for the progress indicator dialog box and related windows.</span></span> <span data-ttu-id="bf780-123">El parámetro _ulUIParam_ se omite a menos que se establece la marca FOLDER_DIALOG en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="bf780-123">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="bf780-124">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="bf780-124">_lpProgress_</span></span>
  
> <span data-ttu-id="bf780-125">[entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="bf780-125">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="bf780-126">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI.</span><span class="sxs-lookup"><span data-stu-id="bf780-126">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="bf780-127">El parámetro _lpProgress_ se omite a menos que se establece la marca FOLDER_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="bf780-127">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="bf780-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bf780-128">_ulFlags_</span></span>
  
> <span data-ttu-id="bf780-129">[entrada] Una máscara de bits de indicadores que controla cómo se lleva a cabo la operación de copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="bf780-129">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="bf780-130">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="bf780-130">The following flags can be set:</span></span>
    
<span data-ttu-id="bf780-131">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="bf780-131">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="bf780-132">Todas las subcarpetas de la carpeta deben ser copiado o movido.</span><span class="sxs-lookup"><span data-stu-id="bf780-132">All of the folder's subfolders should be copied or moved.</span></span> <span data-ttu-id="bf780-133">Cuando COPY_SUBFOLDERS no está establecido para una operación de copia, se copia sólo la carpeta identificada por _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="bf780-133">When COPY_SUBFOLDERS is not set for a copy operation, only the folder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="bf780-134">Con una operación de movimiento, el comportamiento COPY_SUBFOLDERS es el valor predeterminado, independientemente de si se establece la marca.</span><span class="sxs-lookup"><span data-stu-id="bf780-134">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="bf780-135">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="bf780-135">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="bf780-136">Solicita la visualización de un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="bf780-136">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="bf780-137">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="bf780-137">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="bf780-138">La carpeta se va a mover en lugar de copiado.</span><span class="sxs-lookup"><span data-stu-id="bf780-138">The folder should be moved instead of copied.</span></span> <span data-ttu-id="bf780-139">Si no se establece FOLDER_MOVE, se copia la carpeta.</span><span class="sxs-lookup"><span data-stu-id="bf780-139">If FOLDER_MOVE is not set, the folder is copied.</span></span>
    
<span data-ttu-id="bf780-140">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="bf780-140">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bf780-141">El nombre de la carpeta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="bf780-141">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="bf780-142">Si no está establecido el indicador MAPI_UNICODE., el nombre de la carpeta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="bf780-142">If the MAPI_UNICODE flag is not set, the name of the folder is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bf780-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf780-143">Return value</span></span>

<span data-ttu-id="bf780-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="bf780-144">S_OK</span></span> 
  
> <span data-ttu-id="bf780-145">La carpeta se ha copiado o movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="bf780-145">The folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="bf780-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="bf780-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="bf780-147">El nombre de la carpeta que se va a mover o copiar es el mismo que el de una subcarpeta en la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="bf780-147">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="bf780-148">El proveedor de almacén de mensajes requiere que los nombres de carpeta ser únicos.</span><span class="sxs-lookup"><span data-stu-id="bf780-148">The message store provider requires that folder names be unique.</span></span> <span data-ttu-id="bf780-149">Detiene la operación sin completar.</span><span class="sxs-lookup"><span data-stu-id="bf780-149">The operation stops without completing.</span></span>
    
<span data-ttu-id="bf780-150">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="bf780-150">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="bf780-151">La llamada se ha realizado correctamente, pero no todas las entradas se copiaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="bf780-151">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="bf780-152">Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="bf780-152">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="bf780-153">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="bf780-153">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="bf780-154">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="bf780-154">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf780-155">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf780-155">Remarks</span></span>

<span data-ttu-id="bf780-156">El método **IMAPISupport::CopyFolder** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bf780-156">The **IMAPISupport::CopyFolder** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="bf780-157">Los proveedores de almacén de mensajes pueden llamar a **IMAPISupport::CopyFolder** en su implementación de [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) para copiar o mover una sola carpeta desde la carpeta principal de uno a otro.</span><span class="sxs-lookup"><span data-stu-id="bf780-157">Message store providers can call **IMAPISupport::CopyFolder** in their implementation of [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) to copy or move a single folder from one parent folder to another.</span></span> 
  
 <span data-ttu-id="bf780-158">**IMAPISupport::CopyFolder** agrega la carpeta que se ha movido o copiada como una subcarpeta de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="bf780-158">**IMAPISupport::CopyFolder** adds the copied or moved folder as a subfolder of the destination folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bf780-159">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="bf780-159">Notes to callers</span></span>

 <span data-ttu-id="bf780-160">**IMAPISupport::CopyFolder** permite cambiar el nombre y mover de carpetas y la copia o traslado de las subcarpetas de la carpeta afectada simultáneas.</span><span class="sxs-lookup"><span data-stu-id="bf780-160">**IMAPISupport::CopyFolder** allows simultaneous renaming and moving of folders and the copying or moving of subfolders of the affected folder.</span></span> <span data-ttu-id="bf780-161">Para copiar o mover todas las subcarpetas anidadas en la carpeta que se ha movido o copiada, pase el indicador COPY_SUBFOLDERS _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="bf780-161">To copy or move all subfolders nested in the copied or moved folder, pass the COPY_SUBFOLDERS flag in  _ulFlags_.</span></span> 
  
<span data-ttu-id="bf780-162">Esperar que el siguiente devolver valores en las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="bf780-162">Expect the following return values under the following conditions:</span></span>
  
|<span data-ttu-id="bf780-163">**Condición**</span><span class="sxs-lookup"><span data-stu-id="bf780-163">**Condition**</span></span>|<span data-ttu-id="bf780-164">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="bf780-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bf780-165">**CopyFolder** correctamente copiado o había movido la carpeta y todas sus subcarpetas, si procede.</span><span class="sxs-lookup"><span data-stu-id="bf780-165">**CopyFolder** successfully copied or moved the folder and all its subfolders, if applicable.</span></span>  <br/> |<span data-ttu-id="bf780-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="bf780-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="bf780-167">**CopyFolder** no pudo copiar o mover todas las carpetas correctamente.</span><span class="sxs-lookup"><span data-stu-id="bf780-167">**CopyFolder** was unable to successfully copy or move all of the folders.</span></span>  <br/> |<span data-ttu-id="bf780-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="bf780-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="bf780-169">**CopyFolder** no pudo completar.</span><span class="sxs-lookup"><span data-stu-id="bf780-169">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="bf780-170">Cualquier valor de error</span><span class="sxs-lookup"><span data-stu-id="bf780-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="bf780-171">Si **CopyFolder** devuelve un valor de error, no continúe en la suposición de que se ha realizado ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="bf780-171">If **CopyFolder** returns an error value, do not proceed on the assumption that no work was done.</span></span> <span data-ttu-id="bf780-172">Una o varias carpetas podrían se han copiado o movido antes de **CopyFolder** tuvo el error.</span><span class="sxs-lookup"><span data-stu-id="bf780-172">One or more folders could have been copied or moved before **CopyFolder** experienced the failure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf780-173">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="bf780-173">See also</span></span>



[<span data-ttu-id="bf780-174">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bf780-174">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

