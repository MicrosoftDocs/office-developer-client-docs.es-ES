---
title: Propiedad canónico PidLidNonSendToTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendToTrackStatus
api_type:
- COM
ms.assetid: 50fec332-e7df-4bc6-8c50-59b9ca545f89
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 45d8512d48a1908d81e78b87c5975ab2da8c6c80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818811"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a><span data-ttu-id="03401-103">Propiedad canónico PidLidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="03401-103">PidLidNonSendToTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="03401-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03401-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03401-105">Contiene el valor para cada asistente que aparecen en la propiedad **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03401-105">Contains the value for each attendee listed in the **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03401-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="03401-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03401-107">dispidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="03401-107">dispidNonSendToTrackStatus</span></span>  <br/> |
|<span data-ttu-id="03401-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="03401-108">Property set:</span></span>  <br/> |<span data-ttu-id="03401-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="03401-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="03401-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="03401-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="03401-111">0x00008543</span><span class="sxs-lookup"><span data-stu-id="03401-111">0x00008543</span></span>  <br/> |
|<span data-ttu-id="03401-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="03401-112">Data type:</span></span>  <br/> |<span data-ttu-id="03401-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="03401-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="03401-114">Área:</span><span class="sxs-lookup"><span data-stu-id="03401-114">Area:</span></span>  <br/> |<span data-ttu-id="03401-115">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="03401-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03401-116">Notas</span><span class="sxs-lookup"><span data-stu-id="03401-116">Remarks</span></span>

<span data-ttu-id="03401-117">Esta propiedad es necesaria sólo cuando se establece la propiedad **dispidNonSendableTo** .</span><span class="sxs-lookup"><span data-stu-id="03401-117">This property is required only when the **dispidNonSendableTo** property is set.</span></span> <span data-ttu-id="03401-118">El número de valores de esta propiedad debe ser igual que el número de valores en **dispidNonSendableTo**.</span><span class="sxs-lookup"><span data-stu-id="03401-118">The number of values in this property must equal the number of values in **dispidNonSendableTo**.</span></span> <span data-ttu-id="03401-119">Cada valor PT_LONG en esta propiedad se corresponde con el Asistente en la propiedad **dispidNonSendableTo** en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="03401-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableTo** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="03401-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="03401-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03401-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="03401-121">Protocol specifications</span></span>

<span data-ttu-id="03401-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03401-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03401-123">Proporciona la definición del conjunto de propiedad y referencias a las especificaciones de protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="03401-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="03401-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03401-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03401-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="03401-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03401-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="03401-126">Header files</span></span>

<span data-ttu-id="03401-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03401-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="03401-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="03401-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03401-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="03401-129">See also</span></span>



[<span data-ttu-id="03401-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="03401-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03401-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="03401-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03401-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="03401-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03401-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="03401-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

