---
title: Propiedad canónica PidTagStoreSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreSupportMask
api_type:
- COM
ms.assetid: ada5694a-b5b1-471f-be33-906fc052681a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 143e7f0d2cd89cd4e7956cdda05d1bd512db4027
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340975"
---
# <a name="pidtagstoresupportmask-canonical-property"></a><span data-ttu-id="3e646-103">Propiedad canónica PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="3e646-103">PidTagStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="3e646-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e646-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e646-105">Contiene una máscara de máscara de marcadores que consultan las aplicaciones cliente para determinar las características de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3e646-105">Contains a bitmask of flags that client applications query to determine the characteristics of a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e646-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3e646-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3e646-107">PR_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="3e646-107">PR_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="3e646-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3e646-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3e646-109">0x340D</span><span class="sxs-lookup"><span data-stu-id="3e646-109">0x340D</span></span>  <br/> |
|<span data-ttu-id="3e646-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3e646-110">Data type:</span></span>  <br/> |<span data-ttu-id="3e646-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3e646-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3e646-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3e646-112">Area:</span></span>  <br/> |<span data-ttu-id="3e646-113">Varios</span><span class="sxs-lookup"><span data-stu-id="3e646-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e646-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3e646-114">Remarks</span></span>

<span data-ttu-id="3e646-115">Esta propiedad revela las capacidades de un almacén de mensajes a las aplicaciones cliente que tienen previsto enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="3e646-115">This property discloses the capabilities of a message store to client applications that are planning to send it a message.</span></span> <span data-ttu-id="3e646-116">Las marcas pueden admitir decisiones de un cliente u otro almacén, por ejemplo, si se envía **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) o solo **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3e646-116">The flags can support decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="3e646-117">Un cliente nunca debe establecer **PR_STORE_SUPPORT_MASK**; un intento de establecer esta marca devuelve MAPI_E_COMPUTED.</span><span class="sxs-lookup"><span data-stu-id="3e646-117">A client should never set **PR_STORE_SUPPORT_MASK**; an attempt to set this flag returns MAPI_E_COMPUTED.</span></span> 
  
<span data-ttu-id="3e646-118">Se pueden configurar uno o varios de los siguientes indicadores para la máscara de **PR_STORE_SUPPORT_MASK** :</span><span class="sxs-lookup"><span data-stu-id="3e646-118">One or more of the following flags can be set for the **PR_STORE_SUPPORT_MASK** bitmask:</span></span> 
  
<span data-ttu-id="3e646-119">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-119">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="3e646-120">(131072, 0x00020000) El almacén de mensajes admite propiedades que contienen caracteres ANSI (8 bits).</span><span class="sxs-lookup"><span data-stu-id="3e646-120">(131072, 0x00020000) The message store supports properties that contain ANSI (8-bit) characters.</span></span>
    
<span data-ttu-id="3e646-121">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-121">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="3e646-122">(32, 0x00000020) El almacén de mensajes admite datos adjuntos (OLE o no OLE) a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="3e646-122">(32, 0x00000020) The message store supports attachments (OLE or non-OLE) to messages.</span></span> 
    
<span data-ttu-id="3e646-123">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-123">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="3e646-124">(1024, 0x00000400) El almacén de mensajes admite vistas por categorías de tablas.</span><span class="sxs-lookup"><span data-stu-id="3e646-124">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="3e646-125">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-125">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="3e646-126">(16, 0x00000010) El almacén de mensajes admite la creación de nuevos mensajes.</span><span class="sxs-lookup"><span data-stu-id="3e646-126">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="3e646-127">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="3e646-127">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="3e646-128">(1, 0x00000001) Los identificadores de entrada de los objetos en el almacén de mensajes son únicos, es decir, nunca se reutiliza durante la vida de la tienda.</span><span class="sxs-lookup"><span data-stu-id="3e646-128">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="3e646-129">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-129">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="3e646-130">(65536, 0x00010000) El almacén de mensajes admite mensajes HTML, almacenados en la propiedad **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3e646-130">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="3e646-131">Si el entorno de desarrollo usa un MAPIDEFS. H que no incluye STORE_HTML_OK, use el valor 0x00010000 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="3e646-131">If your development environment uses a MAPIDEFS.H file that does not include STORE_HTML_OK, use the value 0x00010000 instead.</span></span> 
    
