---
title: Propiedad canónica PidTagResponseRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponseRequested
api_type:
- COM
ms.assetid: e52bb48c-7107-4ac4-b030-885409759ee7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 77c724affd2057ca6347d752323c5ba0a3094ecf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330159"
---
# <a name="pidtagresponserequested-canonical-property"></a><span data-ttu-id="33c7e-103">Propiedad canónica PidTagResponseRequested</span><span class="sxs-lookup"><span data-stu-id="33c7e-103">PidTagResponseRequested Canonical Property</span></span>

  
  
<span data-ttu-id="33c7e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33c7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33c7e-105">Contiene TRUE si el remitente del mensaje quiere una respuesta a una solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="33c7e-105">Contains TRUE if the message sender wants a response to a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33c7e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="33c7e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33c7e-107">PR_RESPONSE_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="33c7e-107">PR_RESPONSE_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="33c7e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="33c7e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="33c7e-109">0x0063</span><span class="sxs-lookup"><span data-stu-id="33c7e-109">0x0063</span></span>  <br/> |
|<span data-ttu-id="33c7e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="33c7e-110">Data type:</span></span>  <br/> |<span data-ttu-id="33c7e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="33c7e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="33c7e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="33c7e-112">Area:</span></span>  <br/> |<span data-ttu-id="33c7e-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="33c7e-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33c7e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="33c7e-114">Remarks</span></span>

<span data-ttu-id="33c7e-115">Esta propiedad se usa para las solicitudes de reunión.</span><span class="sxs-lookup"><span data-stu-id="33c7e-115">This property is used for meeting requests.</span></span> <span data-ttu-id="33c7e-116">La aplicación cliente receptora debe pedir al usuario que acepte o rechace la solicitud y, a continuación, envíe esta respuesta al remitente.</span><span class="sxs-lookup"><span data-stu-id="33c7e-116">The receiving client application should prompt the user to accept or decline the request and then send this response back to the sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="33c7e-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="33c7e-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33c7e-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="33c7e-118">Protocol specifications</span></span>

<span data-ttu-id="33c7e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33c7e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33c7e-120">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="33c7e-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="33c7e-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33c7e-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33c7e-122">Especifica las propiedades y las operaciones permitidas en los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="33c7e-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="33c7e-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33c7e-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33c7e-124">Especifica las propiedades y las operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="33c7e-124">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="33c7e-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33c7e-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33c7e-126">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="33c7e-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33c7e-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="33c7e-127">Header files</span></span>

<span data-ttu-id="33c7e-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33c7e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="33c7e-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="33c7e-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="33c7e-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="33c7e-130">Mapitags.h</span></span>
  
> <span data-ttu-id="33c7e-131">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="33c7e-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33c7e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="33c7e-132">See also</span></span>



[<span data-ttu-id="33c7e-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="33c7e-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33c7e-134">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="33c7e-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33c7e-135">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="33c7e-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33c7e-136">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="33c7e-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

