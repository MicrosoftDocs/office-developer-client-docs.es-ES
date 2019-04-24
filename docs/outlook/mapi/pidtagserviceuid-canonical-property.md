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
ms.openlocfilehash: d5c6e1dc30c3ee7862341bce204b4a78bd6d379b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359447"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="be462-103">Propiedad canónica PidTagServiceUid</span><span class="sxs-lookup"><span data-stu-id="be462-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="be462-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be462-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be462-105">Contiene la estructura [MAPIUID](mapiuid.md) de un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="be462-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be462-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="be462-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be462-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="be462-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="be462-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="be462-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be462-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="be462-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="be462-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="be462-110">Data type:</span></span>  <br/> |<span data-ttu-id="be462-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="be462-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="be462-112">Área:</span><span class="sxs-lookup"><span data-stu-id="be462-112">Area:</span></span>  <br/> |<span data-ttu-id="be462-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="be462-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be462-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be462-114">Remarks</span></span>

<span data-ttu-id="be462-115">MAPI calcula esta propiedad en los objetos de sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="be462-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="be462-116">MAPI la usa para agrupar todos los proveedores que pertenecen al mismo servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="be462-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="be462-117">Esta propiedad se proporciona como un parámetro a la mayoría de los métodos [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="be462-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="be462-118">No debe aparecer en MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="be462-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="be462-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="be462-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="be462-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="be462-120">Header files</span></span>

<span data-ttu-id="be462-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="be462-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="be462-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="be462-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="be462-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="be462-123">Mapitags.h</span></span>
  
> <span data-ttu-id="be462-124">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="be462-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be462-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="be462-125">See also</span></span>



[<span data-ttu-id="be462-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be462-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="be462-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="be462-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be462-128">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="be462-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be462-129">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="be462-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be462-130">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="be462-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

