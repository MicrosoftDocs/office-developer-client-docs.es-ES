---
title: Propiedad canónica PidTagOriginalSentRepresentingAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingAddressType
api_type:
- COM
ms.assetid: 93f40161-d4e5-4ef9-a55f-cee62529fc04
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bfb768b774b1fa3d4b65ad2122f49a8ffe11a7b8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391552"
---
# <a name="pidtagoriginalsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="fff91-103">Propiedad canónica PidTagOriginalSentRepresentingAddressType</span><span class="sxs-lookup"><span data-stu-id="fff91-103">PidTagOriginalSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="fff91-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fff91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fff91-105">Contiene el tipo de dirección del usuario de mensajería en cuyo nombre se ha enviado el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="fff91-105">Contains the address type of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fff91-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fff91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fff91-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="fff91-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="fff91-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fff91-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fff91-109">0 x 0068</span><span class="sxs-lookup"><span data-stu-id="fff91-109">0x0068</span></span>  <br/> |
|<span data-ttu-id="fff91-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fff91-110">Data type:</span></span>  <br/> |<span data-ttu-id="fff91-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fff91-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fff91-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fff91-112">Area:</span></span>  <br/> |<span data-ttu-id="fff91-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="fff91-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fff91-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fff91-114">Remarks</span></span>

<span data-ttu-id="fff91-115">Estas propiedades son el tipo de remitente representado original de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="fff91-115">These properties are the type for the original represented sender of a message.</span></span> <span data-ttu-id="fff91-116">Se usan en una secuencia de conversación.</span><span class="sxs-lookup"><span data-stu-id="fff91-116">They are used in a conversation thread.</span></span>
  
<span data-ttu-id="fff91-117">Una aplicación cliente enviar un mensaje en nombre de otro cliente debe establecer estas propiedades en el valor de la propiedad **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) en la primera presentación del mensaje.</span><span class="sxs-lookup"><span data-stu-id="fff91-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="fff91-118">Una vez no establecida, nunca se debe cambiar.</span><span class="sxs-lookup"><span data-stu-id="fff91-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fff91-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fff91-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fff91-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fff91-120">Protocol specifications</span></span>

<span data-ttu-id="fff91-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fff91-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fff91-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fff91-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fff91-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fff91-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fff91-124">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="fff91-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fff91-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fff91-125">Header files</span></span>

<span data-ttu-id="fff91-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fff91-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fff91-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fff91-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="fff91-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fff91-128">Mapitags.h</span></span>
  
> <span data-ttu-id="fff91-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fff91-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fff91-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="fff91-130">See also</span></span>



[<span data-ttu-id="fff91-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fff91-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fff91-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="fff91-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fff91-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fff91-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fff91-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="fff91-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

