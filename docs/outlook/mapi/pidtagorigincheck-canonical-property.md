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
ms.openlocfilehash: a82b1351c9d2d19c32e34b03a537a12bf93deb8a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435764"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="0a530-103">Propiedad canónica PidTagOriginCheck</span><span class="sxs-lookup"><span data-stu-id="0a530-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="0a530-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a530-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a530-105">Contiene un valor de verificación binario que permite que un destinatario del informe de entrega compruebe el origen del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="0a530-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a530-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0a530-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a530-107">PR_ORIGIN_CHECK</span><span class="sxs-lookup"><span data-stu-id="0a530-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="0a530-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0a530-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0a530-109">0x0027</span><span class="sxs-lookup"><span data-stu-id="0a530-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="0a530-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0a530-110">Data type:</span></span>  <br/> |<span data-ttu-id="0a530-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0a530-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0a530-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0a530-112">Area:</span></span>  <br/> |<span data-ttu-id="0a530-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="0a530-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a530-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a530-114">Remarks</span></span>

<span data-ttu-id="0a530-115">Esta propiedad proporciona un medio para que un tercero, como un agente de transferencia de mensajes (MTA) o un usuario de mensajería que recibe un informe de entrega, compruebe el origen del mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="0a530-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="0a530-116">Si está presente en un mensaje recibido, esta propiedad debe copiarse en cualquier informe de entrega generado en respuesta al mensaje.</span><span class="sxs-lookup"><span data-stu-id="0a530-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0a530-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a530-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0a530-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0a530-118">Header files</span></span>

<span data-ttu-id="0a530-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a530-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a530-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0a530-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="0a530-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0a530-121">Mapitags.h</span></span>
  
> <span data-ttu-id="0a530-122">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="0a530-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a530-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0a530-123">See also</span></span>



[<span data-ttu-id="0a530-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0a530-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a530-125">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="0a530-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a530-126">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0a530-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a530-127">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0a530-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

