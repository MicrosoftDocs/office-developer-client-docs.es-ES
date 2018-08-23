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
ms.openlocfilehash: 359eb4ea4cbbcf6244bf3cca2f3a66b369bce6e0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586679"
---
# <a name="pidlidlogstart-canonical-property"></a><span data-ttu-id="273dc-103">Propiedad canónica PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="273dc-103">PidLidLogStart Canonical Property</span></span>

  
  
<span data-ttu-id="273dc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="273dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="273dc-105">Representa la fecha de inicio y la hora para el mensaje de diario.</span><span class="sxs-lookup"><span data-stu-id="273dc-105">Represents the start date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="273dc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="273dc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="273dc-107">dispidLogStart</span><span class="sxs-lookup"><span data-stu-id="273dc-107">dispidLogStart</span></span>  <br/> |
|<span data-ttu-id="273dc-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="273dc-108">Property set:</span></span>  <br/> |<span data-ttu-id="273dc-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="273dc-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="273dc-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="273dc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="273dc-111">0x00008706</span><span class="sxs-lookup"><span data-stu-id="273dc-111">0x00008706</span></span>  <br/> |
|<span data-ttu-id="273dc-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="273dc-112">Data type:</span></span>  <br/> |<span data-ttu-id="273dc-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="273dc-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="273dc-114">Área:</span><span class="sxs-lookup"><span data-stu-id="273dc-114">Area:</span></span>  <br/> |<span data-ttu-id="273dc-115">Journal</span><span class="sxs-lookup"><span data-stu-id="273dc-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="273dc-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="273dc-116">Remarks</span></span>

<span data-ttu-id="273dc-117">El tiempo en hora Universal coordinada (UTC) cuando comenzó la actividad debe ser igual a la propiedad **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="273dc-117">The time in Coordinated Universal Time (UTC) when the activity began must be equal to the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="273dc-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="273dc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="273dc-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="273dc-119">Protocol specifications</span></span>

<span data-ttu-id="273dc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="273dc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="273dc-121">Proporciona la definición del conjunto de propiedad y referencias a las especificaciones de protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="273dc-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="273dc-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="273dc-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="273dc-123">Especifica las propiedades y operaciones que se permiten para diarios.</span><span class="sxs-lookup"><span data-stu-id="273dc-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="273dc-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="273dc-124">Header files</span></span>

<span data-ttu-id="273dc-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="273dc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="273dc-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="273dc-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="273dc-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="273dc-127">See also</span></span>



[<span data-ttu-id="273dc-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="273dc-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="273dc-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="273dc-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="273dc-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="273dc-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="273dc-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="273dc-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

