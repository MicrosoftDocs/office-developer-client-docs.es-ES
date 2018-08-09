---
title: Propiedad canónica PidTagMessageSecurityLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSecurityLabel
api_type:
- HeaderDef
ms.assetid: aae41f1b-19bb-40c7-8564-0c87a5a4e47c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 24cf7d8d7b025e5a013ce3a5c1bb03da5ae8a6a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819743"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="3ae2d-103">Propiedad canónica PidTagMessageSecurityLabel</span><span class="sxs-lookup"><span data-stu-id="3ae2d-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="3ae2d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ae2d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ae2d-105">Contiene una etiqueta de seguridad para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="3ae2d-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3ae2d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3ae2d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3ae2d-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="3ae2d-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="3ae2d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3ae2d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3ae2d-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="3ae2d-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="3ae2d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3ae2d-110">Data type:</span></span>  <br/> |<span data-ttu-id="3ae2d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3ae2d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3ae2d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3ae2d-112">Area:</span></span>  <br/> |<span data-ttu-id="3ae2d-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="3ae2d-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ae2d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3ae2d-114">Remarks</span></span>

<span data-ttu-id="3ae2d-115">Esta propiedad proporciona la base en el que la propiedad **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) protege un mensaje.</span><span class="sxs-lookup"><span data-stu-id="3ae2d-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="3ae2d-116">Su asociación con el contenido del mensaje se garantiza que el símbolo (token).</span><span class="sxs-lookup"><span data-stu-id="3ae2d-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3ae2d-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ae2d-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3ae2d-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3ae2d-118">Header files</span></span>

<span data-ttu-id="3ae2d-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3ae2d-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="3ae2d-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3ae2d-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="3ae2d-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3ae2d-121">Mapitags.h</span></span>
  
> <span data-ttu-id="3ae2d-122">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="3ae2d-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3ae2d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ae2d-123">See also</span></span>



[<span data-ttu-id="3ae2d-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3ae2d-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3ae2d-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="3ae2d-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3ae2d-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3ae2d-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3ae2d-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="3ae2d-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

