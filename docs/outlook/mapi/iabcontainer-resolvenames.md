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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279573"
---
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="99d88-103">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="99d88-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="99d88-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99d88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99d88-105">Realiza la resolución de nombres de una o varias entradas de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="99d88-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="99d88-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="99d88-106">Parameters</span></span>

 <span data-ttu-id="99d88-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="99d88-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="99d88-108">a Un puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que describe las propiedades que se van a incluir en la estructura [ADRLIST](adrlist.md) devuelta por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="99d88-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="99d88-109">Para solicitar el conjunto predeterminado de propiedades del proveedor, pase NULL en el parámetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="99d88-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="99d88-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="99d88-110">_ulFlags_</span></span>
  
> <span data-ttu-id="99d88-111">a Máscara de máscara de marcadores que controla el tipo de texto en las cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="99d88-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="99d88-112">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="99d88-112">The following flags can be set:</span></span>
    
<span data-ttu-id="99d88-113">EMS_AB_ADDRESS_LOOKUP</span><span class="sxs-lookup"><span data-stu-id="99d88-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="99d88-114">Solo se encuentran coincidencias exactas de direcciones de proxy; se omiten las coincidencias parciales.</span><span class="sxs-lookup"><span data-stu-id="99d88-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="99d88-115">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="99d88-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="99d88-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="99d88-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="99d88-117">Solo se usará la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="99d88-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="99d88-118">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo caché de Exchange y obtenga acceso a una entrada de la libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="99d88-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="99d88-119">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="99d88-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="99d88-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="99d88-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="99d88-121">Las propiedades de cadena devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="99d88-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="99d88-122">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="99d88-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="99d88-123">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="99d88-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="99d88-124">[in, out] En la entrada, un puntero a una estructura **ADRLIST** que contiene la lista de los destinatarios que se van a resolver.</span><span class="sxs-lookup"><span data-stu-id="99d88-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="99d88-125">En la salida, un puntero a una estructura **ADRLIST** que contiene los nombres resueltos.</span><span class="sxs-lookup"><span data-stu-id="99d88-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="99d88-126">_lpFlagList_</span><span class="sxs-lookup"><span data-stu-id="99d88-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="99d88-127">[in, out] Un puntero a una matriz de indicadores, cada indicador correspondiente a una estructura [ADRENTRY](adrentry.md) en el parámetro _lpAdrList_ , que proporciona el estado de la operación de resolución de nombres para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="99d88-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="99d88-128">Las marcas del parámetro _lpFlagList_ están en el mismo orden que las entradas de _lpAdrList_.</span><span class="sxs-lookup"><span data-stu-id="99d88-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="99d88-129">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="99d88-129">The following flags can be set:</span></span>
    
<span data-ttu-id="99d88-130">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="99d88-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="99d88-131">Se ha resuelto el destinatario correspondiente, pero no un identificador de entrada único.</span><span class="sxs-lookup"><span data-stu-id="99d88-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="99d88-132">Otros contenedores no deben intentar resolver este destinatario.</span><span class="sxs-lookup"><span data-stu-id="99d88-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="99d88-133">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="99d88-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="99d88-134">El destinatario correspondiente se ha resuelto en un identificador de entrada único.</span><span class="sxs-lookup"><span data-stu-id="99d88-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="99d88-135">Otros contenedores no deben intentar resolver este destinatario.</span><span class="sxs-lookup"><span data-stu-id="99d88-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="99d88-136">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="99d88-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="99d88-137">No se ha resuelto la entrada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="99d88-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="99d88-138">Otros contenedores deben intentar resolver este destinatario.</span><span class="sxs-lookup"><span data-stu-id="99d88-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="99d88-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99d88-139">Return value</span></span>

<span data-ttu-id="99d88-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="99d88-140">S_OK</span></span> 
  
> <span data-ttu-id="99d88-141">El proceso de resolución de nombres se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="99d88-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="99d88-142">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="99d88-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="99d88-143">Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="99d88-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="99d88-144">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="99d88-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="99d88-145">El proveedor de la libreta de direcciones no admite la resolución de nombres en masa mediante este método.</span><span class="sxs-lookup"><span data-stu-id="99d88-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99d88-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99d88-146">Remarks</span></span>

