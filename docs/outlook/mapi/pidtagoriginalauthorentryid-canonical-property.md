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
ms.openlocfilehash: 03244fb240231a105b0a25a0797c13b9bf7f7a80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819797"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a><span data-ttu-id="ac77d-103">Propiedad canónica PidTagOriginalAuthorEntryId</span><span class="sxs-lookup"><span data-stu-id="ac77d-103">PidTagOriginalAuthorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="ac77d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac77d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac77d-105">Contiene el identificador de entrada del autor de la primera versión de un mensaje, es decir, el mensaje antes de que se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="ac77d-105">Contains the entry identifier of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac77d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ac77d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac77d-107">PR_ORIGINAL_AUTHOR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ac77d-107">PR_ORIGINAL_AUTHOR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="ac77d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ac77d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac77d-109">0x004C</span><span class="sxs-lookup"><span data-stu-id="ac77d-109">0x004C</span></span>  <br/> |
|<span data-ttu-id="ac77d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ac77d-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac77d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ac77d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ac77d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ac77d-112">Area:</span></span>  <br/> |<span data-ttu-id="ac77d-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="ac77d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac77d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac77d-114">Remarks</span></span>

<span data-ttu-id="ac77d-115">Esta propiedad es una de las propiedades de dirección para el autor de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="ac77d-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="ac77d-116">En el primer envío del mensaje, la aplicación cliente debe establecer esta propiedad en el valor de **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ac77d-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span></span> <span data-ttu-id="ac77d-117">Nunca se ha cambiado cuando el mensaje se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="ac77d-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="ac77d-118">La propiedad autor original permite la conservación de la información desde fuera del dominio de mensajería local.</span><span class="sxs-lookup"><span data-stu-id="ac77d-118">The original author property allows for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="ac77d-119">No se pierda cuando llegue un mensaje desde otro dominio de mensajería, como desde Internet, esta propiedad proporciona una forma de garantizar que la información original.</span><span class="sxs-lookup"><span data-stu-id="ac77d-119">When a message arrives from another messaging domain, such as from the Internet, this property provides a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ac77d-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac77d-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ac77d-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ac77d-121">Header files</span></span>

<span data-ttu-id="ac77d-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac77d-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac77d-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ac77d-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac77d-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ac77d-124">Mapitags.h</span></span>
  
> <span data-ttu-id="ac77d-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ac77d-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac77d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac77d-126">See also</span></span>



[<span data-ttu-id="ac77d-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ac77d-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac77d-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="ac77d-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac77d-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ac77d-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac77d-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="ac77d-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

