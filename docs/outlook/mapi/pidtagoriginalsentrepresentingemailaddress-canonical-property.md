---
title: Propiedad canónica PidTagOriginalSentRepresentingEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e2c3d2c3-5451-45cb-b0ec-bdbf5b39a0ba
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bfb771c4c5972a770910936b6220c9e11b24e355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819834"
---
# <a name="pidtagoriginalsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="f8b8a-103">Propiedad canónica PidTagOriginalSentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f8b8a-103">PidTagOriginalSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="f8b8a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f8b8a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f8b8a-105">Contiene la dirección de correo electrónico del usuario de mensajería en cuyo nombre se ha enviado el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="f8b8a-105">Contains the email address of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f8b8a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f8b8a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f8b8a-107">PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="f8b8a-107">PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="f8b8a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f8b8a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f8b8a-109">0x0069</span><span class="sxs-lookup"><span data-stu-id="f8b8a-109">0x0069</span></span>  <br/> |
|<span data-ttu-id="f8b8a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f8b8a-110">Data type:</span></span>  <br/> |<span data-ttu-id="f8b8a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f8b8a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f8b8a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f8b8a-112">Area:</span></span>  <br/> |<span data-ttu-id="f8b8a-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="f8b8a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8b8a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8b8a-114">Remarks</span></span>

<span data-ttu-id="f8b8a-115">Estas propiedades son ejemplos de las propiedades de direcciones para el remitente original representado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f8b8a-115">These properties are examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="f8b8a-116">Se utiliza en una secuencia de conversación.</span><span class="sxs-lookup"><span data-stu-id="f8b8a-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="f8b8a-117">Una aplicación cliente enviar un mensaje en nombre de otro cliente debe establecer estas propiedades en el valor de la propiedad **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) en la primera presentación del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f8b8a-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="f8b8a-118">Una vez no establecida, nunca se debe cambiar.</span><span class="sxs-lookup"><span data-stu-id="f8b8a-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f8b8a-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f8b8a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f8b8a-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f8b8a-120">Protocol specifications</span></span>

<span data-ttu-id="f8b8a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8b8a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8b8a-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f8b8a-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f8b8a-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8b8a-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8b8a-124">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f8b8a-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f8b8a-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f8b8a-125">Header files</span></span>

<span data-ttu-id="f8b8a-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8b8a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f8b8a-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f8b8a-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="f8b8a-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f8b8a-128">Mapitags.h</span></span>
  
> <span data-ttu-id="f8b8a-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f8b8a-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8b8a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8b8a-130">See also</span></span>



[<span data-ttu-id="f8b8a-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f8b8a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f8b8a-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f8b8a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f8b8a-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f8b8a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f8b8a-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f8b8a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

