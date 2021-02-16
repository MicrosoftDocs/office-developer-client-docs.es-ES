---
title: Propiedad canónica PidLidLogEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bed1692a4860d59ba7a6c297ab8e88645b023a86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336928"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="79cee-103">Propiedad canónica PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="79cee-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="79cee-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79cee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79cee-105">Representa la fecha y hora de finalización del mensaje de diario.</span><span class="sxs-lookup"><span data-stu-id="79cee-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="79cee-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="79cee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="79cee-107">dispidLogEnd</span><span class="sxs-lookup"><span data-stu-id="79cee-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="79cee-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="79cee-108">Property set:</span></span>  <br/> |<span data-ttu-id="79cee-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="79cee-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="79cee-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="79cee-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="79cee-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="79cee-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="79cee-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="79cee-112">Data type:</span></span>  <br/> |<span data-ttu-id="79cee-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="79cee-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="79cee-114">Área:</span><span class="sxs-lookup"><span data-stu-id="79cee-114">Area:</span></span>  <br/> |<span data-ttu-id="79cee-115">Diario</span><span class="sxs-lookup"><span data-stu-id="79cee-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79cee-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="79cee-116">Remarks</span></span>

<span data-ttu-id="79cee-117">La hora en que la actividad finalizó en hora universal coordinada (UTC), que debe ser igual a la propiedad **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) y mayor o igual que **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="79cee-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="79cee-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="79cee-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="79cee-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="79cee-119">Protocol specifications</span></span>

<span data-ttu-id="79cee-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79cee-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79cee-121">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="79cee-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="79cee-122">[[MS-OJOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79cee-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79cee-123">Especifica las propiedades y operaciones permitidas para los diarios.</span><span class="sxs-lookup"><span data-stu-id="79cee-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="79cee-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="79cee-124">Header files</span></span>

<span data-ttu-id="79cee-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="79cee-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="79cee-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="79cee-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79cee-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="79cee-127">See also</span></span>



[<span data-ttu-id="79cee-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="79cee-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="79cee-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="79cee-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="79cee-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="79cee-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="79cee-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="79cee-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

