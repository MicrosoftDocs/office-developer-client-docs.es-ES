---
title: Propiedad canónica PidLidFInvited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFInvited
api_type:
- COM
ms.assetid: ca1ea5ec-20d5-4b70-95de-c2246a10beae
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 409fc2e01b103378eb0df1bdd06ee8b5647148bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818724"
---
# <a name="pidlidfinvited-canonical-property"></a><span data-ttu-id="5b411-103">Propiedad canónica PidLidFInvited</span><span class="sxs-lookup"><span data-stu-id="5b411-103">PidLidFInvited Canonical Property</span></span>

  
  
<span data-ttu-id="5b411-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5b411-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5b411-105">Indica si se han enviado invitaciones para la reunión que representa esta reunión.</span><span class="sxs-lookup"><span data-stu-id="5b411-105">Indicates whether or not invitations have been sent for the meeting that this meeting represents.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b411-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5b411-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b411-107">dispidFInvited</span><span class="sxs-lookup"><span data-stu-id="5b411-107">dispidFInvited</span></span>  <br/> |
|<span data-ttu-id="5b411-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="5b411-108">Property set:</span></span>  <br/> |<span data-ttu-id="5b411-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="5b411-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="5b411-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="5b411-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5b411-111">0x00008229</span><span class="sxs-lookup"><span data-stu-id="5b411-111">0x00008229</span></span>  <br/> |
|<span data-ttu-id="5b411-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5b411-112">Data type:</span></span>  <br/> |<span data-ttu-id="5b411-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5b411-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5b411-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5b411-114">Area:</span></span>  <br/> |<span data-ttu-id="5b411-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="5b411-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b411-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5b411-116">Remarks</span></span>

<span data-ttu-id="5b411-117">Un valor FALSE, o la ausencia de esta propiedad indica que nunca se ha enviado una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="5b411-117">A value of FALSE, or the absence of this property, indicates that a meeting request has never been sent.</span></span> <span data-ttu-id="5b411-118">Un valor de TRUE indica que se ha enviado una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="5b411-118">A value of TRUE indicates that a meeting request has been sent.</span></span> <span data-ttu-id="5b411-119">Una vez que este valor se establece en TRUE en una reunión, no debe cambiarse.</span><span class="sxs-lookup"><span data-stu-id="5b411-119">Once this value is set to TRUE on a meeting, it must not be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5b411-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b411-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b411-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5b411-121">Protocol specifications</span></span>

<span data-ttu-id="5b411-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b411-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b411-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5b411-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5b411-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b411-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b411-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="5b411-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b411-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5b411-126">Header files</span></span>

<span data-ttu-id="5b411-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b411-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b411-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5b411-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b411-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b411-129">See also</span></span>



[<span data-ttu-id="5b411-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5b411-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b411-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5b411-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b411-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5b411-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b411-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5b411-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

