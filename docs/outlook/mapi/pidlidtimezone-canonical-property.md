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
# <a name="pidlidtimezone-canonical-property"></a><span data-ttu-id="9cde0-103">Propiedad canónica PidLidTimeZone</span><span class="sxs-lookup"><span data-stu-id="9cde0-103">PidLidTimeZone Canonical Property</span></span>

  
  
<span data-ttu-id="9cde0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cde0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cde0-105">Especifica información sobre la zona horaria de una reunión periódica.</span><span class="sxs-lookup"><span data-stu-id="9cde0-105">Specifies information about the time zone of a recurring meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9cde0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9cde0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9cde0-107">LID_TIME_ZONE</span><span class="sxs-lookup"><span data-stu-id="9cde0-107">LID_TIME_ZONE</span></span>  <br/> |
|<span data-ttu-id="9cde0-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="9cde0-108">Property set:</span></span>  <br/> |<span data-ttu-id="9cde0-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="9cde0-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="9cde0-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="9cde0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9cde0-111">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="9cde0-111">0x0000000C</span></span>  <br/> |
|<span data-ttu-id="9cde0-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9cde0-112">Data type:</span></span>  <br/> |<span data-ttu-id="9cde0-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9cde0-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9cde0-114">Área:</span><span class="sxs-lookup"><span data-stu-id="9cde0-114">Area:</span></span>  <br/> |<span data-ttu-id="9cde0-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="9cde0-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cde0-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9cde0-116">Remarks</span></span>

<span data-ttu-id="9cde0-117">Esta propiedad solo se lee si la propiedad **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) no está establecida, pero si la propiedad **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) es TRUE y la propiedad **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) es FALSE.</span><span class="sxs-lookup"><span data-stu-id="9cde0-117">This property is only read if the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property is not set, but if the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property is TRUE and the **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) property is FALSE.</span></span> <span data-ttu-id="9cde0-118">Word inferior especifica un índice en una tabla que contiene información de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9cde0-118">The lower WORD specifies an index into a table that contains time zone information.</span></span> <span data-ttu-id="9cde0-119">Desde word superior, solo se lee el bit más alto.</span><span class="sxs-lookup"><span data-stu-id="9cde0-119">From the upper WORD, only the highest bit is read.</span></span> <span data-ttu-id="9cde0-120">Si se establece ese bit, la zona horaria a la que se hace referencia no observará el horario de verano (DST), de lo contrario se seguirán las fechas de DST detalladas en [[MS-OXOCAL].](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cde0-120">If that bit is set, then the time zone referenced will not observe daylight saving time (DST), otherwise the DST dates detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) will be followed.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9cde0-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9cde0-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9cde0-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="9cde0-122">Protocol specifications</span></span>

<span data-ttu-id="9cde0-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cde0-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cde0-124">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="9cde0-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9cde0-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cde0-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cde0-126">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="9cde0-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9cde0-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9cde0-127">Header files</span></span>

<span data-ttu-id="9cde0-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9cde0-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="9cde0-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9cde0-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9cde0-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cde0-130">See also</span></span>



[<span data-ttu-id="9cde0-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9cde0-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9cde0-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9cde0-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9cde0-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9cde0-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9cde0-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9cde0-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

