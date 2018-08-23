---
title: Propiedad canónica PidLidAllAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAllAttendeesString
api_type:
- COM
ms.assetid: 2ffc0609-341d-4e35-8f53-ed3096c6fa7f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 11b4ea96283bbef2dcb9afb109a6a81102727efc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570460"
---
# <a name="pidlidallattendeesstring-canonical-property"></a><span data-ttu-id="de960-103">Propiedad canónica PidLidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="de960-103">PidLidAllAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="de960-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de960-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de960-105">Especifica una lista de todos los asistentes, excepto el organizador, incluyendo recursos y no se puede enviar a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="de960-105">Specifies a list of all the attendees except for the organizer, including resources and unsendable attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de960-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="de960-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de960-107">dispidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="de960-107">dispidAllAttendeesString</span></span>  <br/> |
|<span data-ttu-id="de960-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="de960-108">Property set:</span></span>  <br/> |<span data-ttu-id="de960-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="de960-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="de960-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="de960-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="de960-111">0x00008238</span><span class="sxs-lookup"><span data-stu-id="de960-111">0x00008238</span></span>  <br/> |
|<span data-ttu-id="de960-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="de960-112">Data type:</span></span>  <br/> |<span data-ttu-id="de960-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="de960-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="de960-114">Área:</span><span class="sxs-lookup"><span data-stu-id="de960-114">Area:</span></span>  <br/> |<span data-ttu-id="de960-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="de960-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de960-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de960-116">Remarks</span></span>

<span data-ttu-id="de960-117">El valor para cada asistente es el nombre del Asistente para mostrar.</span><span class="sxs-lookup"><span data-stu-id="de960-117">The value for each attendee is the attendee's display name.</span></span> <span data-ttu-id="de960-118">Entradas independientes deben estar delimitadas por un punto y coma seguido de un espacio.</span><span class="sxs-lookup"><span data-stu-id="de960-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="de960-119">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="de960-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="de960-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="de960-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de960-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="de960-121">Protocol specifications</span></span>

<span data-ttu-id="de960-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de960-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de960-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="de960-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="de960-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de960-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de960-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="de960-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="de960-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="de960-126">Header files</span></span>

<span data-ttu-id="de960-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de960-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="de960-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="de960-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de960-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="de960-129">See also</span></span>



[<span data-ttu-id="de960-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="de960-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de960-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="de960-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de960-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="de960-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de960-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="de960-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

