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
ms.openlocfilehash: 60704464beb162a614d6619b5e74d362b4af4488
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585111"
---
# <a name="pidtagordinalmost-canonical-property"></a><span data-ttu-id="89abf-103">Propiedad canónica PidTagOrdinalMost</span><span class="sxs-lookup"><span data-stu-id="89abf-103">PidTagOrdinalMost Canonical Property</span></span>

  
  
<span data-ttu-id="89abf-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89abf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89abf-105">Contiene un número positivo cuyo negativo es menor o igual que el valor de la propiedad **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) de todas las tareas en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="89abf-105">Contains a positive number whose negative is less than or equal to the value of the **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) property of all tasks in the folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89abf-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="89abf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="89abf-107">PR_ORDINAL_MOST</span><span class="sxs-lookup"><span data-stu-id="89abf-107">PR_ORDINAL_MOST</span></span>  <br/> |
|<span data-ttu-id="89abf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="89abf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="89abf-109">0x36E2</span><span class="sxs-lookup"><span data-stu-id="89abf-109">0x36E2</span></span>  <br/> |
|<span data-ttu-id="89abf-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="89abf-110">Data type:</span></span>  <br/> |<span data-ttu-id="89abf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="89abf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="89abf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="89abf-112">Area:</span></span>  <br/> |<span data-ttu-id="89abf-113">Task</span><span class="sxs-lookup"><span data-stu-id="89abf-113">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89abf-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89abf-114">Remarks</span></span>

<span data-ttu-id="89abf-115">Esta propiedad se debe actualizar para mantener esta condición siempre que cambia la propiedad **dispidTaskOrdinal** de cualquier objeto de tarea en la carpeta de una manera que podría infringir la condición.</span><span class="sxs-lookup"><span data-stu-id="89abf-115">This property must be updated to maintain this condition whenever the **dispidTaskOrdinal** property of any task object in the folder changes in a way that would violate the condition.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="89abf-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="89abf-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="89abf-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="89abf-117">Protocol specifications</span></span>

<span data-ttu-id="89abf-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89abf-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89abf-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="89abf-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="89abf-120">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89abf-120">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89abf-121">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="89abf-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
  
### <a name="header-files"></a><span data-ttu-id="89abf-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="89abf-122">Header files</span></span>

<span data-ttu-id="89abf-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89abf-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="89abf-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="89abf-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="89abf-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="89abf-125">Mapitags.h</span></span>
  
> <span data-ttu-id="89abf-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="89abf-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89abf-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="89abf-127">See also</span></span>



[<span data-ttu-id="89abf-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="89abf-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="89abf-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="89abf-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="89abf-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="89abf-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="89abf-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="89abf-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

