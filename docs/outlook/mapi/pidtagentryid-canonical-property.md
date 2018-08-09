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
ms.openlocfilehash: 971462b9e85878677b57ec7b53fe46aa64db6dba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819498"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="cc2f9-103">Propiedad canónica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="cc2f9-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="cc2f9-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cc2f9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cc2f9-105">Contiene un identificador de entrada MAPI utilizado para abrir y editar las propiedades de un determinado objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc2f9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cc2f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc2f9-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cc2f9-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="cc2f9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cc2f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc2f9-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="cc2f9-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="cc2f9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cc2f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="cc2f9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cc2f9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cc2f9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cc2f9-112">Area:</span></span>  <br/> |<span data-ttu-id="cc2f9-113">Propiedades de Id.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc2f9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc2f9-114">Remarks</span></span>

<span data-ttu-id="cc2f9-115">Esta propiedad identifica un objeto para **OpenEntry** crear una instancia y proporciona acceso a todas sus propiedades a través de la interfaz derivada adecuada de **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="cc2f9-116">Esta propiedad es una de las propiedades de la dirección base para todos los usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="cc2f9-117">Esta propiedad puede contener una a largo plazo o un identificador a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="cc2f9-118">Los identificadores a corto plazo son más fácil y rápida a la construcción, pero se encuentra limitada en su alcance y la duración, normalmente a la sesión actual y la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="cc2f9-119">Que se usan con frecuencia para objetos de carácter temporal, como las filas de tabla o entradas del cuadro de diálogo y posteriormente son abandonados.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="cc2f9-120">Identificadores a largo plazo se utilizan para los objetos de una naturaleza más amplia y de larga duración.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="cc2f9-121">Esta propiedad siempre está disponible a través del método [IMAPIProp::GetProps](imapiprop-getprops.md) después de la primera llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2f9-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="cc2f9-122">Algunos proveedores de servicios pueden estar disponible inmediatamente después de la creación de instancias.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="cc2f9-123">El proveedor siempre debe devolver un identificador de entrada a largo plazo de **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="cc2f9-124">Por lo tanto, para convertir un identificador a corto plazo en a largo plazo, simplemente abra el objeto y obtener su esta propiedad a través de **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="cc2f9-125">En la siguiente tabla se resume las diferencias importantes entre esta propiedad, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) y **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cc2f9-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="cc2f9-126">**Característica**</span><span class="sxs-lookup"><span data-stu-id="cc2f9-126">**Characteristic**</span></span>|<span data-ttu-id="cc2f9-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="cc2f9-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="cc2f9-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="cc2f9-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="cc2f9-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="cc2f9-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cc2f9-130">Requerido en los objetos de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="cc2f9-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="cc2f9-131">No</span><span class="sxs-lookup"><span data-stu-id="cc2f9-131">No</span></span>  <br/> |<span data-ttu-id="cc2f9-132">Sí</span><span class="sxs-lookup"><span data-stu-id="cc2f9-132">Yes</span></span>  <br/> |<span data-ttu-id="cc2f9-133">No</span><span class="sxs-lookup"><span data-stu-id="cc2f9-133">No</span></span>  <br/> |
|<span data-ttu-id="cc2f9-134">Requerido en los objetos de carpeta</span><span class="sxs-lookup"><span data-stu-id="cc2f9-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="cc2f9-135">Sí</span><span class="sxs-lookup"><span data-stu-id="cc2f9-135">Yes</span></span>  <br/> |<span data-ttu-id="cc2f9-136">Sí</span><span class="sxs-lookup"><span data-stu-id="cc2f9-136">Yes</span></span>  <br/> |<span data-ttu-id="cc2f9-137">No</span><span class="sxs-lookup"><span data-stu-id="cc2f9-137">No</span></span>  <br/> |
|<span data-ttu-id="cc2f9-138">Necesarios en los objetos de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="cc2f9-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="cc2f9-139">Sí</span><span class="sxs-lookup"><span data-stu-id="cc2f9-139">Yes</span></span>  <br/> |<span data-ttu-id="cc2f9-140">Sí</span><span class="sxs-lookup"><span data-stu-id="cc2f9-140">Yes</span></span>  <br/> |<span data-ttu-id="cc2f9-141">No</span><span class="sxs-lookup"><span data-stu-id="cc2f9-141">No</span></span>  <br/> |
|<span data-ttu-id="cc2f9-142">Requerido en los objetos de estado</span><span class="sxs-lookup"><span data-stu-id="cc2f9-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="cc2f9-143">Sí</span><span class="sxs-lookup"><span data-stu-id="cc2f9-143">Yes</span></span>  <br/> |<span data-ttu-id="cc2f9-144">No</span><span class="sxs-lookup"><span data-stu-id="cc2f9-144">No</span></span>  <br/> |<span data-ttu-id="cc2f9-145">No</span><span class="sxs-lookup"><span data-stu-id="cc2f9-145">No</span></span>  <br/> |
|<span data-ttu-id="cc2f9-146">Creado por cliente</span><span class="sxs-lookup"><span data-stu-id="cc2f9-146">Created by client</span></span>  <br/> |<span data-ttu-id="cc2f9-147">No</span><span class="sxs-lookup"><span data-stu-id="cc2f9-147">No</span></span>  <br/> |<span data-ttu-id="cc2f9-148">No</span><span class="sxs-lookup"><span data-stu-id="cc2f9-148">No</span></span>  <br/> |<span data-ttu-id="cc2f9-149">Sí</span><span class="sxs-lookup"><span data-stu-id="cc2f9-149">Yes</span></span>  <br/> |
|<span data-ttu-id="cc2f9-150">Disponible antes de la llamada a **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="cc2f9-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="cc2f9-151">Depende de implementación del proveedor</span><span class="sxs-lookup"><span data-stu-id="cc2f9-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="cc2f9-152">Depende de implementación del proveedor</span><span class="sxs-lookup"><span data-stu-id="cc2f9-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="cc2f9-153">Para los mensajes, sí.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-153">For messages, Yes.</span></span> <span data-ttu-id="cc2f9-154">Para otras personas, depende de implementación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="cc2f9-155">Cambiado en una operación de copia</span><span class="sxs-lookup"><span data-stu-id="cc2f9-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="cc2f9-156">Sí</span><span class="sxs-lookup"><span data-stu-id="cc2f9-156">Yes</span></span>  <br/> |<span data-ttu-id="cc2f9-157">Sí</span><span class="sxs-lookup"><span data-stu-id="cc2f9-157">Yes</span></span>  <br/> |<span data-ttu-id="cc2f9-158">No</span><span class="sxs-lookup"><span data-stu-id="cc2f9-158">No</span></span>  <br/> |
|<span data-ttu-id="cc2f9-159">Se pueden cambiar después de una copia de los clientes</span><span class="sxs-lookup"><span data-stu-id="cc2f9-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="cc2f9-160">No</span><span class="sxs-lookup"><span data-stu-id="cc2f9-160">No</span></span>  <br/> |<span data-ttu-id="cc2f9-161">No</span><span class="sxs-lookup"><span data-stu-id="cc2f9-161">No</span></span>  <br/> |<span data-ttu-id="cc2f9-162">Sí</span><span class="sxs-lookup"><span data-stu-id="cc2f9-162">Yes</span></span>  <br/> |
|<span data-ttu-id="cc2f9-163">Único en</span><span class="sxs-lookup"><span data-stu-id="cc2f9-163">Unique within</span></span>  <br/> |<span data-ttu-id="cc2f9-164">Todo mundo</span><span class="sxs-lookup"><span data-stu-id="cc2f9-164">Entire world</span></span>  <br/> |<span data-ttu-id="cc2f9-165">Instancia de proveedor</span><span class="sxs-lookup"><span data-stu-id="cc2f9-165">Provider instance</span></span>  <br/> |<span data-ttu-id="cc2f9-166">Todo mundo</span><span class="sxs-lookup"><span data-stu-id="cc2f9-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="cc2f9-167">Binario comparable (como sucede con memcmp)</span><span class="sxs-lookup"><span data-stu-id="cc2f9-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="cc2f9-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="cc2f9-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="cc2f9-169">Sí</span><span class="sxs-lookup"><span data-stu-id="cc2f9-169">Yes</span></span>  <br/> |<span data-ttu-id="cc2f9-170">Sí</span><span class="sxs-lookup"><span data-stu-id="cc2f9-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="cc2f9-171">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc2f9-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cc2f9-172">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="cc2f9-172">Protocol specifications</span></span>

