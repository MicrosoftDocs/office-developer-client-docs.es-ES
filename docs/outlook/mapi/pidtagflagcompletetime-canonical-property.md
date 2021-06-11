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
ms.openlocfilehash: 5dd0d4c19f30e189218b1aeddd333df58e42102a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316292"
---
# <a name="pidtagflagcompletetime-canonical-property"></a><span data-ttu-id="296c7-103">Propiedad canónica PidTagFlagCompleteTime</span><span class="sxs-lookup"><span data-stu-id="296c7-103">PidTagFlagCompleteTime Canonical Property</span></span>

  
  
<span data-ttu-id="296c7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="296c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="296c7-105">Especifica la fecha y hora en la hora universal coordinada (UTC) que el objeto de mensaje se marcó como completado.</span><span class="sxs-lookup"><span data-stu-id="296c7-105">Specifies the date and time in Coordinated Universal Time (UTC) that the message object was flagged as completed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="296c7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="296c7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="296c7-107">PR_FLAG_COMPLETE_TIME</span><span class="sxs-lookup"><span data-stu-id="296c7-107">PR_FLAG_COMPLETE_TIME</span></span>  <br/> |
|<span data-ttu-id="296c7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="296c7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="296c7-109">0x1091</span><span class="sxs-lookup"><span data-stu-id="296c7-109">0x1091</span></span>  <br/> |
|<span data-ttu-id="296c7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="296c7-110">Data type:</span></span>  <br/> |<span data-ttu-id="296c7-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="296c7-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="296c7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="296c7-112">Area:</span></span>  <br/> |<span data-ttu-id="296c7-113">Varios</span><span class="sxs-lookup"><span data-stu-id="296c7-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="296c7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="296c7-114">Remarks</span></span>

<span data-ttu-id="296c7-115">Esta propiedad se elimina si el objeto de mensaje no está marcado completo.</span><span class="sxs-lookup"><span data-stu-id="296c7-115">This property is deleted if the message object is not flagged complete.</span></span> <span data-ttu-id="296c7-116">La resolución más pequeña del tiempo debe ser minutos (el valor debe ser un múltiplo de 600 000 000).</span><span class="sxs-lookup"><span data-stu-id="296c7-116">The time's smallest resolution must be minutes (the value must be a multiple of 600,000,000).</span></span> <span data-ttu-id="296c7-117">Esta propiedad no debe existir si el objeto es un objeto relacionado con la reunión y no debe existir en un objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="296c7-117">This property must not exist if the object is a meeting-related object, and it should not exist on a task object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="296c7-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="296c7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="296c7-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="296c7-119">Protocol specifications</span></span>

<span data-ttu-id="296c7-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="296c7-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="296c7-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="296c7-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="296c7-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="296c7-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="296c7-123">Especifica las propiedades y las operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="296c7-123">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="296c7-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="296c7-124">Header files</span></span>

<span data-ttu-id="296c7-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="296c7-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="296c7-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="296c7-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="296c7-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="296c7-127">Mapitags.h</span></span>
  
> <span data-ttu-id="296c7-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="296c7-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="296c7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="296c7-129">See also</span></span>



[<span data-ttu-id="296c7-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="296c7-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="296c7-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="296c7-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="296c7-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="296c7-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="296c7-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="296c7-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

