---
title: Propiedad canónica PidTagStatusString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9b4510a32fe14e4316a6bcddafcc163ee899436e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421567"
---
# <a name="pidtagstatusstring-canonical-property"></a><span data-ttu-id="4c8e0-103">Propiedad canónica PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="4c8e0-103">PidTagStatusString Canonical Property</span></span>

  
  
<span data-ttu-id="4c8e0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c8e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c8e0-105">Contiene un mensaje que indica el estado actual de un recurso de sesión.</span><span class="sxs-lookup"><span data-stu-id="4c8e0-105">Contains a message that indicates the current status of a session resource.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c8e0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4c8e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c8e0-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span><span class="sxs-lookup"><span data-stu-id="4c8e0-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span></span>  <br/> |
|<span data-ttu-id="4c8e0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4c8e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4c8e0-109">0x3E08</span><span class="sxs-lookup"><span data-stu-id="4c8e0-109">0x3E08</span></span>  <br/> |
|<span data-ttu-id="4c8e0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4c8e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="4c8e0-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4c8e0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4c8e0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4c8e0-112">Area:</span></span>  <br/> |<span data-ttu-id="4c8e0-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="4c8e0-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c8e0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c8e0-114">Remarks</span></span>

<span data-ttu-id="4c8e0-115">Estas propiedades ofrecen a los proveedores de servicios y MAPI la oportunidad de proporcionar información específica sobre el estado de un recurso de sesión, como la libreta de direcciones integrada o un proveedor de servicios en particular.</span><span class="sxs-lookup"><span data-stu-id="4c8e0-115">These properties give service providers and MAPI the opportunity to supply specific information about the status of a session resource, such as the integrated address book or a particular service provider.</span></span> <span data-ttu-id="4c8e0-116">Esta propiedad explica y proporciona información adicional sobre un código de estado o la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4c8e0-116">This property explains and provides additional information about a status code, or the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property.</span></span> <span data-ttu-id="4c8e0-117">Mientras que **PR_STATUS_CODE** es necesario para todos los objetos de **estado,** PR_STATUS_STRING y las propiedades asociadas son opcionales.</span><span class="sxs-lookup"><span data-stu-id="4c8e0-117">Whereas **PR_STATUS_CODE** is required for all status objects, **PR_STATUS_STRING** and associated properties are optional.</span></span> <span data-ttu-id="4c8e0-118">Cuando el proveedor de transporte no proporciona un valor, la cola MAPI proporciona un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4c8e0-118">When the transport provider does not supply a value, the MAPI spooler supplies a default value.</span></span> 
  
<span data-ttu-id="4c8e0-119">La cadena se genera en el mismo lado de la llamada de procedimiento remoto que la cola MAPI; viaja a través de la memoria compartida en lugar de ser serializada a través de un límite de proceso.</span><span class="sxs-lookup"><span data-stu-id="4c8e0-119">The string is generated on the same side of the remote procedure call as the MAPI spooler; it travels through shared memory rather than being marshaled across a process boundary.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4c8e0-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c8e0-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4c8e0-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4c8e0-121">Header files</span></span>

<span data-ttu-id="4c8e0-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c8e0-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c8e0-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4c8e0-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="4c8e0-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4c8e0-124">Mapitags.h</span></span>
  
> <span data-ttu-id="4c8e0-125">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4c8e0-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c8e0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c8e0-126">See also</span></span>



[<span data-ttu-id="4c8e0-127">Propiedad canónica PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="4c8e0-127">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)


[<span data-ttu-id="4c8e0-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4c8e0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c8e0-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="4c8e0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c8e0-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4c8e0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c8e0-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4c8e0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

