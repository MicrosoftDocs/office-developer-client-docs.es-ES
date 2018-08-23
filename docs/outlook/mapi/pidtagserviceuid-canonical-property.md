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
ms.openlocfilehash: eabcaaf1db6149ef200e640f5af152758261581b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582255"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="f1d9b-103">Propiedad canónica PidTagServiceUid</span><span class="sxs-lookup"><span data-stu-id="f1d9b-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="f1d9b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1d9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1d9b-105">Contiene la estructura [MAPIUID](mapiuid.md) para un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1d9b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f1d9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1d9b-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="f1d9b-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="f1d9b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f1d9b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f1d9b-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="f1d9b-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="f1d9b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f1d9b-110">Data type:</span></span>  <br/> |<span data-ttu-id="f1d9b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f1d9b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f1d9b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f1d9b-112">Area:</span></span>  <br/> |<span data-ttu-id="f1d9b-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="f1d9b-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1d9b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1d9b-114">Remarks</span></span>

<span data-ttu-id="f1d9b-115">Esta propiedad se calcula mediante MAPI en los objetos de sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="f1d9b-116">MAPI utiliza para todos los proveedores que pertenecen al mismo servicio de mensajes de grupo.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="f1d9b-117">Esta propiedad se proporciona como un parámetro a la mayoría de los métodos de [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="f1d9b-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="f1d9b-118">No debe aparecer en Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f1d9b-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1d9b-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f1d9b-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f1d9b-120">Header files</span></span>

<span data-ttu-id="f1d9b-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f1d9b-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1d9b-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="f1d9b-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f1d9b-123">Mapitags.h</span></span>
  
> <span data-ttu-id="f1d9b-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1d9b-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f1d9b-125">See also</span></span>



[<span data-ttu-id="f1d9b-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f1d9b-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="f1d9b-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f1d9b-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1d9b-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f1d9b-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1d9b-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f1d9b-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1d9b-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f1d9b-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

