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
ms.openlocfilehash: b099bf5df657b5516fbf0948e742d1d1b36af2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820109"
---
# <a name="pidtagresponserequested-canonical-property"></a><span data-ttu-id="08b37-103">Propiedad canónica PidTagResponseRequested</span><span class="sxs-lookup"><span data-stu-id="08b37-103">PidTagResponseRequested Canonical Property</span></span>

  
  
<span data-ttu-id="08b37-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08b37-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08b37-105">Contiene TRUE si el remitente del mensaje desea una respuesta a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="08b37-105">Contains TRUE if the message sender wants a response to a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08b37-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="08b37-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08b37-107">PR_RESPONSE_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="08b37-107">PR_RESPONSE_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="08b37-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="08b37-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08b37-109">0x0063</span><span class="sxs-lookup"><span data-stu-id="08b37-109">0x0063</span></span>  <br/> |
|<span data-ttu-id="08b37-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="08b37-110">Data type:</span></span>  <br/> |<span data-ttu-id="08b37-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="08b37-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="08b37-112">Área:</span><span class="sxs-lookup"><span data-stu-id="08b37-112">Area:</span></span>  <br/> |<span data-ttu-id="08b37-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="08b37-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08b37-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08b37-114">Remarks</span></span>

<span data-ttu-id="08b37-115">Esta propiedad se usa para las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="08b37-115">This property is used for meeting requests.</span></span> <span data-ttu-id="08b37-116">La aplicación receptora de cliente debe solicitar al usuario para aceptar o rechazar la solicitud y, a continuación, enviar esta respuesta al remitente.</span><span class="sxs-lookup"><span data-stu-id="08b37-116">The receiving client application should prompt the user to accept or decline the request and then send this response back to the sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="08b37-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="08b37-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08b37-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="08b37-118">Protocol specifications</span></span>

<span data-ttu-id="08b37-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08b37-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08b37-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="08b37-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="08b37-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08b37-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08b37-122">Especifica las propiedades y operaciones que se permiten en mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="08b37-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="08b37-123">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08b37-123">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08b37-124">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="08b37-124">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="08b37-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08b37-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08b37-126">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="08b37-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08b37-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="08b37-127">Header files</span></span>

<span data-ttu-id="08b37-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08b37-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="08b37-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="08b37-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="08b37-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="08b37-130">Mapitags.h</span></span>
  
> <span data-ttu-id="08b37-131">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="08b37-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08b37-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="08b37-132">See also</span></span>



[<span data-ttu-id="08b37-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="08b37-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08b37-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="08b37-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08b37-135">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="08b37-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08b37-136">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="08b37-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

