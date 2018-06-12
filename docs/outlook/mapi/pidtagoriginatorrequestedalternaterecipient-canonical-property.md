---
title: Propiedad canónico PidTagOriginatorRequestedAlternateRecipient
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c7abd0ae93c5b38c756ec0915dda6a4cdfcebaa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819878"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="d7495-103">Propiedad canónico PidTagOriginatorRequestedAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="d7495-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="d7495-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7495-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7495-105">Contiene un identificador de entrada para un destinatario alternativo designado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="d7495-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7495-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d7495-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7495-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="d7495-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="d7495-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d7495-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7495-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="d7495-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="d7495-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d7495-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7495-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d7495-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d7495-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d7495-112">Area:</span></span>  <br/> |<span data-ttu-id="d7495-113">MIME</span><span class="sxs-lookup"><span data-stu-id="d7495-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7495-114">Notas</span><span class="sxs-lookup"><span data-stu-id="d7495-114">Remarks</span></span>

<span data-ttu-id="d7495-115">Esta propiedad se usa en los mensajes de autoforwarded.</span><span class="sxs-lookup"><span data-stu-id="d7495-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="d7495-116">Si no se permite Autorreenvío o si no se ha designado ningún destinatario alternativo, se debe generar un informe de no entrega.</span><span class="sxs-lookup"><span data-stu-id="d7495-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d7495-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7495-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d7495-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d7495-118">Header files</span></span>

<span data-ttu-id="d7495-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7495-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7495-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d7495-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7495-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d7495-121">Mapitags.h</span></span>
  
> <span data-ttu-id="d7495-122">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d7495-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7495-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="d7495-123">See also</span></span>



[<span data-ttu-id="d7495-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d7495-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7495-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d7495-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7495-126">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="d7495-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7495-127">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d7495-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