<span data-ttu-id="99d88-147">El método **ResolveNames** intenta hacer coincidir los destinatarios sin resolver de la matriz de entradas en el parámetro _lpAdrList_ con los destinatarios de este contenedor de libretas de direcciones.</span><span class="sxs-lookup"><span data-stu-id="99d88-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="99d88-148">Un destinatario sin resolver suele tener sólo la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y, posiblemente, algunas otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="99d88-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="99d88-149">Un destinatario sin resolver no tiene la propiedad de \*\*\*\* ([PidTagEntryId](pidtagentryid-canonical-property.md)) y su marca correspondiente en el parámetro _lpFlagList_ se establece en MAPI_UNRESOLVED.</span><span class="sxs-lookup"><span data-stu-id="99d88-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="99d88-150">Por el contrario, un destinatario resuelto siempre tiene al menos la \*\*\*\* propiedad del tipo de propiedad más otras propiedades, como **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**y **PR_ADDRTYPE** ([ PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="99d88-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="99d88-151">La resolución de nombres suele iniciarse cuando un cliente llama al método [IAddrBook:: ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="99d88-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="99d88-152">MAPI de Outlook responde llamando al método **ResolveNames** de cada contenedor de libretas de direcciones incluido en la ruta de acceso de búsqueda de la libreta de direcciones, especificada por la propiedad **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="99d88-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="99d88-153">Las entradas del parámetro _lpAdrList_ incluyen los destinatarios que ya se han resuelto porque están en contenedores para los que MAPI ya ha llamado a **ResolveNames**, porque las entradas aparecen antes en la ruta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="99d88-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="99d88-154">Cada contenedor intenta resolver las entradas sin resolver haciendo coincidir el nombre para mostrar del destinatario con el nombre para mostrar de una de sus entradas.</span><span class="sxs-lookup"><span data-stu-id="99d88-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="99d88-155">Cuando se encuentra una coincidencia única, **ResolveNames** agrega la \*\*\*\* propiedad número y otras propiedades que se incluyen en el parámetro _lpPropTagArray_ a la entrada correspondiente en la estructura **ADRLIST** de salida.</span><span class="sxs-lookup"><span data-stu-id="99d88-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="99d88-156">A continuación, **ResolveNames** establece la entrada en el parámetro _lpFlagList_ en MAPI_RESOLVED.</span><span class="sxs-lookup"><span data-stu-id="99d88-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="99d88-157">El identificador de entrada almacenado en la \*\*\*\* propiedad o puede ser a corto o largo plazo.</span><span class="sxs-lookup"><span data-stu-id="99d88-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="99d88-158">Una vez que todos los contenedores de la ruta de acceso de búsqueda han intentado realizar el proceso de resolución de nombres, MAPI abre un cuadro de diálogo, si es posible, para solicitar ayuda al usuario para resolver los conflictos restantes.</span><span class="sxs-lookup"><span data-stu-id="99d88-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="99d88-159">Los clientes también pueden usar la estructura **ADRLIST** devuelta en llamadas al método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="99d88-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="99d88-160">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="99d88-160">Notes to implementers</span></span>

<span data-ttu-id="99d88-161">No es necesario que admita la resolución de nombres con el método **ResolveNames** .</span><span class="sxs-lookup"><span data-stu-id="99d88-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="99d88-162">En su lugar, o también puede admitirla con la restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="99d88-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="99d88-163">Si decide utilizar la restricción **PR_ANR** para la resolución de nombres, puede devolver MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="99d88-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="99d88-164">For more information, see [Implementaci�n de la resoluci�n de nombres](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="99d88-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="99d88-165">Establezca la entrada de la marca del destinatario en el parámetro _lpFlagList_ en MAPI_UNRESOLVED si el destinatario no coincide con ninguno de los destinatarios del contenedor.</span><span class="sxs-lookup"><span data-stu-id="99d88-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="99d88-166">Cuando un destinatario coincide con varios destinatarios, establezca su indicador en MAPI_AMBIGUOUS y no cambie su estructura **ADRENTRY** .</span><span class="sxs-lookup"><span data-stu-id="99d88-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="99d88-167">MAPI requiere ciertas propiedades para los destinatarios incluidos en la lista de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="99d88-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="99d88-168">Puede incluirlos en la estructura **ADRENTRY** como parte del proceso de resolución de nombres o esperar a que MAPI los solicite con llamadas a los métodos [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) y [IMAPISupport:: ExpandRecips](imapisupport-expandrecips.md) .</span><span class="sxs-lookup"><span data-stu-id="99d88-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="99d88-169">Puede eliminar estas llamadas adicionales y mejorar el rendimiento si incluye las siguientes propiedades en las estructuras **ADRENTRY** de todos los destinatarios resueltos:</span><span class="sxs-lookup"><span data-stu-id="99d88-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="99d88-170">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="99d88-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="99d88-171">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="99d88-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="99d88-172">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="99d88-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="99d88-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="99d88-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="99d88-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99d88-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="99d88-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99d88-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="99d88-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99d88-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="99d88-177">Si algunas de las propiedades del parámetro _lpPropTagArray_ no están disponibles, normalmente porque la entrada del contenedor no admite las propiedades y no se incluyen en el miembro **ADRENTRY** del destinatario en la estructura **ADRLIST** : Establezca el tipo de propiedad de cada propiedad no disponible en PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="99d88-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="99d88-178">No quite ninguna propiedad de la estructura **ADRENTRY** de un destinatario resuelto.</span><span class="sxs-lookup"><span data-stu-id="99d88-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="99d88-179">Si debe reemplazar en lugar de modificar una estructura **ADRENTRY** , libere primero la estructura **ADRENTRY** original llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) y, a continuación, asigne la estructura **ADRENTRY** de reemplazo por [ MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="99d88-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="99d88-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="99d88-180">See also</span></span>



[<span data-ttu-id="99d88-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="99d88-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="99d88-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="99d88-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="99d88-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="99d88-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="99d88-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="99d88-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="99d88-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="99d88-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="99d88-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="99d88-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="99d88-187">Propiedad canónica PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="99d88-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="99d88-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="99d88-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="99d88-189">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="99d88-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

