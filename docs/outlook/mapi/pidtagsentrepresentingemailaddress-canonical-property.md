---
title: Propiedad canónico PidTagSentRepresentingEmailAddress
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 1ed8797a9f9de223d8ec15bc0eae963ff1e93be4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820278"
---
# <a name="pidtagsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="049d4-103">Propiedad canónico PidTagSentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="049d4-103">PidTagSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="049d4-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="049d4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="049d4-105">Contiene la dirección de correo electrónico del usuario de mensajería que está representada por el remitente.</span><span class="sxs-lookup"><span data-stu-id="049d4-105">Contains the email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="049d4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="049d4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="049d4-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="049d4-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="049d4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="049d4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="049d4-109">0 x 0065</span><span class="sxs-lookup"><span data-stu-id="049d4-109">0x0065</span></span>  <br/> |
|<span data-ttu-id="049d4-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="049d4-110">Data type:</span></span>  <br/> |<span data-ttu-id="049d4-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="049d4-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="049d4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="049d4-112">Area:</span></span>  <br/> |<span data-ttu-id="049d4-113">Address</span><span class="sxs-lookup"><span data-stu-id="049d4-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="049d4-114">Notas</span><span class="sxs-lookup"><span data-stu-id="049d4-114">Remarks</span></span>

<span data-ttu-id="049d4-115">Estas propiedades son ejemplos de las propiedades de dirección para el usuario de mensajería que se está representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="049d4-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="049d4-116">Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representado en los valores para que el cliente.</span><span class="sxs-lookup"><span data-stu-id="049d4-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="049d4-117">Un usuario de mensajería enviar en su propio nombre normalmente deja las propiedades de remitente representado no establecido.</span><span class="sxs-lookup"><span data-stu-id="049d4-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="049d4-118">El proveedor de transporte saliente siempre debe dejar estas propiedades no se modifica si se ha establecido por el cliente envío.</span><span class="sxs-lookup"><span data-stu-id="049d4-118">The outgoing transport provider must always leave these properties unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="049d4-119">Si está establecido, el proveedor de transporte debe establecer para la propiedad **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) en la copia del mensaje saliente y deje sin establecer en la copia local.</span><span class="sxs-lookup"><span data-stu-id="049d4-119">If it is unset, the transport provider should set it to the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="049d4-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="049d4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="049d4-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="049d4-121">Protocol specifications</span></span>

<span data-ttu-id="049d4-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="049d4-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="049d4-123">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="049d4-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="049d4-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="049d4-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="049d4-125">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="049d4-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="049d4-126">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="049d4-126">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="049d4-127">Especifica las propiedades y operaciones que representan elementos RSS.</span><span class="sxs-lookup"><span data-stu-id="049d4-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="049d4-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="049d4-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="049d4-129">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="049d4-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="049d4-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="049d4-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="049d4-131">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="049d4-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="049d4-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="049d4-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="049d4-133">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="049d4-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="049d4-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="049d4-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="049d4-135">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="049d4-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="049d4-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="049d4-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="049d4-137">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="049d4-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="049d4-138">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="049d4-138">Header files</span></span>

<span data-ttu-id="049d4-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="049d4-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="049d4-140">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="049d4-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="049d4-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="049d4-141">Mapitags.h</span></span>
  
> <span data-ttu-id="049d4-142">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="049d4-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="049d4-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="049d4-143">See also</span></span>



[<span data-ttu-id="049d4-144">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="049d4-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="049d4-145">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="049d4-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="049d4-146">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="049d4-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="049d4-147">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="049d4-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

