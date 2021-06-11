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
ms.openlocfilehash: 78423e874becdfc232b0dd964b32ae0c4530d19e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325623"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="fee0f-103">Propiedad canónica PidTagMessageRecipientMe</span><span class="sxs-lookup"><span data-stu-id="fee0f-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="fee0f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fee0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fee0f-105">Contiene TRUE si este usuario de mensajería se denomina específicamente como destinatario principal (Para), copia de carbono (CC) o copia de carbón ciego (CCO) destinatario de este mensaje y no forma parte de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="fee0f-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fee0f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fee0f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fee0f-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="fee0f-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="fee0f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fee0f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fee0f-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="fee0f-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="fee0f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fee0f-110">Data type:</span></span>  <br/> |<span data-ttu-id="fee0f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fee0f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fee0f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fee0f-112">Area:</span></span>  <br/> |<span data-ttu-id="fee0f-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="fee0f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fee0f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fee0f-114">Remarks</span></span>

<span data-ttu-id="fee0f-115">Esta propiedad proporciona una forma cómoda de determinar si el nombre de usuario aparece explícitamente en la lista de destinatarios, sin examinar todas las entradas de la lista.</span><span class="sxs-lookup"><span data-stu-id="fee0f-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="fee0f-116">El valor representa la operación **OR** lógica de las propiedades **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) y **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) y la información CCO (que de lo contrario no aparece en una propiedad).</span><span class="sxs-lookup"><span data-stu-id="fee0f-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="fee0f-117">Esta propiedad ayuda al tratamiento automatizado de los mensajes recibidos en el momento de la recepción.</span><span class="sxs-lookup"><span data-stu-id="fee0f-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="fee0f-118">En la opción del proveedor de transporte, esta propiedad contiene FALSE o no se incluye si el usuario de mensajería no aparece directamente en la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="fee0f-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="fee0f-119">La entrega de mensajes que resulta de la expansión de la lista de distribución no hace que se establezca esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="fee0f-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="fee0f-120">El destinatario debe tener un nombre explícito.</span><span class="sxs-lookup"><span data-stu-id="fee0f-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="fee0f-121">Por lo general, los mensajes no enviados no establecen esta propiedad, **PR_MESSAGE_CC_ME**, o **PR_MESSAGE_TO_ME**.</span><span class="sxs-lookup"><span data-stu-id="fee0f-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="fee0f-122">Si están presentes en mensajes a los que el usuario puede acceder en almacenes de mensajes públicos, en almacenes privados de otros usuarios, en archivos en disco o incrustados dentro de otros mensajes recibidos, generalmente contienen los valores a los que se les estableció la última vez que un proveedor de transporte entregó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fee0f-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fee0f-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fee0f-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fee0f-124">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="fee0f-124">Protocol specifications</span></span>

<span data-ttu-id="fee0f-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fee0f-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fee0f-126">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="fee0f-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fee0f-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fee0f-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fee0f-128">Especifica las propiedades y las operaciones permitidas en objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="fee0f-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fee0f-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fee0f-129">Header files</span></span>

<span data-ttu-id="fee0f-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fee0f-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="fee0f-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fee0f-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="fee0f-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fee0f-132">Mapitags.h</span></span>
  
> <span data-ttu-id="fee0f-133">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fee0f-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fee0f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="fee0f-134">See also</span></span>



[<span data-ttu-id="fee0f-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fee0f-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fee0f-136">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fee0f-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fee0f-137">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fee0f-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fee0f-138">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="fee0f-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

