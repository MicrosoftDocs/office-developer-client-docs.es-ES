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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417409"
---
# <a name="imapifolderdeletefolder"></a><span data-ttu-id="e510a-103">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="e510a-103">IMAPIFolder::DeleteFolder</span></span>

  
  
<span data-ttu-id="e510a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e510a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e510a-105">Elimina una subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="e510a-105">Deletes a subfolder.</span></span>
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e510a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e510a-106">Parameters</span></span>

 <span data-ttu-id="e510a-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e510a-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="e510a-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e510a-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e510a-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e510a-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="e510a-110">a Un puntero al identificador de entrada de la subcarpeta que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="e510a-110">[in] A pointer to the entry identifier of the subfolder to delete.</span></span>
    
 <span data-ttu-id="e510a-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e510a-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="e510a-112">a Identificador de la ventana primaria del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="e510a-112">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="e510a-113">El parámetro _ulUIParam_ se omite a menos que se establezca la marca FOLDER_DIALOG en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="e510a-113">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="e510a-114">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="e510a-114">_lpProgress_</span></span>
  
> <span data-ttu-id="e510a-115">a Un puntero a un objeto Progress que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="e510a-115">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="e510a-116">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI.</span><span class="sxs-lookup"><span data-stu-id="e510a-116">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="e510a-117">El parámetro _lpProgress_ se omite a menos que se establezca la marca FOLDER_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="e510a-117">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="e510a-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e510a-118">_ulFlags_</span></span>
  
> <span data-ttu-id="e510a-119">a Máscara de máscara de marcadores que controla la eliminación de la subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="e510a-119">[in] A bitmask of flags that controls the deletion of the subfolder.</span></span> <span data-ttu-id="e510a-120">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="e510a-120">The following flags can be set:</span></span>
    
<span data-ttu-id="e510a-121">DEL_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="e510a-121">DEL_FOLDERS</span></span> 
  
> <span data-ttu-id="e510a-122">Se deben eliminar todas las subcarpetas de la subcarpeta a la que apunta _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e510a-122">All subfolders of the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="e510a-123">DEL_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="e510a-123">DEL_MESSAGES</span></span> 
  
> <span data-ttu-id="e510a-124">Se deben eliminar todos los mensajes de la subcarpeta a la que apunta _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e510a-124">All messages in the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="e510a-125">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e510a-125">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="e510a-126">Un indicador de progreso debería mostrarse mientras la operación continúa.</span><span class="sxs-lookup"><span data-stu-id="e510a-126">A progress indicator should be displayed while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e510a-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e510a-127">Return value</span></span>

<span data-ttu-id="e510a-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="e510a-128">S_OK</span></span> 
  
> <span data-ttu-id="e510a-129">La carpeta especificada se ha eliminado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e510a-129">The specified folder has been successfully deleted.</span></span>
    
<span data-ttu-id="e510a-130">MAPI_E_HAS_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="e510a-130">MAPI_E_HAS_FOLDERS</span></span> 
  
> <span data-ttu-id="e510a-131">La subcarpeta que se va a eliminar contiene subcarpetas y no se ha establecido la marca DEL_FOLDERS.</span><span class="sxs-lookup"><span data-stu-id="e510a-131">The subfolder being deleted contains subfolders, and the DEL_FOLDERS flag was not set.</span></span> <span data-ttu-id="e510a-132">Las subcarpetas no se eliminaron.</span><span class="sxs-lookup"><span data-stu-id="e510a-132">The subfolders were not deleted.</span></span>
    
<span data-ttu-id="e510a-133">MAPI_E_HAS_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="e510a-133">MAPI_E_HAS_MESSAGES</span></span> 
  
> <span data-ttu-id="e510a-134">La subcarpeta que se va a eliminar contiene mensajes y no se ha establecido la marca DEL_MESSAGES.</span><span class="sxs-lookup"><span data-stu-id="e510a-134">The subfolder being deleted contains messages, and the DEL_MESSAGES flag was not set.</span></span> <span data-ttu-id="e510a-135">No se eliminó la subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="e510a-135">The subfolder was not deleted.</span></span>
    
<span data-ttu-id="e510a-136">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="e510a-136">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="e510a-137">La llamada se realizó correctamente, pero no todas las entradas se eliminaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="e510a-137">The call succeeded, but not all of the entries were successfully deleted.</span></span> <span data-ttu-id="e510a-138">Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta.</span><span class="sxs-lookup"><span data-stu-id="e510a-138">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="e510a-139">Para probar esta advertencia, use la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="e510a-139">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="e510a-140">Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="e510a-140">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e510a-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e510a-141">Remarks</span></span>

