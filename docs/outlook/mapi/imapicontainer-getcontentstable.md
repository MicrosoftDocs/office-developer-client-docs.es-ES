---
title: IMAPIContainerGetContentsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 28315c5a09eba32816a0b63513cb98d1c30a96bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431109"
---
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="ad207-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="ad207-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="ad207-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad207-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad207-105">Devuelve un puntero a la tabla de contenido del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ad207-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="ad207-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad207-106">Parameters</span></span>

 <span data-ttu-id="ad207-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ad207-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ad207-108">[entrada] Máscara de bits de marcas que controla cómo se devuelve la tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="ad207-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="ad207-109">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="ad207-109">The following flags can be set:</span></span>
    
<span data-ttu-id="ad207-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="ad207-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="ad207-111">Se debe devolver la tabla de contenido asociada del contenedor en lugar de la tabla de contenido estándar.</span><span class="sxs-lookup"><span data-stu-id="ad207-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="ad207-112">Esta marca solo se usa con carpetas.</span><span class="sxs-lookup"><span data-stu-id="ad207-112">This flag is used only with folders.</span></span> <span data-ttu-id="ad207-113">Los mensajes que se incluyen en la tabla de contenido asociada se crearon con la marca MAPI_ASSOCIATED establecida en la llamada al método [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md)</span><span class="sxs-lookup"><span data-stu-id="ad207-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="ad207-114">Normalmente, los clientes usan la tabla de contenido asociada para recuperar formularios, vistas y otros mensajes ocultos.</span><span class="sxs-lookup"><span data-stu-id="ad207-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="ad207-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="ad207-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="ad207-116">Habilita el acceso a los derechos frightsFreeBusySimple y frightsFreeBusyDetailed en **PR_MEMBER_RIGHTS**.</span><span class="sxs-lookup"><span data-stu-id="ad207-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="ad207-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ad207-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ad207-118">**GetContentsTable** puede devolverse correctamente, posiblemente antes de que la tabla esté disponible para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ad207-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="ad207-119">Si la tabla no está disponible, realizar una llamada de tabla posterior puede generar un error.</span><span class="sxs-lookup"><span data-stu-id="ad207-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="ad207-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ad207-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ad207-121">Solicita que las columnas que contienen datos de cadena se devuelvan en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ad207-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="ad207-122">Si no MAPI_UNICODE marca, las cadenas deben devolverse en el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ad207-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="ad207-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="ad207-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="ad207-124">Muestra los elementos que están marcados actualmente como eliminados temporalmente, es decir, están en la fase de tiempo de retención de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="ad207-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="ad207-125">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="ad207-125">_lppTable_</span></span>
  
> <span data-ttu-id="ad207-126">[salida] Puntero a un puntero a la tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="ad207-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ad207-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad207-127">Return value</span></span>

<span data-ttu-id="ad207-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad207-128">S_OK</span></span> 
  
> <span data-ttu-id="ad207-129">La tabla de contenido se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ad207-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="ad207-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ad207-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ad207-131">Se estableció MAPI_UNICODE marca y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="ad207-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="ad207-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ad207-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="ad207-133">El contenedor no tiene contenido y no puede proporcionar una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="ad207-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad207-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad207-134">Remarks</span></span>

<span data-ttu-id="ad207-135">El **método IMAPIContainer::GetContentsTable** devuelve un puntero a la tabla de contenido de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="ad207-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="ad207-136">Una tabla de contenido contiene información resumida acerca de los objetos del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ad207-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="ad207-137">Las tablas de contenido tienen conjuntos de columnas largos.</span><span class="sxs-lookup"><span data-stu-id="ad207-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="ad207-138">Para obtener una lista completa de las columnas obligatorias y opcionales de las tablas de contenido, vea [Tablas de contenido.](contents-tables.md)</span><span class="sxs-lookup"><span data-stu-id="ad207-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="ad207-139">Es posible que algunos contenedores no tengan contenido.</span><span class="sxs-lookup"><span data-stu-id="ad207-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="ad207-140">Estos contenedores devuelven MAPI_E_NO_SUPPORT de sus implementaciones **de GetContentsTable**.</span><span class="sxs-lookup"><span data-stu-id="ad207-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ad207-141">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="ad207-141">Notes to implementers</span></span>

