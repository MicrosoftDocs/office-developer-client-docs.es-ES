---
title: Propiedad canónica PidTagRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401702"
---
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="98fac-103">Propiedad canónica PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="98fac-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="98fac-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98fac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98fac-105">Contiene un identificador binario comparable único para un objeto específico.</span><span class="sxs-lookup"><span data-stu-id="98fac-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98fac-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="98fac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98fac-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="98fac-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="98fac-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="98fac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98fac-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="98fac-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="98fac-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="98fac-110">Data type:</span></span>  <br/> |<span data-ttu-id="98fac-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="98fac-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="98fac-112">Área:</span><span class="sxs-lookup"><span data-stu-id="98fac-112">Area:</span></span>  <br/> |<span data-ttu-id="98fac-113">Propiedades de Id.</span><span class="sxs-lookup"><span data-stu-id="98fac-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98fac-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98fac-114">Remarks</span></span>

<span data-ttu-id="98fac-115">Esta propiedad facilita localizar referencias a un objeto, como la búsqueda de la fila correspondiente en una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="98fac-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="98fac-116">Esta propiedad no se puede usar para abrir un objeto; Utilice el identificador de entrada para ese propósito.</span><span class="sxs-lookup"><span data-stu-id="98fac-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="98fac-117">Un subobjetos datos adjuntos deben identificarse de forma única dentro de un mensaje por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="98fac-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="98fac-118">Este identificador es la única característica de datos adjuntos garantizada que permanecen igual después de que el mensaje se cierra y se vuelve a abrir.</span><span class="sxs-lookup"><span data-stu-id="98fac-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="98fac-119">El proveedor de almacenamiento debe conservar esta propiedad a través de las sesiones para garantizar esta garantía.</span><span class="sxs-lookup"><span data-stu-id="98fac-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="98fac-120">Para las carpetas, esta propiedad contiene una clave que se usa en la tabla de jerarquía de carpeta.</span><span class="sxs-lookup"><span data-stu-id="98fac-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="98fac-121">Normalmente, esto es el mismo valor que la proporcionada por la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="98fac-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="98fac-122">Para los almacenes de mensajes, esta propiedad es idéntica a la propiedad **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="98fac-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="98fac-123">En un objeto de almacén de mensajes, esta propiedad debe ser única entre todos los proveedores de almacén.</span><span class="sxs-lookup"><span data-stu-id="98fac-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="98fac-124">Una manera de hacerlo es combinar el valor de la propiedad **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para el almacén (exclusivo de ese tipo de proveedor) con una estructura [GUID](guid.md) u otro valor único para el almacén de mensajes específicos.</span><span class="sxs-lookup"><span data-stu-id="98fac-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="98fac-125">Esta propiedad siempre está disponible a través del método [IMAPIProp::GetProps](imapiprop-getprops.md) después de la primera llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="98fac-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="98fac-126">Algunos proveedores pueden estar disponible inmediatamente después de la creación de instancias.</span><span class="sxs-lookup"><span data-stu-id="98fac-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="98fac-127">Un proveedor de servicio o cliente puede comparar los valores de esta propiedad mediante el uso de memcmp.</span><span class="sxs-lookup"><span data-stu-id="98fac-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="98fac-128">Esto no es posible para los valores de identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="98fac-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="98fac-129">Sin embargo, esta propiedad se garantiza que ser únicos en el mismo almacén de mensajes o contenedor libreta; de direcciones dos objetos de los contenedores diferentes pueden tener el mismo valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="98fac-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="98fac-130">Una distinción entre las claves de registro y la búsqueda es que la clave de registro es específica del objeto, mientras que la clave de búsqueda se puede copiar a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="98fac-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="98fac-131">Por ejemplo, dos copias del objeto pueden tener el mismo valor de **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), pero deben tener valores distintos para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="98fac-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="98fac-132">En la siguiente tabla se resume las diferencias importantes entre la **entrada del objeto**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) y esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="98fac-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="98fac-133">**Característica**</span><span class="sxs-lookup"><span data-stu-id="98fac-133">**Characteristic**</span></span>|<span data-ttu-id="98fac-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="98fac-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="98fac-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="98fac-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="98fac-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="98fac-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="98fac-137">Requerido en los objetos de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="98fac-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="98fac-138">No</span><span class="sxs-lookup"><span data-stu-id="98fac-138">No</span></span>  <br/> |<span data-ttu-id="98fac-139">Sí</span><span class="sxs-lookup"><span data-stu-id="98fac-139">Yes</span></span>  <br/> |<span data-ttu-id="98fac-140">No</span><span class="sxs-lookup"><span data-stu-id="98fac-140">No</span></span>  <br/> |
|<span data-ttu-id="98fac-141">Requerido en los objetos de carpeta</span><span class="sxs-lookup"><span data-stu-id="98fac-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="98fac-142">Sí</span><span class="sxs-lookup"><span data-stu-id="98fac-142">Yes</span></span>  <br/> |<span data-ttu-id="98fac-143">Sí</span><span class="sxs-lookup"><span data-stu-id="98fac-143">Yes</span></span>  <br/> |<span data-ttu-id="98fac-144">No</span><span class="sxs-lookup"><span data-stu-id="98fac-144">No</span></span>  <br/> |
|<span data-ttu-id="98fac-145">Necesarios en los objetos de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="98fac-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="98fac-146">Sí</span><span class="sxs-lookup"><span data-stu-id="98fac-146">Yes</span></span>  <br/> |<span data-ttu-id="98fac-147">Sí</span><span class="sxs-lookup"><span data-stu-id="98fac-147">Yes</span></span>  <br/> |<span data-ttu-id="98fac-148">No</span><span class="sxs-lookup"><span data-stu-id="98fac-148">No</span></span>  <br/> |
|<span data-ttu-id="98fac-149">Requerido en los objetos de estado</span><span class="sxs-lookup"><span data-stu-id="98fac-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="98fac-150">Sí</span><span class="sxs-lookup"><span data-stu-id="98fac-150">Yes</span></span>  <br/> |<span data-ttu-id="98fac-151">No</span><span class="sxs-lookup"><span data-stu-id="98fac-151">No</span></span>  <br/> |<span data-ttu-id="98fac-152">No</span><span class="sxs-lookup"><span data-stu-id="98fac-152">No</span></span>  <br/> |
|<span data-ttu-id="98fac-153">Se puede crear por cliente</span><span class="sxs-lookup"><span data-stu-id="98fac-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="98fac-154">No</span><span class="sxs-lookup"><span data-stu-id="98fac-154">No</span></span>  <br/> |<span data-ttu-id="98fac-155">No</span><span class="sxs-lookup"><span data-stu-id="98fac-155">No</span></span>  <br/> |<span data-ttu-id="98fac-156">Sí</span><span class="sxs-lookup"><span data-stu-id="98fac-156">Yes</span></span>  <br/> |
|<span data-ttu-id="98fac-157">Disponible antes de una llamada a **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="98fac-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="98fac-158">Quizá</span><span class="sxs-lookup"><span data-stu-id="98fac-158">Maybe</span></span>  <br/> |<span data-ttu-id="98fac-159">Quizá</span><span class="sxs-lookup"><span data-stu-id="98fac-159">Maybe</span></span>  <br/> |<span data-ttu-id="98fac-160">Los mensajes de otras personas sí quizá</span><span class="sxs-lookup"><span data-stu-id="98fac-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="98fac-161">Cambiado en una operación de copia</span><span class="sxs-lookup"><span data-stu-id="98fac-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="98fac-162">Sí</span><span class="sxs-lookup"><span data-stu-id="98fac-162">Yes</span></span>  <br/> |<span data-ttu-id="98fac-163">Sí</span><span class="sxs-lookup"><span data-stu-id="98fac-163">Yes</span></span>  <br/> |<span data-ttu-id="98fac-164">No</span><span class="sxs-lookup"><span data-stu-id="98fac-164">No</span></span>  <br/> |
|<span data-ttu-id="98fac-165">Se pueden cambiar por un cliente después de una copia</span><span class="sxs-lookup"><span data-stu-id="98fac-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="98fac-166">No</span><span class="sxs-lookup"><span data-stu-id="98fac-166">No</span></span>  <br/> |<span data-ttu-id="98fac-167">No</span><span class="sxs-lookup"><span data-stu-id="98fac-167">No</span></span>  <br/> |<span data-ttu-id="98fac-168">Sí</span><span class="sxs-lookup"><span data-stu-id="98fac-168">Yes</span></span>  <br/> |
|<span data-ttu-id="98fac-169">UNIQUE dentro de...</span><span class="sxs-lookup"><span data-stu-id="98fac-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="98fac-170">Todo mundo</span><span class="sxs-lookup"><span data-stu-id="98fac-170">Entire world</span></span>  <br/> |<span data-ttu-id="98fac-171">Instancia de proveedor</span><span class="sxs-lookup"><span data-stu-id="98fac-171">Provider instance</span></span>  <br/> |<span data-ttu-id="98fac-172">Todo mundo</span><span class="sxs-lookup"><span data-stu-id="98fac-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="98fac-173">Binario comparable (como sucede con memcmp)</span><span class="sxs-lookup"><span data-stu-id="98fac-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="98fac-174">No--usar **IMAPISupport:: CompareEntryIDs**</span><span class="sxs-lookup"><span data-stu-id="98fac-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="98fac-175">Sí</span><span class="sxs-lookup"><span data-stu-id="98fac-175">Yes</span></span>  <br/> |<span data-ttu-id="98fac-176">Sí</span><span class="sxs-lookup"><span data-stu-id="98fac-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="98fac-177">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="98fac-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98fac-178">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="98fac-178">Protocol specifications</span></span>

<span data-ttu-id="98fac-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98fac-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98fac-180">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="98fac-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="98fac-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98fac-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98fac-182">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="98fac-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="98fac-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98fac-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98fac-184">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="98fac-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98fac-185">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="98fac-185">Header files</span></span>

<span data-ttu-id="98fac-186">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98fac-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="98fac-187">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="98fac-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="98fac-188">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="98fac-188">Mapitags.h</span></span>
  
> <span data-ttu-id="98fac-189">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="98fac-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98fac-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="98fac-190">See also</span></span>



[<span data-ttu-id="98fac-191">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="98fac-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98fac-192">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="98fac-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98fac-193">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="98fac-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98fac-194">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="98fac-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

