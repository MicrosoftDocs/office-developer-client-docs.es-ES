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
ms.openlocfilehash: 11ee944a14f8c9bd881b9c79a4ce66817275e73a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420888"
---
# <a name="imapisupportcopyfolder"></a><span data-ttu-id="1136a-103">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="1136a-103">IMAPISupport::CopyFolder</span></span>

  
  
<span data-ttu-id="1136a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1136a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1136a-105">Copia o mueve una carpeta de su carpeta principal actual a otra carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="1136a-105">Copies or moves a folder from its current parent folder to another parent folder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1136a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1136a-106">Parameters</span></span>

 <span data-ttu-id="1136a-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="1136a-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="1136a-108">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta principal de la carpeta que se va a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="1136a-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the parent folder of the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="1136a-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="1136a-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="1136a-110">[entrada] Puntero a la carpeta principal de la carpeta que se va a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="1136a-110">[in] A pointer to the parent folder of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="1136a-111">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1136a-111">_cbEntryID_</span></span>
  
> <span data-ttu-id="1136a-112">[entrada] El recuento de bytes en el identificador de entrada al que apunta  _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="1136a-112">[in] The byte count in the entry identifier pointed to by  _lpEntryID_.</span></span>
    
 <span data-ttu-id="1136a-113">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1136a-113">_lpEntryID_</span></span>
  
> <span data-ttu-id="1136a-114">[entrada] Puntero al identificador de entrada de la carpeta que se va a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="1136a-114">[in] A pointer to the entry identifier of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="1136a-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1136a-115">_lpInterface_</span></span>
  
> <span data-ttu-id="1136a-116">[entrada] Reservado; debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="1136a-116">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="1136a-117">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="1136a-117">_lpDestFolder_</span></span>
  
> <span data-ttu-id="1136a-118">[entrada] Puntero a la carpeta que va a recibir la carpeta que se va a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="1136a-118">[in] A pointer to the folder that is to receive the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="1136a-119">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="1136a-119">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="1136a-120">[entrada] Puntero al nombre de la carpeta copiada o movida; de lo contrario, NULL, que indica que la carpeta copiada o movida debe tener el mismo nombre que la carpeta de origen (la carpeta a la que  _apunta lpEntryID_).</span><span class="sxs-lookup"><span data-stu-id="1136a-120">[in] A pointer to the name of the copied or moved folder; otherwise, NULL, which indicates that the copied or moved folder should have the same name as the source folder (the folder pointed to by  _lpEntryID_).</span></span>
    
 <span data-ttu-id="1136a-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1136a-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="1136a-122">[entrada] Identificador de la ventana para el cuadro de diálogo del indicador de progreso y las ventanas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1136a-122">[in] A handle of the window for the progress indicator dialog box and related windows.</span></span> <span data-ttu-id="1136a-123">El _parámetro ulUIParam_ se omite a menos FOLDER_DIALOG marca esté establecida en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="1136a-123">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="1136a-124">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="1136a-124">_lpProgress_</span></span>
  
> <span data-ttu-id="1136a-125">[entrada] Puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="1136a-125">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="1136a-126">Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso MAPI.</span><span class="sxs-lookup"><span data-stu-id="1136a-126">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="1136a-127">El  _parámetro lpProgress_ se omite a menos que FOLDER_DIALOG marca esté establecida en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="1136a-127">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="1136a-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1136a-128">_ulFlags_</span></span>
  
> <span data-ttu-id="1136a-129">[entrada] Máscara de bits de marcas que controla cómo se realiza la operación de copia o movimiento.</span><span class="sxs-lookup"><span data-stu-id="1136a-129">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="1136a-130">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="1136a-130">The following flags can be set:</span></span>
    
<span data-ttu-id="1136a-131">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="1136a-131">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="1136a-132">Todas las subcarpetas de la carpeta deben copiarse o moverse.</span><span class="sxs-lookup"><span data-stu-id="1136a-132">All of the folder's subfolders should be copied or moved.</span></span> <span data-ttu-id="1136a-133">Cuando COPY_SUBFOLDERS no se establece para una operación de copia, solo se copia la carpeta identificada por _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="1136a-133">When COPY_SUBFOLDERS is not set for a copy operation, only the folder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="1136a-134">Con una operación de movimiento, COPY_SUBFOLDERS comportamiento predeterminado independientemente de si se establece la marca.</span><span class="sxs-lookup"><span data-stu-id="1136a-134">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="1136a-135">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1136a-135">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="1136a-136">Solicita la presentación de un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="1136a-136">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="1136a-137">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="1136a-137">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="1136a-138">La carpeta debe moverse en lugar de copiarse.</span><span class="sxs-lookup"><span data-stu-id="1136a-138">The folder should be moved instead of copied.</span></span> <span data-ttu-id="1136a-139">Si FOLDER_MOVE no se establece, se copia la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1136a-139">If FOLDER_MOVE is not set, the folder is copied.</span></span>
    
