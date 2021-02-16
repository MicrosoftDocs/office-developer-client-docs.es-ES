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
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331811"
---
# <a name="imapisupportdocopyto"></a><span data-ttu-id="2901d-103">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="2901d-103">IMAPISupport::DoCopyTo</span></span>

  
  
<span data-ttu-id="2901d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2901d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2901d-105">Copia o mueve todas las propiedades de un objeto, excepto las propiedades excluidas específicamente, a otro objeto.</span><span class="sxs-lookup"><span data-stu-id="2901d-105">Copies or moves all properties of one object, except for specifically excluded properties, to another object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="2901d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2901d-106">Parameters</span></span>

 <span data-ttu-id="2901d-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="2901d-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="2901d-108">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para tener acceso al objeto que tiene las propiedades que se van a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="2901d-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="2901d-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="2901d-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="2901d-110">[entrada] Puntero al objeto que tiene las propiedades que se van a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="2901d-110">[in] A pointer to the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="2901d-111">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="2901d-111">_ciidExclude_</span></span>
  
> <span data-ttu-id="2901d-112">[entrada] Recuento de interfaces que se excluirán al copiar o mover propiedades.</span><span class="sxs-lookup"><span data-stu-id="2901d-112">[in] The count of interfaces to exclude when you copy or move properties.</span></span>
    
 <span data-ttu-id="2901d-113">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="2901d-113">_rgiidExclude_</span></span>
  
> <span data-ttu-id="2901d-114">[entrada] Matriz de identificadores de interfaz que indica interfaces que no deben usarse al copiar o mover información complementaria al objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="2901d-114">[in] An array of interface identifiers that indicates interfaces that should not be used when you copy or move supplemental information to the destination object.</span></span>
    
 <span data-ttu-id="2901d-115">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="2901d-115">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="2901d-116">[entrada] Puntero a una matriz de etiquetas de propiedades que identifica las etiquetas de propiedad que se deben excluir de la operación de copia o movimiento.</span><span class="sxs-lookup"><span data-stu-id="2901d-116">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="2901d-117">Pasar NULL en  _el parámetro lpExcludeProps_ indica que todas las propiedades del objeto deben copiarse o moverse.</span><span class="sxs-lookup"><span data-stu-id="2901d-117">Passing NULL in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="2901d-118">**DoCopyTo** devuelve MAPI_E_INVALID_PARAMETER cuando el miembro **cValues** de la estructura [SPropTagArray](sproptagarray.md) a la que apunta  _lpExcludeProps_ está establecido en 0.</span><span class="sxs-lookup"><span data-stu-id="2901d-118">**DoCopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="2901d-119">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2901d-119">_ulUIParam_</span></span>
  
> <span data-ttu-id="2901d-120">[entrada] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="2901d-120">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="2901d-121">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="2901d-121">_lpProgress_</span></span>
  
> <span data-ttu-id="2901d-122">[entrada] Puntero a una implementación de indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="2901d-122">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="2901d-123">Si se pasa NULL en el  _parámetro lpProgress,_ MAPI proporciona la implementación del progreso.</span><span class="sxs-lookup"><span data-stu-id="2901d-123">If NULL is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="2901d-124">El _parámetro lpProgress_ se omite a menos que MAPI_DIALOG marca esté establecida en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="2901d-124">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="2901d-125">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="2901d-125">_lpDestInterface_</span></span>
  
> <span data-ttu-id="2901d-126">[entrada] Puntero al identificador de interfaz que representa la interfaz que se va a usar para tener acceso al objeto para recibir las propiedades copiadas o movida.</span><span class="sxs-lookup"><span data-stu-id="2901d-126">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="2901d-127">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="2901d-127">_lpDestObj_</span></span>
  
> <span data-ttu-id="2901d-128">[entrada] Puntero al objeto para recibir las propiedades copiadas o movida.</span><span class="sxs-lookup"><span data-stu-id="2901d-128">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="2901d-129">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2901d-129">_ulFlags_</span></span>
  
> <span data-ttu-id="2901d-130">[entrada] Máscara de bits de marcas que controla la operación de copia o movimiento.</span><span class="sxs-lookup"><span data-stu-id="2901d-130">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="2901d-131">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="2901d-131">The following flags can be set:</span></span>
    
<span data-ttu-id="2901d-132">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2901d-132">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="2901d-133">Muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="2901d-133">Displays a progress indicator.</span></span> 
    
