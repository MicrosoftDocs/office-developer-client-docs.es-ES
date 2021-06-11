---
title: Propiedad canónica PidLidCalendarType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCalendarType
api_type:
- COM
ms.assetid: 06e066f1-2b7d-4a6b-b88c-85a9bfa83bd3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6a33559a3e047890153f6a8e0ab40e49c2bf80cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341996"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="84bfd-103">Propiedad canónica PidLidCalendarType</span><span class="sxs-lookup"><span data-stu-id="84bfd-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="84bfd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84bfd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84bfd-105">Especifica el valor del campo CalendarType de la **propiedad dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="84bfd-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84bfd-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="84bfd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84bfd-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="84bfd-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="84bfd-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="84bfd-108">Property set:</span></span>  <br/> |<span data-ttu-id="84bfd-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="84bfd-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="84bfd-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="84bfd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="84bfd-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="84bfd-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="84bfd-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="84bfd-112">Data type:</span></span>  <br/> |<span data-ttu-id="84bfd-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="84bfd-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="84bfd-114">Área:</span><span class="sxs-lookup"><span data-stu-id="84bfd-114">Area:</span></span>  <br/> |<span data-ttu-id="84bfd-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="84bfd-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84bfd-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84bfd-116">Remarks</span></span>

<span data-ttu-id="84bfd-117">Cuando la solicitud de reunión representa una serie periódica o una excepción, este es el valor del campo CalendarType de la **propiedad dispidApptRecur.**</span><span class="sxs-lookup"><span data-stu-id="84bfd-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="84bfd-118">De lo contrario, esta propiedad no se establece y se supone que es 0.</span><span class="sxs-lookup"><span data-stu-id="84bfd-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="84bfd-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="84bfd-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84bfd-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="84bfd-120">Protocol specifications</span></span>

<span data-ttu-id="84bfd-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84bfd-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84bfd-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="84bfd-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="84bfd-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84bfd-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84bfd-124">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="84bfd-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84bfd-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="84bfd-125">Header files</span></span>

<span data-ttu-id="84bfd-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84bfd-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="84bfd-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="84bfd-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84bfd-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="84bfd-128">See also</span></span>



[<span data-ttu-id="84bfd-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="84bfd-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84bfd-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="84bfd-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84bfd-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="84bfd-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84bfd-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="84bfd-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

