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
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="9ec11-103">Propiedad canónica PidTagAttachmentLinkId</span><span class="sxs-lookup"><span data-stu-id="9ec11-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="9ec11-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ec11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ec11-105">Indica el tipo de objeto de mensaje al que se vinculan estos datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9ec11-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ec11-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9ec11-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ec11-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="9ec11-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="9ec11-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9ec11-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ec11-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="9ec11-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="9ec11-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9ec11-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ec11-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9ec11-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9ec11-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9ec11-112">Area:</span></span>  <br/> |<span data-ttu-id="9ec11-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="9ec11-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ec11-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ec11-114">Remarks</span></span>

<span data-ttu-id="9ec11-115">Debe ser 0, a menos que lo reemplacen otros protocolos que amplíen el protocolo de objetos de mensajes y datos adJuntos como se indica en [[ms-OXCMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9ec11-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9ec11-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ec11-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ec11-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9ec11-117">Protocol specifications</span></span>

<span data-ttu-id="9ec11-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ec11-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ec11-119">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9ec11-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9ec11-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ec11-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ec11-121">Especifica las propiedades y operaciones que se admiten para los objetos de diario.</span><span class="sxs-lookup"><span data-stu-id="9ec11-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="9ec11-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ec11-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ec11-123">Especifica las propiedades y el modelo de interacción para el correo electrónico y otros recordatorios de objetos.</span><span class="sxs-lookup"><span data-stu-id="9ec11-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ec11-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9ec11-124">Header files</span></span>

<span data-ttu-id="9ec11-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9ec11-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ec11-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9ec11-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ec11-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9ec11-127">Mapitags.h</span></span>
  
> <span data-ttu-id="9ec11-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9ec11-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ec11-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ec11-129">See also</span></span>



[<span data-ttu-id="9ec11-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9ec11-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ec11-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="9ec11-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ec11-132">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9ec11-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ec11-133">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9ec11-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

