---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 15cf8ff7e282035ddff53565aa92e81e3886729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817224"
---
# <a name="imapifolderdeletefolder"></a><span data-ttu-id="518a4-103">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="518a4-103">IMAPIFolder::DeleteFolder</span></span>

  
  
<span data-ttu-id="518a4-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="518a4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="518a4-105">Elimina una subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="518a4-105">Deletes a subfolder.</span></span>
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="518a4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="518a4-106">Parameters</span></span>

 <span data-ttu-id="518a4-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="518a4-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="518a4-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="518a4-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="518a4-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="518a4-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="518a4-110">[entrada] Un puntero al identificador de entrada de la subcarpeta para eliminar.</span><span class="sxs-lookup"><span data-stu-id="518a4-110">[in] A pointer to the entry identifier of the subfolder to delete.</span></span>
    
 <span data-ttu-id="518a4-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="518a4-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="518a4-112">[entrada] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="518a4-112">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="518a4-113">El parámetro _ulUIParam_ se omite a menos que se establece la marca FOLDER_DIALOG en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="518a4-113">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="518a4-114">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="518a4-114">_lpProgress_</span></span>
  
> <span data-ttu-id="518a4-115">[entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="518a4-115">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="518a4-116">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI.</span><span class="sxs-lookup"><span data-stu-id="518a4-116">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="518a4-117">El parámetro _lpProgress_ se omite a menos que se establece la marca FOLDER_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="518a4-117">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="518a4-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="518a4-118">_ulFlags_</span></span>
  
> <span data-ttu-id="518a4-119">[entrada] Una máscara de bits de indicadores que controla la eliminación de la subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="518a4-119">[in] A bitmask of flags that controls the deletion of the subfolder.</span></span> <span data-ttu-id="518a4-120">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="518a4-120">The following flags can be set:</span></span>
    
<span data-ttu-id="518a4-121">DEL_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="518a4-121">DEL_FOLDERS</span></span> 
  
> <span data-ttu-id="518a4-122">Se deben eliminar todas las subcarpetas de la subcarpeta indicada por _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="518a4-122">All subfolders of the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="518a4-123">DEL_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="518a4-123">DEL_MESSAGES</span></span> 
  
> <span data-ttu-id="518a4-124">Se deben eliminar todos los mensajes en la subcarpeta que señala _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="518a4-124">All messages in the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="518a4-125">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="518a4-125">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="518a4-126">Debe mostrarse un indicador de progreso mientras se realiza la operación.</span><span class="sxs-lookup"><span data-stu-id="518a4-126">A progress indicator should be displayed while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="518a4-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="518a4-127">Return value</span></span>

<span data-ttu-id="518a4-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="518a4-128">S_OK</span></span> 
  
> <span data-ttu-id="518a4-129">La carpeta especificada se ha eliminado correctamente.</span><span class="sxs-lookup"><span data-stu-id="518a4-129">The specified folder has been successfully deleted.</span></span>
    
<span data-ttu-id="518a4-130">MAPI_E_HAS_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="518a4-130">MAPI_E_HAS_FOLDERS</span></span> 
  
> <span data-ttu-id="518a4-131">La subcarpeta que se va a eliminar contiene las subcarpetas y no se ha establecido el indicador DEL_FOLDERS.</span><span class="sxs-lookup"><span data-stu-id="518a4-131">The subfolder being deleted contains subfolders, and the DEL_FOLDERS flag was not set.</span></span> <span data-ttu-id="518a4-132">No se han eliminado las subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="518a4-132">The subfolders were not deleted.</span></span>
    
<span data-ttu-id="518a4-133">MAPI_E_HAS_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="518a4-133">MAPI_E_HAS_MESSAGES</span></span> 
  
> <span data-ttu-id="518a4-134">La subcarpeta que se va a eliminar contiene los mensajes, y no se ha establecido el indicador DEL_MESSAGES.</span><span class="sxs-lookup"><span data-stu-id="518a4-134">The subfolder being deleted contains messages, and the DEL_MESSAGES flag was not set.</span></span> <span data-ttu-id="518a4-135">No se ha eliminado la subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="518a4-135">The subfolder was not deleted.</span></span>
    
<span data-ttu-id="518a4-136">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="518a4-136">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="518a4-137">La llamada se ha realizado correctamente, pero no todas las entradas se eliminaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="518a4-137">The call succeeded, but not all of the entries were successfully deleted.</span></span> <span data-ttu-id="518a4-138">Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="518a4-138">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="518a4-139">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="518a4-139">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="518a4-140">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="518a4-140">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="518a4-141">Notas</span><span class="sxs-lookup"><span data-stu-id="518a4-141">Remarks</span></span>

<span data-ttu-id="518a4-142">El método **IMAPIFolder::DeleteFolder** elimina una subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="518a4-142">The **IMAPIFolder::DeleteFolder** method deletes a subfolder.</span></span> <span data-ttu-id="518a4-143">De forma predeterminada, **DeleteFolder** sólo funciona en las carpetas vacías, pero se puede usar correctamente en las carpetas no vacías mediante la configuración de dos indicadores: DEL_FOLDERS y DEL_MESSAGES.</span><span class="sxs-lookup"><span data-stu-id="518a4-143">By default, **DeleteFolder** operates only on empty folders, but you can use it successfully on non-empty folders by setting two flags: DEL_FOLDERS and DEL_MESSAGES.</span></span> <span data-ttu-id="518a4-144">Sólo carpetas vacías o carpetas que establecer los indicadores de la DEL_FOLDERS y la DEL_MESSAGES en la llamada **DeleteFolder** se pueden eliminar.</span><span class="sxs-lookup"><span data-stu-id="518a4-144">Only empty folders or folders that set both the DEL_FOLDERS and DEL_MESSAGES flags on the **DeleteFolder** call can be deleted.</span></span> <span data-ttu-id="518a4-145">DEL_FOLDERS habilita todas las subcarpetas de la carpeta que se va a quitar; DEL_MESSAGES permite que todos los mensajes de la carpeta que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="518a4-145">DEL_FOLDERS enables all of the folder's subfolders to be removed; DEL_MESSAGES enables all of the folder's messages to be removed.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="518a4-146">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="518a4-146">Notes to implementers</span></span>

<span data-ttu-id="518a4-147">Cuando la operación de eliminación implica más de una carpeta, realizar la operación más completo posible para cada carpeta.</span><span class="sxs-lookup"><span data-stu-id="518a4-147">When the delete operation involves more than one folder, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="518a4-148">En ocasiones, una de las carpetas que se va a eliminar no existe o se haya movido o copiado en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="518a4-148">Sometimes one of the folders to be deleted does not exist or has been moved or copied elsewhere.</span></span> <span data-ttu-id="518a4-149">No detiene la operación de forma prematura a menos que se produzca un error que está fuera de su control, como la falta de memoria, está quedando sin espacio en disco o daños en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="518a4-149">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="518a4-150">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="518a4-150">Notes to callers</span></span>

<span data-ttu-id="518a4-151">Espera a que estos valores devueltos en las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="518a4-151">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="518a4-152">**Condición**</span><span class="sxs-lookup"><span data-stu-id="518a4-152">**Condition**</span></span>|<span data-ttu-id="518a4-153">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="518a4-153">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="518a4-154">**DeleteFolder** ha eliminado correctamente todos los mensajes y subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="518a4-154">**DeleteFolder** has successfully deleted every message and subfolder.</span></span>  <br/> |<span data-ttu-id="518a4-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="518a4-155">S_OK</span></span>  <br/> |
|<span data-ttu-id="518a4-156">**DeleteFolder** no pudo eliminar correctamente todos los mensajes y subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="518a4-156">**DeleteFolder** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="518a4-157">MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="518a4-157">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="518a4-158">**DeleteFolder** no pudo completar.</span><span class="sxs-lookup"><span data-stu-id="518a4-158">**DeleteFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="518a4-159">Cualquier valor de error excepto MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="518a4-159">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="518a4-160">Cuando no se puede completar **DeleteFolder** , no asuma que se ha realizado ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="518a4-160">When **DeleteFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="518a4-161">Es posible que han sido **DeleteFolder** podrá eliminar uno o varios de los mensajes y subcarpetas antes de encontrar el error.</span><span class="sxs-lookup"><span data-stu-id="518a4-161">**DeleteFolder** might have been able to delete one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="518a4-162">Si no se puede eliminar una o varias subcarpetas, **DeleteFolder** devuelve MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND, dependiendo de la implementación del proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="518a4-162">If one or more subfolders cannot be deleted, **DeleteFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store provider's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="518a4-163">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="518a4-163">MFCMAPI reference</span></span>

<span data-ttu-id="518a4-164">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="518a4-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="518a4-165">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="518a4-165">**File**</span></span>|<span data-ttu-id="518a4-166">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="518a4-166">**Function**</span></span>|<span data-ttu-id="518a4-167">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="518a4-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="518a4-168">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="518a4-168">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="518a4-169">CMsgStoreDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="518a4-169">CMsgStoreDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="518a4-170">MFCMAPI usa el método **IMAPIFolder::DeleteFolder** para eliminar las carpetas.</span><span class="sxs-lookup"><span data-stu-id="518a4-170">MFCMAPI uses the **IMAPIFolder::DeleteFolder** method to delete folders.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="518a4-171">Ver también</span><span class="sxs-lookup"><span data-stu-id="518a4-171">See also</span></span>



[<span data-ttu-id="518a4-172">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="518a4-172">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="518a4-173">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="518a4-173">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

