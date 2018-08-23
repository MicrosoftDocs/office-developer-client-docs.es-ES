---
title: Propiedad canónica PidTagOriginalSenderEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEmailAddress
api_type:
- COM
ms.assetid: cc86505c-e264-435f-ae21-4a10f0bbf082
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 927710f3530fd95cc1c1ba548870c1058ad7a819
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567436"
---
# <a name="pidtagoriginalsenderemailaddress-canonical-property"></a><span data-ttu-id="969cc-103">Propiedad canónica PidTagOriginalSenderEmailAddress</span><span class="sxs-lookup"><span data-stu-id="969cc-103">PidTagOriginalSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="969cc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="969cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="969cc-105">Contiene la dirección de correo electrónico del remitente de la primera versión de un mensaje, es decir, el mensaje antes de que se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="969cc-105">Contains the email address of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="969cc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="969cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="969cc-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="969cc-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="969cc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="969cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="969cc-109">0x0067</span><span class="sxs-lookup"><span data-stu-id="969cc-109">0x0067</span></span>  <br/> |
|<span data-ttu-id="969cc-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="969cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="969cc-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="969cc-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="969cc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="969cc-112">Area:</span></span>  <br/> |<span data-ttu-id="969cc-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="969cc-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="969cc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="969cc-114">Remarks</span></span>

<span data-ttu-id="969cc-115">Estas propiedades son ejemplos de las propiedades de direcciones para el remitente original de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="969cc-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="969cc-116">En el primer envío del mensaje, la aplicación cliente debe establecer esta propiedad en el valor de **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="969cc-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="969cc-117">Nunca se ha cambiado cuando el mensaje se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="969cc-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="969cc-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="969cc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="969cc-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="969cc-119">Protocol specifications</span></span>

<span data-ttu-id="969cc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="969cc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="969cc-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="969cc-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="969cc-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="969cc-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="969cc-123">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="969cc-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="969cc-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="969cc-124">Header files</span></span>

<span data-ttu-id="969cc-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="969cc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="969cc-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="969cc-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="969cc-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="969cc-127">Mapitags.h</span></span>
  
> <span data-ttu-id="969cc-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="969cc-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="969cc-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="969cc-129">See also</span></span>



[<span data-ttu-id="969cc-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="969cc-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="969cc-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="969cc-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="969cc-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="969cc-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="969cc-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="969cc-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

