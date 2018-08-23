---
title: Propiedad canónica PidTagOriginatorRequestedAlternateRecipient
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorRequestedAlternateRecipient
api_type:
- COM
ms.assetid: c85b7862-18bc-4e17-94db-9097e0ac4a02
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 463f2eb6e730c9250861ce50515a7f662bb75d23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588870"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="35dd8-103">Propiedad canónica PidTagOriginatorRequestedAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="35dd8-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="35dd8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35dd8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35dd8-105">Contiene un identificador de entrada para un destinatario alternativo designado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="35dd8-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35dd8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="35dd8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35dd8-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="35dd8-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="35dd8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="35dd8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35dd8-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="35dd8-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="35dd8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="35dd8-110">Data type:</span></span>  <br/> |<span data-ttu-id="35dd8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="35dd8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="35dd8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="35dd8-112">Area:</span></span>  <br/> |<span data-ttu-id="35dd8-113">MIME</span><span class="sxs-lookup"><span data-stu-id="35dd8-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35dd8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="35dd8-114">Remarks</span></span>

<span data-ttu-id="35dd8-115">Esta propiedad se usa en los mensajes de autoforwarded.</span><span class="sxs-lookup"><span data-stu-id="35dd8-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="35dd8-116">Si no se permite Autorreenvío o si no se ha designado ningún destinatario alternativo, se debe generar un informe de no entrega.</span><span class="sxs-lookup"><span data-stu-id="35dd8-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="35dd8-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="35dd8-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="35dd8-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="35dd8-118">Header files</span></span>

<span data-ttu-id="35dd8-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35dd8-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="35dd8-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="35dd8-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="35dd8-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="35dd8-121">Mapitags.h</span></span>
  
> <span data-ttu-id="35dd8-122">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="35dd8-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35dd8-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="35dd8-123">See also</span></span>



[<span data-ttu-id="35dd8-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="35dd8-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35dd8-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="35dd8-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35dd8-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="35dd8-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35dd8-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="35dd8-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

