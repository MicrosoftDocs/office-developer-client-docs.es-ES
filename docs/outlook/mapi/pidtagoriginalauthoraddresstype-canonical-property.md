---
title: Propiedad canónica PidTagOriginalAuthorAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorAddressType
api_type:
- COM
ms.assetid: 7cdedb1a-e441-469b-be50-2f18203eb30d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 596e416624fb6f2bf1fdaef64c2179feb7787815
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431417"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a><span data-ttu-id="c4c5c-103">Propiedad canónica PidTagOriginalAuthorAddressType</span><span class="sxs-lookup"><span data-stu-id="c4c5c-103">PidTagOriginalAuthorAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="c4c5c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4c5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4c5c-105">Contiene el tipo de dirección del autor de la primera versión de un mensaje, es decir, el mensaje antes de reenviarlo o responderlo.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-105">Contains the address type of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4c5c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c4c5c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4c5c-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="c4c5c-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="c4c5c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c4c5c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c4c5c-109">0x0079</span><span class="sxs-lookup"><span data-stu-id="c4c5c-109">0x0079</span></span>  <br/> |
|<span data-ttu-id="c4c5c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c4c5c-110">Data type:</span></span>  <br/> |<span data-ttu-id="c4c5c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c4c5c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c4c5c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c4c5c-112">Area:</span></span>  <br/> |<span data-ttu-id="c4c5c-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="c4c5c-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4c5c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4c5c-114">Remarks</span></span>

<span data-ttu-id="c4c5c-115">Estas propiedades son ejemplos de las propiedades de dirección del autor de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="c4c5c-116">En el primer envío del mensaje, la aplicación cliente debe establecer esta propiedad en el valor de la propiedad **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c4c5c-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="c4c5c-117">Nunca se cambia cuando se reenvía o se responde al mensaje.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="c4c5c-118">Las propiedades originales del autor permiten conservar la información de fuera del dominio de mensajería local.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="c4c5c-119">Cuando un mensaje llega desde otro dominio de mensajería, como internet, estas propiedades proporcionan una forma de garantizar que no se pierda la información original.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c4c5c-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4c5c-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c4c5c-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c4c5c-121">Header files</span></span>

<span data-ttu-id="c4c5c-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4c5c-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4c5c-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="c4c5c-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c4c5c-124">Mapitags.h</span></span>
  
> <span data-ttu-id="c4c5c-125">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4c5c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4c5c-126">See also</span></span>



[<span data-ttu-id="c4c5c-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c4c5c-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4c5c-128">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c4c5c-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4c5c-129">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c4c5c-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4c5c-130">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c4c5c-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

