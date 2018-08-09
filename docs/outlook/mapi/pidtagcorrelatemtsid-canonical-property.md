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
ms.openlocfilehash: 57da2d4c78914323b5dafa4f5ba5b7628d0e2f2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819407"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="48106-103">Propiedad canónica PidTagCorrelateMtsid</span><span class="sxs-lookup"><span data-stu-id="48106-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="48106-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48106-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48106-105">Contiene el identificador del sistema (MTS) de transferencia de mensaje usado en la correlación de informes con los mensajes enviados.</span><span class="sxs-lookup"><span data-stu-id="48106-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48106-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="48106-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48106-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="48106-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="48106-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="48106-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48106-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="48106-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="48106-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="48106-110">Data type:</span></span>  <br/> |<span data-ttu-id="48106-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="48106-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="48106-112">Área:</span><span class="sxs-lookup"><span data-stu-id="48106-112">Area:</span></span>  <br/> |<span data-ttu-id="48106-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="48106-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48106-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48106-114">Remarks</span></span>

<span data-ttu-id="48106-115">Cuando un proveedor de transporte encuentra un mensaje enviado con esta propiedad establecida en TRUE, se establece esta propiedad para el identificador MTS para ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="48106-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="48106-116">Después de transmisión, esta propiedad se almacena con el mensaje en la carpeta Elementos enviados de mensajes interpersonales (IPM).</span><span class="sxs-lookup"><span data-stu-id="48106-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="48106-117">Los sistemas de mensajería que admiten la correlación por identificador de MTS, como X.400, conservan el identificador como parte de los sobres de transporte del mensaje original y también de los informes generados en respuesta a ella.</span><span class="sxs-lookup"><span data-stu-id="48106-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="48106-118">Cuando un informe se entrega desde como un sistema de mensajería, el proveedor de transporte establece esta propiedad en el identificador MTS original desde sobre de transporte del informe.</span><span class="sxs-lookup"><span data-stu-id="48106-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="48106-119">Esta propiedad se almacena con el informe.</span><span class="sxs-lookup"><span data-stu-id="48106-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="48106-120">Una aplicación cliente puede mantener una carpeta de resultados de búsqueda de todos los mensajes de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="48106-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="48106-121">Cuando se recibe un informe para este tipo de mensaje, el cliente puede aplicar restricciones a la carpeta de resultados de búsqueda, buscar la versión original del mensaje y correlacionar la información del mensaje original con la nueva información.</span><span class="sxs-lookup"><span data-stu-id="48106-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="48106-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="48106-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="48106-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="48106-123">Header files</span></span>

<span data-ttu-id="48106-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48106-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="48106-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="48106-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="48106-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48106-126">Mapitags.h</span></span>
  
> <span data-ttu-id="48106-127">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="48106-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48106-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="48106-128">See also</span></span>



[<span data-ttu-id="48106-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="48106-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48106-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="48106-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48106-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="48106-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48106-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="48106-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

