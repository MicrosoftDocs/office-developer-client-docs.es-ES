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
ms.openlocfilehash: 623b4195b7128667b9aaa6bc97d03c21d62c690a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345699"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="3f179-103">Propiedad canónica PidTagAttachmentLinkId</span><span class="sxs-lookup"><span data-stu-id="3f179-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="3f179-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f179-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f179-105">Indica el tipo de objeto Message al que están vinculados estos datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="3f179-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f179-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3f179-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3f179-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="3f179-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="3f179-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3f179-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3f179-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="3f179-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="3f179-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3f179-110">Data type:</span></span>  <br/> |<span data-ttu-id="3f179-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3f179-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3f179-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3f179-112">Area:</span></span>  <br/> |<span data-ttu-id="3f179-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="3f179-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f179-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f179-114">Remarks</span></span>

<span data-ttu-id="3f179-115">Debe ser 0, a menos que se invalide por otros protocolos que amplían el protocolo de objetos Message y Attachment, como se indica en [[MS-OXCMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f179-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3f179-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f179-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3f179-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="3f179-117">Protocol specifications</span></span>

<span data-ttu-id="3f179-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f179-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3f179-119">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="3f179-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="3f179-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f179-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3f179-121">Especifica las propiedades y las operaciones que son permisibles para los objetos de diario.</span><span class="sxs-lookup"><span data-stu-id="3f179-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="3f179-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f179-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3f179-123">Especifica las propiedades y el modelo de interacción para el correo electrónico y otros avisos de objetos.</span><span class="sxs-lookup"><span data-stu-id="3f179-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3f179-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3f179-124">Header files</span></span>

<span data-ttu-id="3f179-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f179-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="3f179-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3f179-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="3f179-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3f179-127">Mapitags.h</span></span>
  
> <span data-ttu-id="3f179-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="3f179-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3f179-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f179-129">See also</span></span>



[<span data-ttu-id="3f179-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3f179-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3f179-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3f179-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3f179-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3f179-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3f179-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="3f179-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

