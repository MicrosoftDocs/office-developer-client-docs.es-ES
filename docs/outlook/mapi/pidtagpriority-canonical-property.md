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
ms.openlocfilehash: b9c0f5ebeae21d6d683bbb5def727d29a34bcdb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339434"
---
# <a name="pidtagpriority-canonical-property"></a><span data-ttu-id="8c9d7-103">Propiedad canónica PidTagPriority</span><span class="sxs-lookup"><span data-stu-id="8c9d7-103">PidTagPriority Canonical Property</span></span>

  
  
<span data-ttu-id="8c9d7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c9d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c9d7-105">Contiene la prioridad relativa de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8c9d7-105">Contains the relative priority of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c9d7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8c9d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c9d7-107">PR_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="8c9d7-107">PR_PRIORITY</span></span>  <br/> |
|<span data-ttu-id="8c9d7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8c9d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8c9d7-109">0x0026</span><span class="sxs-lookup"><span data-stu-id="8c9d7-109">0x0026</span></span>  <br/> |
|<span data-ttu-id="8c9d7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8c9d7-110">Data type:</span></span>  <br/> |<span data-ttu-id="8c9d7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8c9d7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8c9d7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8c9d7-112">Area:</span></span>  <br/> |<span data-ttu-id="8c9d7-113">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="8c9d7-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c9d7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c9d7-114">Remarks</span></span>

<span data-ttu-id="8c9d7-115">No se debe confundir esta propiedad y la propiedad **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8c9d7-115">This property and the **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="8c9d7-116">Importancia indica un valor para los usuarios, mientras que Priority indica el orden o la velocidad que el software del sistema de mensajería debe enviar al mensaje.</span><span class="sxs-lookup"><span data-stu-id="8c9d7-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="8c9d7-117">Una prioridad más alta suele indicar un costo mayor.</span><span class="sxs-lookup"><span data-stu-id="8c9d7-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="8c9d7-118">La mayor importancia suele estar asociada con una presentación distinta en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8c9d7-118">Higher importance usually is associated with a different display by the user interface.</span></span>
  
<span data-ttu-id="8c9d7-119">La prioridad de un mensaje de informe debe ser la misma que la prioridad del mensaje original que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="8c9d7-119">The priority of a report message should be the same as the priority of the original message being reported.</span></span>
  
<span data-ttu-id="8c9d7-120">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="8c9d7-120">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="8c9d7-121">PRIO_NONURGENT</span><span class="sxs-lookup"><span data-stu-id="8c9d7-121">PRIO_NONURGENT</span></span> 
  
> <span data-ttu-id="8c9d7-122">El mensaje no es urgente.</span><span class="sxs-lookup"><span data-stu-id="8c9d7-122">The message is not urgent.</span></span>
    
<span data-ttu-id="8c9d7-123">PRIO_NORMAL</span><span class="sxs-lookup"><span data-stu-id="8c9d7-123">PRIO_NORMAL</span></span> 
  
> <span data-ttu-id="8c9d7-124">El mensaje tiene prioridad normal.</span><span class="sxs-lookup"><span data-stu-id="8c9d7-124">The message has normal priority.</span></span>
    
<span data-ttu-id="8c9d7-125">PRIO_URGENT</span><span class="sxs-lookup"><span data-stu-id="8c9d7-125">PRIO_URGENT</span></span> 
  
> <span data-ttu-id="8c9d7-126">El mensaje es urgente.</span><span class="sxs-lookup"><span data-stu-id="8c9d7-126">The message is urgent.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="8c9d7-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c9d7-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c9d7-128">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8c9d7-128">Protocol specifications</span></span>

<span data-ttu-id="8c9d7-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c9d7-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c9d7-130">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8c9d7-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c9d7-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c9d7-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c9d7-132">Especifica las propiedades y operaciones que se admiten en los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="8c9d7-132">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c9d7-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8c9d7-133">Header files</span></span>

<span data-ttu-id="8c9d7-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8c9d7-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c9d7-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8c9d7-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="8c9d7-136">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8c9d7-136">Mapitags.h</span></span>
  
> <span data-ttu-id="8c9d7-137">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8c9d7-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c9d7-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c9d7-138">See also</span></span>



[<span data-ttu-id="8c9d7-139">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8c9d7-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c9d7-140">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="8c9d7-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c9d7-141">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8c9d7-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c9d7-142">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8c9d7-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

