---
title: Propiedad canónica PidTagDisplayBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayBcc
api_type:
- HeaderDef
ms.assetid: ab5bcd67-d54e-46e9-b94e-a652aac3e81c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 74669d102462e1a825568615d1d30346e99e90a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360819"
---
# <a name="pidtagdisplaybcc-canonical-property"></a><span data-ttu-id="63e3b-103">Propiedad canónica PidTagDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="63e3b-103">PidTagDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="63e3b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63e3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63e3b-105">Contiene una lista ASCII de los nombres para mostrar de los destinatarios del mensaje de copia oculta (CCO), separados por punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="63e3b-105">Contains an ASCII list of the display names of any blind carbon copy (BCC) message recipients, separated by semicolons (;).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63e3b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="63e3b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63e3b-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="63e3b-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="63e3b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="63e3b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="63e3b-109">0x0E02</span><span class="sxs-lookup"><span data-stu-id="63e3b-109">0x0E02</span></span>  <br/> |
|<span data-ttu-id="63e3b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="63e3b-110">Data type:</span></span>  <br/> |<span data-ttu-id="63e3b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="63e3b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="63e3b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="63e3b-112">Area:</span></span>  <br/> |<span data-ttu-id="63e3b-113">Mensaje</span><span class="sxs-lookup"><span data-stu-id="63e3b-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63e3b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63e3b-114">Remarks</span></span>

<span data-ttu-id="63e3b-115">El almacén de mensajes calcula estas propiedades en objetos de mensaje mediante el método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="63e3b-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="63e3b-116">El almacén de mensajes también mantiene estas propiedades para que siempre refleje el último estado guardado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="63e3b-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="63e3b-117">El valor se sincroniza en el momento de cada llamada al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="63e3b-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="63e3b-118">Si un mensaje no tiene destinatarios ocultos de copia, el almacén de mensajes debe responder a una llamada de [IMAPIProp:: GetProps](imapiprop-getprops.md) con un valor devuelto de S_OK y una cadena vacía para **PR_DISPLAY_BCC**.</span><span class="sxs-lookup"><span data-stu-id="63e3b-118">If a message has no blind carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_BCC**.</span></span> 
  
<span data-ttu-id="63e3b-119">Debido a la posible necesidad de localización, MAPI proporciona estas directrices para todos los nombres de los destinatarios:</span><span class="sxs-lookup"><span data-stu-id="63e3b-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="63e3b-120">Todos los nombres deben poder localizarse.</span><span class="sxs-lookup"><span data-stu-id="63e3b-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="63e3b-121">El punto y coma debe ser el carácter que se usa para separar los nombres en las propiedades **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) y **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="63e3b-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="63e3b-122">No se permiten signos de punto y coma en los nombres de los destinatarios en MAPI.</span><span class="sxs-lookup"><span data-stu-id="63e3b-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="63e3b-123">Los clientes deben traducir cada punto y coma encontrado en esta propiedad a un carácter separador localizado antes de hacer visible la información de propiedad en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="63e3b-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="63e3b-124">Al reenviar mensajes, no es necesario que los clientes traduzcan los caracteres separadores de la línea de destinatarios con copia oculta.</span><span class="sxs-lookup"><span data-stu-id="63e3b-124">When forwarding messages, clients do not need to translate the separator characters on the blind carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="63e3b-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="63e3b-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63e3b-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="63e3b-126">Protocol specifications</span></span>

<span data-ttu-id="63e3b-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63e3b-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63e3b-128">Describe el formato de los mensajes usados para enviar información relacionada con carpetas de uso compartido en el cliente.</span><span class="sxs-lookup"><span data-stu-id="63e3b-128">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63e3b-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="63e3b-129">Header files</span></span>

<span data-ttu-id="63e3b-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="63e3b-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="63e3b-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="63e3b-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="63e3b-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="63e3b-132">Mapitags.h</span></span>
  
> <span data-ttu-id="63e3b-133">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="63e3b-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63e3b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="63e3b-134">See also</span></span>



[<span data-ttu-id="63e3b-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="63e3b-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63e3b-136">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="63e3b-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63e3b-137">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="63e3b-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63e3b-138">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="63e3b-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

