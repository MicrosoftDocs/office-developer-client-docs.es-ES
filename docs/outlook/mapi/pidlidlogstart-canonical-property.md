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
ms.openlocfilehash: 55ba18a1dcbce5e3f7996184dae45a638f9531e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818788"
---
# <a name="pidlidlogstart-canonical-property"></a><span data-ttu-id="04618-103">Propiedad canónica PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="04618-103">PidLidLogStart Canonical Property</span></span>

  
  
<span data-ttu-id="04618-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="04618-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="04618-105">Representa la fecha de inicio y la hora para el mensaje de diario.</span><span class="sxs-lookup"><span data-stu-id="04618-105">Represents the start date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="04618-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="04618-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="04618-107">dispidLogStart</span><span class="sxs-lookup"><span data-stu-id="04618-107">dispidLogStart</span></span>  <br/> |
|<span data-ttu-id="04618-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="04618-108">Property set:</span></span>  <br/> |<span data-ttu-id="04618-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="04618-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="04618-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="04618-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="04618-111">0x00008706</span><span class="sxs-lookup"><span data-stu-id="04618-111">0x00008706</span></span>  <br/> |
|<span data-ttu-id="04618-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="04618-112">Data type:</span></span>  <br/> |<span data-ttu-id="04618-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="04618-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="04618-114">Área:</span><span class="sxs-lookup"><span data-stu-id="04618-114">Area:</span></span>  <br/> |<span data-ttu-id="04618-115">Journal</span><span class="sxs-lookup"><span data-stu-id="04618-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04618-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04618-116">Remarks</span></span>

<span data-ttu-id="04618-117">El tiempo en hora Universal coordinada (UTC) cuando comenzó la actividad debe ser igual a la propiedad **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="04618-117">The time in Coordinated Universal Time (UTC) when the activity began must be equal to the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="04618-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="04618-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="04618-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="04618-119">Protocol specifications</span></span>

<span data-ttu-id="04618-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04618-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04618-121">Proporciona la definición del conjunto de propiedad y referencias a las especificaciones de protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="04618-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="04618-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04618-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04618-123">Especifica las propiedades y operaciones que se permiten para diarios.</span><span class="sxs-lookup"><span data-stu-id="04618-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="04618-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="04618-124">Header files</span></span>

<span data-ttu-id="04618-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="04618-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="04618-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="04618-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04618-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="04618-127">See also</span></span>



[<span data-ttu-id="04618-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="04618-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="04618-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="04618-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="04618-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="04618-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="04618-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="04618-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

