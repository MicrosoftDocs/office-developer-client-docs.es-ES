---
title: Propiedad canónica PidTagContentIntegrityCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 53226daafd1c0a53f96db5af3432d6f34738fd93
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585814"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="8e7d3-103">Propiedad canónica PidTagContentIntegrityCheck</span><span class="sxs-lookup"><span data-stu-id="8e7d3-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="8e7d3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e7d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e7d3-105">Contiene un valor de comprobación de integridad del contenido de ASN.1 que permite a un remitente del mensaje proteger el contenido del mensaje de divulgación a destinatarios no autorizados.</span><span class="sxs-lookup"><span data-stu-id="8e7d3-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e7d3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8e7d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e7d3-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="8e7d3-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="8e7d3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8e7d3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e7d3-109">0x0c00</span><span class="sxs-lookup"><span data-stu-id="8e7d3-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="8e7d3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8e7d3-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e7d3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8e7d3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8e7d3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8e7d3-112">Area:</span></span>  <br/> |<span data-ttu-id="8e7d3-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="8e7d3-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e7d3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8e7d3-114">Remarks</span></span>

<span data-ttu-id="8e7d3-115">Esta propiedad se proporciona para el no rechazo del contenido del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8e7d3-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="8e7d3-116">Junto con **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), se asegura de que el contenido de un mensaje llega a su destino sin cambios.</span><span class="sxs-lookup"><span data-stu-id="8e7d3-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8e7d3-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e7d3-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8e7d3-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8e7d3-118">Header files</span></span>

<span data-ttu-id="8e7d3-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e7d3-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e7d3-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8e7d3-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e7d3-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8e7d3-121">Mapitags.h</span></span>
  
> <span data-ttu-id="8e7d3-122">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="8e7d3-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e7d3-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8e7d3-123">See also</span></span>



[<span data-ttu-id="8e7d3-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8e7d3-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e7d3-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8e7d3-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e7d3-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8e7d3-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e7d3-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8e7d3-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

