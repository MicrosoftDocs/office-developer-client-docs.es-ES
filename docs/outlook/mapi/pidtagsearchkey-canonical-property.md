---
title: Propiedad canónica PidTagSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da7d19407856570a628529877252360d1537bae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595394"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="a0303-103">Propiedad canónica PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="a0303-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="a0303-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0303-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0303-105">Contiene una clave binario comparable que identifica objetos correlacionados para una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a0303-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0303-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a0303-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0303-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="a0303-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="a0303-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a0303-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a0303-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="a0303-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="a0303-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a0303-110">Data type:</span></span>  <br/> |<span data-ttu-id="a0303-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a0303-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a0303-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a0303-112">Area:</span></span>  <br/> |<span data-ttu-id="a0303-113">Propiedades de Id.</span><span class="sxs-lookup"><span data-stu-id="a0303-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0303-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a0303-114">Remarks</span></span>

<span data-ttu-id="a0303-115">Esta propiedad proporciona un seguimiento de los objetos relacionados, como copias de los mensajes y facilita encontrar repeticiones no deseadas, como destinatarios duplicados.</span><span class="sxs-lookup"><span data-stu-id="a0303-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="a0303-116">MAPI utiliza reglas específicas para la construcción de las claves de búsqueda para los destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a0303-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="a0303-117">La clave de búsqueda se forma concatenando el tipo de dirección (en caracteres en mayúsculas), el carácter de punto y coma ':', la dirección de correo electrónico en forma canónica y el carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="a0303-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="a0303-118">Aquí forma canónica significa que distingue mayúsculas de minúsculas direcciones aparecen en mayúsculas y minúsculas, y las direcciones que no distinguen mayúsculas de minúsculas se convierten en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="a0303-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="a0303-119">Esto es importante para preservar la correlación entre los mensajes.</span><span class="sxs-lookup"><span data-stu-id="a0303-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="a0303-120">Para los objetos de mensaje, esta propiedad está disponible a través del método [IMAPIProp::GetProps](imapiprop-getprops.md) inmediatamente después de la creación del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a0303-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="a0303-121">Para otros objetos, está disponible después de la primera llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="a0303-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="a0303-122">Debido a que esta propiedad es modificable, es poco confiable para obtenerlo a través de **GetProps** hasta que una llamada de **SaveChanges** haya confirmado cualquiera de los valores establecer o modificados por el método [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="a0303-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="a0303-123">Para los perfiles, MAPI también proporciona una sección de perfil codificado de forma rígida denominada **MUID_PROFILE_INSTANCE**, con esta propiedad como su propiedad único.</span><span class="sxs-lookup"><span data-stu-id="a0303-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="a0303-124">Esta clave se garantiza que es único entre todos los perfiles que nunca se ha creado y puede ser más confiable que la propiedad **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), que puede, por ejemplo, eliminar y volver a crear con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="a0303-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="a0303-125">En la siguiente tabla se resume las diferencias importantes entre la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) y esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="a0303-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="a0303-126">**Característica**</span><span class="sxs-lookup"><span data-stu-id="a0303-126">**Characteristic**</span></span>|<span data-ttu-id="a0303-127">ENTRADA DEL OBJETO \*\*\*</span><span class="sxs-lookup"><span data-stu-id="a0303-127">****PR_ENTRYID****</span></span>|<span data-ttu-id="a0303-128">PR_RECORD_KEY \*\*\*</span><span class="sxs-lookup"><span data-stu-id="a0303-128">****PR_RECORD_KEY****</span></span>|<span data-ttu-id="a0303-129">PR_SEARCH_KEY \*\*\*</span><span class="sxs-lookup"><span data-stu-id="a0303-129">****PR_SEARCH_KEY****</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a0303-130">Requerido en los objetos de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="a0303-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="a0303-131">No</span><span class="sxs-lookup"><span data-stu-id="a0303-131">No</span></span>  <br/> |<span data-ttu-id="a0303-132">Sí</span><span class="sxs-lookup"><span data-stu-id="a0303-132">Yes</span></span>  <br/> |<span data-ttu-id="a0303-133">No</span><span class="sxs-lookup"><span data-stu-id="a0303-133">No</span></span>  <br/> |
|<span data-ttu-id="a0303-134">Requerido en los objetos de carpeta</span><span class="sxs-lookup"><span data-stu-id="a0303-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="a0303-135">Sí</span><span class="sxs-lookup"><span data-stu-id="a0303-135">Yes</span></span>  <br/> |<span data-ttu-id="a0303-136">Sí</span><span class="sxs-lookup"><span data-stu-id="a0303-136">Yes</span></span>  <br/> |<span data-ttu-id="a0303-137">No</span><span class="sxs-lookup"><span data-stu-id="a0303-137">No</span></span>  <br/> |
|<span data-ttu-id="a0303-138">Necesarios en los objetos de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="a0303-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="a0303-139">Sí</span><span class="sxs-lookup"><span data-stu-id="a0303-139">Yes</span></span>  <br/> |<span data-ttu-id="a0303-140">Sí</span><span class="sxs-lookup"><span data-stu-id="a0303-140">Yes</span></span>  <br/> |<span data-ttu-id="a0303-141">No</span><span class="sxs-lookup"><span data-stu-id="a0303-141">No</span></span>  <br/> |
|<span data-ttu-id="a0303-142">Requerido en los objetos de estado</span><span class="sxs-lookup"><span data-stu-id="a0303-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="a0303-143">Sí</span><span class="sxs-lookup"><span data-stu-id="a0303-143">Yes</span></span>  <br/> |<span data-ttu-id="a0303-144">No</span><span class="sxs-lookup"><span data-stu-id="a0303-144">No</span></span>  <br/> |<span data-ttu-id="a0303-145">No</span><span class="sxs-lookup"><span data-stu-id="a0303-145">No</span></span>  <br/> |
|<span data-ttu-id="a0303-146">Se puede crear por cliente</span><span class="sxs-lookup"><span data-stu-id="a0303-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="a0303-147">No</span><span class="sxs-lookup"><span data-stu-id="a0303-147">No</span></span>  <br/> |<span data-ttu-id="a0303-148">No</span><span class="sxs-lookup"><span data-stu-id="a0303-148">No</span></span>  <br/> |<span data-ttu-id="a0303-149">Sí</span><span class="sxs-lookup"><span data-stu-id="a0303-149">Yes</span></span>  <br/> |
|<span data-ttu-id="a0303-150">Disponible antes de **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="a0303-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="a0303-151">Depende de la implementación del proveedor</span><span class="sxs-lookup"><span data-stu-id="a0303-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="a0303-152">Depende de la implementación del proveedor</span><span class="sxs-lookup"><span data-stu-id="a0303-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="a0303-153">Para los mensajes, sí.</span><span class="sxs-lookup"><span data-stu-id="a0303-153">For messages, Yes.</span></span> <span data-ttu-id="a0303-154">Para otras personas, depende de la implementación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="a0303-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="a0303-155">Cambiado en una operación de copia</span><span class="sxs-lookup"><span data-stu-id="a0303-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="a0303-156">Sí</span><span class="sxs-lookup"><span data-stu-id="a0303-156">Yes</span></span>  <br/> |<span data-ttu-id="a0303-157">Sí</span><span class="sxs-lookup"><span data-stu-id="a0303-157">Yes</span></span>  <br/> |<span data-ttu-id="a0303-158">No</span><span class="sxs-lookup"><span data-stu-id="a0303-158">No</span></span>  <br/> |
|<span data-ttu-id="a0303-159">Se pueden cambiar después de una copia de los clientes</span><span class="sxs-lookup"><span data-stu-id="a0303-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="a0303-160">No</span><span class="sxs-lookup"><span data-stu-id="a0303-160">No</span></span>  <br/> |<span data-ttu-id="a0303-161">No</span><span class="sxs-lookup"><span data-stu-id="a0303-161">No</span></span>  <br/> |<span data-ttu-id="a0303-162">Sí</span><span class="sxs-lookup"><span data-stu-id="a0303-162">Yes</span></span>  <br/> |
|<span data-ttu-id="a0303-163">UNIQUE dentro de...</span><span class="sxs-lookup"><span data-stu-id="a0303-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="a0303-164">Todo mundo</span><span class="sxs-lookup"><span data-stu-id="a0303-164">Entire world</span></span>  <br/> |<span data-ttu-id="a0303-165">Instancia de proveedor</span><span class="sxs-lookup"><span data-stu-id="a0303-165">Provider instance</span></span>  <br/> |<span data-ttu-id="a0303-166">Todo mundo</span><span class="sxs-lookup"><span data-stu-id="a0303-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="a0303-167">Binario comparable (como sucede con memcmp)</span><span class="sxs-lookup"><span data-stu-id="a0303-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="a0303-168">No--usar [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="a0303-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="a0303-169">Sí</span><span class="sxs-lookup"><span data-stu-id="a0303-169">Yes</span></span>  <br/> |<span data-ttu-id="a0303-170">Sí</span><span class="sxs-lookup"><span data-stu-id="a0303-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a0303-171">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0303-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a0303-172">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a0303-172">Protocol specifications</span></span>

<span data-ttu-id="a0303-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0303-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0303-174">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a0303-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a0303-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0303-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0303-176">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a0303-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="a0303-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0303-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0303-178">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="a0303-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a0303-179">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a0303-179">Header files</span></span>

<span data-ttu-id="a0303-180">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0303-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0303-181">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a0303-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="a0303-182">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a0303-182">Mapitags.h</span></span>
  
> <span data-ttu-id="a0303-183">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a0303-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0303-184">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a0303-184">See also</span></span>



[<span data-ttu-id="a0303-185">Propiedad canónica PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="a0303-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="a0303-186">Propiedad canónica PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="a0303-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="a0303-187">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a0303-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0303-188">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a0303-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0303-189">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a0303-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0303-190">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="a0303-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

