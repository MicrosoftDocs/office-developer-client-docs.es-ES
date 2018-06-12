---
title: Propiedad canónico PidLidReminderTime
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 6e74dbb1f8e0e64feb2c86eb04e146e201089a4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818892"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="d6779-103">Propiedad canónico PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="d6779-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="d6779-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d6779-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d6779-105">Especifica la hora de señal inicial de un aviso.</span><span class="sxs-lookup"><span data-stu-id="d6779-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d6779-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d6779-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6779-107">dispidReminderTime</span><span class="sxs-lookup"><span data-stu-id="d6779-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="d6779-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="d6779-108">Property set:</span></span>  <br/> |<span data-ttu-id="d6779-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d6779-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d6779-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="d6779-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d6779-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="d6779-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="d6779-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d6779-112">Data type:</span></span>  <br/> |<span data-ttu-id="d6779-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d6779-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d6779-114">Área:</span><span class="sxs-lookup"><span data-stu-id="d6779-114">Area:</span></span>  <br/> |<span data-ttu-id="d6779-115">Aviso</span><span class="sxs-lookup"><span data-stu-id="d6779-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6779-116">Notas</span><span class="sxs-lookup"><span data-stu-id="d6779-116">Remarks</span></span>

<span data-ttu-id="d6779-117">Para los objetos de calendario, esta propiedad representa la hora cuando el usuario sería las últimas que es la hora de inicio de la cita.</span><span class="sxs-lookup"><span data-stu-id="d6779-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="d6779-118">Los clientes deben establecer el valor en hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="d6779-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d6779-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6779-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6779-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d6779-120">Protocol specifications</span></span>

<span data-ttu-id="d6779-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6779-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6779-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d6779-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d6779-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6779-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6779-124">Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.</span><span class="sxs-lookup"><span data-stu-id="d6779-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6779-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d6779-125">Header files</span></span>

<span data-ttu-id="d6779-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6779-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6779-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d6779-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6779-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="d6779-128">See also</span></span>



[<span data-ttu-id="d6779-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d6779-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6779-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d6779-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6779-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="d6779-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6779-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d6779-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

