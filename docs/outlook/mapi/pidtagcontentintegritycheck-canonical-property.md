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
ms.openlocfilehash: 30ed8053c9c3d77f4831da37ddd2456ad0564a5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415729"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="07fd5-103">Propiedad canónica PidTagContentIntegrityCheck</span><span class="sxs-lookup"><span data-stu-id="07fd5-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="07fd5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07fd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07fd5-105">Contiene un valor de comprobación de integridad de contenido ASN. 1 que permite que el remitente de un mensaje proteja el contenido de los mensajes para que no se divulgue a destinatarios no autorizados.</span><span class="sxs-lookup"><span data-stu-id="07fd5-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07fd5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="07fd5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="07fd5-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="07fd5-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="07fd5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="07fd5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="07fd5-109">0x0C00</span><span class="sxs-lookup"><span data-stu-id="07fd5-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="07fd5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="07fd5-110">Data type:</span></span>  <br/> |<span data-ttu-id="07fd5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="07fd5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="07fd5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="07fd5-112">Area:</span></span>  <br/> |<span data-ttu-id="07fd5-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="07fd5-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07fd5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07fd5-114">Remarks</span></span>

<span data-ttu-id="07fd5-115">Esta propiedad proporciona el no rechazo del contenido del mensaje.</span><span class="sxs-lookup"><span data-stu-id="07fd5-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="07fd5-116">Junto con **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), garantiza que el contenido de un mensaje llega a su destino sin cambios.</span><span class="sxs-lookup"><span data-stu-id="07fd5-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="07fd5-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="07fd5-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="07fd5-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="07fd5-118">Header files</span></span>

<span data-ttu-id="07fd5-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="07fd5-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="07fd5-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="07fd5-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="07fd5-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="07fd5-121">Mapitags.h</span></span>
  
> <span data-ttu-id="07fd5-122">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="07fd5-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07fd5-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="07fd5-123">See also</span></span>



[<span data-ttu-id="07fd5-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="07fd5-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07fd5-125">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="07fd5-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07fd5-126">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="07fd5-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07fd5-127">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="07fd5-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

