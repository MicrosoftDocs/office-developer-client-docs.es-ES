---
title: Propiedad canónica PidTagStoreUnicodeMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreUnicodeMask
api_type:
- COM
ms.assetid: a6082162-2a74-4850-a0df-4bdbc67b41d8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4bfbaada3ced58a689ca4d4745e6e4c798755d4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574310"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a><span data-ttu-id="1cb3e-103">Propiedad canónica PidTagStoreUnicodeMask</span><span class="sxs-lookup"><span data-stu-id="1cb3e-103">PidTagStoreUnicodeMask Canonical Property</span></span>

  
  
<span data-ttu-id="1cb3e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cb3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cb3e-105">Contiene una máscara de bits de indicadores de que las aplicaciones cliente deben consultar para determinar las características de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-105">Contains a bitmask of flags that client applications should query to determine the characteristics of a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1cb3e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1cb3e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1cb3e-107">PR_STORE_UNICODE_MASK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-107">PR_STORE_UNICODE_MASK</span></span>  <br/> |
|<span data-ttu-id="1cb3e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1cb3e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1cb3e-109">0x340F</span><span class="sxs-lookup"><span data-stu-id="1cb3e-109">0x340F</span></span>  <br/> |
|<span data-ttu-id="1cb3e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1cb3e-110">Data type:</span></span>  <br/> |<span data-ttu-id="1cb3e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1cb3e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1cb3e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1cb3e-112">Area:</span></span>  <br/> |<span data-ttu-id="1cb3e-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="1cb3e-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cb3e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1cb3e-114">Remarks</span></span>

<span data-ttu-id="1cb3e-115">Esta propiedad revela las capacidades de un almacén de mensajes a aplicaciones cliente de planeación enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-115">This property discloses the capabilities of a message store to client applications planning to send it a message.</span></span> <span data-ttu-id="1cb3e-116">Las marcas pueden facilitar las decisiones de un cliente o en otro almacén, por ejemplo, si se enviará un **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) o sólo **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1cb3e-116">The flags can facilitate decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="1cb3e-117">Un cliente nunca debe establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-117">A client should never set this property.</span></span> <span data-ttu-id="1cb3e-118">Un intento de devuelve **MAPI_E_COMPUTED**.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-118">An attempt returns **MAPI_E_COMPUTED**.</span></span> 
  
<span data-ttu-id="1cb3e-119">Esta propiedad se pueden establecer uno o varios de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="1cb3e-119">One or more of the following flags can be set for this property:</span></span> 
  
<span data-ttu-id="1cb3e-120">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-120">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="1cb3e-121">(131072, 0 x 00020000) El almacén de mensajes es compatible con las propiedades que contienen caracteres de estadounidense National Standards Institute (ANSI) (8 bits).</span><span class="sxs-lookup"><span data-stu-id="1cb3e-121">(131072, 0x00020000) The message store supports properties that contain American National Standards Institute (ANSI) (8-bit) characters.</span></span>
    
<span data-ttu-id="1cb3e-122">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-122">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="1cb3e-123">(32, 0 x 00000020) El almacén de mensajes es compatible con la vinculación e incrustación de objetos (OLE) o datos adjuntos que no sean OLE a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-123">(32, 0x00000020) The message store supports Object Linking and Embedding (OLE) or non-OLE attachments to messages.</span></span> 
    
<span data-ttu-id="1cb3e-124">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-124">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="1cb3e-125">(1024, 0 x 00000400) El almacén de mensajes es compatible con vistas ordenadas por categorías de las tablas.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-125">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="1cb3e-126">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-126">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="1cb3e-127">(16, 0 x 00000010) El almacén de mensajes es compatible con la creación de mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-127">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="1cb3e-128">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="1cb3e-128">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="1cb3e-129">(1, 0 x 00000001) Los identificadores de entrada para los objetos en el almacén de mensajes son únicos, es decir, nunca volverá a utilizar durante la vida del almacén.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-129">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="1cb3e-130">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-130">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="1cb3e-131">(65536, 0 x 00010000) El almacén de mensajes es compatible con los mensajes HTML, almacenados en la propiedad **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1cb3e-131">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="1cb3e-132">Tenga en cuenta que **STORE_HTML_OK** no se ha definido en las versiones de MAPIDEFS. H que se incluye con Microsoft Exchange 2000 Server y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-132">Note that **STORE_HTML_OK** is not defined in versions of MAPIDEFS.H that are included with Microsoft Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="1cb3e-133">Si el entorno de desarrollo usa un MAPIDEFS. H del proyecto que no se incluyen **STORE_HTML_OK**, utilice el valor "0 x 00010000" en su lugar.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-133">If your development environment uses a MAPIDEFS.H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span></span> 
    
