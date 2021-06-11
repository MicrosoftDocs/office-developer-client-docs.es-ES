---
title: Propiedad canónica PidLidReminderDelta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderDelta
api_type:
- COM
ms.assetid: 011d73d0-8b38-4a4e-a56f-92dec451946a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 86a0203f930661452bb143e247c17ef6da8ed436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315893"
---
# <a name="pidlidreminderdelta-canonical-property"></a><span data-ttu-id="7b27f-103">Propiedad canónica PidLidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="7b27f-103">PidLidReminderDelta Canonical Property</span></span>

  
  
<span data-ttu-id="7b27f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b27f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b27f-105">Especifica el intervalo, en minutos, entre la hora en la que el aviso llega por primera vez a su fin y la hora de inicio del objeto calendar.</span><span class="sxs-lookup"><span data-stu-id="7b27f-105">Specifies the interval, in minutes, between the time when the reminder first becomes overdue and the start time of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b27f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7b27f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b27f-107">dispidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="7b27f-107">dispidReminderDelta</span></span>  <br/> |
|<span data-ttu-id="7b27f-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="7b27f-108">Property set:</span></span>  <br/> |<span data-ttu-id="7b27f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="7b27f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="7b27f-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="7b27f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7b27f-111">0x00008501</span><span class="sxs-lookup"><span data-stu-id="7b27f-111">0x00008501</span></span>  <br/> |
|<span data-ttu-id="7b27f-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7b27f-112">Data type:</span></span>  <br/> |<span data-ttu-id="7b27f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7b27f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7b27f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="7b27f-114">Area:</span></span>  <br/> |<span data-ttu-id="7b27f-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="7b27f-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b27f-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b27f-116">Remarks</span></span>

<span data-ttu-id="7b27f-117">Esta propiedad debe establecerse en objetos de calendario.</span><span class="sxs-lookup"><span data-stu-id="7b27f-117">This property must be set on calendar objects.</span></span> <span data-ttu-id="7b27f-118">Para todos los objetos que no son de calendario, esta propiedad debe establecerse en "0x00000000" y se omite.</span><span class="sxs-lookup"><span data-stu-id="7b27f-118">For all non-calendar objects, this property should be set to "0x00000000" and is ignored.</span></span> <span data-ttu-id="7b27f-119">Cuando se descarta un aviso para una instancia de un objeto de calendario periódico, el valor de esta propiedad se usa en el cálculo de la hora de señal de la siguiente instancia.</span><span class="sxs-lookup"><span data-stu-id="7b27f-119">When a reminder is dismissed for one instance of a recurring calendar object, the value of this property is used in the calculation of the signal time for the next instance.</span></span> <span data-ttu-id="7b27f-120">Vea [[MS- OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) para obtener más información sobre la creación de objetos de calendario.</span><span class="sxs-lookup"><span data-stu-id="7b27f-120">See [[MS- OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) for details about calendar object creation.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7b27f-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b27f-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b27f-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="7b27f-122">Protocol specifications</span></span>

<span data-ttu-id="7b27f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b27f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b27f-124">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="7b27f-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7b27f-125">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b27f-125">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b27f-126">Especifica las propiedades y el modelo de interacción para el correo electrónico y otros avisos de objetos.</span><span class="sxs-lookup"><span data-stu-id="7b27f-126">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b27f-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7b27f-127">Header files</span></span>

<span data-ttu-id="7b27f-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b27f-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b27f-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7b27f-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b27f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b27f-130">See also</span></span>



[<span data-ttu-id="7b27f-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7b27f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b27f-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7b27f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b27f-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7b27f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b27f-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7b27f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

