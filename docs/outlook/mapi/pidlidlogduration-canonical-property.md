---
title: Propiedad canónica PidLidLogDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogDocumentSaved
api_type:
- COM
ms.assetid: 012a3f6e-fd16-4dc9-845d-2bf4cebeaa42
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 92b9fc9dd5fdf359af06e8a8e5b21d4591933a1b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578090"
---
# <a name="pidlidlogduration-canonical-property"></a><span data-ttu-id="efc00-103">Propiedad canónica PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="efc00-103">PidLidLogDuration Canonical Property</span></span>

  
  
<span data-ttu-id="efc00-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efc00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efc00-105">Representa la duración, en minutos, de un mensaje de diario.</span><span class="sxs-lookup"><span data-stu-id="efc00-105">Represents the duration, in minutes, of a journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="efc00-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="efc00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="efc00-107">dispidLogDuration</span><span class="sxs-lookup"><span data-stu-id="efc00-107">dispidLogDuration</span></span>  <br/> |
|<span data-ttu-id="efc00-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="efc00-108">Property set:</span></span>  <br/> |<span data-ttu-id="efc00-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="efc00-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="efc00-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="efc00-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="efc00-111">0x00008707</span><span class="sxs-lookup"><span data-stu-id="efc00-111">0x00008707</span></span>  <br/> |
|<span data-ttu-id="efc00-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="efc00-112">Data type:</span></span>  <br/> |<span data-ttu-id="efc00-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="efc00-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="efc00-114">Área:</span><span class="sxs-lookup"><span data-stu-id="efc00-114">Area:</span></span>  <br/> |<span data-ttu-id="efc00-115">Journal</span><span class="sxs-lookup"><span data-stu-id="efc00-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efc00-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="efc00-116">Remarks</span></span>

<span data-ttu-id="efc00-117">La duración, en minutos, de la actividad que debe ser la diferencia entre las propiedades de **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) y **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="efc00-117">The duration, in minutes, of the activity that must be the difference between the **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) and **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="efc00-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="efc00-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="efc00-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="efc00-119">Protocol specifications</span></span>

<span data-ttu-id="efc00-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="efc00-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="efc00-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="efc00-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="efc00-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="efc00-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="efc00-123">Especifica las propiedades y operaciones que se permiten para diarios.</span><span class="sxs-lookup"><span data-stu-id="efc00-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="efc00-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="efc00-124">Header files</span></span>

<span data-ttu-id="efc00-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="efc00-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="efc00-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="efc00-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="efc00-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="efc00-127">See also</span></span>



[<span data-ttu-id="efc00-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="efc00-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="efc00-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="efc00-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="efc00-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="efc00-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="efc00-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="efc00-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

