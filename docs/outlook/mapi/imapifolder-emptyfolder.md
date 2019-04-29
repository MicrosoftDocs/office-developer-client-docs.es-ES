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
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416786"
---
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="87286-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="87286-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="87286-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87286-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87286-105">Elimina todos los mensajes y subcarpetas de una carpeta sin eliminar la carpeta en sí.</span><span class="sxs-lookup"><span data-stu-id="87286-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="87286-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="87286-106">Parameters</span></span>

 <span data-ttu-id="87286-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="87286-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="87286-108">a Identificador de la ventana primaria del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="87286-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="87286-109">El parámetro _ulUIParam_ se omite a menos que se establezca la marca FOLDER_DIALOG en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="87286-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="87286-110">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="87286-110">_lpProgress_</span></span>
  
> <span data-ttu-id="87286-111">a Un puntero a un objeto Progress que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="87286-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="87286-112">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI.</span><span class="sxs-lookup"><span data-stu-id="87286-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="87286-113">El parámetro _lpProgress_ se omite a menos que se establezca la marca FOLDER_DIALOG en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="87286-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="87286-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="87286-114">_ulFlags_</span></span>
  
> <span data-ttu-id="87286-115">a Una máscara de máscara de marcas que controla cómo se vacía la carpeta.</span><span class="sxs-lookup"><span data-stu-id="87286-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="87286-116">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="87286-116">The following flags can be set:</span></span>
    
<span data-ttu-id="87286-117">DEL_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="87286-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="87286-118">Elimina todas las subcarpetas, incluidas las subcarpetas que contienen mensajes con contenido asociado.</span><span class="sxs-lookup"><span data-stu-id="87286-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="87286-119">La marca DEL_ASSOCIATED solo tiene significado para la carpeta de nivel superior en la que actúa la llamada.</span><span class="sxs-lookup"><span data-stu-id="87286-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="87286-120">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="87286-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="87286-121">Elimina permanentemente todos los mensajes, incluidos los eliminados temporalmente.</span><span class="sxs-lookup"><span data-stu-id="87286-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="87286-122">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="87286-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="87286-123">Muestra un indicador de progreso mientras se lleva a cabo la operación.</span><span class="sxs-lookup"><span data-stu-id="87286-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="87286-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87286-124">Return value</span></span>

<span data-ttu-id="87286-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="87286-125">S_OK</span></span> 
  
> <span data-ttu-id="87286-126">La carpeta se vació correctamente.</span><span class="sxs-lookup"><span data-stu-id="87286-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="87286-127">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="87286-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="87286-128">La llamada se realizó correctamente, pero la carpeta no se vació completamente.</span><span class="sxs-lookup"><span data-stu-id="87286-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="87286-129">Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta.</span><span class="sxs-lookup"><span data-stu-id="87286-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="87286-130">Para probar esta advertencia, use la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="87286-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="87286-131">Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="87286-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="87286-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="87286-132">Remarks</span></span>

<span data-ttu-id="87286-133">El método **IMAPIFolder:: EmptyFolder** elimina todo el contenido de una carpeta sin eliminar la carpeta en sí.</span><span class="sxs-lookup"><span data-stu-id="87286-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="87286-134">Durante una llamada de **EmptyFolder** , no se eliminan los mensajes enviados.</span><span class="sxs-lookup"><span data-stu-id="87286-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="87286-135">El contenido asociado a una carpeta incluye mensajes que se usan para describir vistas, reglas, formularios personalizados y almacenamiento de soluciones personalizado, y también puede incluir definiciones de formulario.</span><span class="sxs-lookup"><span data-stu-id="87286-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="87286-136">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="87286-136">Notes to implementers</span></span>

<span data-ttu-id="87286-137">No llame al método [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) para los mensajes de la carpeta que se han enviado.</span><span class="sxs-lookup"><span data-stu-id="87286-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="87286-138">Los mensajes enviados no se eliminan.</span><span class="sxs-lookup"><span data-stu-id="87286-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="87286-139">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="87286-139">Notes to callers</span></span>

<span data-ttu-id="87286-140">Espere estos valores devueltos en las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="87286-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="87286-141">**Condición**</span><span class="sxs-lookup"><span data-stu-id="87286-141">**Condition**</span></span>|<span data-ttu-id="87286-142">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="87286-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="87286-143">**EmptyFolder** ha vaciado la carpeta correctamente.</span><span class="sxs-lookup"><span data-stu-id="87286-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="87286-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="87286-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="87286-145">**EmptyFolder** no pudo vaciar por completo la carpeta.</span><span class="sxs-lookup"><span data-stu-id="87286-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="87286-146">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="87286-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="87286-147">**EmptyFolder** no se pudo completar.</span><span class="sxs-lookup"><span data-stu-id="87286-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="87286-148">Cualquier valor de error</span><span class="sxs-lookup"><span data-stu-id="87286-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="87286-149">Cuando **EmptyFolder** no pueda completarse, no dé por supuesto que no se ha realizado ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="87286-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="87286-150">Es posible que **EmptyFolder** haya podido eliminar parte del contenido de la carpeta antes de que se produzca el error.</span><span class="sxs-lookup"><span data-stu-id="87286-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="87286-151">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="87286-151">MFCMAPI reference</span></span>

<span data-ttu-id="87286-152">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="87286-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="87286-153">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="87286-153">**File**</span></span>|<span data-ttu-id="87286-154">**Función**</span><span class="sxs-lookup"><span data-stu-id="87286-154">**Function**</span></span>|<span data-ttu-id="87286-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="87286-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="87286-156">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="87286-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="87286-157">CMsgStoreDlg:: OnEmptyFolder</span><span class="sxs-lookup"><span data-stu-id="87286-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="87286-158">MFCMAPI usa el método **IMAPIFolder:: EmptyFolder** para eliminar el contenido de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="87286-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87286-159">Ver también</span><span class="sxs-lookup"><span data-stu-id="87286-159">See also</span></span>



[<span data-ttu-id="87286-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="87286-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="87286-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="87286-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="87286-162">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="87286-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="87286-163">Uso de macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="87286-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

