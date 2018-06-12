---
title: Propiedad canónico PidTagClientSubmitTime
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: ccf4a6054ecc89e280f2f5cbc4c72b2a8a829055
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819295"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="48ed3-103">Propiedad canónico PidTagClientSubmitTime</span><span class="sxs-lookup"><span data-stu-id="48ed3-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="48ed3-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48ed3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48ed3-105">Contiene la fecha y hora que el remitente del mensaje había enviado un mensaje.</span><span class="sxs-lookup"><span data-stu-id="48ed3-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48ed3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="48ed3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48ed3-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="48ed3-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="48ed3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="48ed3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48ed3-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="48ed3-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="48ed3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="48ed3-110">Data type:</span></span>  <br/> |<span data-ttu-id="48ed3-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="48ed3-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="48ed3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="48ed3-112">Area:</span></span>  <br/> |<span data-ttu-id="48ed3-113">Hora del mensaje</span><span class="sxs-lookup"><span data-stu-id="48ed3-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48ed3-114">Notas</span><span class="sxs-lookup"><span data-stu-id="48ed3-114">Remarks</span></span>

<span data-ttu-id="48ed3-115">El proveedor de almacenamiento establece **PR_CLIENT_SUBMIT_TIME** a la vez que la aplicación cliente llama [IMessage::SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="48ed3-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="48ed3-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="48ed3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48ed3-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="48ed3-117">Protocol specifications</span></span>

<span data-ttu-id="48ed3-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48ed3-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48ed3-119">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="48ed3-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48ed3-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="48ed3-120">Header files</span></span>

<span data-ttu-id="48ed3-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48ed3-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="48ed3-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="48ed3-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="48ed3-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48ed3-123">Mapitags.h</span></span>
  
> <span data-ttu-id="48ed3-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="48ed3-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48ed3-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="48ed3-125">See also</span></span>



[<span data-ttu-id="48ed3-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="48ed3-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48ed3-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="48ed3-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48ed3-128">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="48ed3-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48ed3-129">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="48ed3-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

