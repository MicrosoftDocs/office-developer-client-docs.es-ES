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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383852"
---
# <a name="pidtagdisplaycc-canonical-property"></a><span data-ttu-id="b6b0c-103">Propiedad canónica PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="b6b0c-103">PidTagDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="b6b0c-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6b0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6b0c-105">Contiene una lista de ASCII de los nombres para mostrar de los destinatarios del mensaje con copia (CC), separados por punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="b6b0c-105">Contains an ASCII list of the display names of any carbon copy (CC) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6b0c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b6b0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6b0c-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="b6b0c-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="b6b0c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b6b0c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6b0c-109">0x0E03</span><span class="sxs-lookup"><span data-stu-id="b6b0c-109">0x0E03</span></span>  <br/> |
|<span data-ttu-id="b6b0c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b6b0c-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6b0c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b6b0c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b6b0c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b6b0c-112">Area:</span></span>  <br/> |<span data-ttu-id="b6b0c-113">Message</span><span class="sxs-lookup"><span data-stu-id="b6b0c-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6b0c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b6b0c-114">Remarks</span></span>

<span data-ttu-id="b6b0c-115">El almacén de mensajes calcula estas propiedades en los objetos de mensaje con el método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="b6b0c-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="b6b0c-116">El almacén de mensajes también mantiene estas propiedades para que siempre refleja el último estado guardado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="b6b0c-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="b6b0c-117">El valor se sincroniza en el momento de todas las llamadas a [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="b6b0c-117">The value is synchronized at the time of every call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> 
  
<span data-ttu-id="b6b0c-118">Si un mensaje no tiene ningún destinatarios en copia oculta, el almacén de mensajes debe responder a una llamada [IMAPIProp::GetProps](imapiprop-getprops.md) con un valor devuelto de S_OK y una cadena vacía para estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b6b0c-118">If a message has no carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for these properties.</span></span> 
  
<span data-ttu-id="b6b0c-119">Debido a la necesidad de posible para la localización, MAPI proporciona estas instrucciones para todos los nombres de los destinatarios:</span><span class="sxs-lookup"><span data-stu-id="b6b0c-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="b6b0c-120">Todos los nombres de deberían poder ser localizada.</span><span class="sxs-lookup"><span data-stu-id="b6b0c-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="b6b0c-121">El punto y coma debe ser el carácter que se usa para separar los nombres en las propiedades de **PR_DISPLAY_TO de MAPI** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC**y **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b6b0c-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**, and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="b6b0c-122">Punto y coma no se permite dentro de nombres de los destinatarios en MAPI.</span><span class="sxs-lookup"><span data-stu-id="b6b0c-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="b6b0c-123">Los clientes deben traducir cada punto y coma detectado en esta propiedad para un carácter de separador localizadas antes de realizar la información de la propiedad visible en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b6b0c-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="b6b0c-124">Cuando el reenvío de mensajes, no es necesario traducir los caracteres de separador en la línea de destinatarios con copia oculta los clientes.</span><span class="sxs-lookup"><span data-stu-id="b6b0c-124">When forwarding messages, clients do not need to translate the separator characters on the carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="b6b0c-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6b0c-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b6b0c-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b6b0c-126">Protocol specifications</span></span>

<span data-ttu-id="b6b0c-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6b0c-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6b0c-128">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b6b0c-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b6b0c-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b6b0c-129">Header files</span></span>

<span data-ttu-id="b6b0c-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6b0c-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6b0c-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b6b0c-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6b0c-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b6b0c-132">Mapitags.h</span></span>
  
> <span data-ttu-id="b6b0c-133">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b6b0c-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6b0c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6b0c-134">See also</span></span>



[<span data-ttu-id="b6b0c-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b6b0c-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6b0c-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b6b0c-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6b0c-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b6b0c-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6b0c-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b6b0c-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

