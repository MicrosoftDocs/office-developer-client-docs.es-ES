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
ms.openlocfilehash: f4adbdfc041ebe5213c384db98343baa82af5b05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572728"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a><span data-ttu-id="54138-103">Propiedad canónica PidTagOriginallyIntendedRecipEmailAddress</span><span class="sxs-lookup"><span data-stu-id="54138-103">PidTagOriginallyIntendedRecipEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="54138-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54138-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54138-105">Contiene la dirección de correo electrónico del destinatario de un mensaje de autoforwarded originalmente previsto.</span><span class="sxs-lookup"><span data-stu-id="54138-105">Contains the email address of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54138-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="54138-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54138-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="54138-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="54138-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="54138-108">Identifier:</span></span>  <br/> |<span data-ttu-id="54138-109">0x007C</span><span class="sxs-lookup"><span data-stu-id="54138-109">0x007C</span></span>  <br/> |
|<span data-ttu-id="54138-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="54138-110">Data type:</span></span>  <br/> |<span data-ttu-id="54138-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="54138-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="54138-112">Área:</span><span class="sxs-lookup"><span data-stu-id="54138-112">Area:</span></span>  <br/> |<span data-ttu-id="54138-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="54138-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54138-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54138-114">Remarks</span></span>

<span data-ttu-id="54138-115">Estas propiedades son ejemplos de las propiedades de dirección para el destinatario del mensaje originalmente.</span><span class="sxs-lookup"><span data-stu-id="54138-115">These properties are examples of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="54138-116">Se deben configurar el agente de automática que reenvió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="54138-116">They must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="54138-117">Estas propiedades se corresponden con el atributo X.400 informe por destinatario.</span><span class="sxs-lookup"><span data-stu-id="54138-117">These properties correspond to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="54138-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="54138-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="54138-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="54138-119">Header files</span></span>

<span data-ttu-id="54138-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54138-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="54138-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="54138-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="54138-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="54138-122">Mapitags.h</span></span>
  
> <span data-ttu-id="54138-123">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="54138-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54138-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="54138-124">See also</span></span>



[<span data-ttu-id="54138-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="54138-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54138-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="54138-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54138-127">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="54138-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54138-128">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="54138-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

