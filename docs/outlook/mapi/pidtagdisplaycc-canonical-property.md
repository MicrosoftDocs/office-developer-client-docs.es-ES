---
title: Propiedad canónico PidTagDisplayCc
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 6257557a8848c1abbaf8ceb15f719c50e4fec8c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819455"
---
# <a name="pidtagdisplaycc-canonical-property"></a><span data-ttu-id="29880-103">Propiedad canónico PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="29880-103">PidTagDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="29880-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="29880-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="29880-105">Contiene una lista de ASCII de los nombres para mostrar de los destinatarios del mensaje con copia (CC), separados por punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="29880-105">Contains an ASCII list of the display names of any carbon copy (CC) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29880-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="29880-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="29880-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="29880-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="29880-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="29880-108">Identifier:</span></span>  <br/> |<span data-ttu-id="29880-109">0x0E03</span><span class="sxs-lookup"><span data-stu-id="29880-109">0x0E03</span></span>  <br/> |
|<span data-ttu-id="29880-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="29880-110">Data type:</span></span>  <br/> |<span data-ttu-id="29880-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="29880-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="29880-112">Área:</span><span class="sxs-lookup"><span data-stu-id="29880-112">Area:</span></span>  <br/> |<span data-ttu-id="29880-113">Message</span><span class="sxs-lookup"><span data-stu-id="29880-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29880-114">Notas</span><span class="sxs-lookup"><span data-stu-id="29880-114">Remarks</span></span>

<span data-ttu-id="29880-115">El almacén de mensajes calcula estas propiedades en los objetos de mensaje con el método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="29880-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="29880-116">El almacén de mensajes también mantiene estas propiedades para que siempre refleja el último estado guardado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="29880-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="29880-117">El valor se sincroniza en el momento de todas las llamadas a [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="29880-117">The value is synchronized at the time of every call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> 
  
<span data-ttu-id="29880-118">Si un mensaje no tiene ningún destinatarios en copia oculta, el almacén de mensajes debe responder a una llamada [IMAPIProp::GetProps](imapiprop-getprops.md) con un valor devuelto de S_OK y una cadena vacía para estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="29880-118">If a message has no carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for these properties.</span></span> 
  
<span data-ttu-id="29880-119">Debido a la necesidad de posible para la localización, MAPI proporciona estas instrucciones para todos los nombres de los destinatarios:</span><span class="sxs-lookup"><span data-stu-id="29880-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="29880-120">Todos los nombres de deberían poder ser localizada.</span><span class="sxs-lookup"><span data-stu-id="29880-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="29880-121">El punto y coma debe ser el carácter que se usa para separar los nombres en las propiedades de **PR_DISPLAY_TO de MAPI** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC**y **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="29880-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**, and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="29880-122">Punto y coma no se permite dentro de nombres de los destinatarios en MAPI.</span><span class="sxs-lookup"><span data-stu-id="29880-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="29880-123">Los clientes deben traducir cada punto y coma detectado en esta propiedad para un carácter de separador localizadas antes de realizar la información de la propiedad visible en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="29880-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="29880-124">Cuando el reenvío de mensajes, no es necesario traducir los caracteres de separador en la línea de destinatarios con copia oculta los clientes.</span><span class="sxs-lookup"><span data-stu-id="29880-124">When forwarding messages, clients do not need to translate the separator characters on the carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="29880-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="29880-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="29880-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="29880-126">Protocol specifications</span></span>

<span data-ttu-id="29880-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29880-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29880-128">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="29880-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="29880-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="29880-129">Header files</span></span>

<span data-ttu-id="29880-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="29880-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="29880-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="29880-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="29880-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="29880-132">Mapitags.h</span></span>
  
> <span data-ttu-id="29880-133">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="29880-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29880-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="29880-134">See also</span></span>



[<span data-ttu-id="29880-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="29880-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="29880-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="29880-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="29880-137">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="29880-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="29880-138">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="29880-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

