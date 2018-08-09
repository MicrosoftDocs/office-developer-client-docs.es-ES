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
ms.openlocfilehash: a85851663c22b33ea94099ac0ab14f81c424259b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820265"
---
# <a name="pidtagsendrichinfo-canonical-property"></a><span data-ttu-id="b41d8-103">Propiedad canónica PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="b41d8-103">PidTagSendRichInfo Canonical Property</span></span>

  
  
<span data-ttu-id="b41d8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b41d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b41d8-105">Contiene TRUE si el destinatario puede recibir todo el contenido mensaje, incluido el formato de texto enriquecido (RTF) y objetos de vinculación e incrustación de objetos (OLE).</span><span class="sxs-lookup"><span data-stu-id="b41d8-105">Contains TRUE if the recipient can receive all message content, including Rich Text Format (RTF) and Object Linking and Embedding (OLE) objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b41d8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b41d8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b41d8-107">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="b41d8-107">PR_SEND_RICH_INFO</span></span>  <br/> |
|<span data-ttu-id="b41d8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b41d8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b41d8-109">0x3A40</span><span class="sxs-lookup"><span data-stu-id="b41d8-109">0x3A40</span></span>  <br/> |
|<span data-ttu-id="b41d8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b41d8-110">Data type:</span></span>  <br/> |<span data-ttu-id="b41d8-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b41d8-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b41d8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b41d8-112">Area:</span></span>  <br/> |<span data-ttu-id="b41d8-113">Address</span><span class="sxs-lookup"><span data-stu-id="b41d8-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b41d8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b41d8-114">Remarks</span></span>

<span data-ttu-id="b41d8-115">Se recomienda que la lista de distribución y objetos de usuario de mensajería exponen esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b41d8-115">It is recommended that distribution list and messaging user objects expose this property.</span></span> 
  
<span data-ttu-id="b41d8-116">Esta propiedad indica si el remitente tiene en cuenta el destinatario habilitado para MAPI.</span><span class="sxs-lookup"><span data-stu-id="b41d8-116">This property indicates whether the sender considers the recipient to be MAPI-enabled.</span></span> 
  
<span data-ttu-id="b41d8-117">Cuando esta propiedad se establece en TRUE, el transporte y la puerta de enlace pueden transmitir el contenido completo del mensaje, incluidos los objetos RTF y OLE.</span><span class="sxs-lookup"><span data-stu-id="b41d8-117">When this property is set to TRUE, the transport and gateway can transmit the full content of the message, including RTF and OLE objects.</span></span> <span data-ttu-id="b41d8-118">El proveedor de transporte y puerta de enlace deben usar el formato de encapsulación neutro de transporte (TNEF) para encapsular todas las propiedades que no son nativas de todos los sistemas de mensajería implicados.</span><span class="sxs-lookup"><span data-stu-id="b41d8-118">The transport provider and gateway should use Transport Neutral Encapsulation Format (TNEF) to encapsulate any properties that are not native to all the messaging systems involved.</span></span> 
  
<span data-ttu-id="b41d8-119">Cuando esta propiedad se establece en FALSE, el proveedor de transporte y puerta de enlace están libres para descartar el contenido de los mensajes que no se pueden usar sus clientes nativos.</span><span class="sxs-lookup"><span data-stu-id="b41d8-119">When this property is set to FALSE, the transport provider and gateway are free to discard message content that their native clients cannot use.</span></span> <span data-ttu-id="b41d8-120">Por ejemplo, cuando los clientes no admiten RTF, el proveedor de transporte puede enviar sólo texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="b41d8-120">For example, when the clients do not support RTF, the transport provider can send only plain text.</span></span> 
  
<span data-ttu-id="b41d8-121">Cuando no se establece esta propiedad, el comportamiento predeterminado se determina por la implementación del proveedor de transporte, el agente de transferencia de mensajes (MTA) o la puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="b41d8-121">When this property is not set, default behavior is determined by the implementation of the transport provider, message transfer agent (MTA), or gateway.</span></span> <span data-ttu-id="b41d8-122">Los proveedores de la libreta de direcciones no son necesarios para admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b41d8-122">Address book providers are not required to support this property.</span></span> <span data-ttu-id="b41d8-123">Por ejemplo, puede elegir un proveedor de libreta de direcciones y transporte de dirección acoplado enviar TNEF, pero nunca utilizan el formato RTF.</span><span class="sxs-lookup"><span data-stu-id="b41d8-123">For example, a tightly coupled address book and transport provider can choose to send TNEF but never use RTF.</span></span> 
  
