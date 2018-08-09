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
ms.openlocfilehash: 825f6f1eff94635ca2d0f5226cfc3f421d41bcce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819249"
---
# <a name="pidtagattachmentflags-canonical-property"></a><span data-ttu-id="add71-103">Propiedad canónica PidTagAttachmentFlags</span><span class="sxs-lookup"><span data-stu-id="add71-103">PidTagAttachmentFlags Canonical Property</span></span>

  
  
<span data-ttu-id="add71-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="add71-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="add71-105">Indica un tratamiento especial para este objeto de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="add71-105">Indicates special handling for this Attachment object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="add71-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="add71-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="add71-107">PR_ATTACHMENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="add71-107">PR_ATTACHMENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="add71-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="add71-108">Identifier:</span></span>  <br/> |<span data-ttu-id="add71-109">0x7FFD</span><span class="sxs-lookup"><span data-stu-id="add71-109">0x7FFD</span></span>  <br/> |
|<span data-ttu-id="add71-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="add71-110">Data type:</span></span>  <br/> |<span data-ttu-id="add71-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="add71-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="add71-112">Área:</span><span class="sxs-lookup"><span data-stu-id="add71-112">Area:</span></span>  <br/> |<span data-ttu-id="add71-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="add71-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="add71-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="add71-114">Remarks</span></span>

<span data-ttu-id="add71-115">Debe ser 0 x 00000000, a menos que se reemplaza por otros protocolos que amplían el mensaje y los datos adjuntos de protocolo de objetos como se indicó en [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="add71-115">Must be 0x00000000, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="add71-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="add71-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="add71-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="add71-117">Protocol specifications</span></span>

<span data-ttu-id="add71-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="add71-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="add71-119">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="add71-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="add71-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="add71-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="add71-121">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="add71-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="add71-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="add71-122">Header files</span></span>

<span data-ttu-id="add71-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="add71-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="add71-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="add71-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="add71-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="add71-125">Mapitags.h</span></span>
  
> <span data-ttu-id="add71-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="add71-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="add71-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="add71-127">See also</span></span>



[<span data-ttu-id="add71-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="add71-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="add71-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="add71-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="add71-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="add71-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="add71-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="add71-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

