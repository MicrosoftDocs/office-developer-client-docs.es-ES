---
title: Propiedad canónica PidTagMessageCcMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 82d043adfe6e480b4d490f44ad89d73535c80c9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569781"
---
# <a name="pidtagmessageccme-canonical-property"></a><span data-ttu-id="52951-103">Propiedad canónica PidTagMessageCcMe</span><span class="sxs-lookup"><span data-stu-id="52951-103">PidTagMessageCcMe Canonical Property</span></span>

  
  
<span data-ttu-id="52951-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52951-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52951-105">Contiene TRUE si este usuario de mensajería específicamente con nombre de un destinatario de copia (CC) de este mensaje y no forma parte de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="52951-105">Contains TRUE if this messaging user is specifically named as a carbon copy (CC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52951-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="52951-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52951-107">PR_MESSAGE_CC_ME</span><span class="sxs-lookup"><span data-stu-id="52951-107">PR_MESSAGE_CC_ME</span></span>  <br/> |
|<span data-ttu-id="52951-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="52951-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52951-109">0x0058</span><span class="sxs-lookup"><span data-stu-id="52951-109">0x0058</span></span>  <br/> |
|<span data-ttu-id="52951-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="52951-110">Data type:</span></span>  <br/> |<span data-ttu-id="52951-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="52951-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="52951-112">Área:</span><span class="sxs-lookup"><span data-stu-id="52951-112">Area:</span></span>  <br/> |<span data-ttu-id="52951-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="52951-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52951-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52951-114">Remarks</span></span>

<span data-ttu-id="52951-115">Esta propiedad proporciona una forma cómoda para determinar si el nombre de usuario aparece explícitamente en la lista de destinatarios con copia oculta, sin examinar todas las entradas de la lista.</span><span class="sxs-lookup"><span data-stu-id="52951-115">This property provides a convenient way to determine whether the user name appears explicitly in the carbon copy recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="52951-116">Esta propiedad también ayuda a tratamiento automatizado de los mensajes recibidos en el momento de recepción.</span><span class="sxs-lookup"><span data-stu-id="52951-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="52951-117">En la opción del proveedor de transporte, esta propiedad contiene es FALSE o no se establece si el usuario de mensajería no aparece directamente en la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="52951-117">At the transport provider's option, this property either contains FALSE or is not set if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="52951-118">Entrega del mensaje resultante de expansión de lista de distribución o una designación de copia oculta no causa esta propiedad va a establecer.</span><span class="sxs-lookup"><span data-stu-id="52951-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="52951-119">El destinatario debe denominarse explícitamente.</span><span class="sxs-lookup"><span data-stu-id="52951-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="52951-120">Por lo general, los mensajes no enviados no establezca esta propiedad, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) o **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="52951-120">Unsent messages generally do not set this property, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span></span> <span data-ttu-id="52951-121">Si están presentes en los mensajes que puede obtener acceso el usuario en los almacenes de mensajes pública, en privado de los demás usuarios almacenes de archivos en el disco, o incrustado en otros mensajes recibidos, que generalmente contienen los valores a la que se establece la última vez que un proveedor de transporte entregado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="52951-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="52951-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="52951-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52951-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="52951-123">Protocol specifications</span></span>

<span data-ttu-id="52951-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52951-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52951-125">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="52951-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="52951-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52951-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52951-127">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="52951-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52951-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="52951-128">Header files</span></span>

<span data-ttu-id="52951-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52951-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="52951-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="52951-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="52951-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="52951-131">Mapitags.h</span></span>
  
> <span data-ttu-id="52951-132">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="52951-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52951-133">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="52951-133">See also</span></span>



[<span data-ttu-id="52951-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="52951-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52951-135">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="52951-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52951-136">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="52951-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52951-137">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="52951-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

