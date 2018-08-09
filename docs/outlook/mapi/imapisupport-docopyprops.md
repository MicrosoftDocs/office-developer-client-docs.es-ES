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
ms.openlocfilehash: c93e01b1e4621cddc4c98d528e5f5339cba21dae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817486"
---
# <a name="imapisupportdocopyprops"></a><span data-ttu-id="b2f2c-103">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="b2f2c-103">IMAPISupport::DoCopyProps</span></span>

  
  
<span data-ttu-id="b2f2c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2f2c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2f2c-105">Copia o mueve una o más propiedades de un objeto a otro objeto.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-105">Copies or moves one or more properties of an object to another object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b2f2c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2f2c-106">Parameters</span></span>

 <span data-ttu-id="b2f2c-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="b2f2c-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="b2f2c-108">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto con las propiedades que se pueden copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object with the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="b2f2c-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="b2f2c-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="b2f2c-110">[entrada] Un puntero al objeto que contiene las propiedades para ser copiado o movido.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-110">[in] A pointer to the object that contains the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="b2f2c-111">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="b2f2c-111">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="b2f2c-112">[entrada] Un puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz unidimensional de etiquetas de propiedad que indican las propiedades para copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-112">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains a counted array of property tags that indicate the properties to copy or move.</span></span> <span data-ttu-id="b2f2c-113">El parámetro _lpIncludeProps_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-113">The  _lpIncludeProps_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="b2f2c-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b2f2c-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="b2f2c-115">[entrada] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-115">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="b2f2c-116">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="b2f2c-116">_lpProgress_</span></span>
  
> <span data-ttu-id="b2f2c-117">[entrada] Un puntero a una implementación de un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-117">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="b2f2c-118">Si se pasa NULL en el parámetro _lpProgress_ , se muestra el indicador de progreso mediante el uso de la implementación de MAPI.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-118">If NULL is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="b2f2c-119">El parámetro _lpProgress_ se omite a menos que la marca MAPI_DIALOG se establece en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="b2f2c-119">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b2f2c-120">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="b2f2c-120">_lpDestInterface_</span></span>
  
> <span data-ttu-id="b2f2c-121">[entrada] Un puntero para el identificador de interfaz que representa la interfaz que se usará para tener acceso al objeto para recibir las propiedades que se copian o se mueven.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-121">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the properties that are copied or moved.</span></span>
    
 <span data-ttu-id="b2f2c-122">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="b2f2c-122">_lpDestObj_</span></span>
  
> <span data-ttu-id="b2f2c-123">[entrada] Un puntero al objeto que se va a recibir las propiedades que se ha movido o copiadas.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-123">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="b2f2c-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b2f2c-124">_ulFlags_</span></span>
  
> <span data-ttu-id="b2f2c-125">[entrada] Una máscara de bits de indicadores que controla cómo se realiza la operación de copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-125">[in] A bitmask of flags that controls how the copy or move operation is performed.</span></span> <span data-ttu-id="b2f2c-126">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="b2f2c-126">The following flags can be set:</span></span>
    
<span data-ttu-id="b2f2c-127">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b2f2c-127">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="b2f2c-128">Muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-128">Displays a progress indicator.</span></span>
    
<span data-ttu-id="b2f2c-129">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="b2f2c-129">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="b2f2c-130">**DoCopyProps** debe realizar una operación de movimiento en lugar de una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-130">**DoCopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="b2f2c-131">Cuando no se establece este marcador, **DoCopyProps** realiza una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-131">When this flag is not set, **DoCopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="b2f2c-132">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="b2f2c-132">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="b2f2c-133">No se deben sobrescribir las propiedades existentes en el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-133">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="b2f2c-134">Cuando no se establece este marcador, **DoCopyProps** sobrescribe las propiedades existentes.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-134">When this flag is not set, **DoCopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="b2f2c-135">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="b2f2c-135">_lppProblems_</span></span>
  
> <span data-ttu-id="b2f2c-136">[entrada, salida] En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; de lo contrario, NULL, que indica que no hay necesidad de información de error.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-136">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="b2f2c-137">Si _lppProblems_ es un puntero válido en la entrada, **DoCopyProps** devuelve información detallada acerca de los errores de copiar una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-137">If  _lppProblems_ is a valid pointer on input, **DoCopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b2f2c-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2f2c-138">Return value</span></span>

<span data-ttu-id="b2f2c-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2f2c-139">S_OK</span></span> 
  
