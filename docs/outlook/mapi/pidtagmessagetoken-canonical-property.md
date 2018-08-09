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
ms.openlocfilehash: 7357b7b98d90d08f7d14e965458703e4e193f63a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819754"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="441cf-103">Propiedad canónica PidTagMessageToken</span><span class="sxs-lookup"><span data-stu-id="441cf-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="441cf-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="441cf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="441cf-105">Contiene un token de seguridad ASN.1 para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="441cf-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="441cf-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="441cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="441cf-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="441cf-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="441cf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="441cf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="441cf-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="441cf-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="441cf-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="441cf-110">Data type:</span></span>  <br/> |<span data-ttu-id="441cf-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="441cf-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="441cf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="441cf-112">Area:</span></span>  <br/> |<span data-ttu-id="441cf-113">Propiedades de mensajería de seguro</span><span class="sxs-lookup"><span data-stu-id="441cf-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="441cf-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="441cf-114">Remarks</span></span>

<span data-ttu-id="441cf-115">Esta propiedad transmite protegida información relacionada con la seguridad de su autor a su destinatario.</span><span class="sxs-lookup"><span data-stu-id="441cf-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="441cf-116">Junto con la propiedad **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)), que garantiza la asociación de la etiqueta con el contenido del mensaje.</span><span class="sxs-lookup"><span data-stu-id="441cf-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="441cf-117">Junto con la propiedad **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)), comprueba que el contenido del mensaje no ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="441cf-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="441cf-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="441cf-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="441cf-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="441cf-119">Header files</span></span>

<span data-ttu-id="441cf-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="441cf-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="441cf-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="441cf-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="441cf-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="441cf-122">Mapitags.h</span></span>
  
> <span data-ttu-id="441cf-123">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="441cf-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="441cf-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="441cf-124">See also</span></span>



[<span data-ttu-id="441cf-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="441cf-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="441cf-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="441cf-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="441cf-127">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="441cf-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="441cf-128">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="441cf-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

