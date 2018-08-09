---
title: Propiedad canónica PidTagOriginCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bbf09cb841c633b6f13ae12ec20e120ea3fd7ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819876"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="3d904-103">Propiedad canónica PidTagOriginCheck</span><span class="sxs-lookup"><span data-stu-id="3d904-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="3d904-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3d904-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3d904-105">Contiene un valor binario de comprobación que permite a un destinatario de informe de entrega comprobar el origen del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="3d904-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d904-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3d904-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d904-107">PR_ORIGIN_CHECK</span><span class="sxs-lookup"><span data-stu-id="3d904-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="3d904-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3d904-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d904-109">0x0027</span><span class="sxs-lookup"><span data-stu-id="3d904-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="3d904-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3d904-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d904-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3d904-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3d904-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3d904-112">Area:</span></span>  <br/> |<span data-ttu-id="3d904-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="3d904-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d904-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d904-114">Remarks</span></span>

<span data-ttu-id="3d904-115">Esta propiedad proporciona un medio para un tercero, como un agente de transferencia de mensajes (MTA) o un usuario de mensajería recibir un informe de entrega, para comprobar el origen del mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="3d904-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="3d904-116">Si está presente en un mensaje recibido, esta propiedad debe copiarse en cualquier informe de entrega generado en respuesta al mensaje.</span><span class="sxs-lookup"><span data-stu-id="3d904-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3d904-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d904-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3d904-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3d904-118">Header files</span></span>

<span data-ttu-id="3d904-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d904-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d904-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3d904-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d904-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3d904-121">Mapitags.h</span></span>
  
> <span data-ttu-id="3d904-122">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="3d904-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d904-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d904-123">See also</span></span>



[<span data-ttu-id="3d904-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3d904-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d904-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="3d904-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d904-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3d904-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d904-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="3d904-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