> <span data-ttu-id="b2f2c-140">Propiedades se han copiado o movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-140">Properties were successfully copied or moved.</span></span>
    
<span data-ttu-id="b2f2c-141">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="b2f2c-141">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="b2f2c-142">Una propiedad para ser copiado o movido ya existe en el objeto de destino y se establece la marca MAPI_NOREPLACE.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-142">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="b2f2c-143">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="b2f2c-143">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="b2f2c-144">El objeto de origen, directa o indirectamente contiene el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-144">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="b2f2c-145">Trabajo significativo es posible que se han realizado antes de que se ha detectado esta condición, por lo que los objetos de origen y de destino podrían modificarse parcialmente.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-145">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="b2f2c-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="b2f2c-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="b2f2c-147">La interfaz identificada mediante el parámetro _lpSrcInterface_ no es compatible con el objeto de origen o la interfaz identificada mediante el parámetro _lpDestInterface_ no es compatible con el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-147">The interface identified by the  _lpSrcInterface_ parameter is not supported by the source object, or the interface identified by the  _lpDestInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="b2f2c-148">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b2f2c-148">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b2f2c-149">Se ha intentado tener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-149">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="b2f2c-150">Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-150">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="b2f2c-151">Los siguientes valores se pueden devolver en la estructura de **SPropProblemArray** , pero no como valores devueltos por **DoCopyProps**.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-151">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyProps**.</span></span> <span data-ttu-id="b2f2c-152">Estos errores se aplican a una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-152">These errors apply to a single property.</span></span>
  
<span data-ttu-id="b2f2c-153">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b2f2c-153">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b2f2c-154">Se ha establecido el indicador MAPI_UNICODE y **DoCopyProps** no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y **DoCopyProps** admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-154">Either the MAPI_UNICODE flag was set and **DoCopyProps** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="b2f2c-155">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="b2f2c-155">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="b2f2c-156">La propiedad no puede modificarse el autor de la llamada porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-156">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="b2f2c-157">Este error no es grave; el autor de la llamada debe permitir que la operación de copia continuar.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-157">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="b2f2c-158">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="b2f2c-158">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="b2f2c-159">El tipo de propiedad no es válido.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-159">The property type is invalid.</span></span>
    
<span data-ttu-id="b2f2c-160">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="b2f2c-160">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="b2f2c-161">El tipo de propiedad no es el tipo que espera el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-161">The property type is not the type that the caller expects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b2f2c-162">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2f2c-162">Remarks</span></span>

<span data-ttu-id="b2f2c-163">El método **IMAPISupport::DoCopyProps** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-163">The **IMAPISupport::DoCopyProps** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="b2f2c-164">Los proveedores de almacén de mensajes pueden llamar a **DoCopyProps** para implementar el método [IMAPIProp::CopyProps](imapiprop-copyprops.md) para sus carpetas y mensajes.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-164">Message store providers can call **DoCopyProps** to implement the [IMAPIProp::CopyProps](imapiprop-copyprops.md) method for their folders and messages.</span></span> <span data-ttu-id="b2f2c-165">**DoCopyProps** copia o mueve las propiedades que se identifican en la matriz de etiqueta de propiedad que señala _lpIncludeProps_ y que están presentes en el objeto al que señala por _lpSrcObj_.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-165">**DoCopyProps** copies or moves the properties that are identified in the property tag array pointed to by  _lpIncludeProps_ and that are present in the object pointed to by  _lpSrcObj_.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b2f2c-166">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="b2f2c-166">Notes to callers</span></span>

<span data-ttu-id="b2f2c-167">Cuando se copian propiedades entre objetos del mismo tipo, como dos mensajes, los parámetros _lpSrcInterface_ y _lpDestInterface_ deben contener los mismos parámetros de identificador y _lpSrcObj_ y _lpDestObj_ de interfaz debe apuntar a los objetos del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-167">When you copy properties between objects of the same type, such as two messages, the  _lpSrcInterface_ and  _lpDestInterface_ parameters must contain the same interface identifier, and the  _lpSrcObj_ and  _lpDestObj_ parameters must point to objects of the same type.</span></span> <span data-ttu-id="b2f2c-168">Si _lpDestInterface_ se establece en NULL, **DoCopyProps** devuelve MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-168">If  _lpDestInterface_ is set to NULL, **DoCopyProps** returns MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="b2f2c-169">Si se establece _lpDestInterface_ en un identificador de interfaz aceptable, pero el conjunto _lpDestObj_ a un puntero no válido, los resultados serán impredecibles.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-169">If you set  _lpDestInterface_ to an acceptable interface identifier, but set  _lpDestObj_ to an invalid pointer, the results are unpredictable.</span></span> <span data-ttu-id="b2f2c-170">Es muy probable que se producirá un error en el proveedor.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-170">Most likely your provider will fail.</span></span> 
  
