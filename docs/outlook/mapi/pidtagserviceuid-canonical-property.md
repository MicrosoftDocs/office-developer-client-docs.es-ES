---
title: Propiedad canónica PidTagServiceUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 304efc3f4ea903f9ed0e9fcf95c7100fa6ebfc95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820307"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="94b67-103">Propiedad canónica PidTagServiceUid</span><span class="sxs-lookup"><span data-stu-id="94b67-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="94b67-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="94b67-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="94b67-105">Contiene la estructura [MAPIUID](mapiuid.md) para un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="94b67-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94b67-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="94b67-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94b67-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="94b67-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="94b67-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="94b67-108">Identifier:</span></span>  <br/> |<span data-ttu-id="94b67-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="94b67-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="94b67-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="94b67-110">Data type:</span></span>  <br/> |<span data-ttu-id="94b67-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="94b67-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="94b67-112">Área:</span><span class="sxs-lookup"><span data-stu-id="94b67-112">Area:</span></span>  <br/> |<span data-ttu-id="94b67-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="94b67-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94b67-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94b67-114">Remarks</span></span>

<span data-ttu-id="94b67-115">Esta propiedad se calcula mediante MAPI en los objetos de sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="94b67-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="94b67-116">MAPI utiliza para todos los proveedores que pertenecen al mismo servicio de mensajes de grupo.</span><span class="sxs-lookup"><span data-stu-id="94b67-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="94b67-117">Esta propiedad se proporciona como un parámetro a la mayoría de los métodos de [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="94b67-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="94b67-118">No debe aparecer en Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="94b67-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="94b67-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="94b67-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="94b67-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="94b67-120">Header files</span></span>

<span data-ttu-id="94b67-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94b67-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="94b67-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="94b67-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="94b67-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="94b67-123">Mapitags.h</span></span>
  
> <span data-ttu-id="94b67-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="94b67-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94b67-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="94b67-125">See also</span></span>



[<span data-ttu-id="94b67-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94b67-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="94b67-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="94b67-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94b67-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="94b67-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94b67-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="94b67-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94b67-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="94b67-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

