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
ms.openlocfilehash: 225c0813139a74b735b5b8a3d5a729e630cd3511
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563341"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a><span data-ttu-id="9bfba-103">Propiedad canónica PidTagOriginalAuthorSearchKey</span><span class="sxs-lookup"><span data-stu-id="9bfba-103">PidTagOriginalAuthorSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="9bfba-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bfba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bfba-105">Contiene la clave de búsqueda del autor de la primera versión de un mensaje, es decir, el mensaje antes de que se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="9bfba-105">Contains the search key of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9bfba-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9bfba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9bfba-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="9bfba-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="9bfba-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9bfba-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9bfba-109">0x0056</span><span class="sxs-lookup"><span data-stu-id="9bfba-109">0x0056</span></span>  <br/> |
|<span data-ttu-id="9bfba-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9bfba-110">Data type:</span></span>  <br/> |<span data-ttu-id="9bfba-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9bfba-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9bfba-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9bfba-112">Area:</span></span>  <br/> |<span data-ttu-id="9bfba-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="9bfba-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bfba-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9bfba-114">Remarks</span></span>

<span data-ttu-id="9bfba-115">Esta propiedad es una de las propiedades de dirección para el autor de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="9bfba-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="9bfba-116">En el primer envío del mensaje, la aplicación cliente debe establecer esta propiedad en el valor de la propiedad de[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) **PR_SENDER_SEARCH_KEY**.</span><span class="sxs-lookup"><span data-stu-id="9bfba-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) property.</span></span> <span data-ttu-id="9bfba-117">Nunca se ha cambiado cuando el mensaje se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="9bfba-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="9bfba-118">Permitir que las propiedades autor original para la conservación de la información desde fuera del dominio de mensajería local.</span><span class="sxs-lookup"><span data-stu-id="9bfba-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="9bfba-119">Cuando un mensaje llega desde otro dominio de mensajería, como desde Internet, estas propiedades proporcionan una forma de garantizar que no se pierda la información original.</span><span class="sxs-lookup"><span data-stu-id="9bfba-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9bfba-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9bfba-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9bfba-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9bfba-121">Header files</span></span>

<span data-ttu-id="9bfba-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9bfba-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="9bfba-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9bfba-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="9bfba-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9bfba-124">Mapitags.h</span></span>
  
> <span data-ttu-id="9bfba-125">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="9bfba-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9bfba-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9bfba-126">See also</span></span>



[<span data-ttu-id="9bfba-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9bfba-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9bfba-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9bfba-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9bfba-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9bfba-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9bfba-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="9bfba-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

