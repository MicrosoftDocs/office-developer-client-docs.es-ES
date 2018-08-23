---
title: Propiedad canónica PidLidReminderTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderTime
api_type:
- COM
ms.assetid: f4068ff0-2aa2-4332-be7d-ecebda30dfff
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dd1daddbdf4e953dac53d44181fedf371ce3beb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573883"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="3379d-103">Propiedad canónica PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="3379d-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="3379d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3379d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3379d-105">Especifica la hora de señal inicial de un aviso.</span><span class="sxs-lookup"><span data-stu-id="3379d-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3379d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3379d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3379d-107">dispidReminderTime</span><span class="sxs-lookup"><span data-stu-id="3379d-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="3379d-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="3379d-108">Property set:</span></span>  <br/> |<span data-ttu-id="3379d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="3379d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="3379d-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="3379d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3379d-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="3379d-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="3379d-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3379d-112">Data type:</span></span>  <br/> |<span data-ttu-id="3379d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="3379d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="3379d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3379d-114">Area:</span></span>  <br/> |<span data-ttu-id="3379d-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="3379d-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3379d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3379d-116">Remarks</span></span>

<span data-ttu-id="3379d-117">Para los objetos de calendario, esta propiedad representa la hora cuando el usuario sería las últimas que es la hora de inicio de la cita.</span><span class="sxs-lookup"><span data-stu-id="3379d-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="3379d-118">Los clientes deben establecer el valor en hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="3379d-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3379d-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3379d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3379d-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="3379d-120">Protocol specifications</span></span>

<span data-ttu-id="3379d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3379d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3379d-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3379d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3379d-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3379d-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3379d-124">Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.</span><span class="sxs-lookup"><span data-stu-id="3379d-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3379d-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3379d-125">Header files</span></span>

<span data-ttu-id="3379d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3379d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="3379d-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3379d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3379d-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="3379d-128">See also</span></span>



[<span data-ttu-id="3379d-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3379d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3379d-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="3379d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3379d-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3379d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3379d-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="3379d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

