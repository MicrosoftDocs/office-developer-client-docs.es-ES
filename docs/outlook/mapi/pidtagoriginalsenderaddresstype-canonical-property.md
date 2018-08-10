---
title: Propiedad canónica PidTagOriginalSenderAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderAddressType
api_type:
- COM
ms.assetid: bd777f19-cbb1-4497-8a0b-e05b491c6957
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5cac96287db9638f699b75e0c387e003beb5e197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819838"
---
# <a name="pidtagoriginalsenderaddresstype-canonical-property"></a><span data-ttu-id="332ec-103">Propiedad canónica PidTagOriginalSenderAddressType</span><span class="sxs-lookup"><span data-stu-id="332ec-103">PidTagOriginalSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="332ec-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="332ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="332ec-105">Contiene el tipo de dirección del remitente de la primera versión de un mensaje, es decir, el mensaje antes de que se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="332ec-105">Contains the address type of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="332ec-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="332ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="332ec-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="332ec-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="332ec-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="332ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="332ec-109">0 x 0066</span><span class="sxs-lookup"><span data-stu-id="332ec-109">0x0066</span></span>  <br/> |
|<span data-ttu-id="332ec-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="332ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="332ec-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="332ec-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="332ec-112">Área:</span><span class="sxs-lookup"><span data-stu-id="332ec-112">Area:</span></span>  <br/> |<span data-ttu-id="332ec-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="332ec-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="332ec-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="332ec-114">Remarks</span></span>

<span data-ttu-id="332ec-115">Estas propiedades son ejemplos de las propiedades de direcciones para el remitente original de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="332ec-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="332ec-116">En el primer envío del mensaje, la aplicación cliente debe establecer estas propiedades en el valor de **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="332ec-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span></span> <span data-ttu-id="332ec-117">Nunca se ha cambiado cuando el mensaje se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="332ec-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="332ec-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="332ec-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="332ec-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="332ec-119">Protocol specifications</span></span>

<span data-ttu-id="332ec-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="332ec-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="332ec-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="332ec-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="332ec-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="332ec-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="332ec-123">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="332ec-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="332ec-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="332ec-124">Header files</span></span>

<span data-ttu-id="332ec-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="332ec-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="332ec-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="332ec-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="332ec-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="332ec-127">Mapitags.h</span></span>
  
> <span data-ttu-id="332ec-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="332ec-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="332ec-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="332ec-129">See also</span></span>



[<span data-ttu-id="332ec-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="332ec-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="332ec-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="332ec-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="332ec-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="332ec-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="332ec-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="332ec-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