<span data-ttu-id="2901d-134">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="2901d-134">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="2901d-135">**DoCopyTo debe** realizar una operación de movimiento en lugar de una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="2901d-135">**DoCopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="2901d-136">Cuando no se establece esta marca, **DoCopyTo** realiza una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="2901d-136">When this flag is not set, **DoCopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="2901d-137">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="2901d-137">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="2901d-138">Las propiedades existentes en el objeto de destino no deben sobrescribirse.</span><span class="sxs-lookup"><span data-stu-id="2901d-138">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="2901d-139">Cuando no se establece esta marca, **DoCopyTo** sobrescribe las propiedades existentes.</span><span class="sxs-lookup"><span data-stu-id="2901d-139">When this flag is not set, **DoCopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="2901d-140">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="2901d-140">_lppProblems_</span></span>
  
> <span data-ttu-id="2901d-141">[salida] En la entrada, un puntero a un puntero a una [estructura SPropProblemArray;](spropproblemarray.md) de lo contrario, NULL, que indica que no es necesario obtener información de error.</span><span class="sxs-lookup"><span data-stu-id="2901d-141">[out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="2901d-142">Si  _lppProblems_ es un puntero válido en la entrada, **DoCopyTo** devuelve información detallada acerca de los errores al copiar una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="2901d-142">If  _lppProblems_ is a valid pointer on input, **DoCopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2901d-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2901d-143">Return value</span></span>

<span data-ttu-id="2901d-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="2901d-144">S_OK</span></span> 
  
> <span data-ttu-id="2901d-145">Las propiedades se han copiado o movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="2901d-145">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="2901d-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="2901d-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="2901d-147">Ya existe una propiedad que se va a copiar o mover en el objeto de destino y se MAPI_NOREPLACE marca.</span><span class="sxs-lookup"><span data-stu-id="2901d-147">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="2901d-148">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="2901d-148">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="2901d-149">El objeto de origen contiene directa o indirectamente el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="2901d-149">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="2901d-150">Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que los objetos de origen y destino podrían modificarse parcialmente.</span><span class="sxs-lookup"><span data-stu-id="2901d-150">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="2901d-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="2901d-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="2901d-152">La interfaz identificada por el parámetro  _lpSrcInterface_ no es compatible con el objeto al que apunta  _lpSrcObj_, o la interfaz identificada por el parámetro  _lpDestInterface_ no es compatible con el objeto que apunta  _lpDestObj_.</span><span class="sxs-lookup"><span data-stu-id="2901d-152">The interface identified by the  _lpSrcInterface_ parameter is not supported by the object pointed to by  _lpSrcObj_, or the interface identified by the  _lpDestInterface_ parameter is not supported by the object pointed to by  _lpDestObj_.</span></span> 
    
<span data-ttu-id="2901d-153">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="2901d-153">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="2901d-154">Se intentó obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="2901d-154">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="2901d-155">Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="2901d-155">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="2901d-156">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2901d-156">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="2901d-157">El  _parámetro lpSrcInterface_ es NULL.</span><span class="sxs-lookup"><span data-stu-id="2901d-157">The  _lpSrcInterface_ parameter is NULL.</span></span> 
    
<span data-ttu-id="2901d-158">Los siguientes valores se pueden devolver en la **estructura SPropProblemArray,** pero no como valores devueltos **para DoCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="2901d-158">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyTo**.</span></span> <span data-ttu-id="2901d-159">Estos errores se aplican a una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="2901d-159">These errors apply to a single property.</span></span>
  
<span data-ttu-id="2901d-160">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2901d-160">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2901d-161">Se estableció MAPI_UNICODE marca y **DoCopyTo** no admite Unicode o MAPI_UNICODE no se estableció y **DoCopyTo** solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="2901d-161">Either the MAPI_UNICODE flag was set and **DoCopyTo** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="2901d-162">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="2901d-162">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="2901d-163">El autor de la llamada no puede modificar la propiedad porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="2901d-163">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="2901d-164">Este error no es grave; el autor de la llamada debe permitir que continúe la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="2901d-164">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="2901d-165">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="2901d-165">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="2901d-166">El tipo de propiedad no es válido.</span><span class="sxs-lookup"><span data-stu-id="2901d-166">The property type is invalid.</span></span>
    
<span data-ttu-id="2901d-167">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="2901d-167">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="2901d-168">El tipo de propiedad no es el tipo esperado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2901d-168">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2901d-169">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2901d-169">Remarks</span></span>

<span data-ttu-id="2901d-170">El **método IMAPISupport::D oCopyTo** se implementa para objetos de compatibilidad del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2901d-170">The **IMAPISupport::DoCopyTo** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="2901d-171">Los proveedores de almacenamiento de mensajes pueden llamar **a DoCopyTo** para implementar el método [IMAPIProp::CopyTo](imapiprop-copyto.md) para sus carpetas y mensajes.</span><span class="sxs-lookup"><span data-stu-id="2901d-171">Message store providers can call **DoCopyTo** to implement the [IMAPIProp::CopyTo](imapiprop-copyto.md) method for their folders and messages.</span></span> 
  
<span data-ttu-id="2901d-172">De forma predeterminada, **DoCopyTo** copia o mueve todas las propiedades de un objeto a otro objeto.</span><span class="sxs-lookup"><span data-stu-id="2901d-172">By default, **DoCopyTo** copies or moves all of the properties of one object to another object.</span></span> <span data-ttu-id="2901d-173">Todos los subobjetos del objeto de origen se incluyen automáticamente en la operación y se copian o mueven en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="2901d-173">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety.</span></span> 
  
<span data-ttu-id="2901d-174">Si alguna de las propiedades copiadas o movida ya existe en el objeto de destino, las propiedades existentes se sobrescriben mediante las nuevas propiedades, a menos que la marca MAPI_NOREPLACE esté establecida en el parámetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="2901d-174">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="2901d-175">La información existente en el objeto de destino que no se sobrescribe se deja sin tocar.</span><span class="sxs-lookup"><span data-stu-id="2901d-175">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2901d-176">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="2901d-176">Notes to callers</span></span>

<span data-ttu-id="2901d-177">Para excluir propiedades de la operación de copiar o mover, incluya sus etiquetas de propiedad en el parámetro _lpExcludeProps._</span><span class="sxs-lookup"><span data-stu-id="2901d-177">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="2901d-178">Si pasa los resultados de usar la macro PROP_TAG para crear una etiqueta de propiedad [a](prop_tag.md) partir de un identificador específico en la matriz de etiquetas de propiedad, se excluirán todas las propiedades con ese identificador.</span><span class="sxs-lookup"><span data-stu-id="2901d-178">If you pass the results of using the [PROP_TAG](prop_tag.md) macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="2901d-179">Por ejemplo, la siguiente entrada en la matriz de etiquetas de propiedades hace que todas las propiedades con un identificador de 0x8002 se excluyan, independientemente del tipo:</span><span class="sxs-lookup"><span data-stu-id="2901d-179">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="2901d-180">Para evitar copiar la hora de entrega de un mensaje al copiar el mensaje en otra carpeta, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) en la matriz de exclusión de la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2901d-180">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="2901d-181">Para excluir la lista de destinatarios de un mensaje, agregue la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) a la matriz de exclusión.</span><span class="sxs-lookup"><span data-stu-id="2901d-181">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="2901d-182">Para excluir los datos adjuntos de un mensaje, agregue **la PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) a la matriz.</span><span class="sxs-lookup"><span data-stu-id="2901d-182">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="2901d-183">De forma similar, para evitar copiar o mover la jerarquía o la tabla de contenido de un contenedor de carpeta o libreta de direcciones, incluya **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la matriz de exclusión de la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2901d-183">Similarly, to prevent the copying or moving of a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="2901d-184">Ignore MAPI_E_COMPUTED errores devueltos en la **estructura SPropProblemArray** en el _parámetro lppProblems._</span><span class="sxs-lookup"><span data-stu-id="2901d-184">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
<span data-ttu-id="2901d-185">El identificador de interfaz al _que señala lpSrcInterface_ suele ser el mismo que el identificador de interfaz al que _apunta lpDestInterface._</span><span class="sxs-lookup"><span data-stu-id="2901d-185">The interface identifier that  _lpSrcInterface_ points to is usually the same as the interface identifier that  _lpDestInterface_ points to.</span></span> 
  
