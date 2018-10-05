---
title: Propiedad canónica PidTagSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 7a49b944-cef1-4642-9208-b137fd61171a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a9361f3027453742acbe50c3de01d860289cd0ed
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399546"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="d6df5-103">Propiedad canónica PidTagSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="d6df5-103">PidTagSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="d6df5-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6df5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6df5-105">Contiene la clave de búsqueda para el usuario de mensajería representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="d6df5-105">Contains the search key for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d6df5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d6df5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6df5-107">PR_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="d6df5-107">PR_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="d6df5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d6df5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6df5-109">0x003B</span><span class="sxs-lookup"><span data-stu-id="d6df5-109">0x003B</span></span>  <br/> |
|<span data-ttu-id="d6df5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d6df5-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6df5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d6df5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d6df5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d6df5-112">Area:</span></span>  <br/> |<span data-ttu-id="d6df5-113">Address</span><span class="sxs-lookup"><span data-stu-id="d6df5-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6df5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d6df5-114">Remarks</span></span>

<span data-ttu-id="d6df5-115">Esta propiedad es una de las propiedades de la dirección del usuario de mensajería que se va a representar por el remitente.</span><span class="sxs-lookup"><span data-stu-id="d6df5-115">This property is one of the address properties for the messaging user who is being represented by the sender.</span></span> <span data-ttu-id="d6df5-116">Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representado en los valores para que el cliente.</span><span class="sxs-lookup"><span data-stu-id="d6df5-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="d6df5-117">Un usuario de mensajería enviar en su propio nombre normalmente deja las propiedades de remitente representado no establecido.</span><span class="sxs-lookup"><span data-stu-id="d6df5-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="d6df5-118">El proveedor de transporte saliente siempre debe dejar esta propiedad no se modifica si se ha establecido por el cliente envío.</span><span class="sxs-lookup"><span data-stu-id="d6df5-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="d6df5-119">Si está establecido, el proveedor de transporte debe establecer para **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) en la copia del mensaje saliente y deje sin establecer en la copia local.</span><span class="sxs-lookup"><span data-stu-id="d6df5-119">If it is unset, the transport provider should set it to **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d6df5-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6df5-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6df5-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d6df5-121">Protocol specifications</span></span>

<span data-ttu-id="d6df5-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6df5-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6df5-123">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d6df5-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d6df5-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6df5-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6df5-125">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="d6df5-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="d6df5-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6df5-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6df5-127">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="d6df5-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="d6df5-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6df5-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6df5-129">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="d6df5-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="d6df5-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6df5-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6df5-131">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6df5-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="d6df5-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6df5-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6df5-133">Especifica las propiedades y operaciones que se permiten para registrar objetos.</span><span class="sxs-lookup"><span data-stu-id="d6df5-133">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="d6df5-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6df5-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6df5-135">Especifica las propiedades y operaciones que se permiten las listas de distribución de contactos y personal.</span><span class="sxs-lookup"><span data-stu-id="d6df5-135">Specifies the properties and operations that are permissible for contact and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6df5-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d6df5-136">Header files</span></span>

<span data-ttu-id="d6df5-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6df5-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6df5-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d6df5-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6df5-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d6df5-139">Mapitags.h</span></span>
  
> <span data-ttu-id="d6df5-140">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="d6df5-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6df5-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6df5-141">See also</span></span>



[<span data-ttu-id="d6df5-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d6df5-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6df5-143">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d6df5-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6df5-144">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d6df5-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6df5-145">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d6df5-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

