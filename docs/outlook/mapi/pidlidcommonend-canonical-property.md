---
title: Propiedad canónica PidLidCommonEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonEnd
api_type:
- COM
ms.assetid: c89f388a-1585-4bed-91b4-1b0c268292f3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fc3849ac972ce7e3efbfa981ff950ee3615cb533
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571468"
---
# <a name="pidlidcommonend-canonical-property"></a><span data-ttu-id="f9977-103">Propiedad canónica PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="f9977-103">PidLidCommonEnd Canonical Property</span></span>

  
  
<span data-ttu-id="f9977-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9977-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9977-105">Representa la fecha de finalización y la hora de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f9977-105">Represents the end date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9977-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f9977-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f9977-107">dispidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="f9977-107">dispidCommonEnd</span></span>  <br/> |
|<span data-ttu-id="f9977-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="f9977-108">Property set:</span></span>  <br/> |<span data-ttu-id="f9977-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f9977-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f9977-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="f9977-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f9977-111">0x00008517</span><span class="sxs-lookup"><span data-stu-id="f9977-111">0x00008517</span></span>  <br/> |
|<span data-ttu-id="f9977-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f9977-112">Data type:</span></span>  <br/> |<span data-ttu-id="f9977-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="f9977-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="f9977-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f9977-114">Area:</span></span>  <br/> |<span data-ttu-id="f9977-115">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="f9977-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9977-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9977-116">Remarks</span></span>

<span data-ttu-id="f9977-117">Esta propiedad indica la hora de finalización de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f9977-117">This property indicates the end time for an item.</span></span> <span data-ttu-id="f9977-118">Debe ser mayor o igual que el valor de la propiedad **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f9977-118">It must be greater than or equal to the value of the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="f9977-119">Este valor debe ser el equivalente de hora Universal coordinada (UTC) de la propiedad **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f9977-119">This value must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f9977-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9977-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f9977-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f9977-121">Protocol specifications</span></span>

<span data-ttu-id="f9977-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9977-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9977-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f9977-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f9977-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9977-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9977-125">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f9977-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="f9977-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9977-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9977-127">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="f9977-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f9977-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f9977-128">Header files</span></span>

<span data-ttu-id="f9977-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f9977-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="f9977-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f9977-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f9977-131">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f9977-131">See also</span></span>



[<span data-ttu-id="f9977-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f9977-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f9977-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f9977-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f9977-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f9977-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f9977-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f9977-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

