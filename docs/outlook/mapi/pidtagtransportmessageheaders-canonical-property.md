---
title: Propiedad canónica PidTagTransportMessageHeaders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransportMessageHeaders
api_type:
- COM
ms.assetid: 9f8e3f20-6454-4dfd-9b35-e0401abac6b3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7ad9048a19123b94c10afaddcbedb7f54e8fe477
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392352"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a><span data-ttu-id="b9eeb-103">Propiedad canónica PidTagTransportMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="b9eeb-103">PidTagTransportMessageHeaders Canonical Property</span></span>

  
  
<span data-ttu-id="b9eeb-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9eeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9eeb-105">Contiene información de sobre de mensaje específica de transporte.</span><span class="sxs-lookup"><span data-stu-id="b9eeb-105">Contains transport-specific message envelope information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9eeb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b9eeb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b9eeb-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span><span class="sxs-lookup"><span data-stu-id="b9eeb-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span></span>  <br/> |
|<span data-ttu-id="b9eeb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b9eeb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b9eeb-109">0x007D</span><span class="sxs-lookup"><span data-stu-id="b9eeb-109">0x007D</span></span>  <br/> |
|<span data-ttu-id="b9eeb-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b9eeb-110">Data type:</span></span>  <br/> |<span data-ttu-id="b9eeb-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b9eeb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b9eeb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b9eeb-112">Area:</span></span>  <br/> |<span data-ttu-id="b9eeb-113">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="b9eeb-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9eeb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b9eeb-114">Remarks</span></span>

<span data-ttu-id="b9eeb-115">El proveedor de transporte puede generar la información de encabezado de mensaje para los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="b9eeb-115">The transport provider can generate the message header information for inbound messages.</span></span>
  
<span data-ttu-id="b9eeb-116">Estas propiedades ofrecen una alternativa a descarta la información de encabezado de mensaje de transporte o anteponiendo para el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b9eeb-116">These properties offer an alternative to either discarding the transport message header information or prepending it to the message text.</span></span> <span data-ttu-id="b9eeb-117">El cliente puede elegir si desea o no mostrar la información.</span><span class="sxs-lookup"><span data-stu-id="b9eeb-117">The client can choose whether or not to display the information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b9eeb-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9eeb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b9eeb-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b9eeb-119">Protocol specifications</span></span>

<span data-ttu-id="b9eeb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9eeb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9eeb-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b9eeb-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b9eeb-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9eeb-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9eeb-123">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b9eeb-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="b9eeb-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9eeb-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9eeb-125">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b9eeb-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b9eeb-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b9eeb-126">Header files</span></span>

<span data-ttu-id="b9eeb-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9eeb-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b9eeb-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b9eeb-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="b9eeb-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b9eeb-129">Mapitags.h</span></span>
  
> <span data-ttu-id="b9eeb-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b9eeb-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9eeb-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9eeb-131">See also</span></span>



[<span data-ttu-id="b9eeb-132">Propiedad canónica PidTagBody</span><span class="sxs-lookup"><span data-stu-id="b9eeb-132">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)


[<span data-ttu-id="b9eeb-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b9eeb-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b9eeb-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b9eeb-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b9eeb-135">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b9eeb-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b9eeb-136">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b9eeb-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

