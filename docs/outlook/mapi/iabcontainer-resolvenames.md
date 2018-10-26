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
ms.openlocfilehash: 81f35f659342d6258d60f40b12bd0a3ac2dc20b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588478"
---
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="9d7e3-103">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="9d7e3-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="9d7e3-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d7e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d7e3-105">Realiza la resolución de nombres para una o más entradas de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="9d7e3-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="9d7e3-106">Parameters</span></span>

 <span data-ttu-id="9d7e3-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="9d7e3-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="9d7e3-108">[entrada] Un puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que describe las propiedades que se deben incluir en la estructura [ADRLIST](adrlist.md) devuelta por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="9d7e3-109">Para solicitar el conjunto de propiedades predeterminadas de un proveedor, pase NULL en el parámetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="9d7e3-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="9d7e3-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9d7e3-110">_ulFlags_</span></span>
  
> <span data-ttu-id="9d7e3-111">[entrada] Una máscara de bits de indicadores que controla el tipo de texto de las cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="9d7e3-112">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="9d7e3-112">The following flags can be set:</span></span>
    
<span data-ttu-id="9d7e3-113">EMS_AB_ADDRESS_LOOKUP</span><span class="sxs-lookup"><span data-stu-id="9d7e3-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="9d7e3-114">Se encontrará sólo coincidencias de dirección de proxy exacta; se omiten las coincidencias parciales.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="9d7e3-115">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="9d7e3-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="9d7e3-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="9d7e3-117">Sólo la libreta de direcciones sin conexión se usará para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="9d7e3-118">Por ejemplo, puede usar esta marca para habilitar una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="9d7e3-119">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="9d7e3-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9d7e3-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9d7e3-121">Las propiedades de la cadena devuelta se encuentran en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="9d7e3-122">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="9d7e3-123">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="9d7e3-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="9d7e3-124">[entrada, salida] En la entrada, un puntero a una estructura **ADRLIST** que contiene la lista de los destinatarios que se puede resolver.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="9d7e3-125">En la salida, un puntero a una estructura **ADRLIST** que contiene los nombres resueltos.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="9d7e3-126">_lpFlagList_</span><span class="sxs-lookup"><span data-stu-id="9d7e3-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="9d7e3-127">[entrada, salida] Un puntero a una matriz de marcadores, cada marca correspondiente a una estructura [ADRENTRY](adrentry.md) en el parámetro _lpAdrList_ , que proporciona el estado de la operación de resolución de nombres para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="9d7e3-128">Las marcas en el parámetro _lpFlagList_ se encuentran en el mismo orden que las entradas de _lpAdrList_.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="9d7e3-129">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="9d7e3-129">The following flags can be set:</span></span>
    
<span data-ttu-id="9d7e3-130">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="9d7e3-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="9d7e3-131">El destinatario correspondiente se ha resuelto, pero no a un identificador de entrada único.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="9d7e3-132">No deben intentar resolver a este destinatario otros contenedores.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="9d7e3-133">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="9d7e3-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="9d7e3-134">Se ha resuelto el destinatario correspondiente a un identificador de entrada único.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="9d7e3-135">No deben intentar resolver a este destinatario otros contenedores.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="9d7e3-136">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="9d7e3-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="9d7e3-137">La entrada correspondiente no se ha resuelto.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="9d7e3-138">Otros contenedores deben intentar resolver a este destinatario.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9d7e3-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d7e3-139">Return value</span></span>

<span data-ttu-id="9d7e3-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="9d7e3-140">S_OK</span></span> 
  
> <span data-ttu-id="9d7e3-141">El proceso de resolución de nombres fue correcto.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="9d7e3-142">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9d7e3-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9d7e3-143">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="9d7e3-144">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9d7e3-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9d7e3-145">El proveedor de la libreta de direcciones no es compatible con la resolución de nombres de forma masiva mediante el uso de este método.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d7e3-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d7e3-146">Remarks</span></span>

