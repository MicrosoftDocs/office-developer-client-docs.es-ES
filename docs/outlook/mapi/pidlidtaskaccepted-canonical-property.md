---
title: Propiedad canónica PidLidTaskAccepted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAccepted
api_type:
- COM
ms.assetid: 8e31f893-b639-43da-a535-662153c82d82
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0172bf0d69c3f345b592364be754f58c9e7a4420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331286"
---
# <a name="pidlidtaskaccepted-canonical-property"></a><span data-ttu-id="c0dd7-103">Propiedad canónica PidLidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="c0dd7-103">PidLidTaskAccepted Canonical Property</span></span>

  
  
<span data-ttu-id="c0dd7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0dd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0dd7-105">Indica si el usuario al que se le asigna una tarea ha respondido a una solicitud de tarea.</span><span class="sxs-lookup"><span data-stu-id="c0dd7-105">Indicates whether a task assignee has replied to a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0dd7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c0dd7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c0dd7-107">dispidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="c0dd7-107">dispidTaskAccepted</span></span>  <br/> |
|<span data-ttu-id="c0dd7-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="c0dd7-108">Property set:</span></span>  <br/> |<span data-ttu-id="c0dd7-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="c0dd7-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="c0dd7-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="c0dd7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c0dd7-111">0x00008108</span><span class="sxs-lookup"><span data-stu-id="c0dd7-111">0x00008108</span></span>  <br/> |
|<span data-ttu-id="c0dd7-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c0dd7-112">Data type:</span></span>  <br/> |<span data-ttu-id="c0dd7-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c0dd7-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c0dd7-114">Área:</span><span class="sxs-lookup"><span data-stu-id="c0dd7-114">Area:</span></span>  <br/> |<span data-ttu-id="c0dd7-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="c0dd7-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0dd7-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c0dd7-116">Remarks</span></span>

<span data-ttu-id="c0dd7-117">El cliente establece esta propiedad en FALSE para una nueva tarea, o el cliente establece esta propiedad en TRUE cuando se acepta o rechaza una tarea.</span><span class="sxs-lookup"><span data-stu-id="c0dd7-117">The client sets this property to FALSE for a new task, or the client sets this property to TRUE when a task is either accepted or rejected.</span></span> <span data-ttu-id="c0dd7-118">Si la propiedad se deja no establecida, se asume un valor de FALSE.</span><span class="sxs-lookup"><span data-stu-id="c0dd7-118">If the property is left unset, a value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c0dd7-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0dd7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c0dd7-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c0dd7-120">Protocol specifications</span></span>

<span data-ttu-id="c0dd7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0dd7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0dd7-122">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c0dd7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c0dd7-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0dd7-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0dd7-124">Especifica las propiedades y operaciones que se admiten para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="c0dd7-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c0dd7-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c0dd7-125">Header files</span></span>

<span data-ttu-id="c0dd7-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c0dd7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c0dd7-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c0dd7-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0dd7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0dd7-128">See also</span></span>



[<span data-ttu-id="c0dd7-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c0dd7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c0dd7-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="c0dd7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c0dd7-131">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c0dd7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c0dd7-132">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c0dd7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

