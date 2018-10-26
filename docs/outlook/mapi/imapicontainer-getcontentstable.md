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
ms.openlocfilehash: 9fb8919287420038b5c9165bb14b7d33d1ad2fe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578867"
---
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="61b6c-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="61b6c-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="61b6c-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61b6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61b6c-105">Devuelve un puntero a la tabla de contenido del contenedor.</span><span class="sxs-lookup"><span data-stu-id="61b6c-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="61b6c-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="61b6c-106">Parameters</span></span>

 <span data-ttu-id="61b6c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="61b6c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="61b6c-108">[entrada] Una máscara de bits de indicadores que controla cómo se devuelve en la tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="61b6c-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="61b6c-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="61b6c-109">The following flags can be set:</span></span>
    
<span data-ttu-id="61b6c-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="61b6c-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="61b6c-111">Tabla de contenido asociado del contenedor se debe devolver en lugar de la tabla de contenido estándar.</span><span class="sxs-lookup"><span data-stu-id="61b6c-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="61b6c-112">Este indicador se utiliza sólo con las carpetas.</span><span class="sxs-lookup"><span data-stu-id="61b6c-112">This flag is used only with folders.</span></span> <span data-ttu-id="61b6c-113">Los mensajes que se incluyen en la tabla de contenido asociado se crearon con el indicador MAPI_ASSOCIATED establecido en la llamada al método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="61b6c-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="61b6c-114">Normalmente, los clientes utilizan en la tabla de contenido asociada para recuperar formularios, vistas y otros mensajes ocultos.</span><span class="sxs-lookup"><span data-stu-id="61b6c-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="61b6c-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="61b6c-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="61b6c-116">Permite el acceso a los derechos de frightsFreeBusySimple y frightsFreeBusyDetailed en **PR_MEMBER_RIGHTS**.</span><span class="sxs-lookup"><span data-stu-id="61b6c-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="61b6c-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="61b6c-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="61b6c-118">**GetContentsTable** puede devolver correctamente, posiblemente antes de que la tabla está disponible para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="61b6c-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="61b6c-119">Si no está disponible en la tabla, realizar una llamada de tabla subsiguiente puede producir un error.</span><span class="sxs-lookup"><span data-stu-id="61b6c-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="61b6c-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="61b6c-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="61b6c-121">Solicitudes que se devuelven las columnas que contienen datos de cadena en el formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="61b6c-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="61b6c-122">Si no está establecido el indicador MAPI_UNICODE., se deben devolver las cadenas en el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="61b6c-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="61b6c-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="61b6c-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="61b6c-124">Muestra los elementos que actualmente están marcados como suaves eliminan, es decir, se encuentran en la retención de elementos eliminados fase de tiempo.</span><span class="sxs-lookup"><span data-stu-id="61b6c-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="61b6c-125">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="61b6c-125">_lppTable_</span></span>
  
> <span data-ttu-id="61b6c-126">[out] Un puntero a un puntero a la tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="61b6c-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="61b6c-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61b6c-127">Return value</span></span>

<span data-ttu-id="61b6c-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="61b6c-128">S_OK</span></span> 
  
> <span data-ttu-id="61b6c-129">En la tabla de contenido se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="61b6c-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="61b6c-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="61b6c-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="61b6c-131">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="61b6c-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="61b6c-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="61b6c-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="61b6c-133">El contenedor tiene contenido y no puede proporcionar una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="61b6c-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="61b6c-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61b6c-134">Remarks</span></span>

<span data-ttu-id="61b6c-135">El método **IMAPIContainer::GetContentsTable** devuelve un puntero a la tabla de contenido de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="61b6c-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="61b6c-136">Una tabla de contenido contiene información de resumen acerca de los objetos en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="61b6c-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="61b6c-137">Las tablas de contenido tienen conjuntos de columnas prolongada.</span><span class="sxs-lookup"><span data-stu-id="61b6c-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="61b6c-138">Para obtener una lista completa de las columnas obligatorias y opcionales en las tablas de contenido, vea [Las tablas de contenido](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="61b6c-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="61b6c-139">Es posible que algunos contenedores tener ningún contenido.</span><span class="sxs-lookup"><span data-stu-id="61b6c-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="61b6c-140">Estos contenedores devuelven MAPI_E_NO_SUPPORT de sus implementaciones de **GetContentsTable**.</span><span class="sxs-lookup"><span data-stu-id="61b6c-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="61b6c-141">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="61b6c-141">Notes to implementers</span></span>