<span data-ttu-id="cc2f9-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc2f9-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc2f9-174">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cc2f9-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc2f9-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc2f9-176">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="cc2f9-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc2f9-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc2f9-178">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="cc2f9-179">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc2f9-179">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc2f9-180">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="cc2f9-181">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc2f9-181">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc2f9-182">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="cc2f9-183">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc2f9-183">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc2f9-184">Controla la recuperación de listas de permisos de carpeta que se almacenan en el servidor.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="cc2f9-185">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc2f9-185">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc2f9-186">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="cc2f9-187">[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc2f9-187">[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc2f9-188">Especifica el esquema y los métodos que se utilizan para solicitar información de disponibilidad para los usuarios y recursos.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cc2f9-189">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cc2f9-189">Header files</span></span>

<span data-ttu-id="cc2f9-190">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc2f9-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc2f9-191">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc2f9-192">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cc2f9-192">Mapitags.h</span></span>
  
> <span data-ttu-id="cc2f9-193">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="cc2f9-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc2f9-194">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc2f9-194">See also</span></span>



[<span data-ttu-id="cc2f9-195">Propiedad canónica PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="cc2f9-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="cc2f9-196">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cc2f9-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc2f9-197">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="cc2f9-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc2f9-198">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cc2f9-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc2f9-199">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="cc2f9-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

