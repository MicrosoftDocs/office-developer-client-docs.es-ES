---
title: IABContainerResolveNames
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.ResolveNames
api_type:
- COM
ms.assetid: 27474af2-29a2-4cfb-b94f-72eb91562dac
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fac4978bef94650f85ac3179acd3858602f933ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405817"
---
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="68f48-103">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="68f48-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="68f48-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68f48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68f48-105">Realiza la resolución de nombres para una o varias entradas de destinatario.</span><span class="sxs-lookup"><span data-stu-id="68f48-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="68f48-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68f48-106">Parameters</span></span>

 <span data-ttu-id="68f48-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="68f48-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="68f48-108">[entrada] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que describen las propiedades que se incluirán en la estructura [ADRLIST](adrlist.md) devuelta por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="68f48-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="68f48-109">Para solicitar el conjunto predeterminado de propiedades del proveedor, pase NULL en el _parámetro lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="68f48-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="68f48-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="68f48-110">_ulFlags_</span></span>
  
> <span data-ttu-id="68f48-111">[entrada] Máscara de bits de marcas que controla el tipo de texto en las cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="68f48-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="68f48-112">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="68f48-112">The following flags can be set:</span></span>
    
<span data-ttu-id="68f48-113">EMS_AB_ADDRESS_LOOKUP</span><span class="sxs-lookup"><span data-stu-id="68f48-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="68f48-114">Solo se encontrarán coincidencias exactas de direcciones proxy; se omiten las coincidencias parciales.</span><span class="sxs-lookup"><span data-stu-id="68f48-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="68f48-115">Esta marca solo es compatible con el proveedor de libretas de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="68f48-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="68f48-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="68f48-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="68f48-117">Solo se usará la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="68f48-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="68f48-118">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente abra la lista global de direcciones (GAL) en modo caché de Exchange y obtenga acceso a una entrada de esa libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="68f48-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="68f48-119">Esta marca solo es compatible con el proveedor de libretas de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="68f48-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="68f48-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="68f48-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="68f48-121">Las propiedades de cadena devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="68f48-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="68f48-122">Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="68f48-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="68f48-123">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="68f48-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="68f48-124">[entrada, salida] En la entrada, un puntero a una **estructura ADRLIST** que contiene la lista de destinatarios que se va a resolver.</span><span class="sxs-lookup"><span data-stu-id="68f48-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="68f48-125">En el resultado, un puntero a una **estructura ADRLIST** que contiene los nombres resueltos.</span><span class="sxs-lookup"><span data-stu-id="68f48-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="68f48-126">_lpFlagList_</span><span class="sxs-lookup"><span data-stu-id="68f48-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="68f48-127">[entrada, salida] Puntero a una matriz de marcas, cada marca correspondiente a una estructura [ADRENTRY](adrentry.md) en el parámetro  _lpAdrList,_ que proporciona el estado de la operación de resolución de nombres para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="68f48-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="68f48-128">Las marcas del parámetro  _lpFlagList_ están en el mismo orden que las entradas de  _lpAdrList_.</span><span class="sxs-lookup"><span data-stu-id="68f48-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="68f48-129">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="68f48-129">The following flags can be set:</span></span>
    
<span data-ttu-id="68f48-130">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="68f48-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="68f48-131">El destinatario correspondiente se ha resuelto, pero no a un identificador de entrada único.</span><span class="sxs-lookup"><span data-stu-id="68f48-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="68f48-132">Otros contenedores no deben intentar resolver este destinatario.</span><span class="sxs-lookup"><span data-stu-id="68f48-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="68f48-133">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="68f48-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="68f48-134">El destinatario correspondiente se ha resuelto en un identificador de entrada único.</span><span class="sxs-lookup"><span data-stu-id="68f48-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="68f48-135">Otros contenedores no deben intentar resolver este destinatario.</span><span class="sxs-lookup"><span data-stu-id="68f48-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="68f48-136">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="68f48-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="68f48-137">No se ha resuelto la entrada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="68f48-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="68f48-138">Otros contenedores deben intentar resolver este destinatario.</span><span class="sxs-lookup"><span data-stu-id="68f48-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="68f48-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68f48-139">Return value</span></span>

<span data-ttu-id="68f48-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="68f48-140">S_OK</span></span> 
  
> <span data-ttu-id="68f48-141">El proceso de resolución de nombres se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="68f48-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="68f48-142">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="68f48-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="68f48-143">Se estableció MAPI_UNICODE marca y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="68f48-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="68f48-144">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="68f48-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="68f48-145">El proveedor de libreta de direcciones no admite la resolución de nombres masivos mediante este método.</span><span class="sxs-lookup"><span data-stu-id="68f48-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68f48-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="68f48-146">Remarks</span></span>

