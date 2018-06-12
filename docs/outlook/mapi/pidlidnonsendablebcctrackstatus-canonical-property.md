---
title: Propiedad canónico PidLidNonSendableBccTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBccTrackStatus
api_type:
- COM
ms.assetid: daad8735-a3da-4a0b-9329-6eb253c281fd
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: da2bd4e87c7076872ccff708983cfbe631b27122
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818802"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a><span data-ttu-id="34e00-103">Propiedad canónico PidLidNonSendableBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="34e00-103">PidLidNonSendableBccTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="34e00-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34e00-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34e00-105">Contiene el valor para cada asistente que aparece en la propiedad **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="34e00-105">Contains the value for each attendee that is listed in the **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="34e00-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="34e00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="34e00-107">dispidNonSendBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="34e00-107">dispidNonSendBccTrackStatus</span></span>  <br/> |
|<span data-ttu-id="34e00-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="34e00-108">Property set:</span></span>  <br/> |<span data-ttu-id="34e00-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="34e00-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="34e00-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="34e00-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="34e00-111">0x00008545</span><span class="sxs-lookup"><span data-stu-id="34e00-111">0x00008545</span></span>  <br/> |
|<span data-ttu-id="34e00-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="34e00-112">Data type:</span></span>  <br/> |<span data-ttu-id="34e00-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="34e00-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="34e00-114">Área:</span><span class="sxs-lookup"><span data-stu-id="34e00-114">Area:</span></span>  <br/> |<span data-ttu-id="34e00-115">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="34e00-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34e00-116">Notas</span><span class="sxs-lookup"><span data-stu-id="34e00-116">Remarks</span></span>

<span data-ttu-id="34e00-117">Esta propiedad es necesaria sólo cuando se establece la propiedad **dispidNonSendableBCC** .</span><span class="sxs-lookup"><span data-stu-id="34e00-117">This property is required only when the **dispidNonSendableBCC** property is set.</span></span> <span data-ttu-id="34e00-118">El número de valores de esta propiedad debe ser igual que el número de valores en el **dispidNonSendableBCC**.</span><span class="sxs-lookup"><span data-stu-id="34e00-118">The number of values in this property must equal the number of values in the **dispidNonSendableBCC**.</span></span> <span data-ttu-id="34e00-119">Cada valor de esta propiedad se corresponde con el Asistente en la propiedad **dispidNonSendableBCC** en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="34e00-119">Each value in this property corresponds to the attendee in the **dispidNonSendableBCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="34e00-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="34e00-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="34e00-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="34e00-121">Protocol specifications</span></span>

<span data-ttu-id="34e00-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e00-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34e00-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="34e00-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="34e00-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e00-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34e00-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="34e00-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="34e00-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="34e00-126">Header files</span></span>

<span data-ttu-id="34e00-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34e00-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="34e00-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="34e00-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34e00-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="34e00-129">See also</span></span>



[<span data-ttu-id="34e00-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="34e00-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="34e00-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="34e00-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="34e00-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="34e00-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="34e00-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="34e00-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

