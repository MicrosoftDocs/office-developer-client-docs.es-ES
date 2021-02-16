---
title: Propiedad canónica PidTagSendRichInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendRichInfo
api_type:
- COM
ms.assetid: e85fc766-197a-484f-b600-68cd28a052a2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a7ad27d757d4ed6df58c597bf17d9e5412f83457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342521"
---
# <a name="pidtagsendrichinfo-canonical-property"></a><span data-ttu-id="4f3b3-103">Propiedad canónica PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="4f3b3-103">PidTagSendRichInfo Canonical Property</span></span>

  
  
<span data-ttu-id="4f3b3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f3b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f3b3-105">Contiene TRUE si el destinatario puede recibir todo el contenido del mensaje, incluidos los objetos rtf (rtf) y de vinculación e incrustación de objetos (OLE).</span><span class="sxs-lookup"><span data-stu-id="4f3b3-105">Contains TRUE if the recipient can receive all message content, including Rich Text Format (RTF) and Object Linking and Embedding (OLE) objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f3b3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4f3b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f3b3-107">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="4f3b3-107">PR_SEND_RICH_INFO</span></span>  <br/> |
|<span data-ttu-id="4f3b3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4f3b3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f3b3-109">0x3A40</span><span class="sxs-lookup"><span data-stu-id="4f3b3-109">0x3A40</span></span>  <br/> |
|<span data-ttu-id="4f3b3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4f3b3-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f3b3-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4f3b3-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4f3b3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4f3b3-112">Area:</span></span>  <br/> |<span data-ttu-id="4f3b3-113">Address</span><span class="sxs-lookup"><span data-stu-id="4f3b3-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f3b3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f3b3-114">Remarks</span></span>

<span data-ttu-id="4f3b3-115">Se recomienda que la lista de distribución y los objetos de usuario de mensajería exponán esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-115">It is recommended that distribution list and messaging user objects expose this property.</span></span> 
  
<span data-ttu-id="4f3b3-116">Esta propiedad indica si el remitente considera que el destinatario está habilitado para MAPI.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-116">This property indicates whether the sender considers the recipient to be MAPI-enabled.</span></span> 
  
<span data-ttu-id="4f3b3-117">Cuando esta propiedad se establece en TRUE, el transporte y la puerta de enlace pueden transmitir todo el contenido del mensaje, incluidos los objetos RTF y OLE.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-117">When this property is set to TRUE, the transport and gateway can transmit the full content of the message, including RTF and OLE objects.</span></span> <span data-ttu-id="4f3b3-118">El proveedor de transporte y la puerta de enlace deben usar el formato de encapsulamiento neutro de transporte (TNEF) para encapsular las propiedades que no son nativas para todos los sistemas de mensajería implicados.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-118">The transport provider and gateway should use Transport Neutral Encapsulation Format (TNEF) to encapsulate any properties that are not native to all the messaging systems involved.</span></span> 
  
<span data-ttu-id="4f3b3-119">Cuando esta propiedad se establece en FALSE, el proveedor de transporte y la puerta de enlace pueden descartar contenido de mensajes que sus clientes nativos no pueden usar.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-119">When this property is set to FALSE, the transport provider and gateway are free to discard message content that their native clients cannot use.</span></span> <span data-ttu-id="4f3b3-120">Por ejemplo, cuando los clientes no admiten RTF, el proveedor de transporte solo puede enviar texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-120">For example, when the clients do not support RTF, the transport provider can send only plain text.</span></span> 
  
<span data-ttu-id="4f3b3-121">Cuando no se establece esta propiedad, el comportamiento predeterminado viene determinado por la implementación del proveedor de transporte, el agente de transferencia de mensajes (MTA) o la puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-121">When this property is not set, default behavior is determined by the implementation of the transport provider, message transfer agent (MTA), or gateway.</span></span> <span data-ttu-id="4f3b3-122">No es necesario que los proveedores de libretas de direcciones admitan esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-122">Address book providers are not required to support this property.</span></span> <span data-ttu-id="4f3b3-123">Por ejemplo, un proveedor de transporte y libreta de direcciones estrechamente acoplada puede elegir enviar TNEF pero nunca usar RTF.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-123">For example, a tightly coupled address book and transport provider can choose to send TNEF but never use RTF.</span></span> 
  
