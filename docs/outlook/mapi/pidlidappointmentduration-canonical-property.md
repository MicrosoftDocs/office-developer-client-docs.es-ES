---
title: Propiedad canónica PidLidAppointmentDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentDuration
api_type:
- COM
ms.assetid: 92c07a81-9dec-4118-af1f-02ecad340f07
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8ce9df6290fe6e50e52c632f0a14f226c4d715d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345398"
---
# <a name="pidlidappointmentduration-canonical-property"></a><span data-ttu-id="69faa-103">Propiedad canónica PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="69faa-103">PidLidAppointmentDuration Canonical Property</span></span>

  
  
<span data-ttu-id="69faa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69faa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69faa-105">Representa la cantidad de tiempo, en minutos, cuando se programa una cita.</span><span class="sxs-lookup"><span data-stu-id="69faa-105">Represents the length of time, in minutes, when an appointment is scheduled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69faa-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="69faa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69faa-107">dispidApptDuration</span><span class="sxs-lookup"><span data-stu-id="69faa-107">dispidApptDuration</span></span>  <br/> |
|<span data-ttu-id="69faa-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="69faa-108">Property set:</span></span>  <br/> |<span data-ttu-id="69faa-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="69faa-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="69faa-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="69faa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="69faa-111">0x00008213</span><span class="sxs-lookup"><span data-stu-id="69faa-111">0x00008213</span></span>  <br/> |
|<span data-ttu-id="69faa-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="69faa-112">Data type:</span></span>  <br/> |<span data-ttu-id="69faa-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="69faa-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="69faa-114">Área:</span><span class="sxs-lookup"><span data-stu-id="69faa-114">Area:</span></span>  <br/> |<span data-ttu-id="69faa-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="69faa-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69faa-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69faa-116">Remarks</span></span>

<span data-ttu-id="69faa-117">El valor debe ser el número de minutos entre el valor de las propiedades **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) y **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="69faa-117">The value must be the number of minutes between the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) and the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="69faa-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="69faa-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69faa-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="69faa-119">Protocol specifications</span></span>

<span data-ttu-id="69faa-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69faa-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69faa-121">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="69faa-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69faa-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69faa-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69faa-123">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="69faa-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69faa-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="69faa-124">Header files</span></span>

<span data-ttu-id="69faa-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="69faa-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="69faa-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="69faa-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69faa-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="69faa-127">See also</span></span>



[<span data-ttu-id="69faa-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="69faa-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69faa-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="69faa-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69faa-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="69faa-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69faa-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="69faa-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

