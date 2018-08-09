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
ms.openlocfilehash: e5b283376d018b7b2675e05f994d586126437590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819806"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a><span data-ttu-id="d69d5-103">Propiedad canónica PidTagOriginalAuthorSearchKey</span><span class="sxs-lookup"><span data-stu-id="d69d5-103">PidTagOriginalAuthorSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="d69d5-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d69d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d69d5-105">Contiene la clave de búsqueda del autor de la primera versión de un mensaje, es decir, el mensaje antes de que se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="d69d5-105">Contains the search key of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d69d5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d69d5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d69d5-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="d69d5-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="d69d5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d69d5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d69d5-109">0x0056</span><span class="sxs-lookup"><span data-stu-id="d69d5-109">0x0056</span></span>  <br/> |
|<span data-ttu-id="d69d5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d69d5-110">Data type:</span></span>  <br/> |<span data-ttu-id="d69d5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d69d5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d69d5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d69d5-112">Area:</span></span>  <br/> |<span data-ttu-id="d69d5-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="d69d5-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d69d5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d69d5-114">Remarks</span></span>

<span data-ttu-id="d69d5-115">Esta propiedad es una de las propiedades de dirección para el autor de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d69d5-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="d69d5-116">En el primer envío del mensaje, la aplicación cliente debe establecer esta propiedad en el valor de la propiedad de[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) **PR_SENDER_SEARCH_KEY**.</span><span class="sxs-lookup"><span data-stu-id="d69d5-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) property.</span></span> <span data-ttu-id="d69d5-117">Nunca se ha cambiado cuando el mensaje se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="d69d5-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="d69d5-118">Permitir que las propiedades autor original para la conservación de la información desde fuera del dominio de mensajería local.</span><span class="sxs-lookup"><span data-stu-id="d69d5-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="d69d5-119">Cuando un mensaje llega desde otro dominio de mensajería, como desde Internet, estas propiedades proporcionan una forma de garantizar que no se pierda la información original.</span><span class="sxs-lookup"><span data-stu-id="d69d5-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d69d5-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d69d5-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d69d5-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d69d5-121">Header files</span></span>

<span data-ttu-id="d69d5-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d69d5-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="d69d5-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d69d5-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="d69d5-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d69d5-124">Mapitags.h</span></span>
  
> <span data-ttu-id="d69d5-125">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="d69d5-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d69d5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d69d5-126">See also</span></span>



[<span data-ttu-id="d69d5-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d69d5-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d69d5-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d69d5-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d69d5-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d69d5-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d69d5-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d69d5-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

