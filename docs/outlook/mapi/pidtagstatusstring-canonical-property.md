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
ms.openlocfilehash: ea24b5e721317668c8f43278a5e4c38d73b3e91c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820331"
---
# <a name="pidtagstatusstring-canonical-property"></a><span data-ttu-id="b25ef-103">Propiedad canónica PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="b25ef-103">PidTagStatusString Canonical Property</span></span>

  
  
<span data-ttu-id="b25ef-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b25ef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b25ef-105">Contiene un mensaje que indica el estado actual de un recurso de la sesión.</span><span class="sxs-lookup"><span data-stu-id="b25ef-105">Contains a message that indicates the current status of a session resource.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b25ef-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b25ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b25ef-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span><span class="sxs-lookup"><span data-stu-id="b25ef-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span></span>  <br/> |
|<span data-ttu-id="b25ef-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b25ef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b25ef-109">0x3E08</span><span class="sxs-lookup"><span data-stu-id="b25ef-109">0x3E08</span></span>  <br/> |
|<span data-ttu-id="b25ef-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b25ef-110">Data type:</span></span>  <br/> |<span data-ttu-id="b25ef-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b25ef-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b25ef-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b25ef-112">Area:</span></span>  <br/> |<span data-ttu-id="b25ef-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="b25ef-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b25ef-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b25ef-114">Remarks</span></span>

<span data-ttu-id="b25ef-115">Estas propiedades proporcionan proveedores de servicios y la oportunidad de proporcionar información específica sobre el estado de un recurso de sesión, como la libreta de direcciones integrada o un proveedor de servicio en particular de MAPI.</span><span class="sxs-lookup"><span data-stu-id="b25ef-115">These properties give service providers and MAPI the opportunity to supply specific information about the status of a session resource, such as the integrated address book or a particular service provider.</span></span> <span data-ttu-id="b25ef-116">Esta propiedad se explica y proporciona información adicional acerca de un código de estado o la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b25ef-116">This property explains and provides additional information about a status code, or the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property.</span></span> <span data-ttu-id="b25ef-117">Considerando que es necesario para todos los objetos de estado **PR_STATUS_CODE** , **PR_STATUS_STRING** y las propiedades asociadas son opcionales.</span><span class="sxs-lookup"><span data-stu-id="b25ef-117">Whereas **PR_STATUS_CODE** is required for all status objects, **PR_STATUS_STRING** and associated properties are optional.</span></span> <span data-ttu-id="b25ef-118">Cuando el proveedor de transporte no proporciona un valor, la cola MAPI proporciona un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b25ef-118">When the transport provider does not supply a value, the MAPI spooler supplies a default value.</span></span> 
  
<span data-ttu-id="b25ef-119">La cadena se genera en el mismo lado de la llamada a procedimiento remoto como la cola MAPI; viajan a través de la memoria compartida en lugar de que se puede ordenar a través de un límite de proceso.</span><span class="sxs-lookup"><span data-stu-id="b25ef-119">The string is generated on the same side of the remote procedure call as the MAPI spooler; it travels through shared memory rather than being marshaled across a process boundary.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b25ef-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b25ef-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b25ef-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b25ef-121">Header files</span></span>

<span data-ttu-id="b25ef-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b25ef-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="b25ef-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b25ef-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="b25ef-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b25ef-124">Mapitags.h</span></span>
  
> <span data-ttu-id="b25ef-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b25ef-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b25ef-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b25ef-126">See also</span></span>



[<span data-ttu-id="b25ef-127">Propiedad canónica PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="b25ef-127">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)


[<span data-ttu-id="b25ef-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b25ef-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b25ef-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b25ef-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b25ef-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b25ef-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b25ef-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b25ef-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

