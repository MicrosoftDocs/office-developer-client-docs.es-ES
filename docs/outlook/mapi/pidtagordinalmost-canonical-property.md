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
ms.openlocfilehash: 0c2cf784ff9a86c9e2a2ce1a25b3c4b8ff7d8b75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819794"
---
# <a name="pidtagordinalmost-canonical-property"></a><span data-ttu-id="45d1b-103">Propiedad canónica PidTagOrdinalMost</span><span class="sxs-lookup"><span data-stu-id="45d1b-103">PidTagOrdinalMost Canonical Property</span></span>

  
  
<span data-ttu-id="45d1b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45d1b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45d1b-105">Contiene un número positivo cuyo negativo es menor o igual que el valor de la propiedad **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) de todas las tareas en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="45d1b-105">Contains a positive number whose negative is less than or equal to the value of the **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) property of all tasks in the folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45d1b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="45d1b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45d1b-107">PR_ORDINAL_MOST</span><span class="sxs-lookup"><span data-stu-id="45d1b-107">PR_ORDINAL_MOST</span></span>  <br/> |
|<span data-ttu-id="45d1b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="45d1b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45d1b-109">0x36E2</span><span class="sxs-lookup"><span data-stu-id="45d1b-109">0x36E2</span></span>  <br/> |
|<span data-ttu-id="45d1b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="45d1b-110">Data type:</span></span>  <br/> |<span data-ttu-id="45d1b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="45d1b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="45d1b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="45d1b-112">Area:</span></span>  <br/> |<span data-ttu-id="45d1b-113">Task</span><span class="sxs-lookup"><span data-stu-id="45d1b-113">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45d1b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="45d1b-114">Remarks</span></span>

<span data-ttu-id="45d1b-115">Esta propiedad se debe actualizar para mantener esta condición siempre que cambia la propiedad **dispidTaskOrdinal** de cualquier objeto de tarea en la carpeta de una manera que podría infringir la condición.</span><span class="sxs-lookup"><span data-stu-id="45d1b-115">This property must be updated to maintain this condition whenever the **dispidTaskOrdinal** property of any task object in the folder changes in a way that would violate the condition.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="45d1b-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="45d1b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45d1b-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="45d1b-117">Protocol specifications</span></span>

<span data-ttu-id="45d1b-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45d1b-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45d1b-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="45d1b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45d1b-120">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45d1b-120">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45d1b-121">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="45d1b-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
  
### <a name="header-files"></a><span data-ttu-id="45d1b-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="45d1b-122">Header files</span></span>

<span data-ttu-id="45d1b-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45d1b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="45d1b-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="45d1b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="45d1b-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45d1b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="45d1b-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="45d1b-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45d1b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="45d1b-127">See also</span></span>



[<span data-ttu-id="45d1b-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="45d1b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45d1b-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="45d1b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45d1b-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="45d1b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45d1b-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="45d1b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