<span data-ttu-id="3e646-132">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="3e646-132">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="3e646-133">(2097152, 0x00200000) En un almacén de archivos PST ajustado, indica que cuando llega un mensaje nuevo a la tienda, el almacén realiza reglas y procesamiento de filtros de correo no deseado en el mensaje por separado.</span><span class="sxs-lookup"><span data-stu-id="3e646-133">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store performs rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="3e646-134">El almacén llama a [IMAPISupport:: Notify](imapisupport-notify.md), estableciendo **fnevNewMail** en la estructura de [notificación](notification.md) que se pasa como parámetro y, a continuación, pasa los detalles del mensaje nuevo al cliente de escucha.</span><span class="sxs-lookup"><span data-stu-id="3e646-134">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="3e646-135">Posteriormente, cuando el cliente en escucha recibe la notificación, no procesa las reglas en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="3e646-135">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="3e646-136">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="3e646-136">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="3e646-137">(524288, 0x00080000) Esta marca está reservada y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="3e646-137">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="3e646-138">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-138">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="3e646-139">(8, 0x00000008) El almacén de mensajes admite la modificación de sus mensajes existentes.</span><span class="sxs-lookup"><span data-stu-id="3e646-139">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="3e646-140">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-140">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="3e646-141">(512, 0x00000200) El almacén de mensajes admite propiedades multivalor, garantiza la estabilidad del orden de los valores en una propiedad con varios valores a lo largo de una operación de guardar y admite la creación de instancias de propiedades multivalor en tablas.</span><span class="sxs-lookup"><span data-stu-id="3e646-141">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="3e646-142">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-142">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="3e646-143">(256, 0x00000100) El almacén de mensajes admite notificaciones.</span><span class="sxs-lookup"><span data-stu-id="3e646-143">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="3e646-144">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-144">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="3e646-145">(64, 0x00000040) El almacén de mensajes admite datos adjuntos OLE.</span><span class="sxs-lookup"><span data-stu-id="3e646-145">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="3e646-146">Se puede tener acceso a los datos OLE a través de una interfaz **IStorage** , como la que está disponible a través de la propiedad **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3e646-146">The OLE data can be accessed through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="3e646-147">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="3e646-147">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="3e646-148">(16384, 0x00004000) Las carpetas de este almacén son públicas (multiusuario), no privadas (posiblemente varias instancias pero no multiusuario).</span><span class="sxs-lookup"><span data-stu-id="3e646-148">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="3e646-149">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-149">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="3e646-150">(8388608, 0x00800000) El controlador de protocolo MAPI no rastreará el almacén, y el almacén es responsable de enviar los cambios a través de notificaciones al indizador para que tengan mensajes indizados.</span><span class="sxs-lookup"><span data-stu-id="3e646-150">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible for pushing any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="3e646-151">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="3e646-151">STORE_READONLY</span></span> 
  
> <span data-ttu-id="3e646-152">(2, 0x00000002) Todas las interfaces del almacén de mensajes tienen un nivel de acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3e646-152">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="3e646-153">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-153">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="3e646-154">(4096, 0x00001000) El almacén de mensajes admite restricciones.</span><span class="sxs-lookup"><span data-stu-id="3e646-154">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="3e646-155">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-155">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="3e646-156">(2048, 0x00000800) El almacén de mensajes admite mensajes con formato de texto enriquecido (RTF), normalmente comprimidos, y el propio almacén mantiene sincronizados **PR_BODY** y **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="3e646-156">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="3e646-157">STORE_RULES_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-157">STORE_RULES_OK</span></span>
  
