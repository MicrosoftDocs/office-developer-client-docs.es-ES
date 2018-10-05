---
title: Propiedad canónica PidTagAttachmentFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentFlags
api_type:
- HeaderDef
ms.assetid: 42981aac-f9e7-45dd-91a2-15d9784f30aa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d494f1f14daff75be55e910da56204ecb3dbcf83
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400715"
---
# <a name="pidtagattachmentflags-canonical-property"></a><span data-ttu-id="8b1ed-103">Propiedad canónica PidTagAttachmentFlags</span><span class="sxs-lookup"><span data-stu-id="8b1ed-103">PidTagAttachmentFlags Canonical Property</span></span>

  
  
<span data-ttu-id="8b1ed-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b1ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b1ed-105">Indica un tratamiento especial para este objeto de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-105">Indicates special handling for this Attachment object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b1ed-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8b1ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b1ed-107">PR_ATTACHMENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="8b1ed-107">PR_ATTACHMENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="8b1ed-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8b1ed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b1ed-109">0x7FFD</span><span class="sxs-lookup"><span data-stu-id="8b1ed-109">0x7FFD</span></span>  <br/> |
|<span data-ttu-id="8b1ed-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8b1ed-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b1ed-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8b1ed-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8b1ed-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8b1ed-112">Area:</span></span>  <br/> |<span data-ttu-id="8b1ed-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="8b1ed-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b1ed-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8b1ed-114">Remarks</span></span>

<span data-ttu-id="8b1ed-115">Debe ser 0 x 00000000, a menos que se reemplaza por otros protocolos que amplían el mensaje y los datos adjuntos de protocolo de objetos como se indicó en [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b1ed-115">Must be 0x00000000, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8b1ed-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b1ed-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b1ed-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8b1ed-117">Protocol specifications</span></span>

<span data-ttu-id="8b1ed-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b1ed-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b1ed-119">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="8b1ed-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b1ed-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b1ed-121">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b1ed-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8b1ed-122">Header files</span></span>

<span data-ttu-id="8b1ed-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b1ed-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b1ed-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b1ed-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8b1ed-125">Mapitags.h</span></span>
  
> <span data-ttu-id="8b1ed-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8b1ed-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b1ed-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b1ed-127">See also</span></span>



[<span data-ttu-id="8b1ed-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8b1ed-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b1ed-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8b1ed-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b1ed-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8b1ed-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b1ed-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8b1ed-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

