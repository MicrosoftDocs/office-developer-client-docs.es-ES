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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350858"
---
# <a name="pidlidremindersignaltime-canonical-property"></a><span data-ttu-id="5f392-103">Propiedad canónica PidLidReminderSignalTime</span><span class="sxs-lookup"><span data-stu-id="5f392-103">PidLidReminderSignalTime Canonical Property</span></span>

  
  
<span data-ttu-id="5f392-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f392-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f392-105">Especifica el momento en el que un aviso cambia de pendiente a vencido.</span><span class="sxs-lookup"><span data-stu-id="5f392-105">Specifies the point in time when a reminder transitions from pending to overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f392-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5f392-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f392-107">dispidReminderNextTime</span><span class="sxs-lookup"><span data-stu-id="5f392-107">dispidReminderNextTime</span></span>  <br/> |
|<span data-ttu-id="5f392-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="5f392-108">Property set:</span></span>  <br/> |<span data-ttu-id="5f392-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5f392-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5f392-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="5f392-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5f392-111">0x00008560</span><span class="sxs-lookup"><span data-stu-id="5f392-111">0x00008560</span></span>  <br/> |
|<span data-ttu-id="5f392-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5f392-112">Data type:</span></span>  <br/> |<span data-ttu-id="5f392-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5f392-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5f392-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5f392-114">Area:</span></span>  <br/> |<span data-ttu-id="5f392-115">Recordatorio</span><span class="sxs-lookup"><span data-stu-id="5f392-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f392-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f392-116">Remarks</span></span>

<span data-ttu-id="5f392-117">Esta propiedad se debe establecer si la propiedad **dispidReminderSet** ([PIDLIDREMINDERSET](pidlidreminderset-canonical-property.md)) es true.</span><span class="sxs-lookup"><span data-stu-id="5f392-117">This property must be set if the **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="5f392-118">Los clientes deben establecer el valor en la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="5f392-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5f392-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f392-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f392-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5f392-120">Protocol specifications</span></span>

<span data-ttu-id="5f392-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f392-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f392-122">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5f392-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f392-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f392-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f392-124">Especifica las propiedades y el modelo de interacción para el correo electrónico y otros recordatorios de objetos.</span><span class="sxs-lookup"><span data-stu-id="5f392-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f392-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5f392-125">Header files</span></span>

<span data-ttu-id="5f392-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5f392-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f392-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5f392-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f392-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f392-128">See also</span></span>



[<span data-ttu-id="5f392-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5f392-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f392-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="5f392-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f392-131">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5f392-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f392-132">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="5f392-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