<span data-ttu-id="1136a-140">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1136a-140">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1136a-141">El nombre de la carpeta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1136a-141">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="1136a-142">Si no MAPI_UNICODE marca, el nombre de la carpeta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="1136a-142">If the MAPI_UNICODE flag is not set, the name of the folder is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1136a-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1136a-143">Return value</span></span>

<span data-ttu-id="1136a-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="1136a-144">S_OK</span></span> 
  
> <span data-ttu-id="1136a-145">La carpeta se ha copiado o movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="1136a-145">The folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="1136a-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="1136a-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="1136a-147">El nombre de la carpeta que se va a mover o copiar es el mismo que el de una subcarpeta de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="1136a-147">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="1136a-148">El proveedor del almacén de mensajes requiere que los nombres de carpeta sean únicos.</span><span class="sxs-lookup"><span data-stu-id="1136a-148">The message store provider requires that folder names be unique.</span></span> <span data-ttu-id="1136a-149">La operación se detiene sin completarse.</span><span class="sxs-lookup"><span data-stu-id="1136a-149">The operation stops without completing.</span></span>
    
<span data-ttu-id="1136a-150">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="1136a-150">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="1136a-151">La llamada se ha realizado correctamente, pero no todas las entradas se han copiado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1136a-151">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="1136a-152">Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="1136a-152">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="1136a-153">Para probar esta advertencia, use la **macro HR_FAILED** datos.</span><span class="sxs-lookup"><span data-stu-id="1136a-153">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="1136a-154">Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="1136a-154">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1136a-155">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1136a-155">Remarks</span></span>

<span data-ttu-id="1136a-156">El **método IMAPISupport::CopyFolder** se implementa para objetos de compatibilidad del proveedor de al almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1136a-156">The **IMAPISupport::CopyFolder** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="1136a-157">Los proveedores de almacenamiento de mensajes pueden llamar a **IMAPISupport::CopyFolder** en su implementación de [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) para copiar o mover una sola carpeta de una carpeta principal a otra.</span><span class="sxs-lookup"><span data-stu-id="1136a-157">Message store providers can call **IMAPISupport::CopyFolder** in their implementation of [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) to copy or move a single folder from one parent folder to another.</span></span> 
  
 <span data-ttu-id="1136a-158">**IMAPISupport::CopyFolder** agrega la carpeta copiada o movida como subcarpeta de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="1136a-158">**IMAPISupport::CopyFolder** adds the copied or moved folder as a subfolder of the destination folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1136a-159">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="1136a-159">Notes to callers</span></span>

 <span data-ttu-id="1136a-160">**IMAPISupport::CopyFolder** permite cambiar el nombre y mover las carpetas simultáneamente y copiar o mover subcarpetas de la carpeta afectada.</span><span class="sxs-lookup"><span data-stu-id="1136a-160">**IMAPISupport::CopyFolder** allows simultaneous renaming and moving of folders and the copying or moving of subfolders of the affected folder.</span></span> <span data-ttu-id="1136a-161">Para copiar o mover todas las subcarpetas anidadas en la carpeta copiada o movida, pase la marca COPY_SUBFOLDERS en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="1136a-161">To copy or move all subfolders nested in the copied or moved folder, pass the COPY_SUBFOLDERS flag in  _ulFlags_.</span></span> 
  
<span data-ttu-id="1136a-162">Espere los siguientes valores devueltos en las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="1136a-162">Expect the following return values under the following conditions:</span></span>
  
|<span data-ttu-id="1136a-163">**Condition**</span><span class="sxs-lookup"><span data-stu-id="1136a-163">**Condition**</span></span>|<span data-ttu-id="1136a-164">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="1136a-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1136a-165">**CopyFolder** copió o movió correctamente la carpeta y todas sus subcarpetas, si procede.</span><span class="sxs-lookup"><span data-stu-id="1136a-165">**CopyFolder** successfully copied or moved the folder and all its subfolders, if applicable.</span></span>  <br/> |<span data-ttu-id="1136a-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="1136a-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="1136a-167">**CopyFolder** no pudo copiar o mover correctamente todas las carpetas.</span><span class="sxs-lookup"><span data-stu-id="1136a-167">**CopyFolder** was unable to successfully copy or move all of the folders.</span></span>  <br/> |<span data-ttu-id="1136a-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="1136a-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="1136a-169">**CopyFolder** no se pudo completar.</span><span class="sxs-lookup"><span data-stu-id="1136a-169">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="1136a-170">Cualquier valor de error</span><span class="sxs-lookup"><span data-stu-id="1136a-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="1136a-171">Si **CopyFolder** devuelve un valor de error, no continúe con la suposición de que no se ha realizado ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="1136a-171">If **CopyFolder** returns an error value, do not proceed on the assumption that no work was done.</span></span> <span data-ttu-id="1136a-172">Una o varias carpetas se podrían haber copiado o movido antes de **que CopyFolder** experimentara el error.</span><span class="sxs-lookup"><span data-stu-id="1136a-172">One or more folders could have been copied or moved before **CopyFolder** experienced the failure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1136a-173">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1136a-173">See also</span></span>



[<span data-ttu-id="1136a-174">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1136a-174">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

