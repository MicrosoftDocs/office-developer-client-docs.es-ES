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
ms.openlocfilehash: dcfaf9f4e71a13a8697da0cac98f7ea9cc3d8708
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819609"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a><span data-ttu-id="4e856-103">Propiedad canónica PidTagImplicitConversionProhibited</span><span class="sxs-lookup"><span data-stu-id="4e856-103">PidTagImplicitConversionProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="4e856-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4e856-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4e856-105">Contiene TRUE si un agente de transferencia de mensajes (MTA) no puede crear mensaje implícita las conversiones de texto.</span><span class="sxs-lookup"><span data-stu-id="4e856-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making implicit message text conversions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e856-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4e856-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e856-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="4e856-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="4e856-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4e856-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4e856-109">0x0016</span><span class="sxs-lookup"><span data-stu-id="4e856-109">0x0016</span></span>  <br/> |
|<span data-ttu-id="4e856-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4e856-110">Data type:</span></span>  <br/> |<span data-ttu-id="4e856-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4e856-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4e856-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4e856-112">Area:</span></span>  <br/> |<span data-ttu-id="4e856-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="4e856-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e856-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e856-114">Remarks</span></span>

<span data-ttu-id="4e856-115">Si esta propiedad es TRUE, el sistema de mensajería no debe realizar ninguna conversión del contenido en el mensaje a menos que lo solicita explícitamente en una base por destinatario con la propiedad **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4e856-115">If this property is TRUE, the messaging system must not perform any content conversion on the message unless it is explicitly requested on a per-recipient basis with the **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4e856-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e856-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4e856-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4e856-117">Header files</span></span>

<span data-ttu-id="4e856-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e856-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e856-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4e856-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="4e856-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4e856-120">Mapitags.h</span></span>
  
> <span data-ttu-id="4e856-121">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="4e856-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e856-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e856-122">See also</span></span>



[<span data-ttu-id="4e856-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4e856-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e856-124">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4e856-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e856-125">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4e856-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e856-126">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="4e856-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

