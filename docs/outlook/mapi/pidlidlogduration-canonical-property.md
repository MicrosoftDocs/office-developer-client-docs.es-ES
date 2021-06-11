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
# <a name="pidlidlogduration-canonical-property"></a><span data-ttu-id="9cd51-103">Propiedad canónica PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="9cd51-103">PidLidLogDuration Canonical Property</span></span>

  
  
<span data-ttu-id="9cd51-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cd51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cd51-105">Representa la duración, en minutos, de un mensaje de diario.</span><span class="sxs-lookup"><span data-stu-id="9cd51-105">Represents the duration, in minutes, of a journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9cd51-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9cd51-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9cd51-107">dispidLogDuration</span><span class="sxs-lookup"><span data-stu-id="9cd51-107">dispidLogDuration</span></span>  <br/> |
|<span data-ttu-id="9cd51-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="9cd51-108">Property set:</span></span>  <br/> |<span data-ttu-id="9cd51-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="9cd51-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="9cd51-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="9cd51-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9cd51-111">0x00008707</span><span class="sxs-lookup"><span data-stu-id="9cd51-111">0x00008707</span></span>  <br/> |
|<span data-ttu-id="9cd51-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9cd51-112">Data type:</span></span>  <br/> |<span data-ttu-id="9cd51-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9cd51-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9cd51-114">Área:</span><span class="sxs-lookup"><span data-stu-id="9cd51-114">Area:</span></span>  <br/> |<span data-ttu-id="9cd51-115">Diario</span><span class="sxs-lookup"><span data-stu-id="9cd51-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cd51-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9cd51-116">Remarks</span></span>

<span data-ttu-id="9cd51-117">Duración, en minutos, de la actividad que debe ser la diferencia entre las propiedades **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) y **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9cd51-117">The duration, in minutes, of the activity that must be the difference between the **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) and **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9cd51-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9cd51-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9cd51-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="9cd51-119">Protocol specifications</span></span>

<span data-ttu-id="9cd51-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cd51-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cd51-121">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="9cd51-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9cd51-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cd51-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cd51-123">Especifica las propiedades y las operaciones que son permisibles para los diarios.</span><span class="sxs-lookup"><span data-stu-id="9cd51-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9cd51-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9cd51-124">Header files</span></span>

<span data-ttu-id="9cd51-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9cd51-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9cd51-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9cd51-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9cd51-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cd51-127">See also</span></span>



[<span data-ttu-id="9cd51-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9cd51-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9cd51-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9cd51-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9cd51-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9cd51-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9cd51-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9cd51-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