<span data-ttu-id="e510a-142">El método **IMAPIFolder::D eletefolder** elimina una subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="e510a-142">The **IMAPIFolder::DeleteFolder** method deletes a subfolder.</span></span> <span data-ttu-id="e510a-143">De forma predeterminada, **DeleteFolder** solo funciona en carpetas vacías, pero puede usarla correctamente en carpetas no vacías estableciendo dos marcas: DEL_FOLDERS y DEL_MESSAGES.</span><span class="sxs-lookup"><span data-stu-id="e510a-143">By default, **DeleteFolder** operates only on empty folders, but you can use it successfully on non-empty folders by setting two flags: DEL_FOLDERS and DEL_MESSAGES.</span></span> <span data-ttu-id="e510a-144">Solo se pueden eliminar las carpetas o carpetas vacías que configuran las marcas DEL_FOLDERS y DEL_MESSAGES en la llamada de **DeleteFolder** .</span><span class="sxs-lookup"><span data-stu-id="e510a-144">Only empty folders or folders that set both the DEL_FOLDERS and DEL_MESSAGES flags on the **DeleteFolder** call can be deleted.</span></span> <span data-ttu-id="e510a-145">DEL_FOLDERS permite quitar todas las subcarpetas de la carpeta; DEL_MESSAGES permite quitar todos los mensajes de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e510a-145">DEL_FOLDERS enables all of the folder's subfolders to be removed; DEL_MESSAGES enables all of the folder's messages to be removed.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e510a-146">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="e510a-146">Notes to implementers</span></span>

<span data-ttu-id="e510a-147">Cuando la operación de eliminación implica más de una carpeta, realice la operación lo más completamente posible para cada carpeta.</span><span class="sxs-lookup"><span data-stu-id="e510a-147">When the delete operation involves more than one folder, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="e510a-148">A veces, una de las carpetas que se eliminan no existe o se ha movido o copiado en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="e510a-148">Sometimes one of the folders to be deleted does not exist or has been moved or copied elsewhere.</span></span> <span data-ttu-id="e510a-149">No detenga la operación prematuramente a menos que se produzca un error que esté más allá del control, como la falta de memoria, la falta de espacio en disco o que esté dañada en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e510a-149">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e510a-150">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="e510a-150">Notes to callers</span></span>

<span data-ttu-id="e510a-151">Espere estos valores devueltos en las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="e510a-151">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="e510a-152">**Condición**</span><span class="sxs-lookup"><span data-stu-id="e510a-152">**Condition**</span></span>|<span data-ttu-id="e510a-153">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="e510a-153">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e510a-154">**DeleteFolder** ha eliminado correctamente todos los mensajes y subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="e510a-154">**DeleteFolder** has successfully deleted every message and subfolder.</span></span>  <br/> |<span data-ttu-id="e510a-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="e510a-155">S_OK</span></span>  <br/> |
|<span data-ttu-id="e510a-156">**DeleteFolder** no pudo eliminar correctamente todos los mensajes y subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="e510a-156">**DeleteFolder** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="e510a-157">MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e510a-157">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="e510a-158">**DeleteFolder** no se pudo completar.</span><span class="sxs-lookup"><span data-stu-id="e510a-158">**DeleteFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="e510a-159">Cualquier valor de error excepto MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e510a-159">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="e510a-160">Cuando **DeleteFolder** no pueda completarse, no dé por supuesto que no se ha realizado ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="e510a-160">When **DeleteFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="e510a-161">Es posible que **DeleteFolder** haya podido eliminar uno o varios mensajes y subcarpetas antes de que se produzca el error.</span><span class="sxs-lookup"><span data-stu-id="e510a-161">**DeleteFolder** might have been able to delete one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="e510a-162">Si no se pueden eliminar una o varias subcarpetas, **DeleteFolder** devuelve MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND, en función de la implementación del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e510a-162">If one or more subfolders cannot be deleted, **DeleteFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store provider's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e510a-163">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e510a-163">MFCMAPI reference</span></span>

<span data-ttu-id="e510a-164">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e510a-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e510a-165">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="e510a-165">**File**</span></span>|<span data-ttu-id="e510a-166">**Función**</span><span class="sxs-lookup"><span data-stu-id="e510a-166">**Function**</span></span>|<span data-ttu-id="e510a-167">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="e510a-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e510a-168">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="e510a-168">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="e510a-169">CMsgStoreDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="e510a-169">CMsgStoreDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="e510a-170">MFCMAPI usa el método **IMAPIFolder::D eletefolder** para eliminar carpetas.</span><span class="sxs-lookup"><span data-stu-id="e510a-170">MFCMAPI uses the **IMAPIFolder::DeleteFolder** method to delete folders.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e510a-171">Ver también</span><span class="sxs-lookup"><span data-stu-id="e510a-171">See also</span></span>



[<span data-ttu-id="e510a-172">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="e510a-172">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="e510a-173">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="e510a-173">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

