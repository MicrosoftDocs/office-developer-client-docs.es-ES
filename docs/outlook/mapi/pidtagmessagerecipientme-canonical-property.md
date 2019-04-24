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
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="d4812-103">Propiedad canónica PidTagMessageRecipientMe</span><span class="sxs-lookup"><span data-stu-id="d4812-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="d4812-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4812-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4812-105">ConTains TRUE si este mensaje de mensajería tiene el mismo nombre que el de un destinatario principal (para), con copia carbón (CC) o con copia oculta (CCO) de este mensaje y no forma parte de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="d4812-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4812-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d4812-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4812-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="d4812-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="d4812-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d4812-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d4812-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="d4812-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="d4812-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d4812-110">Data type:</span></span>  <br/> |<span data-ttu-id="d4812-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d4812-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d4812-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d4812-112">Area:</span></span>  <br/> |<span data-ttu-id="d4812-113">Mensajes generales</span><span class="sxs-lookup"><span data-stu-id="d4812-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4812-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d4812-114">Remarks</span></span>

<span data-ttu-id="d4812-115">Esta propiedad proporciona una forma cómoda de determinar si el nombre de usuario aparece de forma explícita en la lista de destinatarios, sin examinar todas las entradas de la lista.</span><span class="sxs-lookup"><span data-stu-id="d4812-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="d4812-116">El valor representa la operación **or** lógica de las propiedades **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) y **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), así como la información de CCO (que no aparece en ningún caso en un propiedad).</span><span class="sxs-lookup"><span data-stu-id="d4812-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="d4812-117">Esta propiedad ayuda a controlar de forma automática los mensajes recibidos en el momento de la recepción.</span><span class="sxs-lookup"><span data-stu-id="d4812-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="d4812-118">En la opción del proveedor de transporte, esta propiedad contiene FALSE o no se incluye si el usuario de mensajería no aparece directamente en la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="d4812-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="d4812-119">La entrega de mensajes resultante de la expansión de la lista de distribución no hace que se establezca esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4812-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="d4812-120">El destinatario debe tener un nombre explícito.</span><span class="sxs-lookup"><span data-stu-id="d4812-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="d4812-121">Por lo general, los mensajes no enviados no establecen esta propiedad, **PR_MESSAGE_CC_ME**o **PR_MESSAGE_TO_ME**.</span><span class="sxs-lookup"><span data-stu-id="d4812-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="d4812-122">Si están presentes en los mensajes a los que el usuario puede tener acceso en los almacenes públicos de mensajes, en los almacenes privados de otros usuarios o en los archivos del disco, o incrustados dentro de otros mensajes recibidos, suelen contener los valores para los que se establecieron la última vez que un proveedor de transporte entregó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d4812-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d4812-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4812-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4812-124">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d4812-124">Protocol specifications</span></span>

<span data-ttu-id="d4812-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4812-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4812-126">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d4812-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d4812-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4812-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4812-128">Especifica las propiedades y operaciones que se admiten en los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="d4812-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4812-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d4812-129">Header files</span></span>

<span data-ttu-id="d4812-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d4812-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4812-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d4812-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="d4812-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d4812-132">Mapitags.h</span></span>
  
> <span data-ttu-id="d4812-133">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d4812-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4812-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4812-134">See also</span></span>



[<span data-ttu-id="d4812-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d4812-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4812-136">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="d4812-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4812-137">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d4812-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4812-138">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="d4812-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

