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
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="a8c88-103">Propiedad canónica PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="a8c88-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="a8c88-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8c88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8c88-105">Contiene un identificador binario comparable único para un objeto específico.</span><span class="sxs-lookup"><span data-stu-id="a8c88-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8c88-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a8c88-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a8c88-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="a8c88-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="a8c88-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a8c88-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a8c88-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="a8c88-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="a8c88-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a8c88-110">Data type:</span></span>  <br/> |<span data-ttu-id="a8c88-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a8c88-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a8c88-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a8c88-112">Area:</span></span>  <br/> |<span data-ttu-id="a8c88-113">Propiedades de identificador</span><span class="sxs-lookup"><span data-stu-id="a8c88-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8c88-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a8c88-114">Remarks</span></span>

<span data-ttu-id="a8c88-115">Esta propiedad facilita la búsqueda de referencias a un objeto, como la búsqueda de su fila en una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="a8c88-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="a8c88-116">Esta propiedad no se puede usar para abrir un objeto; use el identificador de entrada para ese propósito.</span><span class="sxs-lookup"><span data-stu-id="a8c88-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="a8c88-117">Esta propiedad debe identificar de forma única un subobjeto de datos adjuntos dentro de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a8c88-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="a8c88-118">Este identificador es la única característica de datos adjuntos que se garantiza que se mantenga igual después de cerrar y volver a abrir el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a8c88-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="a8c88-119">El proveedor de almacén debe conservar esta propiedad entre sesiones para garantizar esta garantía.</span><span class="sxs-lookup"><span data-stu-id="a8c88-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="a8c88-120">Para las carpetas, esta propiedad contiene una clave usada en la tabla de jerarquía de carpetas.</span><span class="sxs-lookup"><span data-stu-id="a8c88-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="a8c88-121">Normalmente es el mismo valor que proporciona la **propiedad PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a8c88-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="a8c88-122">Para los almacenes de mensajes, esta propiedad es idéntica a **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a8c88-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="a8c88-123">En un objeto de almacén de mensajes, esta propiedad debe ser única en todos los proveedores de almacén.</span><span class="sxs-lookup"><span data-stu-id="a8c88-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="a8c88-124">Una forma de hacerlo es combinar el valor de la propiedad **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para el almacén (único para ese tipo de proveedor) con una estructura [GUID](guid.md) u otro valor único para el almacén de mensajes específico.</span><span class="sxs-lookup"><span data-stu-id="a8c88-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="a8c88-125">Esta propiedad siempre está disponible a través del método [IMAPIProp::GetProps](imapiprop-getprops.md) después de la primera llamada al método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="a8c88-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="a8c88-126">Algunos proveedores pueden hacer que esté disponible inmediatamente después de la creación de instancias.</span><span class="sxs-lookup"><span data-stu-id="a8c88-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="a8c88-127">Un cliente o proveedor de servicios puede comparar valores de esta propiedad mediante memcmp.</span><span class="sxs-lookup"><span data-stu-id="a8c88-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="a8c88-128">Esto no es posible para los valores de identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="a8c88-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="a8c88-129">Sin embargo, se garantiza que esta propiedad sea única dentro del mismo almacén de mensajes o contenedor de libreta de direcciones; dos objetos de contenedores diferentes pueden tener el mismo valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="a8c88-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="a8c88-130">Una distinción entre el registro y las claves de búsqueda es que la clave de registro es específica del objeto, mientras que la clave de búsqueda se puede copiar a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="a8c88-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="a8c88-131">Por ejemplo, dos copias del objeto pueden tener el mismo valor **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), pero deben tener valores diferentes para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="a8c88-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="a8c88-132">En la tabla siguiente se resumen las diferencias **importantes entre PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) y esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="a8c88-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="a8c88-133">**Característica**</span><span class="sxs-lookup"><span data-stu-id="a8c88-133">**Characteristic**</span></span>|<span data-ttu-id="a8c88-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="a8c88-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="a8c88-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="a8c88-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="a8c88-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="a8c88-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a8c88-137">Obligatorio en objetos de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="a8c88-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="a8c88-138">No</span><span class="sxs-lookup"><span data-stu-id="a8c88-138">No</span></span>  <br/> |<span data-ttu-id="a8c88-139">Sí</span><span class="sxs-lookup"><span data-stu-id="a8c88-139">Yes</span></span>  <br/> |<span data-ttu-id="a8c88-140">No</span><span class="sxs-lookup"><span data-stu-id="a8c88-140">No</span></span>  <br/> |
|<span data-ttu-id="a8c88-141">Obligatorio en objetos de carpeta</span><span class="sxs-lookup"><span data-stu-id="a8c88-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="a8c88-142">Sí</span><span class="sxs-lookup"><span data-stu-id="a8c88-142">Yes</span></span>  <br/> |<span data-ttu-id="a8c88-143">Sí</span><span class="sxs-lookup"><span data-stu-id="a8c88-143">Yes</span></span>  <br/> |<span data-ttu-id="a8c88-144">No</span><span class="sxs-lookup"><span data-stu-id="a8c88-144">No</span></span>  <br/> |
|<span data-ttu-id="a8c88-145">Obligatorio en objetos de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="a8c88-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="a8c88-146">Sí</span><span class="sxs-lookup"><span data-stu-id="a8c88-146">Yes</span></span>  <br/> |<span data-ttu-id="a8c88-147">Sí</span><span class="sxs-lookup"><span data-stu-id="a8c88-147">Yes</span></span>  <br/> |<span data-ttu-id="a8c88-148">No</span><span class="sxs-lookup"><span data-stu-id="a8c88-148">No</span></span>  <br/> |
|<span data-ttu-id="a8c88-149">Requerido en objetos de estado</span><span class="sxs-lookup"><span data-stu-id="a8c88-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="a8c88-150">Sí</span><span class="sxs-lookup"><span data-stu-id="a8c88-150">Yes</span></span>  <br/> |<span data-ttu-id="a8c88-151">No</span><span class="sxs-lookup"><span data-stu-id="a8c88-151">No</span></span>  <br/> |<span data-ttu-id="a8c88-152">No</span><span class="sxs-lookup"><span data-stu-id="a8c88-152">No</span></span>  <br/> |
|<span data-ttu-id="a8c88-153">Creable por cliente</span><span class="sxs-lookup"><span data-stu-id="a8c88-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="a8c88-154">No</span><span class="sxs-lookup"><span data-stu-id="a8c88-154">No</span></span>  <br/> |<span data-ttu-id="a8c88-155">No</span><span class="sxs-lookup"><span data-stu-id="a8c88-155">No</span></span>  <br/> |<span data-ttu-id="a8c88-156">Sí</span><span class="sxs-lookup"><span data-stu-id="a8c88-156">Yes</span></span>  <br/> |
|<span data-ttu-id="a8c88-157">Disponible antes de llamar a **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="a8c88-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="a8c88-158">Tal vez</span><span class="sxs-lookup"><span data-stu-id="a8c88-158">Maybe</span></span>  <br/> |<span data-ttu-id="a8c88-159">Tal vez</span><span class="sxs-lookup"><span data-stu-id="a8c88-159">Maybe</span></span>  <br/> |<span data-ttu-id="a8c88-160">Mensajes Sí a otros, tal vez</span><span class="sxs-lookup"><span data-stu-id="a8c88-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="a8c88-161">Se cambió en una operación de copia</span><span class="sxs-lookup"><span data-stu-id="a8c88-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="a8c88-162">Sí</span><span class="sxs-lookup"><span data-stu-id="a8c88-162">Yes</span></span>  <br/> |<span data-ttu-id="a8c88-163">Sí</span><span class="sxs-lookup"><span data-stu-id="a8c88-163">Yes</span></span>  <br/> |<span data-ttu-id="a8c88-164">No</span><span class="sxs-lookup"><span data-stu-id="a8c88-164">No</span></span>  <br/> |
|<span data-ttu-id="a8c88-165">Modificable por un cliente después de una copia</span><span class="sxs-lookup"><span data-stu-id="a8c88-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="a8c88-166">No</span><span class="sxs-lookup"><span data-stu-id="a8c88-166">No</span></span>  <br/> |<span data-ttu-id="a8c88-167">No</span><span class="sxs-lookup"><span data-stu-id="a8c88-167">No</span></span>  <br/> |<span data-ttu-id="a8c88-168">Sí</span><span class="sxs-lookup"><span data-stu-id="a8c88-168">Yes</span></span>  <br/> |
|<span data-ttu-id="a8c88-169">Único dentro de ...</span><span class="sxs-lookup"><span data-stu-id="a8c88-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="a8c88-170">Todo el mundo</span><span class="sxs-lookup"><span data-stu-id="a8c88-170">Entire world</span></span>  <br/> |<span data-ttu-id="a8c88-171">Instancia del proveedor</span><span class="sxs-lookup"><span data-stu-id="a8c88-171">Provider instance</span></span>  <br/> |<span data-ttu-id="a8c88-172">Todo el mundo</span><span class="sxs-lookup"><span data-stu-id="a8c88-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="a8c88-173">Binario comparable (como con memcmp)</span><span class="sxs-lookup"><span data-stu-id="a8c88-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="a8c88-174">No: use **IMAPISupport:: CompareEntryIDs**</span><span class="sxs-lookup"><span data-stu-id="a8c88-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="a8c88-175">Sí</span><span class="sxs-lookup"><span data-stu-id="a8c88-175">Yes</span></span>  <br/> |<span data-ttu-id="a8c88-176">Sí</span><span class="sxs-lookup"><span data-stu-id="a8c88-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a8c88-177">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8c88-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a8c88-178">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="a8c88-178">Protocol specifications</span></span>

<span data-ttu-id="a8c88-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8c88-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8c88-180">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="a8c88-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a8c88-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8c88-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8c88-182">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a8c88-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="a8c88-183">[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8c88-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8c88-184">Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="a8c88-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a8c88-185">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a8c88-185">Header files</span></span>

<span data-ttu-id="a8c88-186">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8c88-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="a8c88-187">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a8c88-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="a8c88-188">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a8c88-188">Mapitags.h</span></span>
  
> <span data-ttu-id="a8c88-189">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a8c88-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8c88-190">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a8c88-190">See also</span></span>



[<span data-ttu-id="a8c88-191">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a8c88-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a8c88-192">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="a8c88-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a8c88-193">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a8c88-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a8c88-194">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="a8c88-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

