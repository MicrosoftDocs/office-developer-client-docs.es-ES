---
title: IMAPIFolderEmptyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 287577babc9a40b771aa9917211ba5dcbf8190ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584943"
---
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="53a8e-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="53a8e-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="53a8e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53a8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53a8e-105">Elimina todos los mensajes y subcarpetas de una carpeta sin eliminar la propia carpeta.</span><span class="sxs-lookup"><span data-stu-id="53a8e-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="53a8e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53a8e-106">Parameters</span></span>

 <span data-ttu-id="53a8e-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="53a8e-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="53a8e-108">[entrada] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="53a8e-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="53a8e-109">El parámetro _ulUIParam_ se omite a menos que se establece la marca FOLDER_DIALOG en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="53a8e-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="53a8e-110">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="53a8e-110">_lpProgress_</span></span>
  
> <span data-ttu-id="53a8e-111">[entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="53a8e-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="53a8e-112">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI.</span><span class="sxs-lookup"><span data-stu-id="53a8e-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="53a8e-113">El parámetro _lpProgress_ se omite a menos que se establece la marca FOLDER_DIALOG en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="53a8e-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="53a8e-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53a8e-114">_ulFlags_</span></span>
  
> <span data-ttu-id="53a8e-115">[entrada] Una máscara de bits de indicadores que controla cómo se vacía la carpeta.</span><span class="sxs-lookup"><span data-stu-id="53a8e-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="53a8e-116">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="53a8e-116">The following flags can be set:</span></span>
    
<span data-ttu-id="53a8e-117">DEL_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="53a8e-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="53a8e-118">Elimina todas las subcarpetas, incluidas las subcarpetas que contienen los mensajes con contenido asociado.</span><span class="sxs-lookup"><span data-stu-id="53a8e-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="53a8e-119">El indicador DEL_ASSOCIATED sólo tiene significado para la llamada actúa en la carpeta de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="53a8e-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="53a8e-120">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="53a8e-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="53a8e-121">Quita de forma permanente todos los mensajes, incluidos los eliminado temporalmente.</span><span class="sxs-lookup"><span data-stu-id="53a8e-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="53a8e-122">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="53a8e-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="53a8e-123">Muestra un indicador de progreso mientras se realiza la operación.</span><span class="sxs-lookup"><span data-stu-id="53a8e-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53a8e-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53a8e-124">Return value</span></span>

<span data-ttu-id="53a8e-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="53a8e-125">S_OK</span></span> 
  
> <span data-ttu-id="53a8e-126">La carpeta se ha vaciado correctamente.</span><span class="sxs-lookup"><span data-stu-id="53a8e-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="53a8e-127">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="53a8e-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="53a8e-128">La llamada se ha realizado correctamente, pero la carpeta no estaba totalmente vacía.</span><span class="sxs-lookup"><span data-stu-id="53a8e-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="53a8e-129">Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="53a8e-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="53a8e-130">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="53a8e-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="53a8e-131">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="53a8e-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53a8e-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53a8e-132">Remarks</span></span>

<span data-ttu-id="53a8e-133">El método **IMAPIFolder::EmptyFolder** elimina todos los del contenido de una carpeta sin eliminar la propia carpeta.</span><span class="sxs-lookup"><span data-stu-id="53a8e-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="53a8e-134">Durante una llamada **EmptyFolder** , no se eliminan los mensajes enviados.</span><span class="sxs-lookup"><span data-stu-id="53a8e-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="53a8e-135">Contenido asociados de una carpeta incluye los mensajes que se utilizan para describir las vistas, reglas, formularios personalizados y el almacenamiento de soluciones personalizadas y también pueden incluir las definiciones del formulario.</span><span class="sxs-lookup"><span data-stu-id="53a8e-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="53a8e-136">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="53a8e-136">Notes to implementers</span></span>

<span data-ttu-id="53a8e-137">No llame al método [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para los mensajes en la carpeta que se han enviado.</span><span class="sxs-lookup"><span data-stu-id="53a8e-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="53a8e-138">No se eliminan los mensajes enviados.</span><span class="sxs-lookup"><span data-stu-id="53a8e-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="53a8e-139">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="53a8e-139">Notes to callers</span></span>

<span data-ttu-id="53a8e-140">Espera a que estos valores devueltos en las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="53a8e-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="53a8e-141">**Condición**</span><span class="sxs-lookup"><span data-stu-id="53a8e-141">**Condition**</span></span>|<span data-ttu-id="53a8e-142">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="53a8e-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53a8e-143">**EmptyFolder** ha vaciado correctamente la carpeta.</span><span class="sxs-lookup"><span data-stu-id="53a8e-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="53a8e-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="53a8e-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="53a8e-145">**EmptyFolder** no pudo completamente vacíe la carpeta.</span><span class="sxs-lookup"><span data-stu-id="53a8e-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="53a8e-146">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="53a8e-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="53a8e-147">**EmptyFolder** no pudo completar.</span><span class="sxs-lookup"><span data-stu-id="53a8e-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="53a8e-148">Cualquier valor de error</span><span class="sxs-lookup"><span data-stu-id="53a8e-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="53a8e-149">Cuando no se puede completar **EmptyFolder** , no asuma que se ha realizado ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="53a8e-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="53a8e-150">Es posible que han sido **EmptyFolder** podrá eliminar parte del contenido de la carpeta antes de encontrar el error.</span><span class="sxs-lookup"><span data-stu-id="53a8e-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="53a8e-151">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="53a8e-151">MFCMAPI reference</span></span>

<span data-ttu-id="53a8e-152">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="53a8e-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="53a8e-153">**File**</span><span class="sxs-lookup"><span data-stu-id="53a8e-153">**File**</span></span>|<span data-ttu-id="53a8e-154">**Función**</span><span class="sxs-lookup"><span data-stu-id="53a8e-154">**Function**</span></span>|<span data-ttu-id="53a8e-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="53a8e-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="53a8e-156">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="53a8e-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="53a8e-157">CMsgStoreDlg::OnEmptyFolder</span><span class="sxs-lookup"><span data-stu-id="53a8e-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="53a8e-158">MFCMAPI usa el método **IMAPIFolder::EmptyFolder** para eliminar el contenido de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="53a8e-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53a8e-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="53a8e-159">See also</span></span>



[<span data-ttu-id="53a8e-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="53a8e-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="53a8e-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="53a8e-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="53a8e-162">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="53a8e-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="53a8e-163">Usar Macros para el tratamiento de errores</span><span class="sxs-lookup"><span data-stu-id="53a8e-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

