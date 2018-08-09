---
title: Propiedad canónica PidTagAttachmentLinkId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentLinkId
api_type:
- HeaderDef
ms.assetid: 5d0daae7-248d-459f-9d96-cb949b86f590
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e467fb7c05a647265d007429930ee522fd77b2fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819230"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="ddf6b-103">Propiedad canónica PidTagAttachmentLinkId</span><span class="sxs-lookup"><span data-stu-id="ddf6b-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="ddf6b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ddf6b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ddf6b-105">Indica el tipo de objeto de mensaje a la que está vinculado este archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="ddf6b-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ddf6b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ddf6b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ddf6b-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="ddf6b-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="ddf6b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ddf6b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ddf6b-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="ddf6b-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="ddf6b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ddf6b-110">Data type:</span></span>  <br/> |<span data-ttu-id="ddf6b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ddf6b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ddf6b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ddf6b-112">Area:</span></span>  <br/> |<span data-ttu-id="ddf6b-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="ddf6b-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddf6b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ddf6b-114">Remarks</span></span>

<span data-ttu-id="ddf6b-115">Debe ser 0, a menos que se reemplaza por el protocolo de objeto de datos adjuntos como se indicó en [[MS-OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)y otros protocolos que amplían el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ddf6b-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ddf6b-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ddf6b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ddf6b-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="ddf6b-117">Protocol specifications</span></span>

<span data-ttu-id="ddf6b-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ddf6b-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ddf6b-119">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ddf6b-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="ddf6b-120">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ddf6b-120">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ddf6b-121">Especifica las propiedades y operaciones que se permiten para objetos de diario.</span><span class="sxs-lookup"><span data-stu-id="ddf6b-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="ddf6b-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ddf6b-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ddf6b-123">Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.</span><span class="sxs-lookup"><span data-stu-id="ddf6b-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ddf6b-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ddf6b-124">Header files</span></span>

<span data-ttu-id="ddf6b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ddf6b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ddf6b-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ddf6b-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="ddf6b-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ddf6b-127">Mapitags.h</span></span>
  
> <span data-ttu-id="ddf6b-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ddf6b-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ddf6b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddf6b-129">See also</span></span>



[<span data-ttu-id="ddf6b-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ddf6b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ddf6b-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="ddf6b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ddf6b-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ddf6b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ddf6b-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="ddf6b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

