---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1f09c88d9bd6720720e2d30ac24fa4a19aed5538
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567233"
---
# <a name="iaddrbookresolvename"></a><span data-ttu-id="01efb-103">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="01efb-103">IAddrBook::ResolveName</span></span>

  
  
<span data-ttu-id="01efb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01efb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01efb-105">Realiza la resolución de nombres, asignar los identificadores de entrada a los destinatarios en una lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="01efb-105">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="01efb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01efb-106">Parameters</span></span>

 <span data-ttu-id="01efb-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="01efb-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="01efb-108">[entrada] Un identificador de la ventana principal de un cuadro de diálogo que se muestra, si se especifica, para que solicite al usuario que resuelva la ambigüedad.</span><span class="sxs-lookup"><span data-stu-id="01efb-108">[in] A handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span></span>
    
 <span data-ttu-id="01efb-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="01efb-109">_ulFlags_</span></span>
  
> <span data-ttu-id="01efb-110">[entrada] Una máscara de bits de indicadores que controlan los distintos aspectos del proceso de resolución.</span><span class="sxs-lookup"><span data-stu-id="01efb-110">[in] A bitmask of flags that control various aspects of the resolution process.</span></span> <span data-ttu-id="01efb-111">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="01efb-111">The following flags can be set:</span></span>
    
<span data-ttu-id="01efb-112">AB_UNICODEUI</span><span class="sxs-lookup"><span data-stu-id="01efb-112">AB_UNICODEUI</span></span>
  
> <span data-ttu-id="01efb-113">Indica que _lpszNewEntryTitle_ es una cadena UNICODE.</span><span class="sxs-lookup"><span data-stu-id="01efb-113">Indicates that  _lpszNewEntryTitle_ is a UNICODE string.</span></span> 
    
<span data-ttu-id="01efb-114">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="01efb-114">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="01efb-115">Usar sólo la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="01efb-115">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="01efb-116">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="01efb-116">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="01efb-117">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="01efb-117">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="01efb-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="01efb-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="01efb-119">Muestra un cuadro de diálogo para preguntar al usuario para la información de resolución de nombres adicionales.</span><span class="sxs-lookup"><span data-stu-id="01efb-119">Displays a dialog box to prompt the user for additional name resolution information.</span></span> <span data-ttu-id="01efb-120">Si no se establece este marcador, no se muestra ningún cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="01efb-120">If this flag is not set, no dialog box is displayed.</span></span> 
    
<span data-ttu-id="01efb-121">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="01efb-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="01efb-122">Indica que las propiedades devueltas en la lista de direcciones deben ser de tipo PT_UNICODE en lugar de PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="01efb-122">Indicates that the properties returned in the address list should be of type PT_UNICODE instead of PT_STRING8.</span></span> 
    
 <span data-ttu-id="01efb-123">_lpszNewEntryTitle_</span><span class="sxs-lookup"><span data-stu-id="01efb-123">_lpszNewEntryTitle_</span></span>
  
> <span data-ttu-id="01efb-124">[entrada] Un puntero al texto del título del control en el cuadro de diálogo que solicita al usuario que escriba a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="01efb-124">[in] A pointer to text for the title of the control in the dialog box that prompts the user to enter a recipient.</span></span> <span data-ttu-id="01efb-125">El título varía según el tipo de destinatario.</span><span class="sxs-lookup"><span data-stu-id="01efb-125">The title varies depending on the type of recipient.</span></span> <span data-ttu-id="01efb-126">El parámetro _lpszNewEntryTitle_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="01efb-126">The  _lpszNewEntryTitle_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="01efb-127">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="01efb-127">_lpAdrList_</span></span>
  
> <span data-ttu-id="01efb-128">[entrada salida] Un puntero a una estructura [ADRLIST](adrlist.md) que contiene la lista de nombres de los destinatarios que se va a resolver.</span><span class="sxs-lookup"><span data-stu-id="01efb-128">[in-out] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipient names to be resolved.</span></span> <span data-ttu-id="01efb-129">Esta estructura **ADRLIST** puede crearse mediante el método [IAddrBook::Address](iaddrbook-address.md) .</span><span class="sxs-lookup"><span data-stu-id="01efb-129">This **ADRLIST** structure can be created by the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="01efb-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01efb-130">Return value</span></span>

<span data-ttu-id="01efb-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="01efb-131">S_OK</span></span> 
  
> <span data-ttu-id="01efb-132">El proceso de resolución de nombres se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="01efb-132">The name resolution process succeeded.</span></span>
    
