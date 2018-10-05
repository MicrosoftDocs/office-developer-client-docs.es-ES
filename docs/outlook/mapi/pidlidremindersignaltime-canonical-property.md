---
title: Propiedad canónica PidLidReminderSignalTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSignalTime
api_type:
- COM
ms.assetid: 58f6432e-6e88-420b-959f-7f365899f7eb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3fcfd00f71a308dce625e6636edbe647f3d7258a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393393"
---
# <a name="pidlidremindersignaltime-canonical-property"></a><span data-ttu-id="103c0-103">Propiedad canónica PidLidReminderSignalTime</span><span class="sxs-lookup"><span data-stu-id="103c0-103">PidLidReminderSignalTime Canonical Property</span></span>

  
  
<span data-ttu-id="103c0-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="103c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="103c0-105">Especifica el punto en el tiempo cuando un aviso de transición de pendientes a vencidas.</span><span class="sxs-lookup"><span data-stu-id="103c0-105">Specifies the point in time when a reminder transitions from pending to overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="103c0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="103c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="103c0-107">dispidReminderNextTime</span><span class="sxs-lookup"><span data-stu-id="103c0-107">dispidReminderNextTime</span></span>  <br/> |
|<span data-ttu-id="103c0-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="103c0-108">Property set:</span></span>  <br/> |<span data-ttu-id="103c0-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="103c0-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="103c0-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="103c0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="103c0-111">0x00008560</span><span class="sxs-lookup"><span data-stu-id="103c0-111">0x00008560</span></span>  <br/> |
|<span data-ttu-id="103c0-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="103c0-112">Data type:</span></span>  <br/> |<span data-ttu-id="103c0-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="103c0-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="103c0-114">Área:</span><span class="sxs-lookup"><span data-stu-id="103c0-114">Area:</span></span>  <br/> |<span data-ttu-id="103c0-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="103c0-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="103c0-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="103c0-116">Remarks</span></span>

<span data-ttu-id="103c0-117">Si la propiedad **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) es TRUE, se debe establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="103c0-117">This property must be set if the **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="103c0-118">Los clientes deben establecer el valor en hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="103c0-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="103c0-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="103c0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="103c0-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="103c0-120">Protocol specifications</span></span>

<span data-ttu-id="103c0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="103c0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="103c0-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="103c0-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="103c0-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="103c0-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="103c0-124">Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.</span><span class="sxs-lookup"><span data-stu-id="103c0-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="103c0-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="103c0-125">Header files</span></span>

<span data-ttu-id="103c0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="103c0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="103c0-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="103c0-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="103c0-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="103c0-128">See also</span></span>



[<span data-ttu-id="103c0-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="103c0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="103c0-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="103c0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="103c0-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="103c0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="103c0-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="103c0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

