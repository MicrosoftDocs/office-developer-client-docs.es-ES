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
ms.openlocfilehash: c39fce40fb508370e62cb8b38123fa6ccc0e7d7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342633"
---
# <a name="pidtagsendersmtpaddress-canonical-property"></a><span data-ttu-id="03cf6-103">Propiedad canónica PidTagSenderSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="03cf6-103">PidTagSenderSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="03cf6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03cf6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03cf6-105">Contiene el formato de la dirección de correo electrónico del Protocolo simple de transferencia de correo (SMTP) del propietario del buzón de correo remitente.</span><span class="sxs-lookup"><span data-stu-id="03cf6-105">Contains the format of the Simple Mail Transport Protocol (SMTP) email address of the sending mailbox owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03cf6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="03cf6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03cf6-107">PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="03cf6-107">PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="03cf6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="03cf6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03cf6-109">0x5D01</span><span class="sxs-lookup"><span data-stu-id="03cf6-109">0x5D01</span></span>  <br/> |
|<span data-ttu-id="03cf6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="03cf6-110">Data type:</span></span>  <br/> |<span data-ttu-id="03cf6-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="03cf6-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="03cf6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="03cf6-112">Area:</span></span>  <br/> |<span data-ttu-id="03cf6-113">Address</span><span class="sxs-lookup"><span data-stu-id="03cf6-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03cf6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="03cf6-114">Remarks</span></span>

<span data-ttu-id="03cf6-115">Esta propiedad es un ejemplo de las propiedades de dirección del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="03cf6-115">This property is an example of the address properties for the message sender.</span></span> <span data-ttu-id="03cf6-116">Debe establecerlo el proveedor de transporte saliente, que nunca debe propagar los valores existentes previamente.</span><span class="sxs-lookup"><span data-stu-id="03cf6-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="03cf6-117">Si ningún proveedor de transporte ha proporcionado ninguna propiedad de dirección de remitente, la cola MAPI intenta rellenarla llamando al método [IMAPISession:: QueryIdentity](imapisession-queryidentity.md) para un identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="03cf6-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="03cf6-118">Si no se han proporcionado identificadores de entrada, la cola MAPI almacena "Unknown" en todas las propiedades de dirección del remitente de tipo PT_UNICODE o PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="03cf6-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_UNICODE or PT_STRING8.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="03cf6-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="03cf6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03cf6-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="03cf6-120">Protocol specifications</span></span>

<span data-ttu-id="03cf6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03cf6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03cf6-122">Proporciona referencias a especificaciones del Protocolo de Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="03cf6-122">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="03cf6-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03cf6-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03cf6-124">Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="03cf6-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="03cf6-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03cf6-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03cf6-126">Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="03cf6-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="03cf6-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03cf6-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03cf6-128">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="03cf6-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="03cf6-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03cf6-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03cf6-130">Especifica las propiedades y operaciones que se admiten para los objetos post.</span><span class="sxs-lookup"><span data-stu-id="03cf6-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="03cf6-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03cf6-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03cf6-132">Especifica las propiedades y operaciones que se admiten para los objetos de contacto y de lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="03cf6-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="03cf6-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03cf6-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03cf6-134">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="03cf6-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03cf6-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="03cf6-135">Header files</span></span>

<span data-ttu-id="03cf6-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="03cf6-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="03cf6-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="03cf6-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="03cf6-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="03cf6-138">Mapitags.h</span></span>
  
> <span data-ttu-id="03cf6-139">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="03cf6-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03cf6-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="03cf6-140">See also</span></span>



[<span data-ttu-id="03cf6-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="03cf6-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03cf6-142">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="03cf6-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03cf6-143">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="03cf6-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03cf6-144">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="03cf6-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