<span data-ttu-id="01efb-133">MAPI_E_AMBIGUOUS_RECIP</span><span class="sxs-lookup"><span data-stu-id="01efb-133">MAPI_E_AMBIGUOUS_RECIP</span></span> 
  
> <span data-ttu-id="01efb-134">Al menos un destinatario en el parámetro _lpAdrList_ , coincidió con más de una entrada en la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="01efb-134">At least one recipient in the  _lpAdrList_ parameter matched more than one entry in the address book.</span></span> <span data-ttu-id="01efb-135">Normalmente, este valor se devuelve cuando se establece la marca MAPI_DIALOG, prohibir la presentación de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="01efb-135">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
<span data-ttu-id="01efb-136">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="01efb-136">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="01efb-137">No se puede resolver al menos un destinatario en el parámetro _lpAdrList_ .</span><span class="sxs-lookup"><span data-stu-id="01efb-137">At least one recipient in the  _lpAdrList_ parameter cannot be resolved.</span></span> <span data-ttu-id="01efb-138">Normalmente, este valor se devuelve cuando se establece la marca MAPI_DIALOG, prohibir la presentación de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="01efb-138">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="01efb-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="01efb-139">Remarks</span></span>

<span data-ttu-id="01efb-140">Los clientes y proveedores de servicios de llamar al método **ResolveName** para iniciar el proceso de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="01efb-140">Clients and service providers call the **ResolveName** method to initiate the name resolution process.</span></span> <span data-ttu-id="01efb-141">Una entrada no resuelta es una entrada que aún no tiene una propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) o el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="01efb-141">An unresolved entry is an entry that does not yet have an entry identifier or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
 <span data-ttu-id="01efb-142">**ResolveName** pasa por el proceso siguiente para cada entrada sin resolver en la lista de direcciones que se pasa en el parámetro _lpAdrList_ .</span><span class="sxs-lookup"><span data-stu-id="01efb-142">**ResolveName** goes through the following process for each unresolved entry in the address list passed in the  _lpAdrList_ parameter.</span></span> 
  
1. <span data-ttu-id="01efb-143">Si el tipo de dirección del destinatario sigue el formato de una dirección SMTP ( _displayname_@ _dominio de nivel domain.top_), **ResolveName** le asigna un identificador de entrada único.</span><span class="sxs-lookup"><span data-stu-id="01efb-143">If the address type of the recipient adheres to the format of an SMTP address ( _displayname_@ _domain.top-level-domain_), **ResolveName** assigns it a one-off entry identifier.</span></span> 
    
2. <span data-ttu-id="01efb-144">Para cada contenedor de la propiedad **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), **ResolveName** llama el método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) .</span><span class="sxs-lookup"><span data-stu-id="01efb-144">For each container in the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property, **ResolveName** calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="01efb-145">**ResolveNames** intenta hacer coincidir el nombre para mostrar de cada destinatario sin resolver con un nombre para mostrar que pertenece a uno de sus entradas.</span><span class="sxs-lookup"><span data-stu-id="01efb-145">**ResolveNames** tries to match the display name of each unresolved recipient with a display name that belongs to one of its entries.</span></span> 
    
3. <span data-ttu-id="01efb-146">Si un contenedor no admite **ResolveNames**, **ResolveName** restringe la tabla de contenido del contenedor mediante el uso de una restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="01efb-146">If a container does not support **ResolveNames**, **ResolveName** restricts the container's contents table by using a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="01efb-147">Esta restricción hace que el contenedor para llevar a cabo un tipo "mejor adivinar" de búsqueda para buscar a un destinatario coincidente.</span><span class="sxs-lookup"><span data-stu-id="01efb-147">This restriction causes the container to perform a "best guess" type of search to locate a matching recipient.</span></span> <span data-ttu-id="01efb-148">Todos los contenedores deben admitir la restricción de propiedad **PR_ANR** .</span><span class="sxs-lookup"><span data-stu-id="01efb-148">All containers must support the **PR_ANR** property restriction.</span></span> 
    
4. <span data-ttu-id="01efb-149">Cuando un contenedor devuelve un destinatario que coincida con varios nombres, **ResolveName** muestra un cuadro de diálogo si se establece la marca MAPI_DIALOG, que permite al usuario seleccionar el nombre correcto.</span><span class="sxs-lookup"><span data-stu-id="01efb-149">When a container returns a recipient that matches multiple names, **ResolveName** displays a dialog box if the MAPI_DIALOG flag is set, which lets the user select the correct name.</span></span> 
    