<span data-ttu-id="9d7e3-147">El método **ResolveNames** intenta hacer coincidir a los destinatarios sin resolver de la matriz de entradas en el parámetro _lpAdrList_ a los destinatarios de este contenedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="9d7e3-148">Un destinatario sin resolver normalmente tiene sólo la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y, posiblemente, algunas otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="9d7e3-149">Un destinatario sin resolver no tiene la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y su marca correspondiente en el parámetro _lpFlagList_ se establece en MAPI_UNRESOLVED.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="9d7e3-150">Por el contrario, un destinatario resuelto siempre tiene al menos la propiedad de **entrada del objeto** además de otras propiedades, como **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**y **PR_ADDRTYPE** ([ PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9d7e3-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="9d7e3-151">Resolución de nombres normalmente se inicia cuando un cliente llama al método [IAddrBook::ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="9d7e3-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="9d7e3-152">MAPI de Outlook responde llamando al método **ResolveNames** de cada contenedor de la libreta de direcciones incluida en la ruta de búsqueda de la libreta de direcciones, especificada por la propiedad **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9d7e3-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="9d7e3-153">Las entradas en el parámetro _lpAdrList_ incluyen a destinatarios ya resueltos porque están en contenedores para la que MAPI ya ha llamado **ResolveNames**, debido a que las entradas que aparece anteriormente en la ruta de acceso de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="9d7e3-154">Cada contenedor intenta resolver las entradas sin resolver de forma que coincidan con el nombre para mostrar del destinatario con el nombre para mostrar de uno de sus entradas.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="9d7e3-155">Cuando se encuentra una coincidencia única, **ResolveNames** agrega la propiedad de **entrada del objeto** y otras propiedades que se incluyen en el parámetro _lpPropTagArray_ a la entrada correspondiente en la estructura **ADRLIST** saliente.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="9d7e3-156">**ResolveNames** , a continuación, Establece la entrada en el parámetro _lpFlagList_ a MAPI_RESOLVED.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="9d7e3-157">Puede ser el identificador de entrada que se almacenan en la propiedad de **entrada del objeto** a corto plazo o a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="9d7e3-158">Después de todos los contenedores en la búsqueda de ruta de acceso ha intentado realizar el proceso de resolución de nombres, MAPI abre un cuadro de diálogo, si es posible, para preguntar al usuario para obtener ayuda y resolver los conflictos restantes.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="9d7e3-159">Los clientes también pueden usar la estructura **ADRLIST** devuelta en las llamadas al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="9d7e3-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9d7e3-160">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="9d7e3-160">Notes to implementers</span></span>

<span data-ttu-id="9d7e3-161">No son necesarios para admitir la resolución de nombres con el método **ResolveNames** .</span><span class="sxs-lookup"><span data-stu-id="9d7e3-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="9d7e3-162">En su lugar, o además, se pueden admitir con la restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9d7e3-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="9d7e3-163">Si decide se basan en la restricción de **PR_ANR** para la resolución de nombres, puede devolver MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="9d7e3-164">For more information, see [Implementaci�n de la resoluci�n de nombres](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="9d7e3-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="9d7e3-165">Establezca la entrada de marca de un destinatario en el parámetro _lpFlagList_ a MAPI_UNRESOLVED si el destinatario no coincide con ninguno de los destinatarios del contenedor.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="9d7e3-166">Cuando un destinatario coincide con varios destinatarios, establezca su marca en MAPI_AMBIGUOUS y no cambie su estructura **ADRENTRY** .</span><span class="sxs-lookup"><span data-stu-id="9d7e3-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="9d7e3-167">MAPI requiere algunas propiedades para los destinatarios que se incluyen en la lista de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="9d7e3-168">Puede incluir en la estructura **ADRENTRY** como parte del proceso de resolución de nombre o esperar MAPI solicitar ellos con las llamadas a los métodos [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) y [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) .</span><span class="sxs-lookup"><span data-stu-id="9d7e3-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="9d7e3-169">Puede eliminar estas llamadas adicionales y mejorar el rendimiento mediante la inclusión de las siguientes propiedades en las estructuras **ADRENTRY** de todos los destinatarios resueltos:</span><span class="sxs-lookup"><span data-stu-id="9d7e3-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="9d7e3-170">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="9d7e3-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="9d7e3-171">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="9d7e3-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="9d7e3-172">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="9d7e3-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="9d7e3-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="9d7e3-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="9d7e3-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9d7e3-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="9d7e3-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9d7e3-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="9d7e3-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9d7e3-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="9d7e3-177">Si algunas de las propiedades en el parámetro _lpPropTagArray_ no están disponibles, normalmente debido a que la entrada de contenedor no es compatible con las propiedades y no se incluyen en el miembro **ADRENTRY** del destinatario de la estructura de **ADRLIST** : Establezca el tipo de propiedad de cada propiedad no está disponible en PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="9d7e3-178">No quite todas las propiedades de la estructura **ADRENTRY** resuelve un destinatario.</span><span class="sxs-lookup"><span data-stu-id="9d7e3-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="9d7e3-179">Si debe reemplazar en lugar de modificar una estructura **ADRENTRY** , libre de la estructura **ADRENTRY** original en primer lugar por llamar a la función [MAPIFreeBuffer](mapifreebuffer.md) y, a continuación, asignar la estructura **ADRENTRY** con [de sustitución MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="9d7e3-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9d7e3-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d7e3-180">See also</span></span>



[<span data-ttu-id="9d7e3-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="9d7e3-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="9d7e3-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="9d7e3-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="9d7e3-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="9d7e3-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="9d7e3-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="9d7e3-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="9d7e3-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="9d7e3-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="9d7e3-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="9d7e3-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="9d7e3-187">Propiedad canónico PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="9d7e3-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="9d7e3-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="9d7e3-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="9d7e3-189">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="9d7e3-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

