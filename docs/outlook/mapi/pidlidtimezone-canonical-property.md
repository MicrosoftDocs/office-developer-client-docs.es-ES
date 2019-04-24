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
ms.openlocfilehash: b62779567a7dbd298fdd313e90b13fb223e4e47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319274"
---
# <a name="pidlidtimezone-canonical-property"></a><span data-ttu-id="00748-103">Propiedad canónica PidLidTimeZone</span><span class="sxs-lookup"><span data-stu-id="00748-103">PidLidTimeZone Canonical Property</span></span>

  
  
<span data-ttu-id="00748-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00748-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00748-105">Especifica información sobre la zona horaria de una reunión periódica.</span><span class="sxs-lookup"><span data-stu-id="00748-105">Specifies information about the time zone of a recurring meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00748-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="00748-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00748-107">LID_TIME_ZONE</span><span class="sxs-lookup"><span data-stu-id="00748-107">LID_TIME_ZONE</span></span>  <br/> |
|<span data-ttu-id="00748-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="00748-108">Property set:</span></span>  <br/> |<span data-ttu-id="00748-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="00748-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="00748-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="00748-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="00748-111">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="00748-111">0x0000000C</span></span>  <br/> |
|<span data-ttu-id="00748-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="00748-112">Data type:</span></span>  <br/> |<span data-ttu-id="00748-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="00748-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="00748-114">Área:</span><span class="sxs-lookup"><span data-stu-id="00748-114">Area:</span></span>  <br/> |<span data-ttu-id="00748-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="00748-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00748-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00748-116">Remarks</span></span>

<span data-ttu-id="00748-117">Esta propiedad sólo se lee si no se establece la propiedad **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)), pero si la propiedad **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) es true y el **LID_IS_EXCEPTION** ([ PidLidIsException](pidlidisexception-canonical-property.md)) es false.</span><span class="sxs-lookup"><span data-stu-id="00748-117">This property is only read if the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property is not set, but if the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property is TRUE and the **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) property is FALSE.</span></span> <span data-ttu-id="00748-118">La palabra inferior especifica un índice en una tabla que contiene información de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="00748-118">The lower WORD specifies an index into a table that contains time zone information.</span></span> <span data-ttu-id="00748-119">Desde la palabra superior, solo se lee el bit más alto.</span><span class="sxs-lookup"><span data-stu-id="00748-119">From the upper WORD, only the highest bit is read.</span></span> <span data-ttu-id="00748-120">Si se establece ese bit, la zona horaria a la que se hace referencia no observará el horario de verano (DST), de lo contrario, se seguirán las fechas de horario de verano detalladas en [[ms-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="00748-120">If that bit is set, then the time zone referenced will not observe daylight saving time (DST), otherwise the DST dates detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) will be followed.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="00748-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="00748-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00748-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="00748-122">Protocol specifications</span></span>

<span data-ttu-id="00748-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00748-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00748-124">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="00748-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00748-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00748-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00748-126">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="00748-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00748-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="00748-127">Header files</span></span>

<span data-ttu-id="00748-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="00748-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="00748-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="00748-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00748-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="00748-130">See also</span></span>



[<span data-ttu-id="00748-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="00748-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00748-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="00748-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00748-133">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="00748-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00748-134">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="00748-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

