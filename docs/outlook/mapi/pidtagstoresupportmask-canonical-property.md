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
ms.openlocfilehash: 1936cb8e95e3faef8c92d6bf28f5b63b3ff72df5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572707"
---
# <a name="pidtagstoresupportmask-canonical-property"></a><span data-ttu-id="cc1dc-103">Propiedad canónica PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="cc1dc-103">PidTagStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="cc1dc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc1dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc1dc-105">Contiene una máscara de bits de indicadores de esa consulta de aplicaciones de cliente para determinar las características de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-105">Contains a bitmask of flags that client applications query to determine the characteristics of a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc1dc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cc1dc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc1dc-107">PR_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-107">PR_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="cc1dc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cc1dc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc1dc-109">0x340D</span><span class="sxs-lookup"><span data-stu-id="cc1dc-109">0x340D</span></span>  <br/> |
|<span data-ttu-id="cc1dc-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cc1dc-110">Data type:</span></span>  <br/> |<span data-ttu-id="cc1dc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cc1dc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cc1dc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cc1dc-112">Area:</span></span>  <br/> |<span data-ttu-id="cc1dc-113">Varios</span><span class="sxs-lookup"><span data-stu-id="cc1dc-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc1dc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc1dc-114">Remarks</span></span>

<span data-ttu-id="cc1dc-115">Esta propiedad revela las capacidades de un almacén de mensajes a las aplicaciones cliente que se va a enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-115">This property discloses the capabilities of a message store to client applications that are planning to send it a message.</span></span> <span data-ttu-id="cc1dc-116">Los indicadores pueden admitir las decisiones de un cliente o en otro almacén, por ejemplo, si se enviará un **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) o sólo **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cc1dc-116">The flags can support decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="cc1dc-117">Un cliente que nunca debe establecer **PR_STORE_SUPPORT_MASK**; un intento de establecer esta marca devuelve MAPI_E_COMPUTED.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-117">A client should never set **PR_STORE_SUPPORT_MASK**; an attempt to set this flag returns MAPI_E_COMPUTED.</span></span> 
  
<span data-ttu-id="cc1dc-118">La máscara de bits **PR_STORE_SUPPORT_MASK** se pueden establecer uno o varios de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="cc1dc-118">One or more of the following flags can be set for the **PR_STORE_SUPPORT_MASK** bitmask:</span></span> 
  
<span data-ttu-id="cc1dc-119">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-119">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="cc1dc-120">(131072, 0 x 00020000) El almacén de mensajes es compatible con las propiedades que contienen los caracteres ANSI (8 bits).</span><span class="sxs-lookup"><span data-stu-id="cc1dc-120">(131072, 0x00020000) The message store supports properties that contain ANSI (8-bit) characters.</span></span>
    
<span data-ttu-id="cc1dc-121">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-121">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="cc1dc-122">(32, 0 x 00000020) El almacén de mensajes es compatible con datos adjuntos (OLE o que no sean OLE) a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-122">(32, 0x00000020) The message store supports attachments (OLE or non-OLE) to messages.</span></span> 
    
<span data-ttu-id="cc1dc-123">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-123">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="cc1dc-124">(1024, 0 x 00000400) El almacén de mensajes es compatible con vistas ordenadas por categorías de las tablas.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-124">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="cc1dc-125">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-125">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="cc1dc-126">(16, 0 x 00000010) El almacén de mensajes es compatible con la creación de mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-126">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="cc1dc-127">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="cc1dc-127">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="cc1dc-128">(1, 0 x 00000001) Los identificadores de entrada para los objetos en el almacén de mensajes son únicos, es decir, nunca volverá a utilizar durante la vida del almacén.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-128">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="cc1dc-129">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-129">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="cc1dc-130">(65536, 0 x 00010000) El almacén de mensajes es compatible con los mensajes HTML, almacenados en la propiedad **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cc1dc-130">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="cc1dc-131">Si el entorno de desarrollo usa un MAPIDEFS. H del proyecto que no se incluyen STORE_HTML_OK, use el valor 0 x 00010000 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-131">If your development environment uses a MAPIDEFS.H file that does not include STORE_HTML_OK, use the value 0x00010000 instead.</span></span> 
    
<span data-ttu-id="cc1dc-132">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="cc1dc-132">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="cc1dc-133">(2097152, 0x00200000) En un almacén de archivos PST ajustado, indica que, cuando llegue un nuevo mensaje en el almacén, el almacén de realiza las reglas y filtro de spam por separado de procesamiento en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-133">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store performs rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="cc1dc-134">El almacén de las llamadas [IMAPISupport::Notify](imapisupport-notify.md), **fnevNewMail** del valor de la estructura de [notificación](notification.md) que se pasa como un parámetro y, a continuación, pasa los detalles del nuevo mensaje para el cliente de escucha.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-134">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="cc1dc-135">Posteriormente, cuando el cliente escucha recibe la notificación, no se procesará las reglas en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-135">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="cc1dc-136">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="cc1dc-136">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="cc1dc-137">(524288, 0 x 00080000) Esta marca está reservada y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-137">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="cc1dc-138">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-138">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="cc1dc-139">(8, 0 x 00000008) El almacén de mensajes es compatible con la modificación de los mensajes existentes.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-139">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="cc1dc-140">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-140">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="cc1dc-141">(512, 0 x 00000200) El almacén de mensajes es compatible con propiedades multivalores, garantiza la estabilidad del orden de valor en una propiedad multivalor a lo largo de un proceso de guardar operación y admite creación de instancias de propiedades multivalor en las tablas.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-141">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="cc1dc-142">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-142">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="cc1dc-143">(256, 0 x 00000100) El almacén de mensajes es compatible con las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-143">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="cc1dc-144">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-144">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="cc1dc-145">(64, 0x00000040) El almacén de mensajes es compatible con los datos adjuntos OLE.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-145">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="cc1dc-146">Los datos OLE pueden tener acceso a través de una interfaz **IStorage** , como el disponible a través de la propiedad **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cc1dc-146">The OLE data can be accessed through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="cc1dc-147">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="cc1dc-147">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="cc1dc-148">(16384, 0x00004000) Las carpetas en este almacén son pública not (multiusuario), privada (posiblemente de varias instancias, pero no multiusuario).</span><span class="sxs-lookup"><span data-stu-id="cc1dc-148">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="cc1dc-149">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-149">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="cc1dc-150">(8388608, 0x00800000) El controlador de protocolo MAPI no va a rastrear el almacén y el almacén es responsable de inserción de los cambios a través de notificaciones en el indizador para que los mensajes se indizan.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-150">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible for pushing any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="cc1dc-151">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="cc1dc-151">STORE_READONLY</span></span> 
  
