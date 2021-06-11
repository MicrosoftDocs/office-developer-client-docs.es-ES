---
title: Propiedad canónica PidTagSentRepresentingEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingEmailAddress
api_type:
- COM
ms.assetid: 5fa4edde-475c-4568-946b-73eb08f97a61
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1b82e1e96a5ffbb5c17dd919e78a9f07342194c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341093"
---
# <a name="pidtagsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="a4cd6-103">Propiedad canónica PidTagSentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="a4cd6-103">PidTagSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="a4cd6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4cd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4cd6-105">Contiene la dirección de correo electrónico del usuario de mensajería representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-105">Contains the email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a4cd6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a4cd6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a4cd6-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="a4cd6-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="a4cd6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a4cd6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a4cd6-109">0x0065</span><span class="sxs-lookup"><span data-stu-id="a4cd6-109">0x0065</span></span>  <br/> |
|<span data-ttu-id="a4cd6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a4cd6-110">Data type:</span></span>  <br/> |<span data-ttu-id="a4cd6-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a4cd6-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a4cd6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a4cd6-112">Area:</span></span>  <br/> |<span data-ttu-id="a4cd6-113">Dirección</span><span class="sxs-lookup"><span data-stu-id="a4cd6-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4cd6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4cd6-114">Remarks</span></span>

<span data-ttu-id="a4cd6-115">Estas propiedades son ejemplos de las propiedades de dirección del usuario de mensajería que representa el remitente.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="a4cd6-116">Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representadas en los valores de ese cliente.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="a4cd6-117">Por lo general, un usuario de mensajería que envía en su propio nombre deja sin conjunto las propiedades del remitente representado.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="a4cd6-118">El proveedor de transporte saliente siempre debe dejar estas propiedades sin cambios si el cliente de envío lo ha establecido.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-118">The outgoing transport provider must always leave these properties unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="a4cd6-119">Si no se establece, el proveedor de transporte debe establecerlo en la propiedad **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) en la copia saliente del mensaje y dejarla sin establecer en la copia local.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-119">If it is unset, the transport provider should set it to the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a4cd6-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4cd6-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a4cd6-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="a4cd6-121">Protocol specifications</span></span>

<span data-ttu-id="a4cd6-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4cd6-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4cd6-123">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a4cd6-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4cd6-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4cd6-125">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="a4cd6-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4cd6-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4cd6-127">Especifica las propiedades y las operaciones que representan elementos RSS.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="a4cd6-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4cd6-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4cd6-129">Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="a4cd6-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4cd6-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4cd6-131">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="a4cd6-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4cd6-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4cd6-133">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="a4cd6-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4cd6-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4cd6-135">Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="a4cd6-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4cd6-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4cd6-137">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficiente.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a4cd6-138">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a4cd6-138">Header files</span></span>

<span data-ttu-id="a4cd6-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a4cd6-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="a4cd6-140">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="a4cd6-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a4cd6-141">Mapitags.h</span></span>
  
> <span data-ttu-id="a4cd6-142">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a4cd6-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4cd6-143">See also</span></span>



[<span data-ttu-id="a4cd6-144">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a4cd6-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a4cd6-145">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a4cd6-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a4cd6-146">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a4cd6-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a4cd6-147">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="a4cd6-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

