---
title: Propiedad canónica PidTagProcessed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProcessed
api_type:
- COM
ms.assetid: 44884f60-7e36-45b2-9712-4f9821a0dc1f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5d84e9cb693cbe732295ee1891b4219450eb09ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351439"
---
# <a name="pidtagprocessed-canonical-property"></a><span data-ttu-id="98622-103">Propiedad canónica PidTagProcessed</span><span class="sxs-lookup"><span data-stu-id="98622-103">PidTagProcessed Canonical Property</span></span>

  
  
<span data-ttu-id="98622-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98622-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98622-105">Se establece en TRUE cuando se ha procesado la solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="98622-105">Set to TRUE when the meeting request has been processed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98622-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="98622-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98622-107">PR_PROCESSED</span><span class="sxs-lookup"><span data-stu-id="98622-107">PR_PROCESSED</span></span>  <br/> |
|<span data-ttu-id="98622-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="98622-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98622-109">0x7D01</span><span class="sxs-lookup"><span data-stu-id="98622-109">0x7D01</span></span>  <br/> |
|<span data-ttu-id="98622-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="98622-110">Data type:</span></span>  <br/> |<span data-ttu-id="98622-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="98622-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="98622-112">Área:</span><span class="sxs-lookup"><span data-stu-id="98622-112">Area:</span></span>  <br/> |<span data-ttu-id="98622-113">Calendar</span><span class="sxs-lookup"><span data-stu-id="98622-113">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98622-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98622-114">Remarks</span></span>

<span data-ttu-id="98622-115">Esta propiedad garantiza que las solicitudes de reunión se procese una vez.</span><span class="sxs-lookup"><span data-stu-id="98622-115">This property ensures that meeting requests get processed once.</span></span> <span data-ttu-id="98622-116">El creador de la solicitud debe establecer esta propiedad en FALSE y el receptor debe establecerla en TRUE una vez que la solicitud esté en el calendario.</span><span class="sxs-lookup"><span data-stu-id="98622-116">The creator of the request should set this property to FALSE and the receiver should set it to TRUE once the request is in the calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="98622-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="98622-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98622-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="98622-118">Protocol specifications</span></span>

<span data-ttu-id="98622-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98622-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98622-120">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="98622-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="98622-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98622-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98622-122">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="98622-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="98622-123">[[MS-OJOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98622-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98622-124">Especifica las propiedades y operaciones permitidas para los objetos de lista de distribución personal y de contacto.</span><span class="sxs-lookup"><span data-stu-id="98622-124">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98622-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="98622-125">Header files</span></span>

<span data-ttu-id="98622-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98622-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="98622-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="98622-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="98622-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="98622-128">Mapitags.h</span></span>
  
> <span data-ttu-id="98622-129">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="98622-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98622-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98622-130">See also</span></span>



[<span data-ttu-id="98622-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="98622-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98622-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="98622-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98622-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="98622-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98622-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="98622-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

