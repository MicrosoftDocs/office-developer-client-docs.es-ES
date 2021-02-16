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
ms.openlocfilehash: a0e18ef529b65317abd9446408ed73638c792809
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420671"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a><span data-ttu-id="34f94-103">Propiedad canónica PidTagImplicitConversionProhibited</span><span class="sxs-lookup"><span data-stu-id="34f94-103">PidTagImplicitConversionProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="34f94-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34f94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34f94-105">Contiene TRUE si un agente de transferencia de mensajes (MTA) no puede realizar conversiones implícitas de texto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="34f94-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making implicit message text conversions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="34f94-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="34f94-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="34f94-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="34f94-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="34f94-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="34f94-108">Identifier:</span></span>  <br/> |<span data-ttu-id="34f94-109">0x0016</span><span class="sxs-lookup"><span data-stu-id="34f94-109">0x0016</span></span>  <br/> |
|<span data-ttu-id="34f94-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="34f94-110">Data type:</span></span>  <br/> |<span data-ttu-id="34f94-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="34f94-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="34f94-112">Área:</span><span class="sxs-lookup"><span data-stu-id="34f94-112">Area:</span></span>  <br/> |<span data-ttu-id="34f94-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="34f94-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34f94-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="34f94-114">Remarks</span></span>

<span data-ttu-id="34f94-115">Si esta propiedad es TRUE, el sistema de mensajería no debe realizar ninguna conversión de contenido en el mensaje a menos que se solicite explícitamente para cada destinatario con la propiedad **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="34f94-115">If this property is TRUE, the messaging system must not perform any content conversion on the message unless it is explicitly requested on a per-recipient basis with the **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="34f94-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="34f94-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="34f94-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="34f94-117">Header files</span></span>

<span data-ttu-id="34f94-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34f94-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="34f94-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="34f94-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="34f94-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="34f94-120">Mapitags.h</span></span>
  
> <span data-ttu-id="34f94-121">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="34f94-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34f94-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="34f94-122">See also</span></span>



[<span data-ttu-id="34f94-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="34f94-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="34f94-124">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="34f94-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="34f94-125">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="34f94-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="34f94-126">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="34f94-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

