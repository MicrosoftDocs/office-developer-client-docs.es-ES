---
title: Propiedad canónica PidTagOriginalAuthorEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEmailAddress
api_type:
- COM
ms.assetid: 67cda756-ba71-4f29-a601-55359e44d93b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7918c5d5b585ffb199bfbc140edfb8286b499b40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436170"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a><span data-ttu-id="2ca5f-103">Propiedad canónica PidTagOriginalAuthorEmailAddress</span><span class="sxs-lookup"><span data-stu-id="2ca5f-103">PidTagOriginalAuthorEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="2ca5f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ca5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ca5f-105">Contiene la dirección de correo electrónico del autor de la primera versión de un mensaje, es decir, el mensaje antes de reenviarlo o responderlo.</span><span class="sxs-lookup"><span data-stu-id="2ca5f-105">Contains the email address of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ca5f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2ca5f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ca5f-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="2ca5f-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="2ca5f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2ca5f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ca5f-109">0x007A</span><span class="sxs-lookup"><span data-stu-id="2ca5f-109">0x007A</span></span>  <br/> |
|<span data-ttu-id="2ca5f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2ca5f-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ca5f-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2ca5f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2ca5f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2ca5f-112">Area:</span></span>  <br/> |<span data-ttu-id="2ca5f-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="2ca5f-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ca5f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2ca5f-114">Remarks</span></span>

<span data-ttu-id="2ca5f-115">Estas propiedades son ejemplos de las propiedades de dirección para el autor de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="2ca5f-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="2ca5f-116">En el primer envío del mensaje, la aplicación cliente debe establecer estas propiedades en el valor de la propiedad **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2ca5f-116">At first submission of the message, the client application should set these properties to the value of the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="2ca5f-117">Nunca se cambia cuando se reenvía o se responde al mensaje.</span><span class="sxs-lookup"><span data-stu-id="2ca5f-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="2ca5f-118">Las propiedades de autor originales permiten preservar la información desde fuera del dominio de mensajería local.</span><span class="sxs-lookup"><span data-stu-id="2ca5f-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="2ca5f-119">Cuando un mensaje llega desde otro dominio de mensajería, como desde Internet, estas propiedades proporcionan una forma de garantizar que no se pierda la información original.</span><span class="sxs-lookup"><span data-stu-id="2ca5f-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2ca5f-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ca5f-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2ca5f-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2ca5f-121">Header files</span></span>

<span data-ttu-id="2ca5f-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2ca5f-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ca5f-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2ca5f-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ca5f-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2ca5f-124">Mapitags.h</span></span>
  
> <span data-ttu-id="2ca5f-125">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="2ca5f-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ca5f-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="2ca5f-126">See also</span></span>



[<span data-ttu-id="2ca5f-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2ca5f-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ca5f-128">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="2ca5f-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ca5f-129">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2ca5f-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ca5f-130">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2ca5f-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

