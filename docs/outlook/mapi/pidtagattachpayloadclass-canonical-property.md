---
title: Propiedad canónica PidTagAttachPayloadClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadClass
api_type:
- HeaderDef
ms.assetid: bc4de217-8241-45e7-9e97-8f0c1b16691a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cef412d212bf29cfd1a1d5c4b2911440fae6a15e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819251"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a><span data-ttu-id="471b9-103">Propiedad canónica PidTagAttachPayloadClass</span><span class="sxs-lookup"><span data-stu-id="471b9-103">PidTagAttachPayloadClass Canonical Property</span></span>

  
  
<span data-ttu-id="471b9-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="471b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="471b9-105">Contiene el valor de un campo de encabezado MIME X-carga-Class.</span><span class="sxs-lookup"><span data-stu-id="471b9-105">Contains the value of a MIME X-Payload-Class header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="471b9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="471b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="471b9-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="471b9-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="471b9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="471b9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="471b9-109">0x371A</span><span class="sxs-lookup"><span data-stu-id="471b9-109">0x371A</span></span>  <br/> |
|<span data-ttu-id="471b9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="471b9-110">Data type:</span></span>  <br/> |<span data-ttu-id="471b9-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="471b9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="471b9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="471b9-112">Area:</span></span>  <br/> |<span data-ttu-id="471b9-113">Aplicación de Outlook</span><span class="sxs-lookup"><span data-stu-id="471b9-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="471b9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="471b9-114">Remarks</span></span>

<span data-ttu-id="471b9-115">Para establecer el valor de estas propiedades, los clientes MIME deben escribir un campo de encabezado X-carga-clase a una entidad MIME que se va a analizar como datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="471b9-115">To set the value of these properties, MIME clients should write an X-Payload-Class header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="471b9-116">Lectores MIME deben copiar este valor de campo de encabezado para el valor de la propiedad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="471b9-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="471b9-117">Lectores MIME deben omitir este campo de encabezado cuando aparece en una entidad MIME que se analiza como un mensaje o el cuerpo del mensaje, en lugar de como datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="471b9-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="471b9-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="471b9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="471b9-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="471b9-119">Protocol specifications</span></span>

<span data-ttu-id="471b9-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="471b9-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="471b9-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="471b9-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="471b9-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="471b9-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="471b9-123">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="471b9-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="471b9-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="471b9-124">Header files</span></span>

<span data-ttu-id="471b9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="471b9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="471b9-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="471b9-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="471b9-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="471b9-127">Mapitags.h</span></span>
  
> <span data-ttu-id="471b9-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="471b9-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="471b9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="471b9-129">See also</span></span>



[<span data-ttu-id="471b9-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="471b9-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="471b9-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="471b9-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="471b9-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="471b9-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="471b9-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="471b9-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

