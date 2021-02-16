---
title: Propiedad canónica PidTagMessageToMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToMe
api_type:
- HeaderDef
ms.assetid: aeb0fa71-f471-46c5-ad9c-f8afb3fed533
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 96a0b010a8ba26a0c1b0cb409f1aaabb308a1c01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356199"
---
# <a name="pidtagmessagetome-canonical-property"></a><span data-ttu-id="d4b4b-103">Propiedad canónica PidTagMessageToMe</span><span class="sxs-lookup"><span data-stu-id="d4b4b-103">PidTagMessageToMe Canonical Property</span></span>

  
  
<span data-ttu-id="d4b4b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4b4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4b4b-105">Contiene TRUE si este usuario de mensajería se denomina específicamente como destinatario principal (Para) de este mensaje y no forma parte de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="d4b4b-105">Contains TRUE if this messaging user is specifically named as a primary (To) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4b4b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d4b4b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4b4b-107">PR_MESSAGE_TO_ME</span><span class="sxs-lookup"><span data-stu-id="d4b4b-107">PR_MESSAGE_TO_ME</span></span>  <br/> |
|<span data-ttu-id="d4b4b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d4b4b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d4b4b-109">0x0057</span><span class="sxs-lookup"><span data-stu-id="d4b4b-109">0x0057</span></span>  <br/> |
|<span data-ttu-id="d4b4b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d4b4b-110">Data type:</span></span>  <br/> |<span data-ttu-id="d4b4b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d4b4b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d4b4b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d4b4b-112">Area:</span></span>  <br/> |<span data-ttu-id="d4b4b-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="d4b4b-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4b4b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d4b4b-114">Remarks</span></span>

<span data-ttu-id="d4b4b-115">Esta propiedad proporciona una forma cómoda de determinar si el nombre de usuario aparece explícitamente en la lista de destinatarios principal, sin examinar todas las entradas de la lista.</span><span class="sxs-lookup"><span data-stu-id="d4b4b-115">This property provides a convenient way to determine whether the user name appears explicitly in the primary recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="d4b4b-116">Esta propiedad también ayuda a controlar de forma automatizada los mensajes recibidos en el momento de la recepción.</span><span class="sxs-lookup"><span data-stu-id="d4b4b-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="d4b4b-117">En la opción del proveedor de transporte, esta propiedad contiene FALSE o no se incluye si el usuario de mensajería no aparece directamente en la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="d4b4b-117">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="d4b4b-118">La entrega de mensajes resultante de la expansión de la lista de distribución o una designación de copia carbón no hace que se establezca esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4b4b-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="d4b4b-119">El destinatario debe tener un nombre explícito.</span><span class="sxs-lookup"><span data-stu-id="d4b4b-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="d4b4b-120">Por lo general, los mensajes no enviados no establecen el PR_MESSAGE_CC_ME **(** [PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) o esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4b4b-120">Unsent messages generally do not set the **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or this property.</span></span> <span data-ttu-id="d4b4b-121">Si están presentes en mensajes a los que el usuario puede acceder en almacenes de mensajes públicos, en almacenes privados de otros usuarios, en archivos en disco o incrustados dentro de otros mensajes recibidos, generalmente contienen los valores a los que se estableció la última vez que un proveedor de transporte entregó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d4b4b-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d4b4b-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4b4b-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4b4b-123">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="d4b4b-123">Protocol specifications</span></span>

<span data-ttu-id="d4b4b-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4b4b-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4b4b-125">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="d4b4b-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d4b4b-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4b4b-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4b4b-127">Especifica las propiedades y operaciones permitidas en los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="d4b4b-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4b4b-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d4b4b-128">Header files</span></span>

<span data-ttu-id="d4b4b-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4b4b-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4b4b-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d4b4b-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="d4b4b-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d4b4b-131">Mapitags.h</span></span>
  
> <span data-ttu-id="d4b4b-132">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d4b4b-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4b4b-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d4b4b-133">See also</span></span>



[<span data-ttu-id="d4b4b-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d4b4b-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4b4b-135">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="d4b4b-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4b4b-136">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d4b4b-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4b4b-137">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="d4b4b-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

