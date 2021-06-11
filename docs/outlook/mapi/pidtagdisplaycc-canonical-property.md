---
title: Propiedad canónica PidTagDisplayCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayCc
api_type:
- HeaderDef
ms.assetid: 00377e78-a208-4942-a7a6-893b2a71ab0b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2bf862317ca1d2f2a09a71e1af62b82661b33326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360812"
---
# <a name="pidtagdisplaycc-canonical-property"></a><span data-ttu-id="bbff7-103">Propiedad canónica PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="bbff7-103">PidTagDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="bbff7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbff7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbff7-105">Contiene una lista ASCII de los nombres para mostrar de los destinatarios de mensajes de copia de carbono (CC), separados por punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="bbff7-105">Contains an ASCII list of the display names of any carbon copy (CC) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbff7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="bbff7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bbff7-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="bbff7-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="bbff7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bbff7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bbff7-109">0x0E03</span><span class="sxs-lookup"><span data-stu-id="bbff7-109">0x0E03</span></span>  <br/> |
|<span data-ttu-id="bbff7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="bbff7-110">Data type:</span></span>  <br/> |<span data-ttu-id="bbff7-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bbff7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bbff7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bbff7-112">Area:</span></span>  <br/> |<span data-ttu-id="bbff7-113">Mensaje</span><span class="sxs-lookup"><span data-stu-id="bbff7-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbff7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bbff7-114">Remarks</span></span>

<span data-ttu-id="bbff7-115">El almacén de mensajes calcula estas propiedades en objetos de mensaje mediante el [método IMessage::ModifyRecipients.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="bbff7-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="bbff7-116">El almacén de mensajes también mantiene estas propiedades para que siempre refleje el último estado guardado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="bbff7-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="bbff7-117">El valor se sincroniza en el momento de cada llamada a [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="bbff7-117">The value is synchronized at the time of every call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> 
  
<span data-ttu-id="bbff7-118">Si un mensaje no tiene destinatarios de copia de carbono, el almacén de mensajes debe responder a una llamada [IMAPIProp::GetProps](imapiprop-getprops.md) con un valor devuelto de S_OK y una cadena vacía para estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bbff7-118">If a message has no carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for these properties.</span></span> 
  
<span data-ttu-id="bbff7-119">Debido a la posible necesidad de localización, MAPI proporciona estas directrices para todos los nombres de destinatarios:</span><span class="sxs-lookup"><span data-stu-id="bbff7-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="bbff7-120">Todos los nombres deben poder localizarse.</span><span class="sxs-lookup"><span data-stu-id="bbff7-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="bbff7-121">El punto y coma debe ser el carácter que se usa para separar nombres en las propiedades **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** y **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bbff7-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**, and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="bbff7-122">Los puntos y coma no están permitidos en los nombres de destinatarios de MAPI.</span><span class="sxs-lookup"><span data-stu-id="bbff7-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="bbff7-123">Los clientes deben traducir cada punto y coma encontrado en esta propiedad a un carácter separador localizado antes de hacer que la información de la propiedad sea visible en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="bbff7-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="bbff7-124">Al reenviar mensajes, los clientes no necesitan traducir los caracteres separadores en la línea de destinatario de copia de carbono.</span><span class="sxs-lookup"><span data-stu-id="bbff7-124">When forwarding messages, clients do not need to translate the separator characters on the carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="bbff7-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bbff7-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bbff7-126">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="bbff7-126">Protocol specifications</span></span>

<span data-ttu-id="bbff7-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbff7-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbff7-128">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="bbff7-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bbff7-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="bbff7-129">Header files</span></span>

<span data-ttu-id="bbff7-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bbff7-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="bbff7-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="bbff7-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="bbff7-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bbff7-132">Mapitags.h</span></span>
  
> <span data-ttu-id="bbff7-133">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="bbff7-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbff7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbff7-134">See also</span></span>



[<span data-ttu-id="bbff7-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bbff7-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bbff7-136">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="bbff7-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bbff7-137">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="bbff7-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bbff7-138">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="bbff7-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

