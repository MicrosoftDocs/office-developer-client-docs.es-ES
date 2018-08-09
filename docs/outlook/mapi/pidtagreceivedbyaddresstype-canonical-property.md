---
title: Propiedad canónica PidTagReceivedByAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByAddressType
api_type:
- COM
ms.assetid: 0eef299d-6923-4dae-9a18-91ea82ea0f3e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 96a53e427460990983242009500ade9ae0c5ada5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819998"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a><span data-ttu-id="f61c8-103">Propiedad canónica PidTagReceivedByAddressType</span><span class="sxs-lookup"><span data-stu-id="f61c8-103">PidTagReceivedByAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="f61c8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f61c8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f61c8-105">Contiene el tipo de dirección de correo electrónico, como SMTP, para el usuario de mensajería que reciba el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f61c8-105">Contains the email address type, such as SMTP, for the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f61c8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f61c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f61c8-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="f61c8-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="f61c8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f61c8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f61c8-109">0x0075</span><span class="sxs-lookup"><span data-stu-id="f61c8-109">0x0075</span></span>  <br/> |
|<span data-ttu-id="f61c8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f61c8-110">Data type:</span></span>  <br/> |<span data-ttu-id="f61c8-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f61c8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f61c8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f61c8-112">Area:</span></span>  <br/> |<span data-ttu-id="f61c8-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="f61c8-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f61c8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f61c8-114">Remarks</span></span>

<span data-ttu-id="f61c8-115">Estas propiedades son ejemplos de las propiedades de la dirección del usuario de mensajería que reciba el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f61c8-115">These properties are examples of the address properties for the messaging user who actually receives the message.</span></span> <span data-ttu-id="f61c8-116">Se deben configurar por el proveedor de transporte entrante.</span><span class="sxs-lookup"><span data-stu-id="f61c8-116">They must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="f61c8-117">La cadena de tipo de dirección puede contener sólo el A caracteres alfabéticos en mayúsculas a la Z y los números de cero a nueve.</span><span class="sxs-lookup"><span data-stu-id="f61c8-117">The address type string can contain only the uppercase alphabetic characters A through Z and the numbers zero through nine.</span></span> <span data-ttu-id="f61c8-118">Estas propiedades calificar la propiedad **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) mediante la especificación de un tipo de dirección, como SMTP, con lo que indica cómo se debe construir la dirección.</span><span class="sxs-lookup"><span data-stu-id="f61c8-118">These properties qualify the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property by specifying an address type, such as SMTP, thereby indicating how the address should be constructed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f61c8-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f61c8-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f61c8-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f61c8-120">Protocol specifications</span></span>

<span data-ttu-id="f61c8-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f61c8-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f61c8-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f61c8-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f61c8-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f61c8-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f61c8-124">Especifica las propiedades y operaciones que se permiten en mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f61c8-124">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f61c8-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f61c8-125">Header files</span></span>

<span data-ttu-id="f61c8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f61c8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f61c8-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f61c8-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="f61c8-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f61c8-128">Mapitags.h</span></span>
  
> <span data-ttu-id="f61c8-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f61c8-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f61c8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f61c8-130">See also</span></span>



[<span data-ttu-id="f61c8-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f61c8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f61c8-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f61c8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f61c8-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f61c8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f61c8-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f61c8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

