---
title: Propiedad canónico PidLidReminderSignalTime
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 375cde94d0ecd989908fccbdd69710c1961fba17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818883"
---
# <a name="pidlidremindersignaltime-canonical-property"></a><span data-ttu-id="6ab4f-103">Propiedad canónico PidLidReminderSignalTime</span><span class="sxs-lookup"><span data-stu-id="6ab4f-103">PidLidReminderSignalTime Canonical Property</span></span>

  
  
<span data-ttu-id="6ab4f-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ab4f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ab4f-105">Especifica el punto en el tiempo cuando un aviso de transición de pendientes a vencidas.</span><span class="sxs-lookup"><span data-stu-id="6ab4f-105">Specifies the point in time when a reminder transitions from pending to overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ab4f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6ab4f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ab4f-107">dispidReminderNextTime</span><span class="sxs-lookup"><span data-stu-id="6ab4f-107">dispidReminderNextTime</span></span>  <br/> |
|<span data-ttu-id="6ab4f-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="6ab4f-108">Property set:</span></span>  <br/> |<span data-ttu-id="6ab4f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="6ab4f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="6ab4f-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="6ab4f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6ab4f-111">0x00008560</span><span class="sxs-lookup"><span data-stu-id="6ab4f-111">0x00008560</span></span>  <br/> |
|<span data-ttu-id="6ab4f-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6ab4f-112">Data type:</span></span>  <br/> |<span data-ttu-id="6ab4f-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="6ab4f-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="6ab4f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="6ab4f-114">Area:</span></span>  <br/> |<span data-ttu-id="6ab4f-115">Aviso</span><span class="sxs-lookup"><span data-stu-id="6ab4f-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ab4f-116">Notas</span><span class="sxs-lookup"><span data-stu-id="6ab4f-116">Remarks</span></span>

<span data-ttu-id="6ab4f-117">Si la propiedad **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) es TRUE, se debe establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="6ab4f-117">This property must be set if the **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="6ab4f-118">Los clientes deben establecer el valor en hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="6ab4f-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6ab4f-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ab4f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ab4f-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6ab4f-120">Protocol specifications</span></span>

<span data-ttu-id="6ab4f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ab4f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ab4f-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6ab4f-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6ab4f-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ab4f-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ab4f-124">Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.</span><span class="sxs-lookup"><span data-stu-id="6ab4f-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6ab4f-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6ab4f-125">Header files</span></span>

<span data-ttu-id="6ab4f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ab4f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ab4f-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6ab4f-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ab4f-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="6ab4f-128">See also</span></span>



[<span data-ttu-id="6ab4f-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6ab4f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ab4f-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6ab4f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ab4f-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="6ab4f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ab4f-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="6ab4f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

