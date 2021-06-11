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
ms.openlocfilehash: 12cdbfcc140fb5ea3bb15a2db93f3689923d9390
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344971"
---
# <a name="pidlidccattendeesstring-canonical-property"></a><span data-ttu-id="09c04-103">Propiedad canónica PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="09c04-103">PidLidCcAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="09c04-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09c04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09c04-105">Contiene una lista de todos los asistentes que se pueden enviar que también son asistentes opcionales.</span><span class="sxs-lookup"><span data-stu-id="09c04-105">Contains a list of all the sendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="09c04-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="09c04-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="09c04-107">dispidCCAttendeesString</span><span class="sxs-lookup"><span data-stu-id="09c04-107">dispidCCAttendeesString</span></span>  <br/> |
|<span data-ttu-id="09c04-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="09c04-108">Property set:</span></span>  <br/> |<span data-ttu-id="09c04-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="09c04-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="09c04-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="09c04-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="09c04-111">0x0000823C</span><span class="sxs-lookup"><span data-stu-id="09c04-111">0x0000823C</span></span>  <br/> |
|<span data-ttu-id="09c04-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="09c04-112">Data type:</span></span>  <br/> |<span data-ttu-id="09c04-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="09c04-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="09c04-114">Área:</span><span class="sxs-lookup"><span data-stu-id="09c04-114">Area:</span></span>  <br/> |<span data-ttu-id="09c04-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="09c04-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09c04-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09c04-116">Remarks</span></span>

<span data-ttu-id="09c04-117">El valor de cada asistente es **la propiedad PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la libreta de direcciones del asistente.</span><span class="sxs-lookup"><span data-stu-id="09c04-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's address book.</span></span> <span data-ttu-id="09c04-118">Las entradas independientes deben delimitarse por un punto y coma seguido de un espacio.</span><span class="sxs-lookup"><span data-stu-id="09c04-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="09c04-119">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="09c04-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="09c04-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="09c04-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="09c04-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="09c04-121">Protocol specifications</span></span>

<span data-ttu-id="09c04-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09c04-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09c04-123">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="09c04-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="09c04-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09c04-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09c04-125">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="09c04-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="09c04-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09c04-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09c04-127">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="09c04-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="09c04-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="09c04-128">Header files</span></span>

<span data-ttu-id="09c04-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="09c04-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="09c04-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="09c04-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="09c04-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="09c04-131">See also</span></span>



[<span data-ttu-id="09c04-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="09c04-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="09c04-133">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="09c04-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="09c04-134">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="09c04-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="09c04-135">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="09c04-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

