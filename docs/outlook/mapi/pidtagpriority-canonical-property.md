---
title: Propiedad canónica PidTagPriority
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 67f482e347db1b69a248c542f2cb172c41d6f9f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819936"
---
# <a name="pidtagpriority-canonical-property"></a><span data-ttu-id="988e9-103">Propiedad canónica PidTagPriority</span><span class="sxs-lookup"><span data-stu-id="988e9-103">PidTagPriority Canonical Property</span></span>

  
  
<span data-ttu-id="988e9-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="988e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="988e9-105">Contiene la prioridad relativa de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="988e9-105">Contains the relative priority of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="988e9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="988e9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="988e9-107">PR_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="988e9-107">PR_PRIORITY</span></span>  <br/> |
|<span data-ttu-id="988e9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="988e9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="988e9-109">0x0026</span><span class="sxs-lookup"><span data-stu-id="988e9-109">0x0026</span></span>  <br/> |
|<span data-ttu-id="988e9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="988e9-110">Data type:</span></span>  <br/> |<span data-ttu-id="988e9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="988e9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="988e9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="988e9-112">Area:</span></span>  <br/> |<span data-ttu-id="988e9-113">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="988e9-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="988e9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="988e9-114">Remarks</span></span>

<span data-ttu-id="988e9-115">No se deben confundir esta propiedad y la propiedad **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="988e9-115">This property and the **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="988e9-116">Importancia indica un valor a los usuarios, mientras que la prioridad indica el orden o la velocidad a la que se debe enviar el mensaje por el software del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="988e9-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="988e9-117">Normalmente, una mayor prioridad indica un costo mayor.</span><span class="sxs-lookup"><span data-stu-id="988e9-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="988e9-118">Mayor importancia generalmente se asocia con una presentación diferentes mediante la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="988e9-118">Higher importance usually is associated with a different display by the user interface.</span></span>
  
<span data-ttu-id="988e9-119">La prioridad de un mensaje de informe debe ser la misma que la prioridad del mensaje original se notifiquen.</span><span class="sxs-lookup"><span data-stu-id="988e9-119">The priority of a report message should be the same as the priority of the original message being reported.</span></span>
  
<span data-ttu-id="988e9-120">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="988e9-120">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="988e9-121">PRIO_NONURGENT</span><span class="sxs-lookup"><span data-stu-id="988e9-121">PRIO_NONURGENT</span></span> 
  
> <span data-ttu-id="988e9-122">El mensaje no sea urgente.</span><span class="sxs-lookup"><span data-stu-id="988e9-122">The message is not urgent.</span></span>
    
<span data-ttu-id="988e9-123">PRIO_NORMAL</span><span class="sxs-lookup"><span data-stu-id="988e9-123">PRIO_NORMAL</span></span> 
  
> <span data-ttu-id="988e9-124">El mensaje tiene prioridad normal.</span><span class="sxs-lookup"><span data-stu-id="988e9-124">The message has normal priority.</span></span>
    
<span data-ttu-id="988e9-125">PRIO_URGENT</span><span class="sxs-lookup"><span data-stu-id="988e9-125">PRIO_URGENT</span></span> 
  
> <span data-ttu-id="988e9-126">El mensaje es urgente.</span><span class="sxs-lookup"><span data-stu-id="988e9-126">The message is urgent.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="988e9-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="988e9-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="988e9-128">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="988e9-128">Protocol specifications</span></span>

<span data-ttu-id="988e9-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="988e9-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="988e9-130">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="988e9-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="988e9-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="988e9-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="988e9-132">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="988e9-132">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="988e9-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="988e9-133">Header files</span></span>

<span data-ttu-id="988e9-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="988e9-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="988e9-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="988e9-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="988e9-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="988e9-136">Mapitags.h</span></span>
  
> <span data-ttu-id="988e9-137">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="988e9-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="988e9-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="988e9-138">See also</span></span>



[<span data-ttu-id="988e9-139">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="988e9-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="988e9-140">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="988e9-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="988e9-141">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="988e9-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="988e9-142">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="988e9-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

