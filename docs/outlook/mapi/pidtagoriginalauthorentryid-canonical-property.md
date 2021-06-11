---
title: Propiedad canónica PidTagOriginalAuthorEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEntryId
api_type:
- COM
ms.assetid: 34654660-b003-42f5-9fcd-24ebaccd735d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 866c28bc08f669d18487c99c9a13bc7347b605fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425592"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a><span data-ttu-id="94faf-103">Propiedad canónica PidTagOriginalAuthorEntryId</span><span class="sxs-lookup"><span data-stu-id="94faf-103">PidTagOriginalAuthorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="94faf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94faf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94faf-105">Contiene el identificador de entrada del autor de la primera versión de un mensaje, es decir, el mensaje antes de reenviarlo o responderlo.</span><span class="sxs-lookup"><span data-stu-id="94faf-105">Contains the entry identifier of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94faf-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="94faf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94faf-107">PR_ORIGINAL_AUTHOR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="94faf-107">PR_ORIGINAL_AUTHOR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="94faf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="94faf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="94faf-109">0x004C</span><span class="sxs-lookup"><span data-stu-id="94faf-109">0x004C</span></span>  <br/> |
|<span data-ttu-id="94faf-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="94faf-110">Data type:</span></span>  <br/> |<span data-ttu-id="94faf-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="94faf-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="94faf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="94faf-112">Area:</span></span>  <br/> |<span data-ttu-id="94faf-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="94faf-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94faf-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94faf-114">Remarks</span></span>

<span data-ttu-id="94faf-115">Esta propiedad es una de las propiedades de dirección del autor de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="94faf-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="94faf-116">En el primer envío del mensaje, la aplicación cliente debe establecer esta propiedad en el valor **de PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="94faf-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span></span> <span data-ttu-id="94faf-117">Nunca se cambia cuando se reenvía o se responde al mensaje.</span><span class="sxs-lookup"><span data-stu-id="94faf-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="94faf-118">La propiedad author original permite conservar la información de fuera del dominio de mensajería local.</span><span class="sxs-lookup"><span data-stu-id="94faf-118">The original author property allows for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="94faf-119">Cuando un mensaje llega desde otro dominio de mensajería, como internet, esta propiedad proporciona una forma de garantizar que no se pierda la información original.</span><span class="sxs-lookup"><span data-stu-id="94faf-119">When a message arrives from another messaging domain, such as from the Internet, this property provides a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="94faf-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="94faf-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="94faf-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="94faf-121">Header files</span></span>

<span data-ttu-id="94faf-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94faf-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="94faf-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="94faf-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="94faf-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="94faf-124">Mapitags.h</span></span>
  
> <span data-ttu-id="94faf-125">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="94faf-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94faf-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="94faf-126">See also</span></span>



[<span data-ttu-id="94faf-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="94faf-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94faf-128">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="94faf-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94faf-129">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="94faf-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94faf-130">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="94faf-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