5. <span data-ttu-id="01efb-150">Si se ha llamado a todos los contenedores en la propiedad **PR_AB_SEARCH_PATH** y se ha encontrado ninguna coincidencia, el destinatario se quede sin resolver.</span><span class="sxs-lookup"><span data-stu-id="01efb-150">If all of the containers in the **PR_AB_SEARCH_PATH** property have been called and no match has been found, the recipient remains unresolved.</span></span> 
    
<span data-ttu-id="01efb-151">Si uno o más destinatarios están sin resolver, **ResolveName** devuelve MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="01efb-151">If one or more recipients are unresolved, **ResolveName** returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="01efb-152">Si uno o más destinatarios tenían ambiguo resolución que no se pudo resolver con un cuadro de diálogo, o porque no se ha establecido el indicador MAPI_DIALOG, **ResolveName** devuelve MAPI_E_AMBIGUOUS_RECIP.</span><span class="sxs-lookup"><span data-stu-id="01efb-152">If one or more recipients had ambiguous resolution that could not be resolved with a dialog box, or because the MAPI_DIALOG flag was not set, **ResolveName** returns MAPI_E_AMBIGUOUS_RECIP.</span></span> <span data-ttu-id="01efb-153">Cuando algunos de los destinatarios son ambiguos y algunas no se puede resolver, **ResolveName** puede devolver cualquiera de estos valores de error.</span><span class="sxs-lookup"><span data-stu-id="01efb-153">When some of the recipients are ambiguous and some cannot be resolved, **ResolveName** can return either error value.</span></span> 
  
<span data-ttu-id="01efb-154">Si no se puede resolver un nombre, el cliente puede crear una dirección de uso único que tiene una dirección con un formato especial y el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="01efb-154">If a name cannot be resolved, the client can create a one-off address that has a specially formatted address and entry identifier.</span></span> <span data-ttu-id="01efb-155">Para obtener más información acerca del formato de los identificadores de entrada único, vea [Identificadores de entrada de uso único](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="01efb-155">For more information about the format of one-off entry identifiers, see [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span> <span data-ttu-id="01efb-156">Para obtener más información acerca del formato de direcciones de uso único, consulte [Direcciones de uso único](one-off-addresses.md).</span><span class="sxs-lookup"><span data-stu-id="01efb-156">For more information about the format of one-off addresses, see [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="01efb-157">MAPI admite cadenas de caracteres Unicode para el **ADRLIST** y los nuevos parámetros de título de entrada a **ResolveName**; Si se establece el indicador MAPI_UNICODE., las siguientes propiedades se devuelven como tipo PT_UNICODE en las estructuras [ADRENTRY](adrentry.md) :</span><span class="sxs-lookup"><span data-stu-id="01efb-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; if you set the MAPI_UNICODE flag, the following properties are returned as type PT_UNICODE in the [ADRENTRY](adrentry.md) structures:</span></span> 
  
- <span data-ttu-id="01efb-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="01efb-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="01efb-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="01efb-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="01efb-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="01efb-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
- <span data-ttu-id="01efb-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="01efb-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="01efb-162">Sin embargo, siempre se devuelve la propiedad de **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) mientras escribe PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="01efb-162">However, the **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) property is always returned as type PT_STRING8.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="01efb-163">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="01efb-163">MFCMAPI reference</span></span>

<span data-ttu-id="01efb-164">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="01efb-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="01efb-165">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="01efb-165">**File**</span></span>|<span data-ttu-id="01efb-166">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="01efb-166">**Function**</span></span>|<span data-ttu-id="01efb-167">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="01efb-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="01efb-168">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="01efb-168">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="01efb-169">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="01efb-169">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="01efb-170">MFCMAPI utiliza el método **ResolveName** para resolver una dirección de uso único antes de agregar a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="01efb-170">MFCMAPI uses the **ResolveName** method to resolve a one-off address before adding it to a message.</span></span>  <br/> |
|<span data-ttu-id="01efb-171">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="01efb-171">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="01efb-172">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="01efb-172">AddRecipient</span></span>  <br/> |<span data-ttu-id="01efb-173">MFCMAPI utiliza el método **ResolveName** para buscar una entrada de la libreta de direcciones por nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="01efb-173">MFCMAPI uses the **ResolveName** method to look up an address book entry by display name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01efb-174">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="01efb-174">See also</span></span>



[<span data-ttu-id="01efb-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="01efb-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="01efb-176">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="01efb-176">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)
  
[<span data-ttu-id="01efb-177">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="01efb-177">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="01efb-178">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="01efb-178">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="01efb-179">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="01efb-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

