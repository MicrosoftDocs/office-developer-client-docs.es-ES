---
title: Propiedad canónica PidLidReminderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSet
api_type:
- COM
ms.assetid: 06b7792c-1b43-4e20-9a3b-44f2664b2125
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c056b0e587de06f6c32ceb3cebbb96f2fb737208
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579084"
---
# <a name="pidlidreminderset-canonical-property"></a><span data-ttu-id="26f82-103">Propiedad canónica PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="26f82-103">PidLidReminderSet Canonical Property</span></span>

  
  
<span data-ttu-id="26f82-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26f82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26f82-105">Especifica si se ha establecido un aviso en el objeto.</span><span class="sxs-lookup"><span data-stu-id="26f82-105">Specifies whether a reminder is set on the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="26f82-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="26f82-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="26f82-107">dispidReminderSet</span><span class="sxs-lookup"><span data-stu-id="26f82-107">dispidReminderSet</span></span>  <br/> |
|<span data-ttu-id="26f82-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="26f82-108">Property set:</span></span>  <br/> |<span data-ttu-id="26f82-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="26f82-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="26f82-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="26f82-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="26f82-111">0x00008503</span><span class="sxs-lookup"><span data-stu-id="26f82-111">0x00008503</span></span>  <br/> |
|<span data-ttu-id="26f82-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="26f82-112">Data type:</span></span>  <br/> |<span data-ttu-id="26f82-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="26f82-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="26f82-114">Área:</span><span class="sxs-lookup"><span data-stu-id="26f82-114">Area:</span></span>  <br/> |<span data-ttu-id="26f82-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="26f82-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26f82-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26f82-116">Remarks</span></span>

<span data-ttu-id="26f82-117">Si un objeto calendar periódica tiene esta propiedad establecida en TRUE, el cliente puede invalidar este valor para las excepciones.</span><span class="sxs-lookup"><span data-stu-id="26f82-117">If a recurring calendar object has this property set to TRUE, the client can override this value for exceptions.</span></span>
  
<span data-ttu-id="26f82-118">Si esta propiedad es FALSE en un objeto de calendario periódico, se deshabilitan los avisos para toda la serie, incluidas las excepciones.</span><span class="sxs-lookup"><span data-stu-id="26f82-118">If this property is FALSE on a recurring calendar object, reminders are disabled for the entire series, including exceptions.</span></span> <span data-ttu-id="26f82-119">Para los objetos de tarea periódica, esta propiedad no se puede reemplazar por excepciones (vea [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) y [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) para obtener información detallada).</span><span class="sxs-lookup"><span data-stu-id="26f82-119">For recurring task objects, this property cannot be overridden by exceptions (see [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) and [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) for details).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="26f82-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="26f82-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="26f82-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="26f82-121">Protocol specifications</span></span>

<span data-ttu-id="26f82-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26f82-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26f82-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="26f82-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="26f82-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26f82-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26f82-125">Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.</span><span class="sxs-lookup"><span data-stu-id="26f82-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="26f82-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="26f82-126">Header files</span></span>

<span data-ttu-id="26f82-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26f82-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="26f82-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="26f82-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26f82-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="26f82-129">See also</span></span>



[<span data-ttu-id="26f82-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="26f82-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="26f82-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="26f82-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="26f82-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="26f82-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="26f82-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="26f82-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

