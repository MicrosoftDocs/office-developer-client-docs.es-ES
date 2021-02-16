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
ms.openlocfilehash: e15c259003ed2cb425eb181f4383f3054967b993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437941"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a><span data-ttu-id="219f9-103">Propiedad canónica PidTagStoreUnicodeMask</span><span class="sxs-lookup"><span data-stu-id="219f9-103">PidTagStoreUnicodeMask Canonical Property</span></span>

  
  
<span data-ttu-id="219f9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="219f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="219f9-105">Contiene una máscara de bits de marcas que las aplicaciones cliente deben consultar para determinar las características de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="219f9-105">Contains a bitmask of flags that client applications should query to determine the characteristics of a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="219f9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="219f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="219f9-107">PR_STORE_UNICODE_MASK</span><span class="sxs-lookup"><span data-stu-id="219f9-107">PR_STORE_UNICODE_MASK</span></span>  <br/> |
|<span data-ttu-id="219f9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="219f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="219f9-109">0x340F</span><span class="sxs-lookup"><span data-stu-id="219f9-109">0x340F</span></span>  <br/> |
|<span data-ttu-id="219f9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="219f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="219f9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="219f9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="219f9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="219f9-112">Area:</span></span>  <br/> |<span data-ttu-id="219f9-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="219f9-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="219f9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="219f9-114">Remarks</span></span>

<span data-ttu-id="219f9-115">Esta propiedad divulga las capacidades de un almacén de mensajes a las aplicaciones cliente que planean enviarle un mensaje.</span><span class="sxs-lookup"><span data-stu-id="219f9-115">This property discloses the capabilities of a message store to client applications planning to send it a message.</span></span> <span data-ttu-id="219f9-116">Las marcas pueden facilitar las decisiones de un cliente u otro almacén, como si se va a enviar **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) o solo **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="219f9-116">The flags can facilitate decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="219f9-117">Un cliente nunca debe establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="219f9-117">A client should never set this property.</span></span> <span data-ttu-id="219f9-118">Un intento devuelve **MAPI_E_COMPUTED**.</span><span class="sxs-lookup"><span data-stu-id="219f9-118">An attempt returns **MAPI_E_COMPUTED**.</span></span> 
  
<span data-ttu-id="219f9-119">Se pueden establecer una o varias de las siguientes marcas para esta propiedad:</span><span class="sxs-lookup"><span data-stu-id="219f9-119">One or more of the following flags can be set for this property:</span></span> 
  
<span data-ttu-id="219f9-120">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-120">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="219f9-121">(131072, 0x00020000) El almacén de mensajes admite propiedades que contienen caracteres del American National Standards Institute (ANSI) (8 bits).</span><span class="sxs-lookup"><span data-stu-id="219f9-121">(131072, 0x00020000) The message store supports properties that contain American National Standards Institute (ANSI) (8-bit) characters.</span></span>
    
<span data-ttu-id="219f9-122">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-122">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="219f9-123">(32, 0x00000020) El almacén de mensajes admite la vinculación e incrustación de objetos (OLE) o datos adjuntos que no son OLE para los mensajes.</span><span class="sxs-lookup"><span data-stu-id="219f9-123">(32, 0x00000020) The message store supports Object Linking and Embedding (OLE) or non-OLE attachments to messages.</span></span> 
    
<span data-ttu-id="219f9-124">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-124">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="219f9-125">(1024, 0x00000400) El almacén de mensajes admite vistas de tablas categorizadas.</span><span class="sxs-lookup"><span data-stu-id="219f9-125">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="219f9-126">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-126">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="219f9-127">(16, 0x00000010) El almacén de mensajes admite la creación de mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="219f9-127">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="219f9-128">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="219f9-128">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="219f9-129">(1, 0x00000001) Los identificadores de entrada de los objetos del almacén de mensajes son únicos, es decir, nunca se reutilizan durante la vida útil del almacén.</span><span class="sxs-lookup"><span data-stu-id="219f9-129">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="219f9-130">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-130">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="219f9-131">(65536, 0x00010000) El almacén de mensajes admite mensajes HTML, almacenados en **la PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="219f9-131">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="219f9-132">Tenga en **cuenta STORE_HTML_OK** no se define en las versiones de MAPIDEFS. H que se incluyen con Microsoft Exchange 2000 Server y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="219f9-132">Note that **STORE_HTML_OK** is not defined in versions of MAPIDEFS.H that are included with Microsoft Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="219f9-133">Si el entorno de desarrollo usa un MAPIDEFS. H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span><span class="sxs-lookup"><span data-stu-id="219f9-133">If your development environment uses a MAPIDEFS.H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span></span> 
    
