---
title: Propiedad canónica PidTagFlagCompleteTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: efaa8cf84204234697431a190a5cb6745b55ecae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819491"
---
# <a name="pidtagflagcompletetime-canonical-property"></a><span data-ttu-id="6b9d7-103">Propiedad canónica PidTagFlagCompleteTime</span><span class="sxs-lookup"><span data-stu-id="6b9d7-103">PidTagFlagCompleteTime Canonical Property</span></span>

  
  
<span data-ttu-id="6b9d7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6b9d7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6b9d7-105">Especifica la fecha y hora en Universal coordinada (UTC) que el objeto de mensaje se marcó como completada.</span><span class="sxs-lookup"><span data-stu-id="6b9d7-105">Specifies the date and time in Coordinated Universal Time (UTC) that the message object was flagged as completed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6b9d7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6b9d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6b9d7-107">PR_FLAG_COMPLETE_TIME</span><span class="sxs-lookup"><span data-stu-id="6b9d7-107">PR_FLAG_COMPLETE_TIME</span></span>  <br/> |
|<span data-ttu-id="6b9d7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6b9d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6b9d7-109">0x1091</span><span class="sxs-lookup"><span data-stu-id="6b9d7-109">0x1091</span></span>  <br/> |
|<span data-ttu-id="6b9d7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6b9d7-110">Data type:</span></span>  <br/> |<span data-ttu-id="6b9d7-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="6b9d7-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="6b9d7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6b9d7-112">Area:</span></span>  <br/> |<span data-ttu-id="6b9d7-113">Varios</span><span class="sxs-lookup"><span data-stu-id="6b9d7-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b9d7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b9d7-114">Remarks</span></span>

<span data-ttu-id="6b9d7-115">Esta propiedad se elimina si el objeto de mensaje está marcado no completado.</span><span class="sxs-lookup"><span data-stu-id="6b9d7-115">This property is deleted if the message object is not flagged complete.</span></span> <span data-ttu-id="6b9d7-116">Resolución más pequeña de la hora debe ser minutos (el valor debe ser un múltiplo de 600,000,000).</span><span class="sxs-lookup"><span data-stu-id="6b9d7-116">The time's smallest resolution must be minutes (the value must be a multiple of 600,000,000).</span></span> <span data-ttu-id="6b9d7-117">Esta propiedad no debe existir si el objeto es un objeto relacionado con la reunión y no debe existir en un objeto task.</span><span class="sxs-lookup"><span data-stu-id="6b9d7-117">This property must not exist if the object is a meeting-related object, and it should not exist on a task object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6b9d7-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b9d7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6b9d7-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6b9d7-119">Protocol specifications</span></span>

<span data-ttu-id="6b9d7-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b9d7-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b9d7-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6b9d7-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6b9d7-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b9d7-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b9d7-123">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="6b9d7-123">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6b9d7-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6b9d7-124">Header files</span></span>

<span data-ttu-id="6b9d7-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b9d7-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="6b9d7-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6b9d7-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="6b9d7-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6b9d7-127">Mapitags.h</span></span>
  
> <span data-ttu-id="6b9d7-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="6b9d7-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6b9d7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b9d7-129">See also</span></span>



[<span data-ttu-id="6b9d7-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6b9d7-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6b9d7-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6b9d7-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6b9d7-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6b9d7-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6b9d7-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="6b9d7-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

