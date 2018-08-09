---
title: Propiedad canónica PidTagMessageRecipientMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e8ae52df1dd9775f706e2b1b2dc8b17b1f47a0bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819762"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="f3424-103">Propiedad canónica PidTagMessageRecipientMe</span><span class="sxs-lookup"><span data-stu-id="f3424-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="f3424-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f3424-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f3424-105">Contiene TRUE si este usuario de mensajería específicamente con nombre de un servidor principal (a), copia (CC) o destinatario de copia oculta (CCO) del mensaje y no forma parte de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="f3424-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3424-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f3424-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3424-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="f3424-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="f3424-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f3424-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f3424-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="f3424-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="f3424-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f3424-110">Data type:</span></span>  <br/> |<span data-ttu-id="f3424-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f3424-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f3424-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f3424-112">Area:</span></span>  <br/> |<span data-ttu-id="f3424-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="f3424-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3424-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3424-114">Remarks</span></span>

<span data-ttu-id="f3424-115">Esta propiedad proporciona una forma cómoda para determinar si el nombre de usuario aparece explícitamente en la lista de destinatarios, sin examinar todas las entradas de la lista.</span><span class="sxs-lookup"><span data-stu-id="f3424-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="f3424-116">El valor representa la operación de **OR** lógica de las propiedades **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) y **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) y la información de CCO (que no aparece en caso contrario, en una propiedad).</span><span class="sxs-lookup"><span data-stu-id="f3424-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="f3424-117">Esta propiedad ayuda a tratamiento automatizado de los mensajes recibidos en el momento de recepción.</span><span class="sxs-lookup"><span data-stu-id="f3424-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="f3424-118">En la opción del proveedor de transporte, esta propiedad contiene es FALSE o no se incluye si el usuario de mensajería no aparece directamente en la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="f3424-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="f3424-119">Entrega de mensajes que dan como resultado de la expansión de la lista de distribución no provoca que se establezca esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f3424-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="f3424-120">El destinatario debe denominarse explícitamente.</span><span class="sxs-lookup"><span data-stu-id="f3424-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="f3424-121">Por lo general los mensajes no enviados no establecer esta propiedad, **PR_MESSAGE_CC_ME**o **PR_MESSAGE_TO_ME**.</span><span class="sxs-lookup"><span data-stu-id="f3424-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="f3424-122">Si están presentes en los mensajes que puede obtener acceso el usuario en los almacenes de mensajes pública, en privado de los demás usuarios almacenes de archivos en el disco, o incrustado en otros mensajes recibidos, que generalmente contienen los valores a la que se establece la última vez que un proveedor de transporte entregado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f3424-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f3424-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f3424-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f3424-124">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f3424-124">Protocol specifications</span></span>

<span data-ttu-id="f3424-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3424-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3424-126">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f3424-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f3424-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3424-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3424-128">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f3424-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f3424-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f3424-129">Header files</span></span>

<span data-ttu-id="f3424-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f3424-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3424-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f3424-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="f3424-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f3424-132">Mapitags.h</span></span>
  
> <span data-ttu-id="f3424-133">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f3424-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3424-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3424-134">See also</span></span>



[<span data-ttu-id="f3424-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f3424-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3424-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f3424-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3424-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f3424-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3424-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f3424-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

