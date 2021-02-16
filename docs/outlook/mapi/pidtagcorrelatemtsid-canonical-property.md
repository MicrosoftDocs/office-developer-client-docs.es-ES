---
title: Propiedad canónica PidTagCorrelateMtsid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 96bfc184752b6a3e15434ad67ac8c2b4b26cac4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426838"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="cc02e-103">Propiedad canónica PidTagCorrelateMtsid</span><span class="sxs-lookup"><span data-stu-id="cc02e-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="cc02e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc02e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc02e-105">Contiene el identificador del sistema de transferencia de mensajes (MTS) usado en los informes correlacionados con los mensajes enviados.</span><span class="sxs-lookup"><span data-stu-id="cc02e-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc02e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cc02e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc02e-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="cc02e-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="cc02e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cc02e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc02e-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="cc02e-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="cc02e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cc02e-110">Data type:</span></span>  <br/> |<span data-ttu-id="cc02e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cc02e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cc02e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cc02e-112">Area:</span></span>  <br/> |<span data-ttu-id="cc02e-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="cc02e-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc02e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc02e-114">Remarks</span></span>

<span data-ttu-id="cc02e-115">Cuando un proveedor de transporte encuentra un mensaje enviado con esta propiedad establecida en TRUE, establece esta propiedad en el identificador MTS de ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="cc02e-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="cc02e-116">Después de la transmisión, esta propiedad se almacena con el mensaje en la carpeta elementos enviados del mensaje interpersonal (IPM).</span><span class="sxs-lookup"><span data-stu-id="cc02e-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="cc02e-117">Los sistemas de mensajería que admiten la correlación por el identificador MTS, como X.400, conservan el identificador como parte del sobre de transporte del mensaje original y también de los informes generados en respuesta a él.</span><span class="sxs-lookup"><span data-stu-id="cc02e-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="cc02e-118">Cuando un informe se entrega desde dicho sistema de mensajería, el proveedor de transporte establece esta propiedad en el identificador MTS original del sobre de transporte del informe.</span><span class="sxs-lookup"><span data-stu-id="cc02e-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="cc02e-119">A continuación, esta propiedad se almacena con el informe.</span><span class="sxs-lookup"><span data-stu-id="cc02e-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="cc02e-120">Una aplicación cliente puede mantener una carpeta de resultados de búsqueda de todos los mensajes que tienen esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="cc02e-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="cc02e-121">Cuando llega un informe para este mensaje, el cliente puede aplicar restricciones a la carpeta de resultados de búsqueda, buscar la versión original del mensaje y correlacionar la información original del mensaje con la nueva información.</span><span class="sxs-lookup"><span data-stu-id="cc02e-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cc02e-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc02e-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cc02e-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cc02e-123">Header files</span></span>

<span data-ttu-id="cc02e-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc02e-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc02e-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cc02e-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc02e-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cc02e-126">Mapitags.h</span></span>
  
> <span data-ttu-id="cc02e-127">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="cc02e-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc02e-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cc02e-128">See also</span></span>



[<span data-ttu-id="cc02e-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cc02e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc02e-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="cc02e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc02e-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cc02e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc02e-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="cc02e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

