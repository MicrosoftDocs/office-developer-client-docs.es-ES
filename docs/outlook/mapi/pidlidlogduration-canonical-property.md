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
ms.openlocfilehash: 6f25c1a72882f9236d56532b7259f51512734945
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336921"
---
# <a name="pidlidlogduration-canonical-property"></a><span data-ttu-id="afc6c-103">Propiedad canónica PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="afc6c-103">PidLidLogDuration Canonical Property</span></span>

  
  
<span data-ttu-id="afc6c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="afc6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="afc6c-105">Representa la duración, en minutos, de un mensaje del diario.</span><span class="sxs-lookup"><span data-stu-id="afc6c-105">Represents the duration, in minutes, of a journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="afc6c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="afc6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="afc6c-107">dispidLogDuration</span><span class="sxs-lookup"><span data-stu-id="afc6c-107">dispidLogDuration</span></span>  <br/> |
|<span data-ttu-id="afc6c-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="afc6c-108">Property set:</span></span>  <br/> |<span data-ttu-id="afc6c-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="afc6c-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="afc6c-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="afc6c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="afc6c-111">0x00008707</span><span class="sxs-lookup"><span data-stu-id="afc6c-111">0x00008707</span></span>  <br/> |
|<span data-ttu-id="afc6c-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="afc6c-112">Data type:</span></span>  <br/> |<span data-ttu-id="afc6c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="afc6c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="afc6c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="afc6c-114">Area:</span></span>  <br/> |<span data-ttu-id="afc6c-115">Diario</span><span class="sxs-lookup"><span data-stu-id="afc6c-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="afc6c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="afc6c-116">Remarks</span></span>

<span data-ttu-id="afc6c-117">La duración, en minutos, de la actividad que debe ser la diferencia entre las propiedades **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) y **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="afc6c-117">The duration, in minutes, of the activity that must be the difference between the **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) and **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="afc6c-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="afc6c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="afc6c-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="afc6c-119">Protocol specifications</span></span>

<span data-ttu-id="afc6c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="afc6c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="afc6c-121">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="afc6c-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="afc6c-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="afc6c-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="afc6c-123">Especifica las propiedades y operaciones que se admiten para los diarios.</span><span class="sxs-lookup"><span data-stu-id="afc6c-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="afc6c-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="afc6c-124">Header files</span></span>

<span data-ttu-id="afc6c-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="afc6c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="afc6c-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="afc6c-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="afc6c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="afc6c-127">See also</span></span>



[<span data-ttu-id="afc6c-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="afc6c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="afc6c-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="afc6c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="afc6c-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="afc6c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="afc6c-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="afc6c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

