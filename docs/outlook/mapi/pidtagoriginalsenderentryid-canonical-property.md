---
title: Propiedad canónica PidTagOriginalSenderEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEntryId
api_type:
- COM
ms.assetid: bd182589-afea-4967-92f5-ba1914e4db3f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bd32ef6540e0deec1b793bd49bab651d864754c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393834"
---
# <a name="pidtagoriginalsenderentryid-canonical-property"></a><span data-ttu-id="20965-103">Propiedad canónica PidTagOriginalSenderEntryId</span><span class="sxs-lookup"><span data-stu-id="20965-103">PidTagOriginalSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="20965-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20965-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20965-105">Contiene el identificador de entrada del remitente de la primera versión de un mensaje, es decir, el mensaje antes de que se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="20965-105">Contains the entry identifier of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20965-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="20965-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="20965-107">PR_ORIGINAL_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="20965-107">PR_ORIGINAL_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="20965-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="20965-108">Identifier:</span></span>  <br/> |<span data-ttu-id="20965-109">0x005B</span><span class="sxs-lookup"><span data-stu-id="20965-109">0x005B</span></span>  <br/> |
|<span data-ttu-id="20965-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="20965-110">Data type:</span></span>  <br/> |<span data-ttu-id="20965-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="20965-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="20965-112">Área:</span><span class="sxs-lookup"><span data-stu-id="20965-112">Area:</span></span>  <br/> |<span data-ttu-id="20965-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="20965-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20965-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20965-114">Remarks</span></span>

<span data-ttu-id="20965-115">Esta propiedad es una de las propiedades de direcciones para el remitente original de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="20965-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="20965-116">En el primer envío del mensaje, una aplicación cliente debe establecer esta propiedad en el valor de la propiedad **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="20965-116">At first submission of the message, a client application should set this property to the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="20965-117">Nunca se ha cambiado cuando el mensaje se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="20965-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="20965-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="20965-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="20965-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="20965-119">Protocol specifications</span></span>

<span data-ttu-id="20965-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20965-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20965-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="20965-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="20965-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20965-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20965-123">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="20965-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="20965-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="20965-124">Header files</span></span>

<span data-ttu-id="20965-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20965-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="20965-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="20965-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="20965-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="20965-127">Mapitags.h</span></span>
  
> <span data-ttu-id="20965-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="20965-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20965-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="20965-129">See also</span></span>



[<span data-ttu-id="20965-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="20965-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20965-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="20965-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20965-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="20965-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20965-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="20965-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

