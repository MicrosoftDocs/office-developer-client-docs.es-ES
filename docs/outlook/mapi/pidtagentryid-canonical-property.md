---
title: Propiedad canónica PidTagEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328591"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="1f622-103">Propiedad canónica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="1f622-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="1f622-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f622-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f622-105">Contiene un identificador de entrada MAPI que se usa para abrir y editar las propiedades de un objeto MAPI en particular.</span><span class="sxs-lookup"><span data-stu-id="1f622-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f622-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1f622-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f622-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1f622-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="1f622-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1f622-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f622-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="1f622-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="1f622-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1f622-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f622-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1f622-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1f622-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1f622-112">Area:</span></span>  <br/> |<span data-ttu-id="1f622-113">Propiedades de identificador</span><span class="sxs-lookup"><span data-stu-id="1f622-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f622-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1f622-114">Remarks</span></span>

<span data-ttu-id="1f622-115">Esta propiedad identifica un objeto para que **OpenEntry** cree una instancia y proporciona acceso a todas sus propiedades a través de la interfaz derivada adecuada de **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="1f622-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="1f622-116">Esta propiedad es una de las propiedades de dirección base para todos los usuarios de la mensajería.</span><span class="sxs-lookup"><span data-stu-id="1f622-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="1f622-117">Esta propiedad puede contener un identificador a largo plazo o a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="1f622-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="1f622-118">Los identificadores a corto plazo son más sencillos y rápidos de construir, pero están limitados en su ámbito y duración, normalmente para la sesión y la estación de trabajo actuales.</span><span class="sxs-lookup"><span data-stu-id="1f622-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="1f622-119">Se suelen usar para objetos de naturaleza temporal, como filas de tabla o entradas de cuadro de diálogo y, a continuación, abandonados.</span><span class="sxs-lookup"><span data-stu-id="1f622-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="1f622-120">Los identificadores a largo plazo se usan para los objetos de un tipo más amplio y de larga duración.</span><span class="sxs-lookup"><span data-stu-id="1f622-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="1f622-121">Esta propiedad siempre está disponible a través del método [IMAPIProp:: GetProps](imapiprop-getprops.md) después de la primera llamada al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="1f622-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="1f622-122">Algunos proveedores de servicios pueden hacer que estén disponibles inmediatamente después de la creación de instancias.</span><span class="sxs-lookup"><span data-stu-id="1f622-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="1f622-123">El proveedor siempre debe devolver un identificador de entrada a largo plazo desde **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="1f622-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="1f622-124">Por lo tanto, para convertir un identificador a corto plazo en largo plazo, basta con abrir el objeto y obtener su propiedad mediante **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="1f622-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="1f622-125">En la tabla siguiente se resumen las diferencias importantes entre esta propiedad, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) y **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1f622-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="1f622-126">**Característica**</span><span class="sxs-lookup"><span data-stu-id="1f622-126">**Characteristic**</span></span>|<span data-ttu-id="1f622-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="1f622-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="1f622-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="1f622-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="1f622-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="1f622-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1f622-130">Necesario en los objetos Attachment</span><span class="sxs-lookup"><span data-stu-id="1f622-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="1f622-131">No</span><span class="sxs-lookup"><span data-stu-id="1f622-131">No</span></span>  <br/> |<span data-ttu-id="1f622-132">Sí</span><span class="sxs-lookup"><span data-stu-id="1f622-132">Yes</span></span>  <br/> |<span data-ttu-id="1f622-133">No</span><span class="sxs-lookup"><span data-stu-id="1f622-133">No</span></span>  <br/> |
|<span data-ttu-id="1f622-134">Necesario en objetos Folder</span><span class="sxs-lookup"><span data-stu-id="1f622-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="1f622-135">Sí</span><span class="sxs-lookup"><span data-stu-id="1f622-135">Yes</span></span>  <br/> |<span data-ttu-id="1f622-136">Sí</span><span class="sxs-lookup"><span data-stu-id="1f622-136">Yes</span></span>  <br/> |<span data-ttu-id="1f622-137">No</span><span class="sxs-lookup"><span data-stu-id="1f622-137">No</span></span>  <br/> |
|<span data-ttu-id="1f622-138">Obligatorio en objetos de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="1f622-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="1f622-139">Sí</span><span class="sxs-lookup"><span data-stu-id="1f622-139">Yes</span></span>  <br/> |<span data-ttu-id="1f622-140">Sí</span><span class="sxs-lookup"><span data-stu-id="1f622-140">Yes</span></span>  <br/> |<span data-ttu-id="1f622-141">No</span><span class="sxs-lookup"><span data-stu-id="1f622-141">No</span></span>  <br/> |
|<span data-ttu-id="1f622-142">Obligatorio en objetos de estado</span><span class="sxs-lookup"><span data-stu-id="1f622-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="1f622-143">Sí</span><span class="sxs-lookup"><span data-stu-id="1f622-143">Yes</span></span>  <br/> |<span data-ttu-id="1f622-144">No</span><span class="sxs-lookup"><span data-stu-id="1f622-144">No</span></span>  <br/> |<span data-ttu-id="1f622-145">No</span><span class="sxs-lookup"><span data-stu-id="1f622-145">No</span></span>  <br/> |
|<span data-ttu-id="1f622-146">Creado por el cliente</span><span class="sxs-lookup"><span data-stu-id="1f622-146">Created by client</span></span>  <br/> |<span data-ttu-id="1f622-147">No</span><span class="sxs-lookup"><span data-stu-id="1f622-147">No</span></span>  <br/> |<span data-ttu-id="1f622-148">No</span><span class="sxs-lookup"><span data-stu-id="1f622-148">No</span></span>  <br/> |<span data-ttu-id="1f622-149">Sí</span><span class="sxs-lookup"><span data-stu-id="1f622-149">Yes</span></span>  <br/> |
|<span data-ttu-id="1f622-150">Disponible antes de llamar a **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="1f622-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="1f622-151">Depende de la implementación del proveedor</span><span class="sxs-lookup"><span data-stu-id="1f622-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="1f622-152">Depende de la implementación del proveedor</span><span class="sxs-lookup"><span data-stu-id="1f622-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="1f622-153">Para los mensajes, sí.</span><span class="sxs-lookup"><span data-stu-id="1f622-153">For messages, Yes.</span></span> <span data-ttu-id="1f622-154">Para otros, depende de la implementación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="1f622-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="1f622-155">Modificado en una operación de copia</span><span class="sxs-lookup"><span data-stu-id="1f622-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="1f622-156">Sí</span><span class="sxs-lookup"><span data-stu-id="1f622-156">Yes</span></span>  <br/> |<span data-ttu-id="1f622-157">Sí</span><span class="sxs-lookup"><span data-stu-id="1f622-157">Yes</span></span>  <br/> |<span data-ttu-id="1f622-158">No</span><span class="sxs-lookup"><span data-stu-id="1f622-158">No</span></span>  <br/> |
|<span data-ttu-id="1f622-159">Cambiable por cliente después de una copia</span><span class="sxs-lookup"><span data-stu-id="1f622-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="1f622-160">No</span><span class="sxs-lookup"><span data-stu-id="1f622-160">No</span></span>  <br/> |<span data-ttu-id="1f622-161">No</span><span class="sxs-lookup"><span data-stu-id="1f622-161">No</span></span>  <br/> |<span data-ttu-id="1f622-162">Sí</span><span class="sxs-lookup"><span data-stu-id="1f622-162">Yes</span></span>  <br/> |
|<span data-ttu-id="1f622-163">Único dentro de</span><span class="sxs-lookup"><span data-stu-id="1f622-163">Unique within</span></span>  <br/> |<span data-ttu-id="1f622-164">Todo el mundo</span><span class="sxs-lookup"><span data-stu-id="1f622-164">Entire world</span></span>  <br/> |<span data-ttu-id="1f622-165">Instancia del proveedor</span><span class="sxs-lookup"><span data-stu-id="1f622-165">Provider instance</span></span>  <br/> |<span data-ttu-id="1f622-166">Todo el mundo</span><span class="sxs-lookup"><span data-stu-id="1f622-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="1f622-167">Comparable binario (como con memcmp)</span><span class="sxs-lookup"><span data-stu-id="1f622-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="1f622-168">No usar [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="1f622-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="1f622-169">Sí</span><span class="sxs-lookup"><span data-stu-id="1f622-169">Yes</span></span>  <br/> |<span data-ttu-id="1f622-170">Sí</span><span class="sxs-lookup"><span data-stu-id="1f622-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1f622-171">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f622-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f622-172">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1f622-172">Protocol specifications</span></span>

<span data-ttu-id="1f622-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f622-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f622-174">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1f622-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1f622-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f622-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f622-176">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="1f622-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="1f622-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f622-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f622-178">Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="1f622-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="1f622-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f622-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f622-180">Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="1f622-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="1f622-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f622-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f622-182">Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="1f622-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="1f622-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f622-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f622-184">Controla la recuperación de listas de permisos de carpetas que se almacenan en el servidor.</span><span class="sxs-lookup"><span data-stu-id="1f622-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="1f622-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f622-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f622-186">Especifica los métodos para conectarse a los buzones y configurarlos como delegados, e interacciones con los objetos Message y Calendar cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="1f622-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="1f622-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f622-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f622-188">Especifica el esquema y los métodos que se usan para solicitar información de disponibilidad para usuarios y recursos.</span><span class="sxs-lookup"><span data-stu-id="1f622-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f622-189">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1f622-189">Header files</span></span>

<span data-ttu-id="1f622-190">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1f622-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f622-191">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1f622-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f622-192">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="1f622-192">Mapitags.h</span></span>
  
> <span data-ttu-id="1f622-193">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1f622-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f622-194">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f622-194">See also</span></span>



[<span data-ttu-id="1f622-195">Propiedad canónica PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="1f622-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="1f622-196">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1f622-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f622-197">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="1f622-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f622-198">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1f622-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f622-199">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="1f622-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

