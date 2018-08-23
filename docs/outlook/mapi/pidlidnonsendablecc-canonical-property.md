---
title: Propiedad canónica PidLidNonSendableCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableCc
api_type:
- COM
ms.assetid: 170afe1f-1223-4689-825c-d21ab14b213b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 76ea38db86f678c250016c2f5e2feea3a173bb5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589388"
---
# <a name="pidlidnonsendablecc-canonical-property"></a><span data-ttu-id="5073d-103">Propiedad canónica PidLidNonSendableCc</span><span class="sxs-lookup"><span data-stu-id="5073d-103">PidLidNonSendableCc Canonical Property</span></span>

  
  
<span data-ttu-id="5073d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5073d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5073d-105">Contiene una lista de todos los asistentes compuestas que también son los asistentes opcionales.</span><span class="sxs-lookup"><span data-stu-id="5073d-105">Contains a list of all the unsendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5073d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5073d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5073d-107">dispidNonSendableCC</span><span class="sxs-lookup"><span data-stu-id="5073d-107">dispidNonSendableCC</span></span>  <br/> |
|<span data-ttu-id="5073d-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="5073d-108">Property set:</span></span>  <br/> |<span data-ttu-id="5073d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5073d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5073d-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="5073d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5073d-111">0x00008537</span><span class="sxs-lookup"><span data-stu-id="5073d-111">0x00008537</span></span>  <br/> |
|<span data-ttu-id="5073d-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5073d-112">Data type:</span></span>  <br/> |<span data-ttu-id="5073d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5073d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5073d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5073d-114">Area:</span></span>  <br/> |<span data-ttu-id="5073d-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="5073d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5073d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5073d-116">Remarks</span></span>

<span data-ttu-id="5073d-117">El valor para cada asistente es la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la libreta de direcciones del asistente.</span><span class="sxs-lookup"><span data-stu-id="5073d-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="5073d-118">Entradas independientes deben estar delimitadas por un punto y coma seguido de un espacio.</span><span class="sxs-lookup"><span data-stu-id="5073d-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="5073d-119">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="5073d-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5073d-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5073d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5073d-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5073d-121">Protocol specifications</span></span>

<span data-ttu-id="5073d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5073d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5073d-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5073d-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5073d-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5073d-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5073d-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="5073d-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="5073d-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5073d-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5073d-127">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="5073d-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5073d-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5073d-128">Header files</span></span>

<span data-ttu-id="5073d-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5073d-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="5073d-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5073d-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5073d-131">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5073d-131">See also</span></span>



[<span data-ttu-id="5073d-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5073d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5073d-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5073d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5073d-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5073d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5073d-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5073d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