<span data-ttu-id="68f48-147">El **método ResolveNames** intenta hacer coincidir los destinatarios sin resolver de la matriz de entradas del parámetro  _lpAdrList_ con los destinatarios de este contenedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="68f48-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="68f48-148">Normalmente, un destinatario sin resolver solo **tiene la PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y posiblemente algunas otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="68f48-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="68f48-149">Un destinatario sin resolver no tiene la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y su marca correspondiente en el parámetro  _lpFlagList_ se establece en MAPI_UNRESOLVED.</span><span class="sxs-lookup"><span data-stu-id="68f48-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="68f48-150">Por el contrario, un destinatario resuelto siempre tiene al menos la propiedad **PR_ENTRYID** más otras propiedades, como **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME** y **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="68f48-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="68f48-151">La resolución de nombres normalmente se inicia cuando un cliente llama al [método IAddrBook::ResolveName.](iaddrbook-resolvename.md)</span><span class="sxs-lookup"><span data-stu-id="68f48-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="68f48-152">Mapi de Outlook responde llamando al método **ResolveNames** de cada contenedor de libreta de direcciones incluido en la ruta de acceso de búsqueda de la libreta de direcciones, especificado por la **propiedad PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="68f48-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="68f48-153">Las entradas del parámetro  _lpAdrList_ incluyen destinatarios ya resueltos porque están en contenedores para los que MAPI ya ha llamado **ResolveNames**, porque las entradas aparecen anteriormente en la ruta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="68f48-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="68f48-154">Cada contenedor intenta resolver las entradas no resueltas haciendo coincidir el nombre para mostrar del destinatario con el nombre para mostrar de una de sus entradas.</span><span class="sxs-lookup"><span data-stu-id="68f48-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="68f48-155">Cuando se encuentra una coincidencia única, **ResolveNames** agrega la propiedad PR_ENTRYID y otras propiedades que se incluyen en el parámetro _lpPropTagArray_ **a** la entrada correspondiente en la estructura **ADRLIST saliente.**</span><span class="sxs-lookup"><span data-stu-id="68f48-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="68f48-156">**ResolveNames,** a continuación, establece la entrada en el  _parámetro lpFlagList_ en MAPI_RESOLVED.</span><span class="sxs-lookup"><span data-stu-id="68f48-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="68f48-157">El identificador de entrada almacenado en **PR_ENTRYID** propiedad puede ser a corto o largo plazo.</span><span class="sxs-lookup"><span data-stu-id="68f48-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="68f48-158">Después de que todos los contenedores de la ruta de búsqueda han intentado el proceso de resolución de nombres, MAPI abre un cuadro de diálogo, si es posible, para solicitar ayuda al usuario para resolver los conflictos restantes.</span><span class="sxs-lookup"><span data-stu-id="68f48-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="68f48-159">Los clientes también pueden usar la estructura **ADRLIST devuelta** en llamadas al método [IMessage::ModifyRecipients.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="68f48-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="68f48-160">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="68f48-160">Notes to implementers</span></span>

<span data-ttu-id="68f48-161">No es necesario que admita la resolución de nombres con el **método ResolveNames.**</span><span class="sxs-lookup"><span data-stu-id="68f48-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="68f48-162">En su lugar, o además, puede admitirlo con la restricción PR_ANR **propiedad** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="68f48-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="68f48-163">Si decide confiar en la restricción de **PR_ANR** para la resolución de nombres, puede devolver MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="68f48-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="68f48-164">For more information, see [Implementaci�n de la resoluci�n de nombres](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="68f48-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="68f48-165">Establezca la entrada de marca de un destinatario en el parámetro  _lpFlagList_ en MAPI_UNRESOLVED si el destinatario no coincide con ninguno de los destinatarios del contenedor.</span><span class="sxs-lookup"><span data-stu-id="68f48-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="68f48-166">Cuando un destinatario coincide con varios destinatarios, establezca su marca en MAPI_AMBIGUOUS y no cambie su **estructura ADRENTRY.**</span><span class="sxs-lookup"><span data-stu-id="68f48-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="68f48-167">MAPI requiere ciertas propiedades para los destinatarios que se incluyen en la lista de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="68f48-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="68f48-168">Puede incluirlos en la estructura **ADRENTRY** como parte del proceso de resolución de nombres o esperar a que MAPI los solicite con llamadas a los métodos [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) e [IMAPISupport::ExpandRecips.](imapisupport-expandrecips.md)</span><span class="sxs-lookup"><span data-stu-id="68f48-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="68f48-169">Puede eliminar estas llamadas adicionales y mejorar el rendimiento si incluye las siguientes propiedades en las estructuras **ADRENTRY** de todos los destinatarios resueltos:</span><span class="sxs-lookup"><span data-stu-id="68f48-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="68f48-170">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="68f48-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="68f48-171">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="68f48-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="68f48-172">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="68f48-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="68f48-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="68f48-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="68f48-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="68f48-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="68f48-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="68f48-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="68f48-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="68f48-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="68f48-177">Si algunas de las propiedades del parámetro  _lpPropTagArray_ no están disponibles (normalmente porque la entrada del contenedor no admite las propiedades y no se incluyen en el miembro **ADRENTRY** del destinatario en la estructura **ADRLIST),** establezca el tipo de propiedad de cada propiedad no disponible en PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="68f48-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="68f48-178">No quite ninguna propiedad de la estructura **ADRENTRY** de un destinatario resuelto.</span><span class="sxs-lookup"><span data-stu-id="68f48-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="68f48-179">Si debe reemplazar en lugar de modificar una estructura **ADRENTRY,** primero debe liberar la estructura **ADRENTRY** original llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) y, a continuación, asigne la estructura **ADRENTRY** de reemplazo con [MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="68f48-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="68f48-180">Consulte también</span><span class="sxs-lookup"><span data-stu-id="68f48-180">See also</span></span>



[<span data-ttu-id="68f48-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="68f48-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="68f48-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="68f48-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="68f48-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="68f48-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="68f48-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="68f48-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="68f48-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="68f48-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="68f48-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="68f48-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="68f48-187">Propiedad canónica PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="68f48-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="68f48-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="68f48-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="68f48-189">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="68f48-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

