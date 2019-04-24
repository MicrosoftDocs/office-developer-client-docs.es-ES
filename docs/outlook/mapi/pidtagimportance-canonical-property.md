---
title: Propiedad canónica PidTagImportance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6bef8b05f2fbf94b74ee126b80dfc6ae0c5e9d11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327926"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="3fc63-103">Propiedad canónica PidTagImportance</span><span class="sxs-lookup"><span data-stu-id="3fc63-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="3fc63-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fc63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fc63-105">Contiene un valor que indica el remitente del mensaje dictamen de la importancia de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="3fc63-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3fc63-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3fc63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3fc63-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="3fc63-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="3fc63-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3fc63-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3fc63-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="3fc63-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="3fc63-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3fc63-110">Data type:</span></span>  <br/> |<span data-ttu-id="3fc63-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3fc63-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3fc63-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3fc63-112">Area:</span></span>  <br/> |<span data-ttu-id="3fc63-113">Mensajes generales</span><span class="sxs-lookup"><span data-stu-id="3fc63-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fc63-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3fc63-114">Remarks</span></span>

<span data-ttu-id="3fc63-115">No se debe confundir esta propiedad y la propiedad **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3fc63-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="3fc63-116">Importancia indica un valor para los usuarios, mientras que Priority indica el orden o la velocidad que el software del sistema de mensajería debe enviar al mensaje.</span><span class="sxs-lookup"><span data-stu-id="3fc63-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="3fc63-117">Una prioridad más alta suele indicar un costo mayor.</span><span class="sxs-lookup"><span data-stu-id="3fc63-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="3fc63-118">La mayor importancia suele estar asociada con una presentación distinta en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3fc63-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="3fc63-119">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="3fc63-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="3fc63-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="3fc63-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="3fc63-121">El mensaje tiene poca importancia.</span><span class="sxs-lookup"><span data-stu-id="3fc63-121">The message has low importance.</span></span>
    
<span data-ttu-id="3fc63-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="3fc63-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="3fc63-123">El mensaje tiene importancia alta.</span><span class="sxs-lookup"><span data-stu-id="3fc63-123">The message has high importance.</span></span>
    
<span data-ttu-id="3fc63-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="3fc63-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="3fc63-125">El mensaje tiene importancia normal.</span><span class="sxs-lookup"><span data-stu-id="3fc63-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="3fc63-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3fc63-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3fc63-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="3fc63-127">Protocol specifications</span></span>

<span data-ttu-id="3fc63-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fc63-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fc63-129">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3fc63-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3fc63-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fc63-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fc63-131">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="3fc63-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3fc63-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3fc63-132">Header files</span></span>

<span data-ttu-id="3fc63-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3fc63-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="3fc63-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3fc63-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="3fc63-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="3fc63-135">Mapitags.h</span></span>
  
> <span data-ttu-id="3fc63-136">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="3fc63-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3fc63-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fc63-137">See also</span></span>



[<span data-ttu-id="3fc63-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3fc63-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3fc63-139">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="3fc63-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3fc63-140">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3fc63-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3fc63-141">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="3fc63-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

