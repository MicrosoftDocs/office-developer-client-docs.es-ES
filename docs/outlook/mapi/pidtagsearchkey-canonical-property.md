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
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345468"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="b746f-103">Propiedad canónica PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="b746f-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="b746f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b746f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b746f-105">Contiene una clave binaria comparable que identifica objetos correlacionados para una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b746f-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b746f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b746f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b746f-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="b746f-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="b746f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b746f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b746f-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="b746f-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="b746f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b746f-110">Data type:</span></span>  <br/> |<span data-ttu-id="b746f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b746f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b746f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b746f-112">Area:</span></span>  <br/> |<span data-ttu-id="b746f-113">Propiedades de identificador</span><span class="sxs-lookup"><span data-stu-id="b746f-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b746f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b746f-114">Remarks</span></span>

<span data-ttu-id="b746f-115">Esta propiedad proporciona un seguimiento de objetos relacionados, como copias de mensajes, y facilita la búsqueda de repeticiones no deseadas, como destinatarios duplicados.</span><span class="sxs-lookup"><span data-stu-id="b746f-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="b746f-116">MAPI usa reglas específicas para crear claves de búsqueda para destinatarios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b746f-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="b746f-117">La clave de búsqueda se forma concatenando el tipo de dirección (en mayúsculas), el carácter de dos puntos ":", la dirección de correo electrónico en forma canónica y el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="b746f-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="b746f-118">La forma canónica aquí significa que las direcciones que distinguen mayúsculas de minúsculas aparecen en el caso correcto y las direcciones que no distinguen mayúsculas de minúsculas se convierten en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="b746f-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="b746f-119">Esto es importante para conservar las correlaciones entre mensajes.</span><span class="sxs-lookup"><span data-stu-id="b746f-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="b746f-120">Para los objetos de mensaje, esta propiedad está disponible a través del método [IMAPIProp::GetProps](imapiprop-getprops.md) inmediatamente después de la creación del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b746f-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="b746f-121">Para otros objetos, está disponible después de la primera llamada al método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="b746f-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="b746f-122">Dado que esta propiedad es modificable, no es confiable obtenerla a través de **GetProps** hasta que una llamada **a SaveChanges** haya confirmado los valores establecidos o modificados por el método [IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="b746f-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="b746f-123">Para los perfiles, MAPI también proporciona una sección de perfil codificada de forma MUID_PROFILE_INSTANCE **,** con esta propiedad como su única propiedad.</span><span class="sxs-lookup"><span data-stu-id="b746f-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="b746f-124">Se garantiza que esta clave es única entre todos los perfiles creados y puede ser más confiable que la propiedad **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), que puede, por ejemplo, eliminarse y volver a crearse con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="b746f-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="b746f-125">En la tabla siguiente se resumen las diferencias importantes entre PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) y esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b746f-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="b746f-126">**Característica**</span><span class="sxs-lookup"><span data-stu-id="b746f-126">**Characteristic**</span></span>|<span data-ttu-id="b746f-127">PR_ENTRYID\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b746f-127">\*\*\*\*PR_ENTRYID\*\*\*\*</span></span>|<span data-ttu-id="b746f-128">PR_RECORD_KEY\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b746f-128">\*\*\*\*PR_RECORD_KEY\*\*\*\*</span></span>|<span data-ttu-id="b746f-129">PR_SEARCH_KEY\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b746f-129">\*\*\*\*PR_SEARCH_KEY\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b746f-130">Obligatorio en objetos de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="b746f-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="b746f-131">No</span><span class="sxs-lookup"><span data-stu-id="b746f-131">No</span></span>  <br/> |<span data-ttu-id="b746f-132">Sí</span><span class="sxs-lookup"><span data-stu-id="b746f-132">Yes</span></span>  <br/> |<span data-ttu-id="b746f-133">No</span><span class="sxs-lookup"><span data-stu-id="b746f-133">No</span></span>  <br/> |
|<span data-ttu-id="b746f-134">Obligatorio en objetos de carpeta</span><span class="sxs-lookup"><span data-stu-id="b746f-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="b746f-135">Sí</span><span class="sxs-lookup"><span data-stu-id="b746f-135">Yes</span></span>  <br/> |<span data-ttu-id="b746f-136">Sí</span><span class="sxs-lookup"><span data-stu-id="b746f-136">Yes</span></span>  <br/> |<span data-ttu-id="b746f-137">No</span><span class="sxs-lookup"><span data-stu-id="b746f-137">No</span></span>  <br/> |
|<span data-ttu-id="b746f-138">Obligatorio en objetos de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="b746f-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="b746f-139">Sí</span><span class="sxs-lookup"><span data-stu-id="b746f-139">Yes</span></span>  <br/> |<span data-ttu-id="b746f-140">Sí</span><span class="sxs-lookup"><span data-stu-id="b746f-140">Yes</span></span>  <br/> |<span data-ttu-id="b746f-141">No</span><span class="sxs-lookup"><span data-stu-id="b746f-141">No</span></span>  <br/> |
|<span data-ttu-id="b746f-142">Requerido en objetos de estado</span><span class="sxs-lookup"><span data-stu-id="b746f-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="b746f-143">Sí</span><span class="sxs-lookup"><span data-stu-id="b746f-143">Yes</span></span>  <br/> |<span data-ttu-id="b746f-144">No</span><span class="sxs-lookup"><span data-stu-id="b746f-144">No</span></span>  <br/> |<span data-ttu-id="b746f-145">No</span><span class="sxs-lookup"><span data-stu-id="b746f-145">No</span></span>  <br/> |
|<span data-ttu-id="b746f-146">Creable por cliente</span><span class="sxs-lookup"><span data-stu-id="b746f-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="b746f-147">No</span><span class="sxs-lookup"><span data-stu-id="b746f-147">No</span></span>  <br/> |<span data-ttu-id="b746f-148">No</span><span class="sxs-lookup"><span data-stu-id="b746f-148">No</span></span>  <br/> |<span data-ttu-id="b746f-149">Sí</span><span class="sxs-lookup"><span data-stu-id="b746f-149">Yes</span></span>  <br/> |
|<span data-ttu-id="b746f-150">Disponible antes **de SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="b746f-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="b746f-151">Depende de la implementación del proveedor</span><span class="sxs-lookup"><span data-stu-id="b746f-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="b746f-152">Depende de la implementación del proveedor</span><span class="sxs-lookup"><span data-stu-id="b746f-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="b746f-153">Para los mensajes, sí.</span><span class="sxs-lookup"><span data-stu-id="b746f-153">For messages, Yes.</span></span> <span data-ttu-id="b746f-154">Para otros, depende de la implementación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b746f-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="b746f-155">Se cambió en una operación de copia</span><span class="sxs-lookup"><span data-stu-id="b746f-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="b746f-156">Sí</span><span class="sxs-lookup"><span data-stu-id="b746f-156">Yes</span></span>  <br/> |<span data-ttu-id="b746f-157">Sí</span><span class="sxs-lookup"><span data-stu-id="b746f-157">Yes</span></span>  <br/> |<span data-ttu-id="b746f-158">No</span><span class="sxs-lookup"><span data-stu-id="b746f-158">No</span></span>  <br/> |
|<span data-ttu-id="b746f-159">Modificable por el cliente después de una copia</span><span class="sxs-lookup"><span data-stu-id="b746f-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="b746f-160">No</span><span class="sxs-lookup"><span data-stu-id="b746f-160">No</span></span>  <br/> |<span data-ttu-id="b746f-161">No</span><span class="sxs-lookup"><span data-stu-id="b746f-161">No</span></span>  <br/> |<span data-ttu-id="b746f-162">Sí</span><span class="sxs-lookup"><span data-stu-id="b746f-162">Yes</span></span>  <br/> |
|<span data-ttu-id="b746f-163">Único dentro de ...</span><span class="sxs-lookup"><span data-stu-id="b746f-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="b746f-164">Todo el mundo</span><span class="sxs-lookup"><span data-stu-id="b746f-164">Entire world</span></span>  <br/> |<span data-ttu-id="b746f-165">Instancia de proveedor</span><span class="sxs-lookup"><span data-stu-id="b746f-165">Provider instance</span></span>  <br/> |<span data-ttu-id="b746f-166">Todo el mundo</span><span class="sxs-lookup"><span data-stu-id="b746f-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="b746f-167">Binario comparable (como con memcmp)</span><span class="sxs-lookup"><span data-stu-id="b746f-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="b746f-168">No: use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="b746f-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="b746f-169">Sí</span><span class="sxs-lookup"><span data-stu-id="b746f-169">Yes</span></span>  <br/> |<span data-ttu-id="b746f-170">Sí</span><span class="sxs-lookup"><span data-stu-id="b746f-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b746f-171">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b746f-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b746f-172">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="b746f-172">Protocol specifications</span></span>

<span data-ttu-id="b746f-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b746f-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b746f-174">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="b746f-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b746f-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b746f-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b746f-176">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="b746f-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="b746f-177">[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b746f-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b746f-178">Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="b746f-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b746f-179">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b746f-179">Header files</span></span>

<span data-ttu-id="b746f-180">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b746f-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="b746f-181">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b746f-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="b746f-182">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b746f-182">Mapitags.h</span></span>
  
> <span data-ttu-id="b746f-183">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b746f-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b746f-184">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b746f-184">See also</span></span>



[<span data-ttu-id="b746f-185">Propiedad canónica PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="b746f-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="b746f-186">Propiedad canónica PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="b746f-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="b746f-187">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b746f-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b746f-188">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="b746f-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b746f-189">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b746f-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b746f-190">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="b746f-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

