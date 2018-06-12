---
title: Propiedad canónico PidLidCcAttendeesString
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: bb24d17e478de6b428750efb8d61797c8628b16d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818604"
---
# <a name="pidlidccattendeesstring-canonical-property"></a><span data-ttu-id="6885a-103">Propiedad canónico PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="6885a-103">PidLidCcAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="6885a-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6885a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6885a-105">Contiene una lista de todos los asistentes que se puedan enviar que también son los asistentes opcionales.</span><span class="sxs-lookup"><span data-stu-id="6885a-105">Contains a list of all the sendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6885a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6885a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6885a-107">dispidCCAttendeesString</span><span class="sxs-lookup"><span data-stu-id="6885a-107">dispidCCAttendeesString</span></span>  <br/> |
|<span data-ttu-id="6885a-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="6885a-108">Property set:</span></span>  <br/> |<span data-ttu-id="6885a-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="6885a-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="6885a-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="6885a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6885a-111">0x0000823C</span><span class="sxs-lookup"><span data-stu-id="6885a-111">0x0000823C</span></span>  <br/> |
|<span data-ttu-id="6885a-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6885a-112">Data type:</span></span>  <br/> |<span data-ttu-id="6885a-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6885a-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6885a-114">Área:</span><span class="sxs-lookup"><span data-stu-id="6885a-114">Area:</span></span>  <br/> |<span data-ttu-id="6885a-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="6885a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6885a-116">Notas</span><span class="sxs-lookup"><span data-stu-id="6885a-116">Remarks</span></span>

<span data-ttu-id="6885a-117">El valor para cada asistente es la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la libreta de direcciones del asistente.</span><span class="sxs-lookup"><span data-stu-id="6885a-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's address book.</span></span> <span data-ttu-id="6885a-118">Entradas independientes deben estar delimitadas por un punto y coma seguido de un espacio.</span><span class="sxs-lookup"><span data-stu-id="6885a-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="6885a-119">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="6885a-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6885a-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6885a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6885a-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6885a-121">Protocol specifications</span></span>

<span data-ttu-id="6885a-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6885a-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6885a-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6885a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6885a-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6885a-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6885a-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="6885a-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="6885a-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6885a-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6885a-127">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="6885a-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6885a-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6885a-128">Header files</span></span>

<span data-ttu-id="6885a-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6885a-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="6885a-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6885a-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6885a-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="6885a-131">See also</span></span>



[<span data-ttu-id="6885a-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6885a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6885a-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6885a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6885a-134">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="6885a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6885a-135">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="6885a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

