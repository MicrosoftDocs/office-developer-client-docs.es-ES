---
title: Propiedad canónica PidTagImplicitConversionProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7635dd24f4fbc5128d3d96556802ab2e3fe56e35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571846"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a><span data-ttu-id="faa13-103">Propiedad canónica PidTagImplicitConversionProhibited</span><span class="sxs-lookup"><span data-stu-id="faa13-103">PidTagImplicitConversionProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="faa13-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="faa13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="faa13-105">Contiene TRUE si un agente de transferencia de mensajes (MTA) no puede crear mensaje implícita las conversiones de texto.</span><span class="sxs-lookup"><span data-stu-id="faa13-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making implicit message text conversions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="faa13-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="faa13-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="faa13-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="faa13-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="faa13-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="faa13-108">Identifier:</span></span>  <br/> |<span data-ttu-id="faa13-109">0x0016</span><span class="sxs-lookup"><span data-stu-id="faa13-109">0x0016</span></span>  <br/> |
|<span data-ttu-id="faa13-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="faa13-110">Data type:</span></span>  <br/> |<span data-ttu-id="faa13-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="faa13-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="faa13-112">Área:</span><span class="sxs-lookup"><span data-stu-id="faa13-112">Area:</span></span>  <br/> |<span data-ttu-id="faa13-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="faa13-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="faa13-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="faa13-114">Remarks</span></span>

<span data-ttu-id="faa13-115">Si esta propiedad es TRUE, el sistema de mensajería no debe realizar ninguna conversión del contenido en el mensaje a menos que lo solicita explícitamente en una base por destinatario con la propiedad **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="faa13-115">If this property is TRUE, the messaging system must not perform any content conversion on the message unless it is explicitly requested on a per-recipient basis with the **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="faa13-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="faa13-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="faa13-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="faa13-117">Header files</span></span>

<span data-ttu-id="faa13-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="faa13-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="faa13-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="faa13-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="faa13-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="faa13-120">Mapitags.h</span></span>
  
> <span data-ttu-id="faa13-121">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="faa13-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="faa13-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="faa13-122">See also</span></span>



[<span data-ttu-id="faa13-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="faa13-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="faa13-124">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="faa13-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="faa13-125">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="faa13-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="faa13-126">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="faa13-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

