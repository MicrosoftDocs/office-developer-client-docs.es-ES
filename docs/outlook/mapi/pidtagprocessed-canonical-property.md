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
ms.openlocfilehash: 0918f079769a70aa11e4f26551ec232308e5eef0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819941"
---
# <a name="pidtagprocessed-canonical-property"></a><span data-ttu-id="db467-103">Propiedad canónica PidTagProcessed</span><span class="sxs-lookup"><span data-stu-id="db467-103">PidTagProcessed Canonical Property</span></span>

  
  
<span data-ttu-id="db467-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="db467-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="db467-105">Se establece en TRUE cuando se han procesado la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="db467-105">Set to TRUE when the meeting request has been processed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db467-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="db467-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="db467-107">PR_PROCESSED</span><span class="sxs-lookup"><span data-stu-id="db467-107">PR_PROCESSED</span></span>  <br/> |
|<span data-ttu-id="db467-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="db467-108">Identifier:</span></span>  <br/> |<span data-ttu-id="db467-109">0x7D01</span><span class="sxs-lookup"><span data-stu-id="db467-109">0x7D01</span></span>  <br/> |
|<span data-ttu-id="db467-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="db467-110">Data type:</span></span>  <br/> |<span data-ttu-id="db467-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="db467-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="db467-112">Área:</span><span class="sxs-lookup"><span data-stu-id="db467-112">Area:</span></span>  <br/> |<span data-ttu-id="db467-113">Calendario</span><span class="sxs-lookup"><span data-stu-id="db467-113">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db467-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db467-114">Remarks</span></span>

<span data-ttu-id="db467-115">Esta propiedad se asegura de que las convocatorias de reunión se procesan una sola vez.</span><span class="sxs-lookup"><span data-stu-id="db467-115">This property ensures that meeting requests get processed once.</span></span> <span data-ttu-id="db467-116">El creador de la solicitud debe establecer esta propiedad en FALSE y el receptor debe establecer en TRUE una vez que la solicitud se encuentra en el calendario.</span><span class="sxs-lookup"><span data-stu-id="db467-116">The creator of the request should set this property to FALSE and the receiver should set it to TRUE once the request is in the calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="db467-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="db467-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="db467-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="db467-118">Protocol specifications</span></span>

<span data-ttu-id="db467-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db467-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db467-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="db467-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="db467-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db467-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db467-122">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="db467-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="db467-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db467-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db467-124">Especifica las propiedades y operaciones que se permiten para el contacto y objetos de lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="db467-124">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="db467-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="db467-125">Header files</span></span>

<span data-ttu-id="db467-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="db467-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="db467-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="db467-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="db467-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="db467-128">Mapitags.h</span></span>
  
> <span data-ttu-id="db467-129">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="db467-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db467-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="db467-130">See also</span></span>



[<span data-ttu-id="db467-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="db467-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="db467-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="db467-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="db467-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="db467-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="db467-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="db467-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

