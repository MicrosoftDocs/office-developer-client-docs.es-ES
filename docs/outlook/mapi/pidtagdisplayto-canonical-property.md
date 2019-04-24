---
title: Propiedad canónica PidTagDisplayTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTo
api_type:
- HeaderDef
ms.assetid: 700cc03b-5d98-40ce-adb5-a11fdac8aa28
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0c7ae8951b02f099161871b17ff59ea23f8fbcc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360791"
---
# <a name="pidtagdisplayto-canonical-property"></a><span data-ttu-id="4d8f6-103">Propiedad canónica PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="4d8f6-103">PidTagDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="4d8f6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d8f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d8f6-105">Contiene una lista de los nombres para mostrar de los destinatarios de mensajes principales (para), separados por punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="4d8f6-105">Contains a list of the display names of the primary (To) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d8f6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4d8f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d8f6-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="4d8f6-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="4d8f6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4d8f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4d8f6-109">0x0E04</span><span class="sxs-lookup"><span data-stu-id="4d8f6-109">0x0E04</span></span>  <br/> |
|<span data-ttu-id="4d8f6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4d8f6-110">Data type:</span></span>  <br/> |<span data-ttu-id="4d8f6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4d8f6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4d8f6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4d8f6-112">Area:</span></span>  <br/> |<span data-ttu-id="4d8f6-113">Mensaje</span><span class="sxs-lookup"><span data-stu-id="4d8f6-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d8f6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d8f6-114">Remarks</span></span>

<span data-ttu-id="4d8f6-115">El almacén de mensajes calcula estas propiedades en objetos de mensaje mediante el método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="4d8f6-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="4d8f6-116">El almacén de mensajes también mantiene estas propiedades para que siempre refleje el último estado guardado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4d8f6-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="4d8f6-117">El valor se sincroniza en el momento de cada llamada al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="4d8f6-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="4d8f6-118">Si un mensaje no tiene destinatarios principales, el almacén de mensajes debe responder a una llamada [IMAPIProp:: GetProps](imapiprop-getprops.md) con un valor devuelto de S_OK y una cadena vacía para **PR_DISPLAY_TO**.</span><span class="sxs-lookup"><span data-stu-id="4d8f6-118">If a message has no primary recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_TO**.</span></span> 
  
<span data-ttu-id="4d8f6-119">Debido a la posible necesidad de localización, MAPI proporciona estas directrices para todos los nombres de los destinatarios:</span><span class="sxs-lookup"><span data-stu-id="4d8f6-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="4d8f6-120">Todos los nombres deben poder localizarse.</span><span class="sxs-lookup"><span data-stu-id="4d8f6-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="4d8f6-121">El punto y coma debe ser el carácter que se usa para separar los nombres en las propiedades **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) y **PR_DISPLAY_TO** .</span><span class="sxs-lookup"><span data-stu-id="4d8f6-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** properties.</span></span> <span data-ttu-id="4d8f6-122">No se permiten signos de punto y coma en los nombres de los destinatarios en MAPI.</span><span class="sxs-lookup"><span data-stu-id="4d8f6-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="4d8f6-123">Los clientes deben traducir cada punto y coma detectado en **PR_DISPLAY_TO** y las propiedades relacionadas a un carácter separador localizado antes de que la información sea visible en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d8f6-123">Clients should translate each semicolon encountered in the **PR_DISPLAY_TO** and related properties to a localized separator character before making the information visible in the user interface.</span></span> 
    
- <span data-ttu-id="4d8f6-124">Al reenviar mensajes, no es necesario que los clientes traduzcan los caracteres separadores de la línea de destinatario principal.</span><span class="sxs-lookup"><span data-stu-id="4d8f6-124">When forwarding messages, clients do not need to translate the separator characters on the primary recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="4d8f6-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d8f6-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4d8f6-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4d8f6-126">Protocol specifications</span></span>

<span data-ttu-id="4d8f6-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d8f6-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d8f6-128">Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4d8f6-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4d8f6-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4d8f6-129">Header files</span></span>

<span data-ttu-id="4d8f6-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4d8f6-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d8f6-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4d8f6-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="4d8f6-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4d8f6-132">Mapitags.h</span></span>
  
> <span data-ttu-id="4d8f6-133">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4d8f6-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d8f6-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d8f6-134">See also</span></span>



[<span data-ttu-id="4d8f6-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4d8f6-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d8f6-136">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="4d8f6-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d8f6-137">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4d8f6-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d8f6-138">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4d8f6-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