<span data-ttu-id="2901d-186">Si pasa un identificador de interfaz aceptable en  _lpDestInterface_ pero un puntero no válido en  _lpDestObj_, los resultados son impredecibles.</span><span class="sxs-lookup"><span data-stu-id="2901d-186">If you pass an acceptable interface identifier in  _lpDestInterface_ but an invalid pointer in  _lpDestObj_, the results are unpredictable.</span></span> <span data-ttu-id="2901d-187">Lo más probable es que esto cause un error en el proveedor.</span><span class="sxs-lookup"><span data-stu-id="2901d-187">Most likely this will cause your provider to fail.</span></span> 
  
<span data-ttu-id="2901d-188">Por el contrario, si conoce información complementaria que no se debe copiar ni mover, agregue los identificadores de interfaz de las interfaces que se excluirán en la matriz pasada en el parámetro _rgiidExclude._</span><span class="sxs-lookup"><span data-stu-id="2901d-188">Conversely, if you are aware of supplemental information that should not be copied or moved, add the interface identifiers for the interfaces to be excluded in the array passed in the  _rgiidExclude_ parameter.</span></span> <span data-ttu-id="2901d-189">Por ejemplo, si va a copiar mensajes, pero no ninguno de sus datos adjuntos, pase IID_IMessage en la matriz _rgiidExclude._</span><span class="sxs-lookup"><span data-stu-id="2901d-189">For example, if you are copying messages, but not any of their message attachments, pass IID_IMessage in the  _rgiidExclude_ array.</span></span> <span data-ttu-id="2901d-190">**DoCopyTo omite** las interfaces enumeradas  _en rgiidExclude_ que no reconoce.</span><span class="sxs-lookup"><span data-stu-id="2901d-190">**DoCopyTo** ignores any interfaces listed in  _rgiidExclude_ that it does not recognize.</span></span> 
  
