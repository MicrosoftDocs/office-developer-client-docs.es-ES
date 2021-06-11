---
title: Propiedad canónica PidTagClientSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 851441e419c17d8f5fef27c785ea4b829a4ae443
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345720"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="dd8b0-103">Propiedad canónica PidTagClientSubmitTime</span><span class="sxs-lookup"><span data-stu-id="dd8b0-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="dd8b0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd8b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd8b0-105">Contiene la fecha y hora en que el remitente del mensaje envió un mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd8b0-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd8b0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="dd8b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dd8b0-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="dd8b0-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="dd8b0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dd8b0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dd8b0-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="dd8b0-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="dd8b0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="dd8b0-110">Data type:</span></span>  <br/> |<span data-ttu-id="dd8b0-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="dd8b0-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="dd8b0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dd8b0-112">Area:</span></span>  <br/> |<span data-ttu-id="dd8b0-113">Hora del mensaje</span><span class="sxs-lookup"><span data-stu-id="dd8b0-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd8b0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd8b0-114">Remarks</span></span>

<span data-ttu-id="dd8b0-115">El proveedor de **almacenamiento establece PR_CLIENT_SUBMIT_TIME** la hora en que la aplicación cliente llamó a [IMessage::SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="dd8b0-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dd8b0-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd8b0-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dd8b0-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="dd8b0-117">Protocol specifications</span></span>

<span data-ttu-id="dd8b0-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd8b0-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd8b0-119">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="dd8b0-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dd8b0-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="dd8b0-120">Header files</span></span>

<span data-ttu-id="dd8b0-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dd8b0-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="dd8b0-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="dd8b0-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="dd8b0-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dd8b0-123">Mapitags.h</span></span>
  
> <span data-ttu-id="dd8b0-124">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="dd8b0-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dd8b0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd8b0-125">See also</span></span>



[<span data-ttu-id="dd8b0-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dd8b0-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dd8b0-127">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="dd8b0-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dd8b0-128">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="dd8b0-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dd8b0-129">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="dd8b0-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

