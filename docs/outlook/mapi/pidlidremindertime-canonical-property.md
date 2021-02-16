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
ms.openlocfilehash: 8371418aabc557f48c74039320305df59624d7ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358712"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="ec44e-103">Propiedad canónica PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="ec44e-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="ec44e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec44e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec44e-105">Especifica la hora de señal inicial de un aviso.</span><span class="sxs-lookup"><span data-stu-id="ec44e-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec44e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ec44e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ec44e-107">dispidReminderTime</span><span class="sxs-lookup"><span data-stu-id="ec44e-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="ec44e-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="ec44e-108">Property set:</span></span>  <br/> |<span data-ttu-id="ec44e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ec44e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ec44e-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ec44e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ec44e-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="ec44e-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="ec44e-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ec44e-112">Data type:</span></span>  <br/> |<span data-ttu-id="ec44e-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ec44e-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ec44e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ec44e-114">Area:</span></span>  <br/> |<span data-ttu-id="ec44e-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="ec44e-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec44e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec44e-116">Remarks</span></span>

<span data-ttu-id="ec44e-117">Para los objetos de calendario, esta propiedad representa la hora en que el usuario llegaría tarde, que es la hora de inicio de la cita.</span><span class="sxs-lookup"><span data-stu-id="ec44e-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="ec44e-118">Los clientes deben establecer el valor en hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="ec44e-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ec44e-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec44e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ec44e-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="ec44e-120">Protocol specifications</span></span>

<span data-ttu-id="ec44e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec44e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec44e-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="ec44e-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ec44e-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec44e-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec44e-124">Especifica las propiedades y el modelo de interacción para el correo electrónico y otros avisos de objetos.</span><span class="sxs-lookup"><span data-stu-id="ec44e-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ec44e-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ec44e-125">Header files</span></span>

<span data-ttu-id="ec44e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ec44e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ec44e-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ec44e-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec44e-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ec44e-128">See also</span></span>



[<span data-ttu-id="ec44e-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ec44e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ec44e-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="ec44e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ec44e-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ec44e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ec44e-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ec44e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

