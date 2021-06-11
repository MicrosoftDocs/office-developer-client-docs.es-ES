---
title: Propiedad canónica PidTagOriginalSentRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingName
api_type:
- COM
ms.assetid: 1be45cad-05a2-44cb-8c3d-7f6ac092fa0d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 771a7c9cdf37a94875c881d8d7e8fd292893a0ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341107"
---
# <a name="pidtagoriginalsentrepresentingname-canonical-property"></a><span data-ttu-id="dac30-103">Propiedad canónica PidTagOriginalSentRepresentingName</span><span class="sxs-lookup"><span data-stu-id="dac30-103">PidTagOriginalSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="dac30-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dac30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dac30-105">Contiene el nombre para mostrar del usuario de mensajería en cuyo nombre se envió el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="dac30-105">Contains the display name of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dac30-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="dac30-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dac30-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="dac30-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="dac30-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dac30-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dac30-109">0x005D</span><span class="sxs-lookup"><span data-stu-id="dac30-109">0x005D</span></span>  <br/> |
|<span data-ttu-id="dac30-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="dac30-110">Data type:</span></span>  <br/> |<span data-ttu-id="dac30-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dac30-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dac30-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dac30-112">Area:</span></span>  <br/> |<span data-ttu-id="dac30-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="dac30-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dac30-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dac30-114">Remarks</span></span>

<span data-ttu-id="dac30-115">Estos ejemplos de propiedades de las propiedades de dirección del remitente representado original de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="dac30-115">These properties examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="dac30-116">Se usa en un hilo de conversación.</span><span class="sxs-lookup"><span data-stu-id="dac30-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="dac30-117">Una aplicación cliente que envíe un mensaje en nombre de otro cliente debe establecer estas propiedades en el valor de la propiedad **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) en el primer envío del mensaje.</span><span class="sxs-lookup"><span data-stu-id="dac30-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="dac30-118">Una vez establecido, nunca se debe cambiar.</span><span class="sxs-lookup"><span data-stu-id="dac30-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dac30-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dac30-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dac30-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="dac30-120">Protocol specifications</span></span>

<span data-ttu-id="dac30-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dac30-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dac30-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="dac30-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dac30-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dac30-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dac30-124">Especifica las propiedades y las operaciones permitidas en objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="dac30-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dac30-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="dac30-125">Header files</span></span>

<span data-ttu-id="dac30-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dac30-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="dac30-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="dac30-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="dac30-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dac30-128">Mapitags.h</span></span>
  
> <span data-ttu-id="dac30-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="dac30-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dac30-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="dac30-130">See also</span></span>



[<span data-ttu-id="dac30-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dac30-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dac30-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="dac30-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dac30-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="dac30-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dac30-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="dac30-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

