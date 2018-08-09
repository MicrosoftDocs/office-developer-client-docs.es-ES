---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1040a0730c4b26b51d3c2b7763488502b2c5323c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817508"
---
# <a name="imapisupportdocopyto"></a><span data-ttu-id="56116-103">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="56116-103">IMAPISupport::DoCopyTo</span></span>

  
  
<span data-ttu-id="56116-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56116-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56116-105">Copia o mueve todas las propiedades de un objeto, excepto propiedades excluidas específicamente, a otro objeto.</span><span class="sxs-lookup"><span data-stu-id="56116-105">Copies or moves all properties of one object, except for specifically excluded properties, to another object.</span></span>
  
```cpp
HRESULT DoCopyTo(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  ULONG ciidExclude,
  LPCIID rgiidExclude,
  LPSPropTagArray lpExcludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="56116-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56116-106">Parameters</span></span>

 <span data-ttu-id="56116-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="56116-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="56116-108">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto que tiene las propiedades que se pueden copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="56116-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="56116-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="56116-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="56116-110">[entrada] Un puntero al objeto que tiene las propiedades que se pueden copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="56116-110">[in] A pointer to the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="56116-111">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="56116-111">_ciidExclude_</span></span>
  
> <span data-ttu-id="56116-112">[entrada] El recuento de interfaces que se deben excluir al copiar o mover las propiedades.</span><span class="sxs-lookup"><span data-stu-id="56116-112">[in] The count of interfaces to exclude when you copy or move properties.</span></span>
    
 <span data-ttu-id="56116-113">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="56116-113">_rgiidExclude_</span></span>
  
> <span data-ttu-id="56116-114">[entrada] Una matriz de identificadores de interfaz que indica las interfaces que no se deben usar cuando se copie o mueva información complementaria para el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="56116-114">[in] An array of interface identifiers that indicates interfaces that should not be used when you copy or move supplemental information to the destination object.</span></span>
    
 <span data-ttu-id="56116-115">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="56116-115">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="56116-116">[entrada] Un puntero a una matriz de etiqueta de propiedad que identifica las etiquetas de propiedad que se deben excluir de la copia o la operación de movimiento.</span><span class="sxs-lookup"><span data-stu-id="56116-116">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="56116-117">Pasar NULL en el parámetro _lpExcludeProps_ indica que todas las propiedades del objeto deben copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="56116-117">Passing NULL in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="56116-118">**DoCopyTo** devuelve MAPI_E_INVALID_PARAMETER cuando el miembro **cValues** de la estructura del [elemento SPropTagArray](sproptagarray.md) que apunta _lpExcludeProps_ se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="56116-118">**DoCopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="56116-119">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="56116-119">_ulUIParam_</span></span>
  
> <span data-ttu-id="56116-120">[entrada] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="56116-120">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="56116-121">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="56116-121">_lpProgress_</span></span>
  
> <span data-ttu-id="56116-122">[entrada] Un puntero a una implementación de indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="56116-122">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="56116-123">Si se pasa NULL en el parámetro _lpProgress_ , MAPI proporciona la implementación de progreso.</span><span class="sxs-lookup"><span data-stu-id="56116-123">If NULL is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="56116-124">El parámetro _lpProgress_ se omite a menos que la marca MAPI_DIALOG se establece en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="56116-124">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="56116-125">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="56116-125">_lpDestInterface_</span></span>
  
> <span data-ttu-id="56116-126">[entrada] Un puntero para el identificador de interfaz que representa la interfaz que se usará para tener acceso al objeto para recibir las propiedades que se ha movido o copiadas.</span><span class="sxs-lookup"><span data-stu-id="56116-126">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="56116-127">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="56116-127">_lpDestObj_</span></span>
  
> <span data-ttu-id="56116-128">[entrada] Un puntero al objeto que se va a recibir las propiedades que se ha movido o copiadas.</span><span class="sxs-lookup"><span data-stu-id="56116-128">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="56116-129">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="56116-129">_ulFlags_</span></span>
  
> <span data-ttu-id="56116-130">[entrada] Una máscara de bits de indicadores que controla la operación de copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="56116-130">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="56116-131">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="56116-131">The following flags can be set:</span></span>
    
<span data-ttu-id="56116-132">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="56116-132">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="56116-133">Muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="56116-133">Displays a progress indicator.</span></span> 
    
<span data-ttu-id="56116-134">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="56116-134">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="56116-135">**DoCopyTo** debe realizar una operación de movimiento en lugar de una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="56116-135">**DoCopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="56116-136">Cuando no se establece este marcador, **DoCopyTo** realiza una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="56116-136">When this flag is not set, **DoCopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="56116-137">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="56116-137">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="56116-138">No se deben sobrescribir las propiedades existentes en el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="56116-138">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="56116-139">Cuando no se establece este marcador, **DoCopyTo** sobrescribe las propiedades existentes.</span><span class="sxs-lookup"><span data-stu-id="56116-139">When this flag is not set, **DoCopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="56116-140">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="56116-140">_lppProblems_</span></span>
  
> <span data-ttu-id="56116-141">[out] En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; de lo contrario, NULL, que indica que no hay necesidad de información de error.</span><span class="sxs-lookup"><span data-stu-id="56116-141">[out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="56116-142">Si _lppProblems_ es un puntero válido en la entrada, **DoCopyTo** devuelve información detallada acerca de los errores de copiar una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="56116-142">If  _lppProblems_ is a valid pointer on input, **DoCopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="56116-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56116-143">Return value</span></span>

<span data-ttu-id="56116-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="56116-144">S_OK</span></span> 
  
> <span data-ttu-id="56116-145">Las propiedades se hayan copiado o movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="56116-145">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="56116-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="56116-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="56116-147">Una propiedad para ser copiado o movido ya existe en el objeto de destino y se establece la marca MAPI_NOREPLACE.</span><span class="sxs-lookup"><span data-stu-id="56116-147">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="56116-148">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="56116-148">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="56116-149">El objeto de origen, directa o indirectamente contiene el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="56116-149">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="56116-150">Trabajo significativo es posible que se han realizado antes de que se ha detectado esta condición, por lo que los objetos de origen y de destino podrían modificarse parcialmente.</span><span class="sxs-lookup"><span data-stu-id="56116-150">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="56116-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="56116-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="56116-152">La interfaz identificada mediante el parámetro _lpSrcInterface_ no es compatible con el objeto al que señala por _lpSrcObj_o la interfaz identificada mediante el parámetro _lpDestInterface_ no es compatible con el objeto al que señala por _lpDestObj _.</span><span class="sxs-lookup"><span data-stu-id="56116-152">The interface identified by the  _lpSrcInterface_ parameter is not supported by the object pointed to by  _lpSrcObj_, or the interface identified by the  _lpDestInterface_ parameter is not supported by the object pointed to by  _lpDestObj_.</span></span> 
    
<span data-ttu-id="56116-153">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="56116-153">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="56116-154">Se ha intentado tener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="56116-154">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="56116-155">Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="56116-155">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="56116-156">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="56116-156">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="56116-157">El parámetro _lpSrcInterface_ es NULL.</span><span class="sxs-lookup"><span data-stu-id="56116-157">The  _lpSrcInterface_ parameter is NULL.</span></span> 
    
<span data-ttu-id="56116-158">Los siguientes valores se pueden devolver en la estructura de **SPropProblemArray** , pero no como valores devueltos por **DoCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="56116-158">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyTo**.</span></span> <span data-ttu-id="56116-159">Estos errores se aplican a una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="56116-159">These errors apply to a single property.</span></span>
  
<span data-ttu-id="56116-160">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="56116-160">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="56116-161">Se ha establecido el indicador MAPI_UNICODE y **DoCopyTo** no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y **DoCopyTo** admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="56116-161">Either the MAPI_UNICODE flag was set and **DoCopyTo** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="56116-162">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="56116-162">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="56116-163">La propiedad no puede modificarse el autor de la llamada porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="56116-163">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="56116-164">Este error no es grave; el autor de la llamada debe permitir que la operación de copia continuar.</span><span class="sxs-lookup"><span data-stu-id="56116-164">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="56116-165">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="56116-165">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="56116-166">El tipo de propiedad no es válido.</span><span class="sxs-lookup"><span data-stu-id="56116-166">The property type is invalid.</span></span>
    
<span data-ttu-id="56116-167">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="56116-167">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="56116-168">El tipo de propiedad no es el tipo esperado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="56116-168">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="56116-169">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56116-169">Remarks</span></span>

<span data-ttu-id="56116-170">El método **IMAPISupport::DoCopyTo** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="56116-170">The **IMAPISupport::DoCopyTo** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="56116-171">Los proveedores de almacén de mensajes pueden llamar a **DoCopyTo** para implementar el método [IMAPIProp::CopyTo](imapiprop-copyto.md) para sus carpetas y mensajes.</span><span class="sxs-lookup"><span data-stu-id="56116-171">Message store providers can call **DoCopyTo** to implement the [IMAPIProp::CopyTo](imapiprop-copyto.md) method for their folders and messages.</span></span> 
  
<span data-ttu-id="56116-172">De forma predeterminada, **DoCopyTo** copia o mueve todas las propiedades de un objeto a otro objeto.</span><span class="sxs-lookup"><span data-stu-id="56116-172">By default, **DoCopyTo** copies or moves all of the properties of one object to another object.</span></span> <span data-ttu-id="56116-173">Los objetos secundarios en el objeto de origen automáticamente se incluyen en la operación y copiados o movidos en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="56116-173">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety.</span></span> 
  
<span data-ttu-id="56116-174">Si cualquiera de las propiedades que se ha movido o copiadas ya existe en el objeto de destino, se sobrescriben las propiedades existentes por las nuevas propiedades, a menos que se establece la marca MAPI_NOREPLACE en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="56116-174">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="56116-175">Información existente en el objeto de destino que no se sobrescribe se toca.</span><span class="sxs-lookup"><span data-stu-id="56116-175">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="56116-176">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="56116-176">Notes to callers</span></span>

<span data-ttu-id="56116-177">Para excluir las propiedades de la copia o la operación de movimiento, incluir sus etiquetas de propiedad en el parámetro _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="56116-177">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="56116-178">Si pasa los resultados del uso de la macro [PROP_TAG](prop_tag.md) para crear una etiqueta de propiedad de un identificador específico de la matriz de la etiqueta de propiedad, se excluirán todas las propiedades con ese identificador.</span><span class="sxs-lookup"><span data-stu-id="56116-178">If you pass the results of using the [PROP_TAG](prop_tag.md) macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="56116-179">Por ejemplo, la siguiente entrada en la matriz de la etiqueta de propiedad hace que todas las propiedades con un identificador de 0x8002 que se deben excluir, independientemente del tipo de:</span><span class="sxs-lookup"><span data-stu-id="56116-179">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="56116-180">Para evitar el tiempo de entrega de un mensaje cuando se copia el mensaje a una carpeta diferente de copia, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) en la matriz de exclusión de etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="56116-180">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="56116-181">Para excluir lista de destinatarios de un mensaje, agregue la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) a la matriz de exclusión.</span><span class="sxs-lookup"><span data-stu-id="56116-181">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="56116-182">Para excluir los datos adjuntos de un mensaje, agregue la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) a la matriz.</span><span class="sxs-lookup"><span data-stu-id="56116-182">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="56116-183">De forma similar, para evitar que las acciones como copiar o mover de una carpeta o la jerarquía del contenedor de la libreta de direcciones o la tabla de contenido, incluya **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la propiedad etiqueta excluir matriz.</span><span class="sxs-lookup"><span data-stu-id="56116-183">Similarly, to prevent the copying or moving of a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="56116-184">Omitir MAPI_E_COMPUTED devuelven errores en la estructura de **SPropProblemArray** en el parámetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="56116-184">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
<span data-ttu-id="56116-185">El identificador de interfaz que _lpSrcInterface_ puntos que suele ser el mismo que el identificador de interfaz que señala _lpDestInterface_ .</span><span class="sxs-lookup"><span data-stu-id="56116-185">The interface identifier that  _lpSrcInterface_ points to is usually the same as the interface identifier that  _lpDestInterface_ points to.</span></span> 
  
<span data-ttu-id="56116-186">Si se pasan un identificador de interfaz aceptable en _lpDestInterface_ pero un puntero no válido en _lpDestObj_, los resultados serán impredecibles.</span><span class="sxs-lookup"><span data-stu-id="56116-186">If you pass an acceptable interface identifier in  _lpDestInterface_ but an invalid pointer in  _lpDestObj_, the results are unpredictable.</span></span> <span data-ttu-id="56116-187">Es muy probable que esto hará que el proveedor se lleve a cabo.</span><span class="sxs-lookup"><span data-stu-id="56116-187">Most likely this will cause your provider to fail.</span></span> 
  
<span data-ttu-id="56116-188">Por el contrario, si tiene constancia de información complementaria que no se puede copiar o mover, agregar los identificadores de interfaz de las interfaces que se deben excluir de la matriz que se pasa en el parámetro _rgiidExclude_ .</span><span class="sxs-lookup"><span data-stu-id="56116-188">Conversely, if you are aware of supplemental information that should not be copied or moved, add the interface identifiers for the interfaces to be excluded in the array passed in the  _rgiidExclude_ parameter.</span></span> <span data-ttu-id="56116-189">Por ejemplo, si va a copiar los mensajes, pero no en cualquiera de sus datos adjuntos de mensajes, pase IID_IMessage en la matriz _rgiidExclude_ .</span><span class="sxs-lookup"><span data-stu-id="56116-189">For example, if you are copying messages, but not any of their message attachments, pass IID_IMessage in the  _rgiidExclude_ array.</span></span> <span data-ttu-id="56116-190">**DoCopyTo** pasa por alto cualquier interfaces que aparecen en _rgiidExclude_ que no reconoce.</span><span class="sxs-lookup"><span data-stu-id="56116-190">**DoCopyTo** ignores any interfaces listed in  _rgiidExclude_ that it does not recognize.</span></span> 
  
<span data-ttu-id="56116-191">Cuando se usa el parámetro _rgiidExclude_ para excluir una interfaz, también excluye todas las interfaces derivadas de dicha interfaz.</span><span class="sxs-lookup"><span data-stu-id="56116-191">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="56116-192">Por ejemplo, la exclusión de la interfaz de [IMAPIContainer](imapicontainerimapiprop.md) hace que las carpetas o los contenedores de la libreta de direcciones que se deben excluir, según el tipo de proveedor de.</span><span class="sxs-lookup"><span data-stu-id="56116-192">For example, excluding the [IMAPIContainer](imapicontainerimapiprop.md) interface causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="56116-193">No excluya [IMAPIProp](imapipropiunknown.md) o [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) debido a que muchas interfaces derivan de ellos.</span><span class="sxs-lookup"><span data-stu-id="56116-193">Do not exclude [IMAPIProp](imapipropiunknown.md) or [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) because so many interfaces derive from them.</span></span> 
  
 <span data-ttu-id="56116-194">**DoCopyTo** informes de errores global que se aplican a la operación como un todo y errores individuales que se aplican a las propiedades individuales.</span><span class="sxs-lookup"><span data-stu-id="56116-194">**DoCopyTo** reports global errors that apply to the operation as a whole, and individual errors that apply to individual properties.</span></span> <span data-ttu-id="56116-195">Estos errores individuales se colocan en una estructura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="56116-195">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="56116-196">Puede suprimir informes en el nivel de propiedad pasando NULL, en lugar de un puntero válido para el parámetro de estructura de matriz de propiedad problema de error.</span><span class="sxs-lookup"><span data-stu-id="56116-196">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="56116-197">Si desea recibir información acerca de los errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="56116-197">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="56116-198">Cuando **DoCopyTo** devuelve S_OK, comprobar los posibles errores con las propiedades individuales de la estructura de.</span><span class="sxs-lookup"><span data-stu-id="56116-198">When **DoCopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="56116-199">Cuando **DoCopyTo** devuelve un error, no se devuelve información de la estructura de **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="56116-199">When **DoCopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="56116-200">En su lugar, llame al método de [IMAPISupport::GetLastError](imapisupport-getlasterror.md) para recuperar información detallada del error.</span><span class="sxs-lookup"><span data-stu-id="56116-200">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="56116-201">Si **DoCopyTo** devuelve S_OK, liberar la estructura **SPropProblemArray** devuelta por una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="56116-201">If **DoCopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="56116-202">Si se produce un error global en la llamada **DoCopyTo** , no utilice ni libre la estructura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="56116-202">If a global error occurs on the **DoCopyTo** call, do not use or free the **SPropProblemArray** structure.</span></span> <span data-ttu-id="56116-203">Proveedores de deben omitir al miembro _ulIndex_ en estructuras **SPropProblemArray** devuelto por **DoCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="56116-203">Providers should ignore the  _ulIndex_ member in **SPropProblemArray** structures returned by **DoCopyTo**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="56116-204">Vea también</span><span class="sxs-lookup"><span data-stu-id="56116-204">See also</span></span>



[<span data-ttu-id="56116-205">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="56116-205">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="56116-206">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="56116-206">IMAPISupport::CopyFolder</span></span>](imapisupport-copyfolder.md)
  
[<span data-ttu-id="56116-207">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="56116-207">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="56116-208">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="56116-208">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="56116-209">Propiedad canónica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="56116-209">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="56116-210">Propiedad canónica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="56116-210">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="56116-211">Propiedad canónica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="56116-211">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="56116-212">Propiedad canónica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="56116-212">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="56116-213">Propiedad canónica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="56116-213">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="56116-214">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="56116-214">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="56116-215">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="56116-215">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="56116-216">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="56116-216">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

