---
title: Propiedad canónica PidTagOriginalAuthorSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 09331e1201b6f6e45bb9e26e618ee59e67efbf8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409583"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a><span data-ttu-id="3f7cc-103">Propiedad canónica PidTagOriginalAuthorSearchKey</span><span class="sxs-lookup"><span data-stu-id="3f7cc-103">PidTagOriginalAuthorSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="3f7cc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f7cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f7cc-105">Contiene la clave de búsqueda del autor de la primera versión de un mensaje, es decir, el mensaje antes de reenviarlo o responderlo.</span><span class="sxs-lookup"><span data-stu-id="3f7cc-105">Contains the search key of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f7cc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3f7cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3f7cc-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="3f7cc-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="3f7cc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3f7cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3f7cc-109">0x0056</span><span class="sxs-lookup"><span data-stu-id="3f7cc-109">0x0056</span></span>  <br/> |
|<span data-ttu-id="3f7cc-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3f7cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="3f7cc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3f7cc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3f7cc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3f7cc-112">Area:</span></span>  <br/> |<span data-ttu-id="3f7cc-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="3f7cc-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f7cc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f7cc-114">Remarks</span></span>

<span data-ttu-id="3f7cc-115">Esta propiedad es una de las propiedades de dirección del autor de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="3f7cc-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="3f7cc-116">En el primer envío del mensaje, la aplicación cliente debe establecer esta propiedad en el valor de la PR_SENDER_SEARCH_KEY[propiedad PidTagSenderSearchKey.](pidtagsendersearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3f7cc-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) property.</span></span> <span data-ttu-id="3f7cc-117">Nunca se cambia cuando se reenvía o se responde al mensaje.</span><span class="sxs-lookup"><span data-stu-id="3f7cc-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="3f7cc-118">Las propiedades originales del autor permiten conservar la información de fuera del dominio de mensajería local.</span><span class="sxs-lookup"><span data-stu-id="3f7cc-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="3f7cc-119">Cuando un mensaje llega desde otro dominio de mensajería, como internet, estas propiedades proporcionan una forma de garantizar que no se pierda la información original.</span><span class="sxs-lookup"><span data-stu-id="3f7cc-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3f7cc-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f7cc-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3f7cc-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3f7cc-121">Header files</span></span>

<span data-ttu-id="3f7cc-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f7cc-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="3f7cc-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3f7cc-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="3f7cc-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3f7cc-124">Mapitags.h</span></span>
  
> <span data-ttu-id="3f7cc-125">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="3f7cc-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3f7cc-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f7cc-126">See also</span></span>



[<span data-ttu-id="3f7cc-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3f7cc-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3f7cc-128">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3f7cc-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3f7cc-129">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3f7cc-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3f7cc-130">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="3f7cc-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

