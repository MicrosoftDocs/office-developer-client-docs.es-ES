---
title: Propiedad canónica PidTagAttachPayloadProviderGuidString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadProviderGuidString
api_type:
- HeaderDef
ms.assetid: c9d4b561-53b3-492b-9324-9376dd7abddf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5051784ea08316477f3c8888ada9170e3d99c2b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361106"
---
# <a name="pidtagattachpayloadproviderguidstring-canonical-property"></a><span data-ttu-id="70ce2-103">Propiedad canónica PidTagAttachPayloadProviderGuidString</span><span class="sxs-lookup"><span data-stu-id="70ce2-103">PidTagAttachPayloadProviderGuidString Canonical Property</span></span>

  
  
<span data-ttu-id="70ce2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70ce2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70ce2-105">Contiene el valor de un campo de encabezado MIME X-Payload-Provider-Guid.</span><span class="sxs-lookup"><span data-stu-id="70ce2-105">Contains the value of a MIME X-Payload-Provider-Guid header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70ce2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="70ce2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70ce2-107">PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W</span><span class="sxs-lookup"><span data-stu-id="70ce2-107">PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W</span></span>  <br/> |
|<span data-ttu-id="70ce2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="70ce2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="70ce2-109">0x3719</span><span class="sxs-lookup"><span data-stu-id="70ce2-109">0x3719</span></span>  <br/> |
|<span data-ttu-id="70ce2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="70ce2-110">Data type:</span></span>  <br/> |<span data-ttu-id="70ce2-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="70ce2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="70ce2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="70ce2-112">Area:</span></span>  <br/> |<span data-ttu-id="70ce2-113">Aplicación de Outlook</span><span class="sxs-lookup"><span data-stu-id="70ce2-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70ce2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="70ce2-114">Remarks</span></span>

<span data-ttu-id="70ce2-115">Para establecer el valor de estas propiedades, los clientes MIME deben escribir un campo de encabezado X-Payload-Provider-Guid en una entidad MIME que se analizará como datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="70ce2-115">To set the value of these properties, MIME clients should write an X-Payload-Provider-Guid header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="70ce2-116">Los lectores MIME deben copiar este valor de campo de encabezado en el valor de la propiedad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="70ce2-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="70ce2-117">Los lectores MIME deben omitir este campo de encabezado cuando aparece en una entidad MIME que se analiza como un mensaje o cuerpo del mensaje, en lugar de como datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="70ce2-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="70ce2-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="70ce2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="70ce2-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="70ce2-119">Protocol specifications</span></span>

<span data-ttu-id="70ce2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70ce2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70ce2-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="70ce2-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="70ce2-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70ce2-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70ce2-123">Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="70ce2-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="70ce2-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="70ce2-124">Header files</span></span>

<span data-ttu-id="70ce2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70ce2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="70ce2-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="70ce2-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="70ce2-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="70ce2-127">Mapitags.h</span></span>
  
> <span data-ttu-id="70ce2-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="70ce2-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70ce2-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="70ce2-129">See also</span></span>



[<span data-ttu-id="70ce2-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="70ce2-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70ce2-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="70ce2-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70ce2-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="70ce2-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70ce2-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="70ce2-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

