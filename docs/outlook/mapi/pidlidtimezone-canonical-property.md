---
title: Propiedad canónica PidLidTimeZone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5eb9842da78541bc8c73cd5b2c52abeb927f9031
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819015"
---
# <a name="pidlidtimezone-canonical-property"></a><span data-ttu-id="29d58-103">Propiedad canónica PidLidTimeZone</span><span class="sxs-lookup"><span data-stu-id="29d58-103">PidLidTimeZone Canonical Property</span></span>

  
  
<span data-ttu-id="29d58-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="29d58-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="29d58-105">Especifica información acerca de la zona horaria de una reunión periódica.</span><span class="sxs-lookup"><span data-stu-id="29d58-105">Specifies information about the time zone of a recurring meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="29d58-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="29d58-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="29d58-107">LID_TIME_ZONE</span><span class="sxs-lookup"><span data-stu-id="29d58-107">LID_TIME_ZONE</span></span>  <br/> |
|<span data-ttu-id="29d58-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="29d58-108">Property set:</span></span>  <br/> |<span data-ttu-id="29d58-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="29d58-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="29d58-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="29d58-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="29d58-111">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="29d58-111">0x0000000C</span></span>  <br/> |
|<span data-ttu-id="29d58-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="29d58-112">Data type:</span></span>  <br/> |<span data-ttu-id="29d58-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="29d58-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="29d58-114">Área:</span><span class="sxs-lookup"><span data-stu-id="29d58-114">Area:</span></span>  <br/> |<span data-ttu-id="29d58-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="29d58-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29d58-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29d58-116">Remarks</span></span>

<span data-ttu-id="29d58-117">Esta propiedad es de sólo lectura si no se establece la propiedad **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)), pero si la propiedad **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) es TRUE y la **LID_IS_EXCEPTION** ([ PidLidIsException](pidlidisexception-canonical-property.md)) la propiedad es FALSE.</span><span class="sxs-lookup"><span data-stu-id="29d58-117">This property is only read if the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property is not set, but if the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property is TRUE and the **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) property is FALSE.</span></span> <span data-ttu-id="29d58-118">La palabra inferior especifica un índice en una tabla que contiene la información de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="29d58-118">The lower WORD specifies an index into a table that contains time zone information.</span></span> <span data-ttu-id="29d58-119">Desde la palabra superior, es de lectura sólo el bit más alto.</span><span class="sxs-lookup"><span data-stu-id="29d58-119">From the upper WORD, only the highest bit is read.</span></span> <span data-ttu-id="29d58-120">Si ese bit está establecido, a continuación, la zona horaria que hace referencia no observará se seguirá el horario de verano (DST), en caso contrario, las fechas de horario de verano se detallan en [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="29d58-120">If that bit is set, then the time zone referenced will not observe daylight saving time (DST), otherwise the DST dates detailed in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) will be followed.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="29d58-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="29d58-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="29d58-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="29d58-122">Protocol specifications</span></span>

<span data-ttu-id="29d58-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29d58-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29d58-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="29d58-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="29d58-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29d58-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29d58-126">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="29d58-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="29d58-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="29d58-127">Header files</span></span>

<span data-ttu-id="29d58-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="29d58-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="29d58-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="29d58-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29d58-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="29d58-130">See also</span></span>



[<span data-ttu-id="29d58-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="29d58-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="29d58-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="29d58-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="29d58-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="29d58-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="29d58-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="29d58-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

