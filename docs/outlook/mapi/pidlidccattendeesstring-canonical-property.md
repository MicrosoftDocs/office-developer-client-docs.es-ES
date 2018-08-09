---
title: Propiedad canónica PidLidCcAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCcAttendeesString
api_type:
- COM
ms.assetid: 697d5c93-ec7f-4608-9866-9e249a093dbc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bb24d17e478de6b428750efb8d61797c8628b16d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818604"
---
# <a name="pidlidccattendeesstring-canonical-property"></a><span data-ttu-id="06e52-103">Propiedad canónica PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="06e52-103">PidLidCcAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="06e52-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06e52-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06e52-105">Contiene una lista de todos los asistentes que se puedan enviar que también son los asistentes opcionales.</span><span class="sxs-lookup"><span data-stu-id="06e52-105">Contains a list of all the sendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06e52-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="06e52-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06e52-107">dispidCCAttendeesString</span><span class="sxs-lookup"><span data-stu-id="06e52-107">dispidCCAttendeesString</span></span>  <br/> |
|<span data-ttu-id="06e52-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="06e52-108">Property set:</span></span>  <br/> |<span data-ttu-id="06e52-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="06e52-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="06e52-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="06e52-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="06e52-111">0x0000823C</span><span class="sxs-lookup"><span data-stu-id="06e52-111">0x0000823C</span></span>  <br/> |
|<span data-ttu-id="06e52-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="06e52-112">Data type:</span></span>  <br/> |<span data-ttu-id="06e52-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="06e52-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="06e52-114">Área:</span><span class="sxs-lookup"><span data-stu-id="06e52-114">Area:</span></span>  <br/> |<span data-ttu-id="06e52-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="06e52-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06e52-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="06e52-116">Remarks</span></span>

<span data-ttu-id="06e52-117">El valor para cada asistente es la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la libreta de direcciones del asistente.</span><span class="sxs-lookup"><span data-stu-id="06e52-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's address book.</span></span> <span data-ttu-id="06e52-118">Entradas independientes deben estar delimitadas por un punto y coma seguido de un espacio.</span><span class="sxs-lookup"><span data-stu-id="06e52-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="06e52-119">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="06e52-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="06e52-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="06e52-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="06e52-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="06e52-121">Protocol specifications</span></span>

<span data-ttu-id="06e52-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06e52-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06e52-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="06e52-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="06e52-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06e52-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06e52-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="06e52-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="06e52-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06e52-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06e52-127">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="06e52-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="06e52-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="06e52-128">Header files</span></span>

<span data-ttu-id="06e52-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06e52-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="06e52-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="06e52-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06e52-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="06e52-131">See also</span></span>



[<span data-ttu-id="06e52-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="06e52-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06e52-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="06e52-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06e52-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="06e52-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06e52-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="06e52-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

