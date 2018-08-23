---
title: Propiedad canónica PidTagSenderSmtpAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 321cde5a-05db-498b-a9b8-cb54c8a14e34
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 10444131248edea2de712429d7c70a8490eb31ff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584726"
---
# <a name="pidtagsendersmtpaddress-canonical-property"></a><span data-ttu-id="64135-103">Propiedad canónica PidTagSenderSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="64135-103">PidTagSenderSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="64135-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64135-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64135-105">Contiene el formato de la dirección de correo electrónico de Protocolo Simple de transferencia de correo (SMTP) del propietario del buzón de envío.</span><span class="sxs-lookup"><span data-stu-id="64135-105">Contains the format of the Simple Mail Transport Protocol (SMTP) email address of the sending mailbox owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64135-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="64135-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64135-107">PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="64135-107">PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="64135-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="64135-108">Identifier:</span></span>  <br/> |<span data-ttu-id="64135-109">0x5D01</span><span class="sxs-lookup"><span data-stu-id="64135-109">0x5D01</span></span>  <br/> |
|<span data-ttu-id="64135-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="64135-110">Data type:</span></span>  <br/> |<span data-ttu-id="64135-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="64135-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="64135-112">Área:</span><span class="sxs-lookup"><span data-stu-id="64135-112">Area:</span></span>  <br/> |<span data-ttu-id="64135-113">Address</span><span class="sxs-lookup"><span data-stu-id="64135-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64135-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="64135-114">Remarks</span></span>

<span data-ttu-id="64135-115">Esta propiedad es un ejemplo de las propiedades de direcciones para el remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="64135-115">This property is an example of the address properties for the message sender.</span></span> <span data-ttu-id="64135-116">Se debe establecer por el proveedor de transporte saliente, que nunca se debe propagar los valores existentes anteriormente.</span><span class="sxs-lookup"><span data-stu-id="64135-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="64135-117">Si no hay proveedor de transporte ha proporcionado las propiedades de dirección del remitente, la cola MAPI intenta rellenar llamando al método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para obtener un identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="64135-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="64135-118">Si se han proporcionado sin los identificadores de entrada, la cola MAPI almacena a "Unknown" en todas las propiedades de dirección de remitente del tipo PT_UNICODE o PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="64135-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_UNICODE or PT_STRING8.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="64135-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="64135-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64135-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="64135-120">Protocol specifications</span></span>

<span data-ttu-id="64135-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64135-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64135-122">Proporciona referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="64135-122">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="64135-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64135-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64135-124">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="64135-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="64135-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64135-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64135-126">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="64135-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="64135-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64135-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64135-128">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="64135-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="64135-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64135-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64135-130">Especifica las propiedades y operaciones que se permiten para registrar objetos.</span><span class="sxs-lookup"><span data-stu-id="64135-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="64135-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64135-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64135-132">Especifica las propiedades y operaciones que se permiten para el contacto y objetos de lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="64135-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="64135-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64135-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64135-134">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="64135-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64135-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="64135-135">Header files</span></span>

<span data-ttu-id="64135-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64135-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="64135-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="64135-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="64135-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="64135-138">Mapitags.h</span></span>
  
> <span data-ttu-id="64135-139">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="64135-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64135-140">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="64135-140">See also</span></span>



[<span data-ttu-id="64135-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="64135-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64135-142">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="64135-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64135-143">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="64135-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64135-144">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="64135-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