<span data-ttu-id="b41d8-124">El cliente no debe asumir el proveedor de transporte y puerta de enlace, usa TNEF en su propia iniciativa.</span><span class="sxs-lookup"><span data-stu-id="b41d8-124">The client should not assume the transport provider and gateway will use TNEF on their own initiative.</span></span> <span data-ttu-id="b41d8-125">Algunos proveedores de transporte y las puertas de enlace que admiten TNEF transmiten sin tener en cuenta el valor de esta propiedad, pero otras personas rechazar construir o enviar TNEF si no está establecido en TRUE.</span><span class="sxs-lookup"><span data-stu-id="b41d8-125">Some transport providers and gateways that support TNEF transmit it without regard to the value of this property, but others decline to construct or send TNEF if it is not set to TRUE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b41d8-126">El valor de esta propiedad así como las decisiones en función de su valor, se encuentran en una base por destinatario.</span><span class="sxs-lookup"><span data-stu-id="b41d8-126">The setting of this property, and the decisions based on its value, are on a per-recipient basis.</span></span> 
  
<span data-ttu-id="b41d8-127">De forma predeterminada, MAPI establece el valor en TRUE.</span><span class="sxs-lookup"><span data-stu-id="b41d8-127">By default, MAPI sets the value to TRUE.</span></span> <span data-ttu-id="b41d8-128">Un cliente de una llamada a [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) o un proveedor de llamar a [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) puede establecer el bit **MAPI_SEND_NO_RICH_INFO** en el parámetro _ulFlags_ , que hace que MAPI establecer esta propiedad en FALSE.</span><span class="sxs-lookup"><span data-stu-id="b41d8-128">A client calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) or a provider calling [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) can set the **MAPI_SEND_NO_RICH_INFO** bit in the  _ulFlags_ parameter, which causes MAPI to set this property to FALSE.</span></span> <span data-ttu-id="b41d8-129">Uso único creado por la interfaz de usuario use el valor especificado por la plantilla de creación.</span><span class="sxs-lookup"><span data-stu-id="b41d8-129">One-offs created by the user interface use the value specified by the creating template.</span></span> 
  
<span data-ttu-id="b41d8-130">En las llamadas al método [IAddrBook::ResolveName](iaddrbook-resolvename.md) cuando no se puede resolver el nombre, pero se puede interpretar como una dirección de Internet (SMTP), esta propiedad se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="b41d8-130">On calls to the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method when the name cannot be resolved but can be interpreted as an Internet address (SMTP), this property is set to FALSE.</span></span> <span data-ttu-id="b41d8-131">Para interpretarse como una dirección de Internet, debe ser el nombre para mostrar de la entrada sin resolver en el formato X@Y. Z, como "pete@pinecone.com".</span><span class="sxs-lookup"><span data-stu-id="b41d8-131">To be construed as an Internet address, the display name of the unresolved entry must be in the format X@Y.Z, such as "pete@pinecone.com".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b41d8-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b41d8-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b41d8-133">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b41d8-133">Protocol specifications</span></span>

<span data-ttu-id="b41d8-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b41d8-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b41d8-135">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b41d8-135">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b41d8-136">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b41d8-136">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b41d8-137">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="b41d8-137">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="b41d8-138">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b41d8-138">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b41d8-139">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b41d8-139">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="b41d8-140">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b41d8-140">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b41d8-141">en las convenciones de correo electrónico estándar de Internet para enviar mensajes a objetos.</span><span class="sxs-lookup"><span data-stu-id="b41d8-141">from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b41d8-142">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b41d8-142">Header files</span></span>

<span data-ttu-id="b41d8-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b41d8-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="b41d8-144">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b41d8-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="b41d8-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b41d8-145">Mapitags.h</span></span>
  
> <span data-ttu-id="b41d8-146">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="b41d8-146">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b41d8-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="b41d8-147">See also</span></span>



[<span data-ttu-id="b41d8-148">Propiedad canónica PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="b41d8-148">PidTagAttachDataObject Canonical Property</span></span>](pidtagattachdataobject-canonical-property.md)


[<span data-ttu-id="b41d8-149">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b41d8-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b41d8-150">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b41d8-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b41d8-151">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b41d8-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b41d8-152">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b41d8-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