<span data-ttu-id="1cb3e-134">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="1cb3e-134">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="1cb3e-135">(2097152, 0x00200000) En un almacén de archivos PST ajustado, indica que cuando llegue un nuevo mensaje en el almacén, el almacén de hace reglas y el correo no deseado de filtro de procesamiento en el mensaje por separado.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-135">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store does rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="1cb3e-136">El almacén de las llamadas [IMAPISupport::Notify](imapisupport-notify.md), **fnevNewMail** del valor de la estructura de [notificación](notification.md) que se pasa como un parámetro y, a continuación, pasa los detalles del nuevo mensaje para el cliente de escucha.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-136">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="1cb3e-137">Posteriormente, cuando el cliente escucha recibe la notificación, no se procesará las reglas en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-137">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="1cb3e-138">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="1cb3e-138">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="1cb3e-139">(524288, 0 x 00080000) Esta marca está reservada y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-139">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="1cb3e-140">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-140">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="1cb3e-141">(8, 0 x 00000008) El almacén de mensajes es compatible con la modificación de los mensajes existentes.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-141">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="1cb3e-142">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-142">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="1cb3e-143">(512, 0 x 00000200) El almacén de mensajes es compatible con propiedades multivalores, garantiza la estabilidad del orden de valor en una propiedad multivalor a lo largo de un proceso de guardar operación y admite creación de instancias de propiedades multivalor en las tablas.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-143">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="1cb3e-144">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-144">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="1cb3e-145">(256, 0 x 00000100) El almacén de mensajes es compatible con las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-145">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="1cb3e-146">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-146">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="1cb3e-147">(64, 0x00000040) El almacén de mensajes es compatible con los datos adjuntos OLE.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-147">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="1cb3e-148">Los datos OLE están accesibles a través de una interfaz **IStorage** , como disponible a través de la propiedad **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1cb3e-148">The OLE data is accessible through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="1cb3e-149">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="1cb3e-149">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="1cb3e-150">(16384, 0x00004000) Las carpetas en este almacén son pública not (multiusuario), privada (posiblemente de varias instancias, pero no multiusuario).</span><span class="sxs-lookup"><span data-stu-id="1cb3e-150">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="1cb3e-151">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-151">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="1cb3e-152">(8388608, 0x00800000) El controlador de protocolo MAPI no va a rastrear el almacén y el almacén es responsable de los cambios a través de notificaciones de inserción al indizador para que los mensajes se indizan.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-152">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="1cb3e-153">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="1cb3e-153">STORE_READONLY</span></span> 
  
> <span data-ttu-id="1cb3e-154">(2, 0 x 00000002) Todas las interfaces para el almacén de mensajes tienen un nivel de acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-154">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="1cb3e-155">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-155">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="1cb3e-156">(4096, 0 x 00001000) El almacén de mensajes es compatible con las restricciones.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-156">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="1cb3e-157">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-157">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="1cb3e-158">(2048, 0x00000800) El almacén de mensajes es compatible con los mensajes de formato de texto enriquecido (RTF), normalmente comprimidos, y el propio almacén mantiene **PR_BODY** y **PR_RTF_COMPRESSED** sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-158">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="1cb3e-159">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-159">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="1cb3e-160">(4, 0 x 00000004) El almacén de mensajes es compatible con las carpetas de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-160">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="1cb3e-161">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-161">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="1cb3e-162">(8192, 0 x 00002000) El almacén de mensajes es compatible con vistas de ordenación de tablas.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-162">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="1cb3e-163">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-163">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="1cb3e-164">(128, 0x00000080) El almacén de mensajes admite marcar un mensaje para el envío.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-164">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="1cb3e-165">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="1cb3e-165">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="1cb3e-166">(32768, 0x00008000) El almacén de mensajes admite el almacenamiento de mensajes de texto (RTF) de formulario revisable en formulario sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-166">(32768, 0x00008000) The message store supports storage of revisable form text (RTF) messages in uncompressed form.</span></span> <span data-ttu-id="1cb3e-167">Una secuencia de RTF sin comprimir se identifica mediante el valor **dwMagicUncompressedRTF** en el encabezado de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-167">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="1cb3e-168">El valor de **dwMagicUncompressedRTF** se define en el RTFLIB. H del proyecto.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-168">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="1cb3e-169">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-169">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="1cb3e-170">(262144, 0 x 00040000) El almacén de mensajes es compatible con las propiedades que contiene caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-170">(262144, 0x00040000) The message store supports properties containing Unicode characters.</span></span>
    
<span data-ttu-id="1cb3e-171">Una versión RTF de un mensaje puede almacenarse siempre, incluso si el almacén de mensajes es no es compatible con RTF.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-171">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="1cb3e-172">Si no está establecido el bit STORE_RTF_OK de un almacén determinado, un cliente de mantenimiento de las versiones RTF debe propio llamar a la función [RTFSync](rtfsync.md) para mantener las versiones **PR_BODY** y **PR_RTF_COMPRESSED** sincronizadas para el contenido de texto.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-172">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="1cb3e-173">RTF siempre se almacena en **PR_RTF_COMPRESSED**, si realmente está comprimido o no.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-173">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1cb3e-174">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1cb3e-174">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1cb3e-175">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1cb3e-175">Header files</span></span>

<span data-ttu-id="1cb3e-176">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1cb3e-176">Mapidefs.h</span></span>
  
> <span data-ttu-id="1cb3e-177">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-177">Provides data type definitions.</span></span>
    
<span data-ttu-id="1cb3e-178">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1cb3e-178">Mapitags.h</span></span>
  
> <span data-ttu-id="1cb3e-179">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-179">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1cb3e-180">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1cb3e-180">See also</span></span>



[<span data-ttu-id="1cb3e-181">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1cb3e-181">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1cb3e-182">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1cb3e-182">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1cb3e-183">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1cb3e-183">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1cb3e-184">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1cb3e-184">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