<span data-ttu-id="219f9-134">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="219f9-134">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="219f9-135">(2097152, 0x00200000) En un almacén pst ajustado, indica que cuando llega un nuevo mensaje al almacén, el almacén realiza reglas y procesamiento de filtro de correo no deseado en el mensaje por separado.</span><span class="sxs-lookup"><span data-stu-id="219f9-135">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store does rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="219f9-136">El almacén llama a [IMAPISupport::Notify](imapisupport-notify.md), configura **fnevNewMail** en la estructura [de](notification.md) notificación que se pasa como parámetro y, a continuación, pasa los detalles del nuevo mensaje al cliente de escucha.</span><span class="sxs-lookup"><span data-stu-id="219f9-136">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="219f9-137">Posteriormente, cuando el cliente en escucha recibe la notificación, no procesa las reglas en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="219f9-137">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="219f9-138">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="219f9-138">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="219f9-139">(524288, 0x00080000) Esta marca está reservada y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="219f9-139">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="219f9-140">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-140">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="219f9-141">(8, 0x00000008) El almacén de mensajes admite la modificación de sus mensajes existentes.</span><span class="sxs-lookup"><span data-stu-id="219f9-141">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="219f9-142">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-142">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="219f9-143">(512, 0x00000200) El almacén de mensajes admite propiedades multivalor, garantiza la estabilidad del orden de los valores en una propiedad multivalor durante una operación de guardado y admite la creación de instancias de propiedades multivalor en tablas.</span><span class="sxs-lookup"><span data-stu-id="219f9-143">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="219f9-144">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-144">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="219f9-145">(256, 0x00000100) El almacén de mensajes admite notificaciones.</span><span class="sxs-lookup"><span data-stu-id="219f9-145">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="219f9-146">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-146">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="219f9-147">(64, 0x00000040) El almacén de mensajes admite datos adjuntos OLE.</span><span class="sxs-lookup"><span data-stu-id="219f9-147">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="219f9-148">Se puede tener acceso a los datos OLE a través de una interfaz **IStorage,** como la disponible a través de **la** PR_ATTACH_DATA_OBJ ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="219f9-148">The OLE data is accessible through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="219f9-149">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="219f9-149">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="219f9-150">(16384, 0x00004000) Las carpetas de este almacén son públicas (de varios usuarios), no privadas (posiblemente de varias instancias, pero no de varios usuarios).</span><span class="sxs-lookup"><span data-stu-id="219f9-150">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="219f9-151">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-151">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="219f9-152">(8388608, 0x00800000) El controlador de protocolo MAPI no rastreará el almacén y el almacén es responsable de enviar cualquier cambio a través de notificaciones al indizador para que los mensajes se indicen.</span><span class="sxs-lookup"><span data-stu-id="219f9-152">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="219f9-153">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="219f9-153">STORE_READONLY</span></span> 
  
> <span data-ttu-id="219f9-154">(2, 0x00000002) Todas las interfaces del almacén de mensajes tienen un nivel de acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="219f9-154">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="219f9-155">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-155">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="219f9-156">(4096, 0x00001000) El almacén de mensajes admite restricciones.</span><span class="sxs-lookup"><span data-stu-id="219f9-156">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="219f9-157">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-157">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="219f9-158">(2048, 0x00000800) El almacén de mensajes admite mensajes con formato de texto enriquecido  (RTF), normalmente comprimidos, y el propio almacén mantiene PR_BODY y **PR_RTF_COMPRESSED** sincronizados.</span><span class="sxs-lookup"><span data-stu-id="219f9-158">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="219f9-159">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-159">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="219f9-160">(4, 0x00000004) El almacén de mensajes admite carpetas de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="219f9-160">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="219f9-161">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-161">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="219f9-162">(8192, 0x00002000) El almacén de mensajes admite la ordenación de vistas de tablas.</span><span class="sxs-lookup"><span data-stu-id="219f9-162">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="219f9-163">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-163">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="219f9-164">(128, 0x00000080) El almacén de mensajes admite el marcado de un mensaje para su envío.</span><span class="sxs-lookup"><span data-stu-id="219f9-164">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="219f9-165">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="219f9-165">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="219f9-166">(32768, 0x00008000) El almacén de mensajes admite el almacenamiento de mensajes de texto de formulario revisable (RTF) sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="219f9-166">(32768, 0x00008000) The message store supports storage of revisable form text (RTF) messages in uncompressed form.</span></span> <span data-ttu-id="219f9-167">Una secuencia RTF sin comprimir se identifica mediante el valor **dwMagicUncompressedRTF** en el encabezado de secuencia.</span><span class="sxs-lookup"><span data-stu-id="219f9-167">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="219f9-168">El **valor dwMagicUncompressedRTF** se define en RTFLIB. Archivo H.</span><span class="sxs-lookup"><span data-stu-id="219f9-168">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="219f9-169">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="219f9-169">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="219f9-170">(262144, 0x00040000) El almacén de mensajes admite propiedades que contienen caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="219f9-170">(262144, 0x00040000) The message store supports properties containing Unicode characters.</span></span>
    
<span data-ttu-id="219f9-171">Siempre se puede almacenar una versión RTF de un mensaje, incluso si el almacén de mensajes no es compatible con RTF.</span><span class="sxs-lookup"><span data-stu-id="219f9-171">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="219f9-172">Si el bit STORE_RTF_OK no se establece para un almacén determinado, un cliente que mantiene versiones RTF debe llamar a la función [RTFSync](rtfsync.md) para mantener sincronizadas las versiones **PR_BODY** y **PR_RTF_COMPRESSED** para el contenido de texto.</span><span class="sxs-lookup"><span data-stu-id="219f9-172">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="219f9-173">RTF siempre se almacena **en PR_RTF_COMPRESSED**, independientemente de si realmente está comprimido o no.</span><span class="sxs-lookup"><span data-stu-id="219f9-173">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="219f9-174">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="219f9-174">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="219f9-175">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="219f9-175">Header files</span></span>

<span data-ttu-id="219f9-176">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="219f9-176">Mapidefs.h</span></span>
  
> <span data-ttu-id="219f9-177">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="219f9-177">Provides data type definitions.</span></span>
    
<span data-ttu-id="219f9-178">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="219f9-178">Mapitags.h</span></span>
  
> <span data-ttu-id="219f9-179">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="219f9-179">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="219f9-180">Consulte también</span><span class="sxs-lookup"><span data-stu-id="219f9-180">See also</span></span>



[<span data-ttu-id="219f9-181">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="219f9-181">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="219f9-182">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="219f9-182">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="219f9-183">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="219f9-183">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="219f9-184">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="219f9-184">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