<span data-ttu-id="61b6c-142">Si decide admitir una tabla de contenido de su contenedor, también debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="61b6c-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="61b6c-143">Admite las llamadas al método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor para abrir la propiedad **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="61b6c-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="61b6c-144">Devolver **PR_CONTAINER_CONTENTS** en respuesta a una llamada en el contenedor</span><span class="sxs-lookup"><span data-stu-id="61b6c-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="61b6c-145">Métodos [IMAPIProp::GetProps](imapiprop-getprops.md) y [IMAPIProp::GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="61b6c-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="61b6c-146">Implementación del proveedor de transporte remoto de este método debe devolver un puntero a un [IMAPITable: IUnknown](imapitableiunknown.md) interfaz en el parámetro _ppTable_ que se pasan al método **GetContentsTable** .</span><span class="sxs-lookup"><span data-stu-id="61b6c-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="61b6c-147">Si su proveedor de transporte tiene una tabla de contenido existente, es suficiente devolver un puntero a ella.</span><span class="sxs-lookup"><span data-stu-id="61b6c-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="61b6c-148">Si no, este método debe crear un nuevo [IMAPITable: IUnknown](imapitableiunknown.md) de objetos, rellenar la tabla con encabezados de mensaje (si hay alguno disponible) y devolver un puntero a la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="61b6c-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="61b6c-149">El método [ITableData::HrGetView](itabledata-hrgetview.md) es útil para generar un valor devuelto y almacenar el puntero de la tabla en el parámetro _ppTable_ .</span><span class="sxs-lookup"><span data-stu-id="61b6c-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="61b6c-150">En la tabla de contenido debe admitir al menos las siguientes columnas de propiedad:</span><span class="sxs-lookup"><span data-stu-id="61b6c-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="61b6c-151">**Entrada del objeto** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-153">**PR_SENT_REPRESENTING_NAME de MAPI** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-154">**PR_DISPLAY_TO de MAPI** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="61b6c-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61b6c-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="61b6c-169">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="61b6c-169">Notes to callers</span></span>

<span data-ttu-id="61b6c-170">Las columnas de tabla de contenido de cadena y binaria se pueden truncar.</span><span class="sxs-lookup"><span data-stu-id="61b6c-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="61b6c-171">Normalmente, los proveedores devuelven 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="61b6c-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="61b6c-172">Debido a que no se conoce de antemano si una tabla incluye columnas truncadas, supongamos que una columna se trunca si la longitud de la columna es de 255 o 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="61b6c-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="61b6c-173">Siempre puede recuperar el valor completo de una columna truncada, si es necesario, directamente desde el objeto mediante su identificador de entrada para abrirlo y, a continuación, llamar al método **IMAPIProp::GetProps** .</span><span class="sxs-lookup"><span data-stu-id="61b6c-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="61b6c-174">Dependiendo del proveedor en la implementación, las restricciones y las operaciones de ordenación pueden aplicar a todos de una cadena o a la versión truncada de dicha cadena.</span><span class="sxs-lookup"><span data-stu-id="61b6c-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="61b6c-175">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="61b6c-175">MFCMAPI reference</span></span>

<span data-ttu-id="61b6c-176">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="61b6c-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="61b6c-177">**File**</span><span class="sxs-lookup"><span data-stu-id="61b6c-177">**File**</span></span>|<span data-ttu-id="61b6c-178">**Función**</span><span class="sxs-lookup"><span data-stu-id="61b6c-178">**Function**</span></span>|<span data-ttu-id="61b6c-179">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="61b6c-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="61b6c-180">ContentsTableDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="61b6c-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="61b6c-181">CContentsTableDlg::CContentsTableDlg</span><span class="sxs-lookup"><span data-stu-id="61b6c-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="61b6c-182">La clase **CContentsTableDlg** utiliza **GetContentsTable** para obtener las entradas en una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="61b6c-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61b6c-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="61b6c-183">See also</span></span>



[<span data-ttu-id="61b6c-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="61b6c-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="61b6c-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="61b6c-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="61b6c-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="61b6c-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="61b6c-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="61b6c-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="61b6c-188">Propiedad canónico PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="61b6c-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="61b6c-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="61b6c-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="61b6c-190">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="61b6c-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

