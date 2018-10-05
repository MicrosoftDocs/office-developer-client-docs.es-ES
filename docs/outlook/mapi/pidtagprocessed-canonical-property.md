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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385028"
---
# <a name="pidtagprocessed-canonical-property"></a><span data-ttu-id="d6250-103">Propiedad canónica PidTagProcessed</span><span class="sxs-lookup"><span data-stu-id="d6250-103">PidTagProcessed Canonical Property</span></span>

  
  
<span data-ttu-id="d6250-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6250-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6250-105">Se establece en TRUE cuando se han procesado la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="d6250-105">Set to TRUE when the meeting request has been processed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d6250-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d6250-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6250-107">PR_PROCESSED</span><span class="sxs-lookup"><span data-stu-id="d6250-107">PR_PROCESSED</span></span>  <br/> |
|<span data-ttu-id="d6250-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d6250-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6250-109">0x7D01</span><span class="sxs-lookup"><span data-stu-id="d6250-109">0x7D01</span></span>  <br/> |
|<span data-ttu-id="d6250-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d6250-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6250-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d6250-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d6250-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d6250-112">Area:</span></span>  <br/> |<span data-ttu-id="d6250-113">Calendario</span><span class="sxs-lookup"><span data-stu-id="d6250-113">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6250-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d6250-114">Remarks</span></span>

<span data-ttu-id="d6250-115">Esta propiedad se asegura de que las convocatorias de reunión se procesan una sola vez.</span><span class="sxs-lookup"><span data-stu-id="d6250-115">This property ensures that meeting requests get processed once.</span></span> <span data-ttu-id="d6250-116">El creador de la solicitud debe establecer esta propiedad en FALSE y el receptor debe establecer en TRUE una vez que la solicitud se encuentra en el calendario.</span><span class="sxs-lookup"><span data-stu-id="d6250-116">The creator of the request should set this property to FALSE and the receiver should set it to TRUE once the request is in the calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d6250-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6250-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6250-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d6250-118">Protocol specifications</span></span>

<span data-ttu-id="d6250-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6250-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6250-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d6250-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d6250-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6250-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6250-122">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6250-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="d6250-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6250-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6250-124">Especifica las propiedades y operaciones que se permiten para el contacto y objetos de lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="d6250-124">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6250-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d6250-125">Header files</span></span>

<span data-ttu-id="d6250-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6250-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6250-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d6250-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6250-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d6250-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d6250-129">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="d6250-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6250-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6250-130">See also</span></span>



[<span data-ttu-id="d6250-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d6250-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6250-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d6250-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6250-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d6250-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6250-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d6250-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