<span data-ttu-id="ad207-142">Si admite una tabla de contenido para el contenedor, también debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ad207-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="ad207-143">Llamadas de soporte técnico al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor para abrir **la PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ad207-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="ad207-144">Devolver **PR_CONTAINER_CONTENTS** respuesta a una llamada al contenedor</span><span class="sxs-lookup"><span data-stu-id="ad207-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="ad207-145">[Métodos IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::GetPropList.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="ad207-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="ad207-146">La implementación de este método por parte de un proveedor de transporte remoto debe devolver un puntero a una interfaz [IMAPITable : IUnknown](imapitableiunknown.md) en el parámetro _ppTable_ pasado al **método GetContentsTable.**</span><span class="sxs-lookup"><span data-stu-id="ad207-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="ad207-147">Si el proveedor de transporte tiene una tabla de contenido existente, es suficiente con devolver un puntero a ella.</span><span class="sxs-lookup"><span data-stu-id="ad207-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="ad207-148">Si no es así, este método debe crear un nuevo objeto [IMAPITable : IUnknown,](imapitableiunknown.md) rellenar la tabla con encabezados de mensaje (si hay alguno disponible) y devolver un puntero a la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="ad207-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="ad207-149">El [método ITableData::HrGetView](itabledata-hrgetview.md) es útil para generar un valor devuelto y almacenar el puntero de tabla en el _parámetro ppTable._</span><span class="sxs-lookup"><span data-stu-id="ad207-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="ad207-150">La tabla de contenido debe admitir al menos las siguientes columnas de propiedad:</span><span class="sxs-lookup"><span data-stu-id="ad207-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="ad207-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad207-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad207-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="ad207-169">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ad207-169">Notes to callers</span></span>

<span data-ttu-id="ad207-170">Las columnas de la tabla de contenido binario y de cadena se pueden truncar.</span><span class="sxs-lookup"><span data-stu-id="ad207-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="ad207-171">Normalmente, los proveedores devuelven 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ad207-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="ad207-172">Como no puede saber de antemano si una tabla incluye columnas truncadas, suponga que una columna se trunca si la longitud de la columna es de 255 o 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="ad207-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="ad207-173">Siempre puede recuperar el valor completo de una columna truncada, si es necesario, directamente desde el objeto usando su identificador de entrada para abrirlo y, a continuación, llamando al método **IMAPIProp::GetProps.**</span><span class="sxs-lookup"><span data-stu-id="ad207-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="ad207-174">Según la implementación del proveedor, las restricciones y las operaciones de ordenación pueden aplicarse a toda una cadena o a la versión truncada de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="ad207-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ad207-175">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ad207-175">MFCMAPI reference</span></span>

<span data-ttu-id="ad207-176">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ad207-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ad207-177">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ad207-177">**File**</span></span>|<span data-ttu-id="ad207-178">**Función**</span><span class="sxs-lookup"><span data-stu-id="ad207-178">**Function**</span></span>|<span data-ttu-id="ad207-179">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ad207-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ad207-180">ContentsTableDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="ad207-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="ad207-181">CContentsTableDlg::CContentsTableDlg</span><span class="sxs-lookup"><span data-stu-id="ad207-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="ad207-182">La **clase CContentsTableDlg** usa **GetContentsTable** para obtener las entradas de una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="ad207-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad207-183">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ad207-183">See also</span></span>



[<span data-ttu-id="ad207-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="ad207-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="ad207-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="ad207-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="ad207-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="ad207-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="ad207-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ad207-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="ad207-188">Propiedad canónica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="ad207-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="ad207-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ad207-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="ad207-190">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ad207-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

