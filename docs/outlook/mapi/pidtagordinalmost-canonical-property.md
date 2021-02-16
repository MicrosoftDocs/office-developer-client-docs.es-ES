---
title: Propiedad canónica PidTagOrdinalMost
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOrdinalMost
api_type:
- COM
ms.assetid: c18de08b-8c28-4cdf-bd2e-b9c650cd6da6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 31f39cfbd0e993bfc28003fd64e8af97e7e76818
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329190"
---
# <a name="pidtagordinalmost-canonical-property"></a><span data-ttu-id="902c5-103">Propiedad canónica PidTagOrdinalMost</span><span class="sxs-lookup"><span data-stu-id="902c5-103">PidTagOrdinalMost Canonical Property</span></span>

  
  
<span data-ttu-id="902c5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="902c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="902c5-105">Contiene un número positivo cuyo negativo es menor o igual que el valor de la propiedad **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) de todas las tareas de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="902c5-105">Contains a positive number whose negative is less than or equal to the value of the **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) property of all tasks in the folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="902c5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="902c5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="902c5-107">PR_ORDINAL_MOST</span><span class="sxs-lookup"><span data-stu-id="902c5-107">PR_ORDINAL_MOST</span></span>  <br/> |
|<span data-ttu-id="902c5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="902c5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="902c5-109">0x36E2</span><span class="sxs-lookup"><span data-stu-id="902c5-109">0x36E2</span></span>  <br/> |
|<span data-ttu-id="902c5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="902c5-110">Data type:</span></span>  <br/> |<span data-ttu-id="902c5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="902c5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="902c5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="902c5-112">Area:</span></span>  <br/> |<span data-ttu-id="902c5-113">Task</span><span class="sxs-lookup"><span data-stu-id="902c5-113">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="902c5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="902c5-114">Remarks</span></span>

<span data-ttu-id="902c5-115">Esta propiedad debe actualizarse para mantener esta condición siempre que la propiedad **dispidTaskOrdinal** de cualquier objeto de tarea de la carpeta cambie de forma que infrinja la condición.</span><span class="sxs-lookup"><span data-stu-id="902c5-115">This property must be updated to maintain this condition whenever the **dispidTaskOrdinal** property of any task object in the folder changes in a way that would violate the condition.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="902c5-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="902c5-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="902c5-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="902c5-117">Protocol specifications</span></span>

<span data-ttu-id="902c5-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="902c5-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="902c5-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="902c5-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="902c5-120">[[MS-OJOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="902c5-120">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="902c5-121">Especifica las propiedades y operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="902c5-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
  
### <a name="header-files"></a><span data-ttu-id="902c5-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="902c5-122">Header files</span></span>

<span data-ttu-id="902c5-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="902c5-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="902c5-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="902c5-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="902c5-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="902c5-125">Mapitags.h</span></span>
  
> <span data-ttu-id="902c5-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="902c5-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="902c5-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="902c5-127">See also</span></span>



[<span data-ttu-id="902c5-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="902c5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="902c5-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="902c5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="902c5-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="902c5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="902c5-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="902c5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

