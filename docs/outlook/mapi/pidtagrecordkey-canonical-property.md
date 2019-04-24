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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355268"
---
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="995cf-103">Propiedad canónica PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="995cf-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="995cf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="995cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="995cf-105">Contiene un identificador único comparable binario para un objeto específico.</span><span class="sxs-lookup"><span data-stu-id="995cf-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="995cf-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="995cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="995cf-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="995cf-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="995cf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="995cf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="995cf-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="995cf-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="995cf-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="995cf-110">Data type:</span></span>  <br/> |<span data-ttu-id="995cf-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="995cf-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="995cf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="995cf-112">Area:</span></span>  <br/> |<span data-ttu-id="995cf-113">Propiedades de identificador</span><span class="sxs-lookup"><span data-stu-id="995cf-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="995cf-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="995cf-114">Remarks</span></span>

<span data-ttu-id="995cf-115">Esta propiedad facilita la búsqueda de referencias a un objeto, como la búsqueda de su fila en una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="995cf-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="995cf-116">Esta propiedad no se puede utilizar para abrir un objeto; Use el identificador de entrada para ese propósito.</span><span class="sxs-lookup"><span data-stu-id="995cf-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="995cf-117">Un subobjeto Attachment debe identificarse de forma exclusiva en un mensaje por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="995cf-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="995cf-118">Este identificador es la única característica de datos adjuntos que se garantiza que permanecerá igual después de cerrar y volver a abrir el mensaje.</span><span class="sxs-lookup"><span data-stu-id="995cf-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="995cf-119">El proveedor de almacenamiento debe conservar esta propiedad en todas las sesiones para garantizar esta garantía.</span><span class="sxs-lookup"><span data-stu-id="995cf-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="995cf-120">Para las carpetas, esta propiedad contiene una clave que se usa en la tabla de jerarquía de carpetas.</span><span class="sxs-lookup"><span data-stu-id="995cf-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="995cf-121">Normalmente, es el mismo valor que el que proporciona la \*\*\*\* propiedad de ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="995cf-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="995cf-122">Para los almacenes de mensajes, esta propiedad es idéntica a la propiedad **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="995cf-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="995cf-123">En un objeto de almacén de mensajes, esta propiedad debe ser única en todos los proveedores de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="995cf-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="995cf-124">Una forma de hacerlo es combinar el valor de la propiedad **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para el almacén (único para ese tipo de proveedor) con una estructura [GUID](guid.md) u otro valor único para el almacén de mensajes específico.</span><span class="sxs-lookup"><span data-stu-id="995cf-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="995cf-125">Esta propiedad siempre está disponible a través del método [IMAPIProp:: GetProps](imapiprop-getprops.md) después de la primera llamada al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="995cf-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="995cf-126">Algunos proveedores pueden hacer que estén disponibles inmediatamente después de la creación de instancias.</span><span class="sxs-lookup"><span data-stu-id="995cf-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="995cf-127">Un cliente o proveedor de servicios puede comparar los valores de esta propiedad mediante memcmp.</span><span class="sxs-lookup"><span data-stu-id="995cf-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="995cf-128">Esto no es posible para los valores de identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="995cf-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="995cf-129">Sin embargo, se garantiza que esta propiedad es única dentro del mismo almacén de mensajes o el mismo contenedor de libretas de direcciones; dos objetos de contenedores distintos pueden tener el mismo valor que esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="995cf-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="995cf-130">Una de las diferencias entre las claves de registro y de búsqueda es que la clave de registro es específica del objeto, mientras que la clave de búsqueda se puede copiar a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="995cf-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="995cf-131">Por ejemplo, dos copias del objeto pueden tener el mismo valor de **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), pero deben tener valores diferentes para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="995cf-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="995cf-132">En la tabla siguiente se resumen las diferencias \*\*\*\* importantes entre **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) y esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="995cf-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="995cf-133">**Característica**</span><span class="sxs-lookup"><span data-stu-id="995cf-133">**Characteristic**</span></span>|<span data-ttu-id="995cf-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="995cf-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="995cf-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="995cf-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="995cf-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="995cf-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="995cf-137">Necesario en los objetos Attachment</span><span class="sxs-lookup"><span data-stu-id="995cf-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="995cf-138">No</span><span class="sxs-lookup"><span data-stu-id="995cf-138">No</span></span>  <br/> |<span data-ttu-id="995cf-139">Sí</span><span class="sxs-lookup"><span data-stu-id="995cf-139">Yes</span></span>  <br/> |<span data-ttu-id="995cf-140">No</span><span class="sxs-lookup"><span data-stu-id="995cf-140">No</span></span>  <br/> |
|<span data-ttu-id="995cf-141">Necesario en objetos Folder</span><span class="sxs-lookup"><span data-stu-id="995cf-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="995cf-142">Sí</span><span class="sxs-lookup"><span data-stu-id="995cf-142">Yes</span></span>  <br/> |<span data-ttu-id="995cf-143">Sí</span><span class="sxs-lookup"><span data-stu-id="995cf-143">Yes</span></span>  <br/> |<span data-ttu-id="995cf-144">No</span><span class="sxs-lookup"><span data-stu-id="995cf-144">No</span></span>  <br/> |
|<span data-ttu-id="995cf-145">Obligatorio en objetos de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="995cf-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="995cf-146">Sí</span><span class="sxs-lookup"><span data-stu-id="995cf-146">Yes</span></span>  <br/> |<span data-ttu-id="995cf-147">Sí</span><span class="sxs-lookup"><span data-stu-id="995cf-147">Yes</span></span>  <br/> |<span data-ttu-id="995cf-148">No</span><span class="sxs-lookup"><span data-stu-id="995cf-148">No</span></span>  <br/> |
|<span data-ttu-id="995cf-149">Obligatorio en objetos de estado</span><span class="sxs-lookup"><span data-stu-id="995cf-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="995cf-150">Sí</span><span class="sxs-lookup"><span data-stu-id="995cf-150">Yes</span></span>  <br/> |<span data-ttu-id="995cf-151">No</span><span class="sxs-lookup"><span data-stu-id="995cf-151">No</span></span>  <br/> |<span data-ttu-id="995cf-152">No</span><span class="sxs-lookup"><span data-stu-id="995cf-152">No</span></span>  <br/> |
|<span data-ttu-id="995cf-153">Se pueda crear por cliente</span><span class="sxs-lookup"><span data-stu-id="995cf-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="995cf-154">No</span><span class="sxs-lookup"><span data-stu-id="995cf-154">No</span></span>  <br/> |<span data-ttu-id="995cf-155">No</span><span class="sxs-lookup"><span data-stu-id="995cf-155">No</span></span>  <br/> |<span data-ttu-id="995cf-156">Sí</span><span class="sxs-lookup"><span data-stu-id="995cf-156">Yes</span></span>  <br/> |
|<span data-ttu-id="995cf-157">Disponible antes de una llamada a **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="995cf-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="995cf-158">Posiblemente</span><span class="sxs-lookup"><span data-stu-id="995cf-158">Maybe</span></span>  <br/> |<span data-ttu-id="995cf-159">Posiblemente</span><span class="sxs-lookup"><span data-stu-id="995cf-159">Maybe</span></span>  <br/> |<span data-ttu-id="995cf-160">Mensajes sí otros maybes</span><span class="sxs-lookup"><span data-stu-id="995cf-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="995cf-161">Modificado en una operación de copia</span><span class="sxs-lookup"><span data-stu-id="995cf-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="995cf-162">Sí</span><span class="sxs-lookup"><span data-stu-id="995cf-162">Yes</span></span>  <br/> |<span data-ttu-id="995cf-163">Sí</span><span class="sxs-lookup"><span data-stu-id="995cf-163">Yes</span></span>  <br/> |<span data-ttu-id="995cf-164">No</span><span class="sxs-lookup"><span data-stu-id="995cf-164">No</span></span>  <br/> |
|<span data-ttu-id="995cf-165">Modificable por un cliente después de una copia</span><span class="sxs-lookup"><span data-stu-id="995cf-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="995cf-166">No</span><span class="sxs-lookup"><span data-stu-id="995cf-166">No</span></span>  <br/> |<span data-ttu-id="995cf-167">No</span><span class="sxs-lookup"><span data-stu-id="995cf-167">No</span></span>  <br/> |<span data-ttu-id="995cf-168">Sí</span><span class="sxs-lookup"><span data-stu-id="995cf-168">Yes</span></span>  <br/> |
|<span data-ttu-id="995cf-169">Único dentro de...</span><span class="sxs-lookup"><span data-stu-id="995cf-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="995cf-170">Todo el mundo</span><span class="sxs-lookup"><span data-stu-id="995cf-170">Entire world</span></span>  <br/> |<span data-ttu-id="995cf-171">Instancia del proveedor</span><span class="sxs-lookup"><span data-stu-id="995cf-171">Provider instance</span></span>  <br/> |<span data-ttu-id="995cf-172">Todo el mundo</span><span class="sxs-lookup"><span data-stu-id="995cf-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="995cf-173">Comparable binario (como con memcmp)</span><span class="sxs-lookup"><span data-stu-id="995cf-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="995cf-174">No--usar **IMAPISupport:: CompareEntryIDs**</span><span class="sxs-lookup"><span data-stu-id="995cf-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="995cf-175">Sí</span><span class="sxs-lookup"><span data-stu-id="995cf-175">Yes</span></span>  <br/> |<span data-ttu-id="995cf-176">Sí</span><span class="sxs-lookup"><span data-stu-id="995cf-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="995cf-177">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="995cf-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="995cf-178">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="995cf-178">Protocol specifications</span></span>

<span data-ttu-id="995cf-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="995cf-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="995cf-180">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="995cf-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="995cf-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="995cf-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="995cf-182">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="995cf-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="995cf-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="995cf-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="995cf-184">Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="995cf-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="995cf-185">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="995cf-185">Header files</span></span>

<span data-ttu-id="995cf-186">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="995cf-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="995cf-187">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="995cf-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="995cf-188">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="995cf-188">Mapitags.h</span></span>
  
> <span data-ttu-id="995cf-189">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="995cf-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="995cf-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="995cf-190">See also</span></span>



[<span data-ttu-id="995cf-191">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="995cf-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="995cf-192">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="995cf-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="995cf-193">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="995cf-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="995cf-194">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="995cf-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

