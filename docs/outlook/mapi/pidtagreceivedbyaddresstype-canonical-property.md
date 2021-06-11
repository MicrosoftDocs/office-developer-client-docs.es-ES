---
title: Propiedad canónica PidTagReceivedByAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByAddressType
api_type:
- COM
ms.assetid: 0eef299d-6923-4dae-9a18-91ea82ea0f3e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 00c07069ed174fe55556dfe48398d65b4e64100e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359230"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a><span data-ttu-id="42990-103">Propiedad canónica PidTagReceivedByAddressType</span><span class="sxs-lookup"><span data-stu-id="42990-103">PidTagReceivedByAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="42990-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42990-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42990-105">Contiene el tipo de dirección de correo electrónico, como SMTP, para el usuario de mensajería que realmente recibe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="42990-105">Contains the email address type, such as SMTP, for the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42990-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="42990-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="42990-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="42990-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="42990-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="42990-108">Identifier:</span></span>  <br/> |<span data-ttu-id="42990-109">0x0075</span><span class="sxs-lookup"><span data-stu-id="42990-109">0x0075</span></span>  <br/> |
|<span data-ttu-id="42990-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="42990-110">Data type:</span></span>  <br/> |<span data-ttu-id="42990-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="42990-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="42990-112">Área:</span><span class="sxs-lookup"><span data-stu-id="42990-112">Area:</span></span>  <br/> |<span data-ttu-id="42990-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="42990-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42990-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42990-114">Remarks</span></span>

<span data-ttu-id="42990-115">Estas propiedades son ejemplos de las propiedades de dirección del usuario de mensajería que realmente recibe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="42990-115">These properties are examples of the address properties for the messaging user who actually receives the message.</span></span> <span data-ttu-id="42990-116">Deben ser establecidas por el proveedor de transporte entrante.</span><span class="sxs-lookup"><span data-stu-id="42990-116">They must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="42990-117">La cadena de tipo de dirección solo puede contener los caracteres alfabéticos en mayúsculas A a Z y los números de cero a nueve.</span><span class="sxs-lookup"><span data-stu-id="42990-117">The address type string can contain only the uppercase alphabetic characters A through Z and the numbers zero through nine.</span></span> <span data-ttu-id="42990-118">Estas propiedades califican la propiedad **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) especificando un tipo de dirección, como SMTP, lo que indica cómo se debe construir la dirección.</span><span class="sxs-lookup"><span data-stu-id="42990-118">These properties qualify the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property by specifying an address type, such as SMTP, thereby indicating how the address should be constructed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="42990-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="42990-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="42990-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="42990-120">Protocol specifications</span></span>

<span data-ttu-id="42990-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42990-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42990-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="42990-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="42990-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42990-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42990-124">Especifica las propiedades y las operaciones permitidas en los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="42990-124">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="42990-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="42990-125">Header files</span></span>

<span data-ttu-id="42990-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="42990-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="42990-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="42990-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="42990-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="42990-128">Mapitags.h</span></span>
  
> <span data-ttu-id="42990-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="42990-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="42990-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="42990-130">See also</span></span>



[<span data-ttu-id="42990-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="42990-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="42990-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="42990-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="42990-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="42990-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="42990-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="42990-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

