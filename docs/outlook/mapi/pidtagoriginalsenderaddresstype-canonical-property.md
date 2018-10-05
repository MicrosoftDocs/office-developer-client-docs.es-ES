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
ms.openlocfilehash: d593b5ae1c2341ae0972ba68bcf42dde64e9a2f1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401709"
---
# <a name="pidtagoriginalsenderaddresstype-canonical-property"></a><span data-ttu-id="c133e-103">Propiedad canónica PidTagOriginalSenderAddressType</span><span class="sxs-lookup"><span data-stu-id="c133e-103">PidTagOriginalSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="c133e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c133e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c133e-105">Contiene el tipo de dirección del remitente de la primera versión de un mensaje, es decir, el mensaje antes de que se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="c133e-105">Contains the address type of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c133e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c133e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c133e-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="c133e-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="c133e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c133e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c133e-109">0 x 0066</span><span class="sxs-lookup"><span data-stu-id="c133e-109">0x0066</span></span>  <br/> |
|<span data-ttu-id="c133e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c133e-110">Data type:</span></span>  <br/> |<span data-ttu-id="c133e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c133e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c133e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c133e-112">Area:</span></span>  <br/> |<span data-ttu-id="c133e-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="c133e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c133e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c133e-114">Remarks</span></span>

<span data-ttu-id="c133e-115">Estas propiedades son ejemplos de las propiedades de direcciones para el remitente original de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="c133e-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="c133e-116">En el primer envío del mensaje, la aplicación cliente debe establecer estas propiedades en el valor de **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c133e-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span></span> <span data-ttu-id="c133e-117">Nunca se ha cambiado cuando el mensaje se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="c133e-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c133e-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c133e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c133e-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c133e-119">Protocol specifications</span></span>

<span data-ttu-id="c133e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c133e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c133e-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c133e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c133e-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c133e-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c133e-123">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c133e-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c133e-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c133e-124">Header files</span></span>

<span data-ttu-id="c133e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c133e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c133e-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c133e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c133e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c133e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c133e-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c133e-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c133e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c133e-129">See also</span></span>



[<span data-ttu-id="c133e-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c133e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c133e-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c133e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c133e-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c133e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c133e-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c133e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