> <span data-ttu-id="cc1dc-152">(2, 0 x 00000002) Todas las interfaces para el almacén de mensajes tienen un nivel de acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-152">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="cc1dc-153">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-153">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="cc1dc-154">(4096, 0 x 00001000) El almacén de mensajes es compatible con las restricciones.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-154">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="cc1dc-155">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-155">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="cc1dc-156">(2048, 0x00000800) El almacén de mensajes es compatible con los mensajes de formato de texto enriquecido (RTF), normalmente comprimidos, y el propio almacén mantiene **PR_BODY** y **PR_RTF_COMPRESSED** sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-156">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="cc1dc-157">STORE_RULES_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-157">STORE_RULES_OK</span></span>
  
> <span data-ttu-id="cc1dc-158">(268435456, 0 x 10000000) Indica que las reglas se almacenen en este almacén de archivos PST, incluso si no es el almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-158">(268435456, 0x10000000) Indicates that rules should be stored in this PST store even if it is not the default store.</span></span> <span data-ttu-id="cc1dc-159">Cuando **STORE_RULES_OK** se usa en combinación con **NON_EMS_XP_SAVE**, las reglas son capaces de ejecutar en almacenes de archivos PST ajustado no predeterminados.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-159">When **STORE_RULES_OK** is used in conjunction with **NON_EMS_XP_SAVE**, rules are able to run on non-default PST wrapped stores.</span></span>
    
<span data-ttu-id="cc1dc-160">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-160">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="cc1dc-161">(4, 0 x 00000004) El almacén de mensajes es compatible con las carpetas de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-161">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="cc1dc-162">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-162">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="cc1dc-163">(8192, 0 x 00002000) El almacén de mensajes es compatible con vistas de ordenación de tablas.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-163">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="cc1dc-164">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-164">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="cc1dc-165">(128, 0x00000080) El almacén de mensajes admite marcar un mensaje para el envío.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-165">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="cc1dc-166">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="cc1dc-166">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="cc1dc-167">(32768, 0x00008000) El almacén de mensajes admite el almacenamiento de mensajes RTF en formulario sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-167">(32768, 0x00008000) The message store supports storage of RTF messages in uncompressed form.</span></span> <span data-ttu-id="cc1dc-168">Una secuencia de RTF sin comprimir se identifica mediante el valor **dwMagicUncompressedRTF** en el encabezado de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-168">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="cc1dc-169">El valor de **dwMagicUncompressedRTF** se define en el RTFLIB. H del proyecto.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-169">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="cc1dc-170">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="cc1dc-170">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="cc1dc-171">(262144, 0 x 00040000) Indica que el almacén de mensajes admite el almacenamiento de Unicode.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-171">(262144, 0x00040000) Indicates that the message store supports Unicode storage.</span></span> <span data-ttu-id="cc1dc-172">Un cliente puede buscar la presencia de la marca de decidir si va a solicitar o guardar información de Unicode en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-172">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span> 
    
<span data-ttu-id="cc1dc-173">Una versión RTF de un mensaje puede almacenarse siempre, incluso si el almacén de mensajes es no es compatible con RTF.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-173">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="cc1dc-174">Si no está establecido el bit STORE_RTF_OK de un almacén determinado, un cliente de mantenimiento de las versiones RTF debe propio llamar a la función [RTFSync](rtfsync.md) para mantener las versiones **PR_BODY** y **PR_RTF_COMPRESSED** sincronizadas para el contenido de texto.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-174">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="cc1dc-175">RTF siempre se almacena en **PR_RTF_COMPRESSED**, si realmente está comprimido o no.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-175">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cc1dc-176">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc1dc-176">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cc1dc-177">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="cc1dc-177">Protocol specifications</span></span>

<span data-ttu-id="cc1dc-178">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc1dc-178">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc1dc-179">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-179">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cc1dc-180">[[MS-OXMSG]](http://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc1dc-180">[[MS-OXMSG]](http://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc1dc-181">Describe el formato de los mensajes que se utiliza para enviar información relacionada con el uso compartido de carpetas en el cliente.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-181">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cc1dc-182">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cc1dc-182">Header files</span></span>

<span data-ttu-id="cc1dc-183">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc1dc-183">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc1dc-184">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-184">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc1dc-185">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cc1dc-185">Mapitags.h</span></span>
  
> <span data-ttu-id="cc1dc-186">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="cc1dc-186">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc1dc-187">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="cc1dc-187">See also</span></span>



[<span data-ttu-id="cc1dc-188">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cc1dc-188">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc1dc-189">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="cc1dc-189">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc1dc-190">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cc1dc-190">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc1dc-191">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="cc1dc-191">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

