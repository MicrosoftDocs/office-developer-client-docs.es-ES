---
title: Propiedad canónica PidLidNonSendCcTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendCcTrackStatus
api_type:
- COM
ms.assetid: e2654fad-444b-45bc-976d-3c5cbbc81b84
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 10b6009bc86df4232c995e7c6bca463f45999528
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319673"
---
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a><span data-ttu-id="b91cf-103">Propiedad canónica PidLidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="b91cf-103">PidLidNonSendCcTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="b91cf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b91cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b91cf-105">Contiene el valor de cada asistente que aparece en la **propiedad dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b91cf-105">Contains the value for each attendee listed in the **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b91cf-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b91cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b91cf-107">dispidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="b91cf-107">dispidNonSendCcTrackStatus</span></span>  <br/> |
|<span data-ttu-id="b91cf-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="b91cf-108">Property set:</span></span>  <br/> |<span data-ttu-id="b91cf-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b91cf-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b91cf-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="b91cf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b91cf-111">0x00008544</span><span class="sxs-lookup"><span data-stu-id="b91cf-111">0x00008544</span></span>  <br/> |
|<span data-ttu-id="b91cf-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b91cf-112">Data type:</span></span>  <br/> |<span data-ttu-id="b91cf-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="b91cf-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="b91cf-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b91cf-114">Area:</span></span>  <br/> |<span data-ttu-id="b91cf-115">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="b91cf-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b91cf-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b91cf-116">Remarks</span></span>

<span data-ttu-id="b91cf-117">Esta propiedad solo es necesaria cuando se establece la propiedad **dispidNonSendableCC.**</span><span class="sxs-lookup"><span data-stu-id="b91cf-117">This property is required only when the **dispidNonSendableCC** property is set.</span></span> <span data-ttu-id="b91cf-118">El número de valores de esta propiedad debe ser igual al número de valores de **dispidNonSendableCC**.</span><span class="sxs-lookup"><span data-stu-id="b91cf-118">The number of values in this property must equal the number of values in **dispidNonSendableCC**.</span></span> <span data-ttu-id="b91cf-119">Cada PT_LONG valor de esta propiedad corresponde al asistente de la propiedad **dispidNonSendableCC** en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="b91cf-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b91cf-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b91cf-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b91cf-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="b91cf-121">Protocol specifications</span></span>

<span data-ttu-id="b91cf-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b91cf-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b91cf-123">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="b91cf-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b91cf-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b91cf-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b91cf-125">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="b91cf-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b91cf-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b91cf-126">Header files</span></span>

<span data-ttu-id="b91cf-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b91cf-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b91cf-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b91cf-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b91cf-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b91cf-129">See also</span></span>



[<span data-ttu-id="b91cf-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b91cf-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b91cf-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b91cf-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b91cf-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b91cf-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b91cf-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="b91cf-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

