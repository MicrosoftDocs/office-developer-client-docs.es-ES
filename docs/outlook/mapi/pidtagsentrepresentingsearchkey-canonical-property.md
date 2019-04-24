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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356689"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="68de0-103">Propiedad canónica PidTagSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="68de0-103">PidTagSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="68de0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68de0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68de0-105">Contiene la clave de búsqueda para el usuario de mensajería representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="68de0-105">Contains the search key for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68de0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="68de0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="68de0-107">PR_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="68de0-107">PR_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="68de0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="68de0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="68de0-109">0x003B</span><span class="sxs-lookup"><span data-stu-id="68de0-109">0x003B</span></span>  <br/> |
|<span data-ttu-id="68de0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="68de0-110">Data type:</span></span>  <br/> |<span data-ttu-id="68de0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="68de0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="68de0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="68de0-112">Area:</span></span>  <br/> |<span data-ttu-id="68de0-113">Address</span><span class="sxs-lookup"><span data-stu-id="68de0-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68de0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="68de0-114">Remarks</span></span>

<span data-ttu-id="68de0-115">Esta propiedad es una de las propiedades de dirección para el usuario de mensajería representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="68de0-115">This property is one of the address properties for the messaging user who is being represented by the sender.</span></span> <span data-ttu-id="68de0-116">Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representadas en los valores de ese cliente.</span><span class="sxs-lookup"><span data-stu-id="68de0-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="68de0-117">Un usuario de mensajería que envía por su cuenta normalmente deja las propiedades de remitente representadas no establecidas.</span><span class="sxs-lookup"><span data-stu-id="68de0-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="68de0-118">El proveedor de transporte de salida siempre debe dejar esta propiedad sin cambios si el cliente de envío lo ha establecido.</span><span class="sxs-lookup"><span data-stu-id="68de0-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="68de0-119">Si está desactivada, el proveedor de transporte debe establecerla en **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) en la copia saliente del mensaje y dejarla sin establecer en la copia local.</span><span class="sxs-lookup"><span data-stu-id="68de0-119">If it is unset, the transport provider should set it to **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="68de0-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="68de0-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="68de0-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="68de0-121">Protocol specifications</span></span>

<span data-ttu-id="68de0-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68de0-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68de0-123">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="68de0-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="68de0-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68de0-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68de0-125">Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="68de0-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="68de0-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68de0-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68de0-127">Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="68de0-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="68de0-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68de0-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68de0-129">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="68de0-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="68de0-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68de0-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68de0-131">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="68de0-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="68de0-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68de0-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68de0-133">Especifica las propiedades y operaciones que se admiten para los objetos post.</span><span class="sxs-lookup"><span data-stu-id="68de0-133">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="68de0-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68de0-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68de0-135">Especifica las propiedades y operaciones que se admiten para las listas de distribución personales y de contacto.</span><span class="sxs-lookup"><span data-stu-id="68de0-135">Specifies the properties and operations that are permissible for contact and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="68de0-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="68de0-136">Header files</span></span>

<span data-ttu-id="68de0-137">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="68de0-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="68de0-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="68de0-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="68de0-139">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="68de0-139">Mapitags.h</span></span>
  
> <span data-ttu-id="68de0-140">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="68de0-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68de0-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="68de0-141">See also</span></span>



[<span data-ttu-id="68de0-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="68de0-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="68de0-143">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="68de0-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="68de0-144">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="68de0-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="68de0-145">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="68de0-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

