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
# <a name="pidtagresponserequested-canonical-property"></a><span data-ttu-id="dd216-103">Propiedad canónica PidTagResponseRequested</span><span class="sxs-lookup"><span data-stu-id="dd216-103">PidTagResponseRequested Canonical Property</span></span>

  
  
<span data-ttu-id="dd216-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd216-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd216-105">Contiene TRUE si el remitente del mensaje desea una respuesta a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="dd216-105">Contains TRUE if the message sender wants a response to a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dd216-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="dd216-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dd216-107">PR_RESPONSE_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="dd216-107">PR_RESPONSE_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="dd216-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dd216-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dd216-109">0x0063</span><span class="sxs-lookup"><span data-stu-id="dd216-109">0x0063</span></span>  <br/> |
|<span data-ttu-id="dd216-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="dd216-110">Data type:</span></span>  <br/> |<span data-ttu-id="dd216-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="dd216-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="dd216-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dd216-112">Area:</span></span>  <br/> |<span data-ttu-id="dd216-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="dd216-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd216-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd216-114">Remarks</span></span>

<span data-ttu-id="dd216-115">Esta propiedad se usa para las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="dd216-115">This property is used for meeting requests.</span></span> <span data-ttu-id="dd216-116">La aplicación cliente de recepción debe solicitar al usuario que acepte o rechace la solicitud y, a continuación, vuelva a enviarla al remitente.</span><span class="sxs-lookup"><span data-stu-id="dd216-116">The receiving client application should prompt the user to accept or decline the request and then send this response back to the sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dd216-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd216-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dd216-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="dd216-118">Protocol specifications</span></span>

<span data-ttu-id="dd216-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd216-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd216-120">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="dd216-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dd216-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd216-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd216-122">Especifica las propiedades y operaciones que se admiten en los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="dd216-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="dd216-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd216-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd216-124">Especifica las propiedades y operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="dd216-124">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="dd216-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd216-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd216-126">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd216-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dd216-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="dd216-127">Header files</span></span>

<span data-ttu-id="dd216-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dd216-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="dd216-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="dd216-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="dd216-130">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="dd216-130">Mapitags.h</span></span>
  
> <span data-ttu-id="dd216-131">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="dd216-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dd216-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd216-132">See also</span></span>



[<span data-ttu-id="dd216-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dd216-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dd216-134">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="dd216-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dd216-135">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="dd216-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dd216-136">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="dd216-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

