---
title: Propiedad canónica PidLidWhere
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidWhere
api_type:
- COM
ms.assetid: b21a3aa4-7536-4728-b4a4-273cfb25c57e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 127627b79782a2a785b00b79b9940b66256a08eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819048"
---
# <a name="pidlidwhere-canonical-property"></a><span data-ttu-id="1bb62-103">Propiedad canónica PidLidWhere</span><span class="sxs-lookup"><span data-stu-id="1bb62-103">PidLidWhere Canonical Property</span></span>

  
  
<span data-ttu-id="1bb62-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1bb62-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1bb62-105">Especifica la ubicación de un evento.</span><span class="sxs-lookup"><span data-stu-id="1bb62-105">Specifies the location of an event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1bb62-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1bb62-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1bb62-107">LID_WHERE</span><span class="sxs-lookup"><span data-stu-id="1bb62-107">LID_WHERE</span></span>  <br/> |
|<span data-ttu-id="1bb62-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="1bb62-108">Property set:</span></span>  <br/> |<span data-ttu-id="1bb62-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="1bb62-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="1bb62-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="1bb62-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1bb62-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1bb62-111">0x00000002</span></span>  <br/> |
|<span data-ttu-id="1bb62-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1bb62-112">Data type:</span></span>  <br/> |<span data-ttu-id="1bb62-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1bb62-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1bb62-114">Área:</span><span class="sxs-lookup"><span data-stu-id="1bb62-114">Area:</span></span>  <br/> |<span data-ttu-id="1bb62-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="1bb62-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bb62-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1bb62-116">Remarks</span></span>

<span data-ttu-id="1bb62-117">El valor de esta propiedad debe ser el mismo que el valor de la propiedad **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) de la reunión asociada.</span><span class="sxs-lookup"><span data-stu-id="1bb62-117">The value of this property should be the same as the value of the **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) property from the associated meeting.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1bb62-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bb62-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1bb62-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1bb62-119">Protocol specifications</span></span>

<span data-ttu-id="1bb62-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1bb62-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1bb62-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1bb62-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1bb62-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1bb62-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1bb62-123">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1bb62-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1bb62-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1bb62-124">Header files</span></span>

<span data-ttu-id="1bb62-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1bb62-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1bb62-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1bb62-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1bb62-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1bb62-127">See also</span></span>



[<span data-ttu-id="1bb62-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1bb62-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1bb62-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1bb62-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1bb62-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1bb62-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1bb62-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1bb62-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

