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
ms.openlocfilehash: e2caccf3cf6ca7e6f15bed1c901d4dfbb198f19b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818857"
---
# <a name="pidlidreminderdelta-canonical-property"></a><span data-ttu-id="0e347-103">Propiedad canónica PidLidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="0e347-103">PidLidReminderDelta Canonical Property</span></span>

  
  
<span data-ttu-id="0e347-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e347-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e347-105">Especifica el intervalo, en minutos, entre la hora cuando el aviso en primer lugar se convierte en vencidas y la hora de inicio del objeto de calendario.</span><span class="sxs-lookup"><span data-stu-id="0e347-105">Specifies the interval, in minutes, between the time when the reminder first becomes overdue and the start time of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e347-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0e347-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e347-107">dispidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="0e347-107">dispidReminderDelta</span></span>  <br/> |
|<span data-ttu-id="0e347-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="0e347-108">Property set:</span></span>  <br/> |<span data-ttu-id="0e347-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="0e347-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="0e347-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="0e347-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0e347-111">0x00008501</span><span class="sxs-lookup"><span data-stu-id="0e347-111">0x00008501</span></span>  <br/> |
|<span data-ttu-id="0e347-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0e347-112">Data type:</span></span>  <br/> |<span data-ttu-id="0e347-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0e347-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0e347-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0e347-114">Area:</span></span>  <br/> |<span data-ttu-id="0e347-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="0e347-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e347-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e347-116">Remarks</span></span>

<span data-ttu-id="0e347-117">Esta propiedad se debe establecer en los objetos de calendario.</span><span class="sxs-lookup"><span data-stu-id="0e347-117">This property must be set on calendar objects.</span></span> <span data-ttu-id="0e347-118">Para todos los objetos que no sean calendario, esta propiedad debe establecerse en "0 x 00000000" y se omite.</span><span class="sxs-lookup"><span data-stu-id="0e347-118">For all non-calendar objects, this property should be set to "0x00000000" and is ignored.</span></span> <span data-ttu-id="0e347-119">Cuando se omite un aviso para una instancia de un objeto de calendario periódico, el valor de esta propiedad se usa en el cálculo de la hora de señal de la siguiente aparición.</span><span class="sxs-lookup"><span data-stu-id="0e347-119">When a reminder is dismissed for one instance of a recurring calendar object, the value of this property is used in the calculation of the signal time for the next instance.</span></span> <span data-ttu-id="0e347-120">Vea [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) para obtener información detallada acerca de la creación de objetos de calendario.</span><span class="sxs-lookup"><span data-stu-id="0e347-120">See [[MS- OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) for details about calendar object creation.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0e347-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e347-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e347-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0e347-122">Protocol specifications</span></span>

<span data-ttu-id="0e347-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e347-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e347-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0e347-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e347-125">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e347-125">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e347-126">Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.</span><span class="sxs-lookup"><span data-stu-id="0e347-126">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e347-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0e347-127">Header files</span></span>

<span data-ttu-id="0e347-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e347-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e347-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0e347-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e347-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e347-130">See also</span></span>



[<span data-ttu-id="0e347-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0e347-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e347-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0e347-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e347-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0e347-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e347-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0e347-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