<span data-ttu-id="b2f2c-171">Establecer la marca MAPI_NOREPLACE si no desea que cualquiera de las propiedades en el objeto de destino se sobrescriban.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-171">Set the MAPI_NOREPLACE flag if you do not want any of the properties in the destination object to be overwritten.</span></span> <span data-ttu-id="b2f2c-172">Las propiedades en el objeto de destino que existen en el objeto de origen y no se sobrescriben no se eliminan o modifican.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-172">Properties in the destination object that exist in the source object and are not overwritten are not deleted or modified.</span></span>
  
<span data-ttu-id="b2f2c-173">Para copiar la lista de destinatarios de un mensaje, incluir la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) en la matriz de etiqueta de la propiedad indicada por el parámetro _lpIncludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="b2f2c-173">To copy a message's recipient list, include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array pointed to by the  _lpIncludeProps_ parameter.</span></span> <span data-ttu-id="b2f2c-174">Para copiar los datos adjuntos del mensaje, incluir la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b2f2c-174">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="b2f2c-175">Para copiar una carpeta o la jerarquía del contenedor de la libreta de direcciones o la tabla de contenido, incluir **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la matriz de la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-175">To copy a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag array.</span></span> <span data-ttu-id="b2f2c-176">Para incluir la tabla de contenido asociada de una carpeta, incluya la propiedad **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) en la matriz.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-176">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span>
  
<span data-ttu-id="b2f2c-177">Si se copian o se mueven las subcarpetas, su contenido se copian o se mueven en su totalidad, independientemente del uso de las propiedades indicado por la estructura del **elemento SPropTagArray** .</span><span class="sxs-lookup"><span data-stu-id="b2f2c-177">If subfolders are copied or moved, their contents are copied or moved in their entirety, regardless of the use of properties indicated by the **SPropTagArray** structure.</span></span> 
  
 <span data-ttu-id="b2f2c-178">**DoCopyProps** informes de errores global que se producen con la operación como un todo y errores individuales que se producen con una o varias de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-178">**DoCopyProps** reports global errors that occur with the operation as a whole, and individual errors that occur with one or more of the properties.</span></span> <span data-ttu-id="b2f2c-179">Estos errores individuales se colocan en una estructura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="b2f2c-179">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="b2f2c-180">Puede suprimir informes en el nivel de propiedad pasando NULL, en lugar de un puntero válido para el parámetro de estructura de matriz de propiedad problema de error.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-180">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="b2f2c-181">Si desea recibir información acerca de los errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="b2f2c-181">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="b2f2c-182">Cuando **DoCopyProps** devuelve S_OK, comprobar los posibles errores con las propiedades individuales de la estructura de.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-182">When **DoCopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="b2f2c-183">Cuando **DoCopyProps** devuelve un error, no se devuelve información de la estructura de **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="b2f2c-183">When **DoCopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="b2f2c-184">En su lugar, llame al método de [IMAPISupport::GetLastError](imapisupport-getlasterror.md) para recuperar información detallada del error.</span><span class="sxs-lookup"><span data-stu-id="b2f2c-184">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="b2f2c-185">Si **DoCopyProps** devuelve S_OK, liberar la estructura **SPropProblemArray** devuelta por una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b2f2c-185">If **DoCopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2f2c-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2f2c-186">See also</span></span>



[<span data-ttu-id="b2f2c-187">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="b2f2c-187">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
  
[<span data-ttu-id="b2f2c-188">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="b2f2c-188">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="b2f2c-189">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="b2f2c-189">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="b2f2c-190">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b2f2c-190">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="b2f2c-191">Propiedad canónica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="b2f2c-191">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="b2f2c-192">Propiedad canónica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="b2f2c-192">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="b2f2c-193">Propiedad canónica PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="b2f2c-193">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="b2f2c-194">Propiedad canónica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="b2f2c-194">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="b2f2c-195">Propiedad canónica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="b2f2c-195">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="b2f2c-196">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="b2f2c-196">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="b2f2c-197">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="b2f2c-197">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="b2f2c-198">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2f2c-198">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