> <span data-ttu-id="3e646-158">(268435456, 0x10000000) Indica que las reglas se deben almacenar en este almacén PST incluso si no es el almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3e646-158">(268435456, 0x10000000) Indicates that rules should be stored in this PST store even if it is not the default store.</span></span> <span data-ttu-id="3e646-159">Cuando se usa **STORE_RULES_OK** junto con **NON_EMS_XP_SAVE**, las reglas se pueden ejecutar en almacenes de archivos PST que no son predeterminados.</span><span class="sxs-lookup"><span data-stu-id="3e646-159">When **STORE_RULES_OK** is used in conjunction with **NON_EMS_XP_SAVE**, rules are able to run on non-default PST wrapped stores.</span></span>
    
<span data-ttu-id="3e646-160">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-160">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="3e646-161">(4, 0x00000004) El almacén de mensajes admite carpetas de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3e646-161">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="3e646-162">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-162">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="3e646-163">(8192, 0x00002000) El almacén de mensajes admite la ordenación de vistas de tablas.</span><span class="sxs-lookup"><span data-stu-id="3e646-163">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="3e646-164">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-164">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="3e646-165">(128, 0x00000080) El almacén de mensajes permite marcar un mensaje para su envío.</span><span class="sxs-lookup"><span data-stu-id="3e646-165">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="3e646-166">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="3e646-166">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="3e646-167">(32768, 0x00008000) El almacén de mensajes admite el almacenamiento de mensajes RTF en un formulario descomprimido.</span><span class="sxs-lookup"><span data-stu-id="3e646-167">(32768, 0x00008000) The message store supports storage of RTF messages in uncompressed form.</span></span> <span data-ttu-id="3e646-168">Una secuencia RTF sin comprimir se identifica por el valor **dwMagicUncompressedRTF** en el encabezado de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="3e646-168">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="3e646-169">El valor **dwMagicUncompressedRTF** se define en RTFLIB. H del archivo.</span><span class="sxs-lookup"><span data-stu-id="3e646-169">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="3e646-170">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="3e646-170">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="3e646-171">(262144, 0x00040000) Indica que el almacén de mensajes admite el almacenamiento Unicode.</span><span class="sxs-lookup"><span data-stu-id="3e646-171">(262144, 0x00040000) Indicates that the message store supports Unicode storage.</span></span> <span data-ttu-id="3e646-172">Un cliente puede buscar la presencia de la marca para decidir si desea solicitar o guardar información Unicode en el almacén.</span><span class="sxs-lookup"><span data-stu-id="3e646-172">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span> 
    
<span data-ttu-id="3e646-173">Siempre se puede almacenar una versión RTF de un mensaje, incluso si el almacén de mensajes no es compatible con RTF.</span><span class="sxs-lookup"><span data-stu-id="3e646-173">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="3e646-174">Si el bit STORE_RTF_OK no se establece para un almacén en particular, un cliente que mantenga versiones RTF debe llamar a la función [RTFSync](rtfsync.md) para mantener las versiones **PR_BODY** y **PR_RTF_COMPRESSED** sincronizadas para el contenido de texto.</span><span class="sxs-lookup"><span data-stu-id="3e646-174">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="3e646-175">RTF siempre se almacena en **PR_RTF_COMPRESSED**, independientemente de si realmente está comprimido o no.</span><span class="sxs-lookup"><span data-stu-id="3e646-175">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3e646-176">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e646-176">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3e646-177">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="3e646-177">Protocol specifications</span></span>

<span data-ttu-id="3e646-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e646-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e646-179">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3e646-179">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3e646-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e646-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e646-181">Describe el formato de los mensajes usados para enviar información relacionada con carpetas de uso compartido en el cliente.</span><span class="sxs-lookup"><span data-stu-id="3e646-181">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3e646-182">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3e646-182">Header files</span></span>

<span data-ttu-id="3e646-183">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3e646-183">Mapidefs.h</span></span>
  
> <span data-ttu-id="3e646-184">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3e646-184">Provides data type definitions.</span></span>
    
<span data-ttu-id="3e646-185">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="3e646-185">Mapitags.h</span></span>
  
> <span data-ttu-id="3e646-186">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="3e646-186">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e646-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e646-187">See also</span></span>



[<span data-ttu-id="3e646-188">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3e646-188">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3e646-189">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="3e646-189">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3e646-190">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3e646-190">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3e646-191">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="3e646-191">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

