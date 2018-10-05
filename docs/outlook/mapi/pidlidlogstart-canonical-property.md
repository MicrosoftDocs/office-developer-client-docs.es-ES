---
title: Propiedad canónica PidLidLogStart
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogStart
api_type:
- COM
ms.assetid: b8c0c871-51d8-4752-ad4b-607463a9f837
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dd5805cb0ee6b172506a532a513d06f57c583eee
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396270"
---
# <a name="pidlidlogstart-canonical-property"></a><span data-ttu-id="e5ba3-103">Propiedad canónica PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="e5ba3-103">PidLidLogStart Canonical Property</span></span>

  
  
<span data-ttu-id="e5ba3-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5ba3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5ba3-105">Representa la fecha de inicio y la hora para el mensaje de diario.</span><span class="sxs-lookup"><span data-stu-id="e5ba3-105">Represents the start date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e5ba3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e5ba3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e5ba3-107">dispidLogStart</span><span class="sxs-lookup"><span data-stu-id="e5ba3-107">dispidLogStart</span></span>  <br/> |
|<span data-ttu-id="e5ba3-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e5ba3-108">Property set:</span></span>  <br/> |<span data-ttu-id="e5ba3-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="e5ba3-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="e5ba3-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="e5ba3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e5ba3-111">0x00008706</span><span class="sxs-lookup"><span data-stu-id="e5ba3-111">0x00008706</span></span>  <br/> |
|<span data-ttu-id="e5ba3-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e5ba3-112">Data type:</span></span>  <br/> |<span data-ttu-id="e5ba3-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e5ba3-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e5ba3-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e5ba3-114">Area:</span></span>  <br/> |<span data-ttu-id="e5ba3-115">Journal</span><span class="sxs-lookup"><span data-stu-id="e5ba3-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5ba3-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e5ba3-116">Remarks</span></span>

<span data-ttu-id="e5ba3-117">El tiempo en hora Universal coordinada (UTC) cuando comenzó la actividad debe ser igual a la propiedad **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e5ba3-117">The time in Coordinated Universal Time (UTC) when the activity began must be equal to the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e5ba3-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5ba3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e5ba3-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e5ba3-119">Protocol specifications</span></span>

<span data-ttu-id="e5ba3-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5ba3-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5ba3-121">Proporciona la definición del conjunto de propiedad y referencias a las especificaciones de protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e5ba3-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e5ba3-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5ba3-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5ba3-123">Especifica las propiedades y operaciones que se permiten para diarios.</span><span class="sxs-lookup"><span data-stu-id="e5ba3-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e5ba3-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e5ba3-124">Header files</span></span>

<span data-ttu-id="e5ba3-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5ba3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e5ba3-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e5ba3-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5ba3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5ba3-127">See also</span></span>



[<span data-ttu-id="e5ba3-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e5ba3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e5ba3-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e5ba3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e5ba3-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e5ba3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e5ba3-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e5ba3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

