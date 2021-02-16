---
title: Propiedad canónica PidLidNonSendToTrackStatus
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bdfbd553e130a4e463017168a76dc94fc0df827b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331370"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a><span data-ttu-id="58533-103">Propiedad canónica PidLidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="58533-103">PidLidNonSendToTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="58533-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58533-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58533-105">Contiene el valor de cada asistente enumerado en la propiedad **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="58533-105">Contains the value for each attendee listed in the **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="58533-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="58533-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58533-107">dispidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="58533-107">dispidNonSendToTrackStatus</span></span>  <br/> |
|<span data-ttu-id="58533-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="58533-108">Property set:</span></span>  <br/> |<span data-ttu-id="58533-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="58533-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="58533-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="58533-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="58533-111">0x00008543</span><span class="sxs-lookup"><span data-stu-id="58533-111">0x00008543</span></span>  <br/> |
|<span data-ttu-id="58533-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="58533-112">Data type:</span></span>  <br/> |<span data-ttu-id="58533-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="58533-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="58533-114">Área:</span><span class="sxs-lookup"><span data-stu-id="58533-114">Area:</span></span>  <br/> |<span data-ttu-id="58533-115">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="58533-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58533-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58533-116">Remarks</span></span>

<span data-ttu-id="58533-117">Esta propiedad solo es necesaria cuando se establece la propiedad **dispidNonSendableTo** .</span><span class="sxs-lookup"><span data-stu-id="58533-117">This property is required only when the **dispidNonSendableTo** property is set.</span></span> <span data-ttu-id="58533-118">El número de valores de esta propiedad debe ser igual al número de valores de **dispidNonSendableTo**.</span><span class="sxs-lookup"><span data-stu-id="58533-118">The number of values in this property must equal the number of values in **dispidNonSendableTo**.</span></span> <span data-ttu-id="58533-119">Cada PT_LONG valor de esta propiedad corresponde al asistente de la propiedad **dispidNonSendableTo** en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="58533-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableTo** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="58533-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="58533-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58533-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="58533-121">Protocol specifications</span></span>

<span data-ttu-id="58533-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58533-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58533-123">Proporciona la definición del conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="58533-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="58533-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58533-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58533-125">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="58533-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58533-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="58533-126">Header files</span></span>

<span data-ttu-id="58533-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58533-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="58533-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="58533-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58533-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="58533-129">See also</span></span>



[<span data-ttu-id="58533-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="58533-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58533-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="58533-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58533-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="58533-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58533-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="58533-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

