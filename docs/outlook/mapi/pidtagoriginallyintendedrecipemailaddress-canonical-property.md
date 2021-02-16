---
title: Propiedad canónica PidTagOriginallyIntendedRecipEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEmailAddress
api_type:
- COM
ms.assetid: 6a85b695-731a-4401-9c9c-fda6bc308558
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4a0e7325618a38addefe562c8207066dfea620f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411375"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a><span data-ttu-id="f5ca3-103">Propiedad canónica PidTagOriginallyIntendedRecipEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f5ca3-103">PidTagOriginallyIntendedRecipEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="f5ca3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5ca3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5ca3-105">Contiene la dirección de correo electrónico del destinatario originalmente deseado de un mensaje de destino automático.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-105">Contains the email address of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5ca3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f5ca3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5ca3-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="f5ca3-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="f5ca3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f5ca3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f5ca3-109">0x007C</span><span class="sxs-lookup"><span data-stu-id="f5ca3-109">0x007C</span></span>  <br/> |
|<span data-ttu-id="f5ca3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f5ca3-110">Data type:</span></span>  <br/> |<span data-ttu-id="f5ca3-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f5ca3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f5ca3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f5ca3-112">Area:</span></span>  <br/> |<span data-ttu-id="f5ca3-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="f5ca3-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5ca3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f5ca3-114">Remarks</span></span>

<span data-ttu-id="f5ca3-115">Estas propiedades son ejemplos de las propiedades de dirección para el destinatario del mensaje originalmente previsto.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-115">These properties are examples of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="f5ca3-116">Deben ser establecidas por el agente automático que reenvía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-116">They must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="f5ca3-117">Estas propiedades corresponden al atributo de informe por destinatario X.400.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-117">These properties correspond to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f5ca3-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5ca3-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f5ca3-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f5ca3-119">Header files</span></span>

<span data-ttu-id="f5ca3-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5ca3-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5ca3-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5ca3-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f5ca3-122">Mapitags.h</span></span>
  
> <span data-ttu-id="f5ca3-123">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="f5ca3-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5ca3-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f5ca3-124">See also</span></span>



[<span data-ttu-id="f5ca3-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f5ca3-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5ca3-126">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f5ca3-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5ca3-127">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f5ca3-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5ca3-128">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f5ca3-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

