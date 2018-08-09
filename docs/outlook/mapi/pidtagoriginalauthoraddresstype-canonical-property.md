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
ms.openlocfilehash: fb30f2b29691984614891e2345fe97abe6316f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819798"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a><span data-ttu-id="45a19-103">Propiedad canónica PidTagOriginalAuthorAddressType</span><span class="sxs-lookup"><span data-stu-id="45a19-103">PidTagOriginalAuthorAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="45a19-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45a19-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45a19-105">Contiene el tipo de dirección del autor de la primera versión de un mensaje, es decir, el mensaje antes de que se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="45a19-105">Contains the address type of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45a19-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="45a19-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45a19-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="45a19-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="45a19-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="45a19-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45a19-109">0 x 0079</span><span class="sxs-lookup"><span data-stu-id="45a19-109">0x0079</span></span>  <br/> |
|<span data-ttu-id="45a19-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="45a19-110">Data type:</span></span>  <br/> |<span data-ttu-id="45a19-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="45a19-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="45a19-112">Área:</span><span class="sxs-lookup"><span data-stu-id="45a19-112">Area:</span></span>  <br/> |<span data-ttu-id="45a19-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="45a19-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45a19-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="45a19-114">Remarks</span></span>

<span data-ttu-id="45a19-115">Estas propiedades son ejemplos de las propiedades de dirección para el autor de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="45a19-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="45a19-116">En el primer envío del mensaje, la aplicación cliente debe establecer esta propiedad en el valor de la propiedad **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="45a19-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="45a19-117">Nunca se ha cambiado cuando el mensaje se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="45a19-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="45a19-118">Permitir que las propiedades autor original para la conservación de la información desde fuera del dominio de mensajería local.</span><span class="sxs-lookup"><span data-stu-id="45a19-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="45a19-119">Cuando un mensaje llega desde otro dominio de mensajería, como desde Internet, estas propiedades proporcionan una forma de garantizar que no se pierda la información original.</span><span class="sxs-lookup"><span data-stu-id="45a19-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45a19-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="45a19-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="45a19-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="45a19-121">Header files</span></span>

<span data-ttu-id="45a19-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45a19-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="45a19-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="45a19-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="45a19-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45a19-124">Mapitags.h</span></span>
  
> <span data-ttu-id="45a19-125">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="45a19-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45a19-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="45a19-126">See also</span></span>



[<span data-ttu-id="45a19-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="45a19-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45a19-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="45a19-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45a19-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="45a19-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45a19-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="45a19-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