<span data-ttu-id="2901d-191">Cuando se usa el  _parámetro rgiidExclude_ para excluir una interfaz, también se excluyen todas las interfaces derivadas de esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="2901d-191">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="2901d-192">Por ejemplo, la exclusión de la [interfaz IMAPIContainer](imapicontainerimapiprop.md) hace que se excluyan carpetas o contenedores de libreta de direcciones, según el tipo de proveedor.</span><span class="sxs-lookup"><span data-stu-id="2901d-192">For example, excluding the [IMAPIContainer](imapicontainerimapiprop.md) interface causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="2901d-193">No excluya [IMAPIProp](imapipropiunknown.md) o [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) porque muchas interfaces derivan de ellas.</span><span class="sxs-lookup"><span data-stu-id="2901d-193">Do not exclude [IMAPIProp](imapipropiunknown.md) or [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) because so many interfaces derive from them.</span></span> 
  
 <span data-ttu-id="2901d-194">**DoCopyTo notifica** los errores globales que se aplican a la operación en su totalidad y los errores individuales que se aplican a propiedades individuales.</span><span class="sxs-lookup"><span data-stu-id="2901d-194">**DoCopyTo** reports global errors that apply to the operation as a whole, and individual errors that apply to individual properties.</span></span> <span data-ttu-id="2901d-195">Estos errores individuales se ponen en una **estructura SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="2901d-195">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="2901d-196">Puede suprimir los informes de errores en el nivel de propiedad pasando NULL, en lugar de un puntero válido, para el parámetro de estructura de la matriz de problemas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2901d-196">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="2901d-197">Si desea recibir información sobre errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems._</span><span class="sxs-lookup"><span data-stu-id="2901d-197">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="2901d-198">Cuando **DoCopyTo devuelve** S_OK, compruebe si hay errores posibles con propiedades individuales en la estructura.</span><span class="sxs-lookup"><span data-stu-id="2901d-198">When **DoCopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="2901d-199">Cuando **DoCopyTo devuelve** un error, no se devuelve información en la **estructura SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="2901d-199">When **DoCopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="2901d-200">En su lugar, llame [al método IMAPISupport::GetLastError](imapisupport-getlasterror.md) para recuperar información detallada del error.</span><span class="sxs-lookup"><span data-stu-id="2901d-200">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="2901d-201">Si **DoCopyTo** devuelve S_OK, libera la estructura **SPropProblemArray** devuelta llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="2901d-201">If **DoCopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="2901d-202">Si se produce un error global en la llamada **a DoCopyTo,** no use ni libre la estructura **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="2901d-202">If a global error occurs on the **DoCopyTo** call, do not use or free the **SPropProblemArray** structure.</span></span> <span data-ttu-id="2901d-203">Los proveedores deben omitir el  _miembro ulIndex_ en **las estructuras SPropProblemArray** devueltas **por DoCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="2901d-203">Providers should ignore the  _ulIndex_ member in **SPropProblemArray** structures returned by **DoCopyTo**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2901d-204">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2901d-204">See also</span></span>



[<span data-ttu-id="2901d-205">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="2901d-205">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="2901d-206">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="2901d-206">IMAPISupport::CopyFolder</span></span>](imapisupport-copyfolder.md)
  
[<span data-ttu-id="2901d-207">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="2901d-207">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="2901d-208">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="2901d-208">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="2901d-209">Propiedad canónica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="2901d-209">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="2901d-210">Propiedad canónica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="2901d-210">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="2901d-211">Propiedad canónica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="2901d-211">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="2901d-212">Propiedad canónica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="2901d-212">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="2901d-213">Propiedad canónica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="2901d-213">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="2901d-214">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="2901d-214">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="2901d-215">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="2901d-215">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="2901d-216">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2901d-216">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

