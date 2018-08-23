---
title: Propiedad canónica PidTagSenderSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderSearchKey
api_type:
- COM
ms.assetid: e15599c5-f40f-46a6-a726-7359efd09ff8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3f73f1ef919bab15a8f89b7fddc43608411635e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573456"
---
# <a name="pidtagsendersearchkey-canonical-property"></a><span data-ttu-id="1b63d-103">Propiedad canónica PidTagSenderSearchKey</span><span class="sxs-lookup"><span data-stu-id="1b63d-103">PidTagSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="1b63d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b63d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b63d-105">Contiene la clave de búsqueda de la dirección del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1b63d-105">Contains the message sender's search key.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b63d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1b63d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b63d-107">PR_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="1b63d-107">PR_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="1b63d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1b63d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b63d-109">0x0C1D</span><span class="sxs-lookup"><span data-stu-id="1b63d-109">0x0C1D</span></span>  <br/> |
|<span data-ttu-id="1b63d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1b63d-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b63d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1b63d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1b63d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1b63d-112">Area:</span></span>  <br/> |<span data-ttu-id="1b63d-113">Address</span><span class="sxs-lookup"><span data-stu-id="1b63d-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b63d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1b63d-114">Remarks</span></span>

<span data-ttu-id="1b63d-115">Esta propiedad es una de las propiedades de direcciones para el remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1b63d-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="1b63d-116">Se debe establecer por el proveedor de transporte saliente, que nunca se debe propagar los valores existentes anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1b63d-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="1b63d-117">Si no hay proveedor de transporte ha proporcionado las propiedades de dirección del remitente, la cola MAPI intenta rellenar llamando al método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para obtener un identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="1b63d-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="1b63d-118">Si se han proporcionado sin los identificadores de entrada, la cola MAPI almacena una clave correspondiente a la cadena "Unknown" en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="1b63d-118">If no entry identifiers have been provided, the MAPI spooler stores a key corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1b63d-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b63d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1b63d-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1b63d-120">Protocol specifications</span></span>

<span data-ttu-id="1b63d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b63d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b63d-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1b63d-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1b63d-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b63d-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b63d-124">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1b63d-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="1b63d-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b63d-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b63d-126">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="1b63d-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="1b63d-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b63d-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b63d-128">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="1b63d-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="1b63d-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b63d-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b63d-130">Especifica las propiedades y operaciones que se permiten para registrar objetos.</span><span class="sxs-lookup"><span data-stu-id="1b63d-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="1b63d-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b63d-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b63d-132">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="1b63d-132">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="1b63d-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b63d-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b63d-134">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="1b63d-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1b63d-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1b63d-135">Header files</span></span>

<span data-ttu-id="1b63d-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b63d-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b63d-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1b63d-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b63d-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1b63d-138">Mapitags.h</span></span>
  
> <span data-ttu-id="1b63d-139">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="1b63d-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b63d-140">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1b63d-140">See also</span></span>



[<span data-ttu-id="1b63d-141">Propiedad canónica PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="1b63d-141">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)
  
[<span data-ttu-id="1b63d-142">Propiedad canónica PidTagSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="1b63d-142">PidTagSentRepresentingSearchKey Canonical Property</span></span>](pidtagsentrepresentingsearchkey-canonical-property.md)


[<span data-ttu-id="1b63d-143">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1b63d-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b63d-144">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1b63d-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b63d-145">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1b63d-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b63d-146">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1b63d-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

