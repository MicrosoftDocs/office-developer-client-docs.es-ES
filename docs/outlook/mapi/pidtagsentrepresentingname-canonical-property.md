---
title: Propiedad canónico PidTagSentRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: bfee6c5e-d4c6-442e-af71-23156569fed5
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 5417b73fe13937a74bc01520a2dd9db359e894ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820288"
---
# <a name="pidtagsentrepresentingname-canonical-property"></a><span data-ttu-id="6944b-103">Propiedad canónico PidTagSentRepresentingName</span><span class="sxs-lookup"><span data-stu-id="6944b-103">PidTagSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="6944b-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6944b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6944b-105">Contiene el nombre para mostrar para el usuario de mensajería representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="6944b-105">Contains the display name for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6944b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6944b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6944b-107">PR_SENT_REPRESENTING_NAME DE MAPI, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="6944b-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="6944b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6944b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6944b-109">0x0042</span><span class="sxs-lookup"><span data-stu-id="6944b-109">0x0042</span></span>  <br/> |
|<span data-ttu-id="6944b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6944b-110">Data type:</span></span>  <br/> |<span data-ttu-id="6944b-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="6944b-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="6944b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6944b-112">Area:</span></span>  <br/> |<span data-ttu-id="6944b-113">Address</span><span class="sxs-lookup"><span data-stu-id="6944b-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6944b-114">Notas</span><span class="sxs-lookup"><span data-stu-id="6944b-114">Remarks</span></span>

<span data-ttu-id="6944b-115">Estas propiedades son ejemplos de las propiedades de dirección para el usuario de mensajería que se está representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="6944b-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="6944b-116">Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representado en los valores para que el cliente.</span><span class="sxs-lookup"><span data-stu-id="6944b-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="6944b-117">Un usuario de mensajería enviar en su propio nombre normalmente deja las propiedades de remitente representado no establecido.</span><span class="sxs-lookup"><span data-stu-id="6944b-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="6944b-118">El proveedor de transporte saliente siempre debe dejar esta propiedad no se modifica si se ha establecido por el cliente envío.</span><span class="sxs-lookup"><span data-stu-id="6944b-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="6944b-119">Si está establecido, el proveedor de transporte debe establecer para **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) en la copia del mensaje saliente y deje sin establecer en la copia local.</span><span class="sxs-lookup"><span data-stu-id="6944b-119">If it is unset, the transport provider should set it to **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6944b-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6944b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6944b-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6944b-121">Protocol specifications</span></span>

<span data-ttu-id="6944b-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6944b-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6944b-123">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6944b-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6944b-124">[[MS-OXOMSG]](http://msdn.microsoft.com/es-es/library/cc433482%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6944b-124">[[MS-OXOMSG]](http://msdn.microsoft.com/es-es/library/cc433482%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="6944b-125">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="6944b-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="6944b-126">[[MS-OXORSS]](http://msdn.microsoft.com/es-es/library/cc463884%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6944b-126">[[MS-OXORSS]](http://msdn.microsoft.com/es-es/library/cc463884%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="6944b-127">Especifica las propiedades y operaciones que representan elementos RSS.</span><span class="sxs-lookup"><span data-stu-id="6944b-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="6944b-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6944b-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6944b-129">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="6944b-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="6944b-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6944b-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6944b-131">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="6944b-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="6944b-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6944b-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6944b-133">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="6944b-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="6944b-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6944b-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6944b-135">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="6944b-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="6944b-136">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6944b-136">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6944b-137">Especifica la ubicación y las propiedades de datos de configuración de cliente y servidor, como las listas de categoría compartida y horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6944b-137">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="6944b-138">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6944b-138">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6944b-139">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="6944b-139">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="6944b-140">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6944b-140">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6944b-141">Especifica las propiedades y operaciones que se permiten para registrar objetos.</span><span class="sxs-lookup"><span data-stu-id="6944b-141">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="6944b-142">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6944b-142">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6944b-143">Especifica las propiedades y operaciones que se permiten para el contacto y objetos de lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="6944b-143">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="6944b-144">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6944b-144">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6944b-145">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="6944b-145">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6944b-146">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6944b-146">Header files</span></span>

<span data-ttu-id="6944b-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6944b-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="6944b-148">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6944b-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="6944b-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6944b-149">Mapitags.h</span></span>
  
> <span data-ttu-id="6944b-150">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="6944b-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6944b-151">Ver también</span><span class="sxs-lookup"><span data-stu-id="6944b-151">See also</span></span>



[<span data-ttu-id="6944b-152">Propiedad canónico PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="6944b-152">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="6944b-153">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6944b-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6944b-154">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6944b-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6944b-155">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="6944b-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6944b-156">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="6944b-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