<span data-ttu-id="4f3b3-124">El cliente no debe asumir que el proveedor de transporte y la puerta de enlace usarán TNEF por su propia iniciativa.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-124">The client should not assume the transport provider and gateway will use TNEF on their own initiative.</span></span> <span data-ttu-id="4f3b3-125">Algunos proveedores de transporte y puertas de enlace compatibles con TNEF lo transmiten sin tener en cuenta el valor de esta propiedad, pero otros rechazan construir o enviar TNEF si no se establece en TRUE.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-125">Some transport providers and gateways that support TNEF transmit it without regard to the value of this property, but others decline to construct or send TNEF if it is not set to TRUE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4f3b3-126">La configuración de esta propiedad y las decisiones basadas en su valor se toman por destinatario.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-126">The setting of this property, and the decisions based on its value, are on a per-recipient basis.</span></span> 
  
<span data-ttu-id="4f3b3-127">De forma predeterminada, MAPI establece el valor en TRUE.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-127">By default, MAPI sets the value to TRUE.</span></span> <span data-ttu-id="4f3b3-128">Un cliente que llama a [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) o un proveedor que llama a [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) puede establecer el bit MAPI_SEND_NO_RICH_INFO en el parámetro _ulFlags,_ lo que hace que MAPI establezca esta propiedad **en** FALSE.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-128">A client calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) or a provider calling [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) can set the **MAPI_SEND_NO_RICH_INFO** bit in the  _ulFlags_ parameter, which causes MAPI to set this property to FALSE.</span></span> <span data-ttu-id="4f3b3-129">Los usos únicos creados por la interfaz de usuario usan el valor especificado por la plantilla de creación.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-129">One-offs created by the user interface use the value specified by the creating template.</span></span> 
  
<span data-ttu-id="4f3b3-130">En las llamadas al método [IAddrBook::ResolveName](iaddrbook-resolvename.md) cuando el nombre no se puede resolver pero se puede interpretar como una dirección de Internet (SMTP), esta propiedad se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-130">On calls to the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method when the name cannot be resolved but can be interpreted as an Internet address (SMTP), this property is set to FALSE.</span></span> <span data-ttu-id="4f3b3-131">Para que se interprete como una dirección de Internet, el nombre para mostrar de la entrada sin resolver debe tener el formato X@Y. Z, como "pete@pinecone.com".</span><span class="sxs-lookup"><span data-stu-id="4f3b3-131">To be construed as an Internet address, the display name of the unresolved entry must be in the format X@Y.Z, such as "pete@pinecone.com".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4f3b3-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f3b3-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f3b3-133">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="4f3b3-133">Protocol specifications</span></span>

<span data-ttu-id="4f3b3-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f3b3-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f3b3-135">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-135">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4f3b3-136">[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f3b3-136">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f3b3-137">Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-137">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="4f3b3-138">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f3b3-138">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f3b3-139">Especifica las propiedades y las operaciones permitidas para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-139">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="4f3b3-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f3b3-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f3b3-141">de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-141">from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4f3b3-142">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4f3b3-142">Header files</span></span>

<span data-ttu-id="4f3b3-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f3b3-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f3b3-144">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f3b3-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4f3b3-145">Mapitags.h</span></span>
  
> <span data-ttu-id="4f3b3-146">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="4f3b3-146">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f3b3-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4f3b3-147">See also</span></span>



[<span data-ttu-id="4f3b3-148">Propiedad canónica PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="4f3b3-148">PidTagAttachDataObject Canonical Property</span></span>](pidtagattachdataobject-canonical-property.md)


[<span data-ttu-id="4f3b3-149">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4f3b3-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f3b3-150">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="4f3b3-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f3b3-151">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4f3b3-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f3b3-152">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4f3b3-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

