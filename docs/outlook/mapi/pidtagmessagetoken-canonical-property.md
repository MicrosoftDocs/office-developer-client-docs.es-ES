---
title: Propiedad canónica PidTagMessageToken
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToken
api_type:
- HeaderDef
ms.assetid: fcb93346-db92-44b5-a447-59fd95f98f45
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2d832b3a53f8056c034b5e87f1f309fa3058173d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408190"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="3cf87-103">Propiedad canónica PidTagMessageToken</span><span class="sxs-lookup"><span data-stu-id="3cf87-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="3cf87-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cf87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cf87-105">Contiene un token de seguridad ASN.1 para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="3cf87-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3cf87-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3cf87-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3cf87-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="3cf87-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="3cf87-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3cf87-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3cf87-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="3cf87-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="3cf87-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3cf87-110">Data type:</span></span>  <br/> |<span data-ttu-id="3cf87-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3cf87-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3cf87-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3cf87-112">Area:</span></span>  <br/> |<span data-ttu-id="3cf87-113">Propiedades de mensajería segura</span><span class="sxs-lookup"><span data-stu-id="3cf87-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cf87-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3cf87-114">Remarks</span></span>

<span data-ttu-id="3cf87-115">Esta propiedad transmite información protegida relacionada con la seguridad desde su originador a su destinatario.</span><span class="sxs-lookup"><span data-stu-id="3cf87-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="3cf87-116">Junto con la **propiedad PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)), garantiza la asociación de la etiqueta con el contenido del mensaje.</span><span class="sxs-lookup"><span data-stu-id="3cf87-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="3cf87-117">Junto con la **propiedad PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)), comprueba que el contenido del mensaje no ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="3cf87-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3cf87-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3cf87-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3cf87-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3cf87-119">Header files</span></span>

<span data-ttu-id="3cf87-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3cf87-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="3cf87-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3cf87-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="3cf87-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3cf87-122">Mapitags.h</span></span>
  
> <span data-ttu-id="3cf87-123">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="3cf87-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3cf87-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3cf87-124">See also</span></span>



[<span data-ttu-id="3cf87-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3cf87-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3cf87-126">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3cf87-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3cf87-127">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3cf87-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3cf87-128">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="3cf87-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

