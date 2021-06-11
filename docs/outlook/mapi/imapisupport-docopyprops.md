---
title: IMAPISupportDoCopyProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 24107ae1926c8590da6a823a354eeae72d72f248
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405586"
---
# <a name="imapisupportdocopyprops"></a><span data-ttu-id="dee66-103">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="dee66-103">IMAPISupport::DoCopyProps</span></span>

  
  
<span data-ttu-id="dee66-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dee66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dee66-105">Copia o mueve una o más propiedades de un objeto a otro objeto.</span><span class="sxs-lookup"><span data-stu-id="dee66-105">Copies or moves one or more properties of an object to another object.</span></span>
  
```cpp
HRESULT DoCopyProps(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="dee66-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="dee66-106">Parameters</span></span>

 <span data-ttu-id="dee66-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="dee66-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="dee66-108">[in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto con las propiedades que se van a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="dee66-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object with the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="dee66-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="dee66-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="dee66-110">[in] Puntero al objeto que contiene las propiedades que se van a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="dee66-110">[in] A pointer to the object that contains the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="dee66-111">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="dee66-111">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="dee66-112">[in] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene una matriz contada de etiquetas de propiedades que indican las propiedades que se copian o se mueven.</span><span class="sxs-lookup"><span data-stu-id="dee66-112">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains a counted array of property tags that indicate the properties to copy or move.</span></span> <span data-ttu-id="dee66-113">El  _parámetro lpIncludeProps_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="dee66-113">The  _lpIncludeProps_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="dee66-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="dee66-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="dee66-115">[in] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="dee66-115">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="dee66-116">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="dee66-116">_lpProgress_</span></span>
  
> <span data-ttu-id="dee66-117">[in] Puntero a una implementación de un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="dee66-117">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="dee66-118">Si se pasa NULL en el  _parámetro lpProgress,_ el indicador de progreso se muestra mediante la implementación MAPI.</span><span class="sxs-lookup"><span data-stu-id="dee66-118">If NULL is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="dee66-119">El _parámetro lpProgress_ se omite a menos que MAPI_DIALOG marca se establezca en _el parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="dee66-119">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="dee66-120">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="dee66-120">_lpDestInterface_</span></span>
  
> <span data-ttu-id="dee66-121">[in] Puntero al identificador de interfaz que representa la interfaz que se va a usar para obtener acceso al objeto para recibir las propiedades que se copian o se mueven.</span><span class="sxs-lookup"><span data-stu-id="dee66-121">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the properties that are copied or moved.</span></span>
    
 <span data-ttu-id="dee66-122">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="dee66-122">_lpDestObj_</span></span>
  
> <span data-ttu-id="dee66-123">[in] Puntero al objeto para recibir las propiedades copiadas o movida.</span><span class="sxs-lookup"><span data-stu-id="dee66-123">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="dee66-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dee66-124">_ulFlags_</span></span>
  
> <span data-ttu-id="dee66-125">[in] Máscara de bits de marcas que controla cómo se realiza la operación de copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="dee66-125">[in] A bitmask of flags that controls how the copy or move operation is performed.</span></span> <span data-ttu-id="dee66-126">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="dee66-126">The following flags can be set:</span></span>
    
<span data-ttu-id="dee66-127">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="dee66-127">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="dee66-128">Muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="dee66-128">Displays a progress indicator.</span></span>
    
<span data-ttu-id="dee66-129">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="dee66-129">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="dee66-130">**DoCopyProps debe** realizar una operación de movimiento en lugar de una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="dee66-130">**DoCopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="dee66-131">Cuando no se establece esta marca, **DoCopyProps** realiza una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="dee66-131">When this flag is not set, **DoCopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="dee66-132">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="dee66-132">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="dee66-133">Las propiedades existentes en el objeto de destino no deben sobrescribirse.</span><span class="sxs-lookup"><span data-stu-id="dee66-133">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="dee66-134">Cuando no se establece esta marca, **DoCopyProps** sobrescribe las propiedades existentes.</span><span class="sxs-lookup"><span data-stu-id="dee66-134">When this flag is not set, **DoCopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="dee66-135">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="dee66-135">_lppProblems_</span></span>
  
> <span data-ttu-id="dee66-136">[in, out] En la entrada, un puntero a un puntero a una [estructura SPropProblemArray;](spropproblemarray.md) en caso contrario, NULL, que indica que no es necesario obtener información de error.</span><span class="sxs-lookup"><span data-stu-id="dee66-136">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="dee66-137">Si  _lppProblems_ es un puntero válido en la entrada, **DoCopyProps** devuelve información detallada acerca de los errores al copiar una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="dee66-137">If  _lppProblems_ is a valid pointer on input, **DoCopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dee66-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dee66-138">Return value</span></span>

<span data-ttu-id="dee66-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="dee66-139">S_OK</span></span> 
  
> <span data-ttu-id="dee66-140">Las propiedades se copiaron o se movieron correctamente.</span><span class="sxs-lookup"><span data-stu-id="dee66-140">Properties were successfully copied or moved.</span></span>
    
<span data-ttu-id="dee66-141">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="dee66-141">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="dee66-142">Una propiedad que se va a copiar o mover ya existe en el objeto de destino y se establece MAPI_NOREPLACE marca.</span><span class="sxs-lookup"><span data-stu-id="dee66-142">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="dee66-143">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="dee66-143">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="dee66-144">El objeto de origen contiene directa o indirectamente el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="dee66-144">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="dee66-145">Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que los objetos de origen y de destino podrían modificarse parcialmente.</span><span class="sxs-lookup"><span data-stu-id="dee66-145">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="dee66-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="dee66-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="dee66-147">La interfaz identificada por el parámetro  _lpSrcInterface_ no es compatible con el objeto de origen o la interfaz identificada por el parámetro  _lpDestInterface_ no es compatible con el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="dee66-147">The interface identified by the  _lpSrcInterface_ parameter is not supported by the source object, or the interface identified by the  _lpDestInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="dee66-148">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="dee66-148">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="dee66-149">Se intentó obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="dee66-149">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="dee66-150">Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="dee66-150">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="dee66-151">Los siguientes valores se pueden devolver en la estructura **SPropProblemArray,** pero no como valores devueltos para **DoCopyProps**.</span><span class="sxs-lookup"><span data-stu-id="dee66-151">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyProps**.</span></span> <span data-ttu-id="dee66-152">Estos errores se aplican a una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="dee66-152">These errors apply to a single property.</span></span>
  
<span data-ttu-id="dee66-153">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="dee66-153">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="dee66-154">La marca MAPI_UNICODE se estableció y **DoCopyProps** no admite Unicode o MAPI_UNICODE no se estableció y **DoCopyProps** solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="dee66-154">Either the MAPI_UNICODE flag was set and **DoCopyProps** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="dee66-155">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="dee66-155">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="dee66-156">El autor de la llamada no puede modificar la propiedad porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="dee66-156">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="dee66-157">Este error no es grave; el autor de la llamada debe permitir que la operación de copia continúe.</span><span class="sxs-lookup"><span data-stu-id="dee66-157">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="dee66-158">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="dee66-158">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="dee66-159">El tipo de propiedad no es válido.</span><span class="sxs-lookup"><span data-stu-id="dee66-159">The property type is invalid.</span></span>
    
<span data-ttu-id="dee66-160">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="dee66-160">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="dee66-161">El tipo de propiedad no es el tipo que espera el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="dee66-161">The property type is not the type that the caller expects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dee66-162">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dee66-162">Remarks</span></span>

<span data-ttu-id="dee66-163">El **método IMAPISupport::D oCopyProps** se implementa para objetos de soporte técnico del proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="dee66-163">The **IMAPISupport::DoCopyProps** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="dee66-164">Los proveedores de almacén de mensajes pueden llamar **a DoCopyProps** para implementar el método [IMAPIProp::CopyProps](imapiprop-copyprops.md) para sus carpetas y mensajes.</span><span class="sxs-lookup"><span data-stu-id="dee66-164">Message store providers can call **DoCopyProps** to implement the [IMAPIProp::CopyProps](imapiprop-copyprops.md) method for their folders and messages.</span></span> <span data-ttu-id="dee66-165">**DoCopyProps** copia o mueve las propiedades identificadas en la matriz de etiquetas de propiedades apuntadas por  _lpIncludeProps_ y que están presentes en el objeto señalado por  _lpSrcObj_.</span><span class="sxs-lookup"><span data-stu-id="dee66-165">**DoCopyProps** copies or moves the properties that are identified in the property tag array pointed to by  _lpIncludeProps_ and that are present in the object pointed to by  _lpSrcObj_.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dee66-166">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="dee66-166">Notes to callers</span></span>

<span data-ttu-id="dee66-167">Al copiar propiedades entre objetos del mismo tipo, como dos mensajes, los parámetros  _lpSrcInterface_ y  _lpDestInterface_ deben contener el mismo identificador de interfaz y los parámetros  _lpSrcObj_ y  _lpDestObj_ deben apuntar a objetos del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="dee66-167">When you copy properties between objects of the same type, such as two messages, the  _lpSrcInterface_ and  _lpDestInterface_ parameters must contain the same interface identifier, and the  _lpSrcObj_ and  _lpDestObj_ parameters must point to objects of the same type.</span></span> <span data-ttu-id="dee66-168">Si  _lpDestInterface_ se establece en NULL, **DoCopyProps** devuelve MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="dee66-168">If  _lpDestInterface_ is set to NULL, **DoCopyProps** returns MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="dee66-169">Si establece  _lpDestInterface_ en un identificador de interfaz aceptable, pero establece  _lpDestObj_ en un puntero no válido, los resultados son impredecibles.</span><span class="sxs-lookup"><span data-stu-id="dee66-169">If you set  _lpDestInterface_ to an acceptable interface identifier, but set  _lpDestObj_ to an invalid pointer, the results are unpredictable.</span></span> <span data-ttu-id="dee66-170">Lo más probable es que el proveedor falle.</span><span class="sxs-lookup"><span data-stu-id="dee66-170">Most likely your provider will fail.</span></span> 
  
<span data-ttu-id="dee66-171">Establezca la MAPI_NOREPLACE si no desea que se sobrescriba ninguna de las propiedades del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="dee66-171">Set the MAPI_NOREPLACE flag if you do not want any of the properties in the destination object to be overwritten.</span></span> <span data-ttu-id="dee66-172">Las propiedades del objeto de destino que existen en el objeto de origen y no se sobrescriben no se eliminan ni modifican.</span><span class="sxs-lookup"><span data-stu-id="dee66-172">Properties in the destination object that exist in the source object and are not overwritten are not deleted or modified.</span></span>
  
<span data-ttu-id="dee66-173">Para copiar la lista de destinatarios de un mensaje, incluya la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) en la matriz de etiquetas de propiedad a la que apunta el parámetro _lpIncludeProps._</span><span class="sxs-lookup"><span data-stu-id="dee66-173">To copy a message's recipient list, include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array pointed to by the  _lpIncludeProps_ parameter.</span></span> <span data-ttu-id="dee66-174">Para copiar los datos adjuntos del mensaje, incluya **la propiedad PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dee66-174">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="dee66-175">Para copiar la jerarquía o la tabla de contenido de un contenedor de carpeta o libreta de direcciones, incluya **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la matriz de etiquetas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="dee66-175">To copy a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag array.</span></span> <span data-ttu-id="dee66-176">Para incluir la tabla de contenido asociada de una carpeta, incluya la propiedad **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) en la matriz.</span><span class="sxs-lookup"><span data-stu-id="dee66-176">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span>
  
<span data-ttu-id="dee66-177">Si las subcarpetas se copian o se mueven, su contenido se copia o se mueve en su totalidad, independientemente del uso de las propiedades indicadas por la estructura **SPropTagArray.**</span><span class="sxs-lookup"><span data-stu-id="dee66-177">If subfolders are copied or moved, their contents are copied or moved in their entirety, regardless of the use of properties indicated by the **SPropTagArray** structure.</span></span> 
  
 <span data-ttu-id="dee66-178">**DoCopyProps notifica** los errores globales que se producen con la operación en su conjunto y los errores individuales que se producen con una o varias de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="dee66-178">**DoCopyProps** reports global errors that occur with the operation as a whole, and individual errors that occur with one or more of the properties.</span></span> <span data-ttu-id="dee66-179">Estos errores individuales se ponen en una **estructura SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="dee66-179">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="dee66-180">Puede suprimir los informes de errores en el nivel de propiedad pasando NULL, en lugar de un puntero válido, para el parámetro de estructura de matriz de problemas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="dee66-180">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="dee66-181">Si desea recibir información sobre errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems._</span><span class="sxs-lookup"><span data-stu-id="dee66-181">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="dee66-182">Cuando **DoCopyProps** devuelve S_OK, compruebe si hay posibles errores con propiedades individuales en la estructura.</span><span class="sxs-lookup"><span data-stu-id="dee66-182">When **DoCopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="dee66-183">Cuando **DoCopyProps** devuelve un error, no se devuelve información en la estructura **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="dee66-183">When **DoCopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="dee66-184">En su lugar, llame [al método IMAPISupport::GetLastError](imapisupport-getlasterror.md) para recuperar información de error detallada.</span><span class="sxs-lookup"><span data-stu-id="dee66-184">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="dee66-185">Si **DoCopyProps** devuelve S_OK, libera la estructura **SPropProblemArray** devuelta llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="dee66-185">If **DoCopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dee66-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="dee66-186">See also</span></span>



[<span data-ttu-id="dee66-187">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="dee66-187">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
  
[<span data-ttu-id="dee66-188">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="dee66-188">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="dee66-189">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="dee66-189">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="dee66-190">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="dee66-190">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="dee66-191">Propiedad canónica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="dee66-191">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="dee66-192">Propiedad canónica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="dee66-192">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="dee66-193">Propiedad canónica PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="dee66-193">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="dee66-194">Propiedad canónica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="dee66-194">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="dee66-195">Propiedad canónica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="dee66-195">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="dee66-196">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="dee66-196">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="dee66-197">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="dee66-197">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="dee66-198">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dee66-198">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

