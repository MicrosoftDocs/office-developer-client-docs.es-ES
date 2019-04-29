---
title: Propiedad canónica PidTagServiceExtraUids
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0fb688e2a845186224c1802f9df2ac537d5bb4d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422309"
---
# <a name="pidtagserviceextrauids-canonical-property"></a><span data-ttu-id="57591-103">Propiedad canónica PidTagServiceExtraUids</span><span class="sxs-lookup"><span data-stu-id="57591-103">PidTagServiceExtraUids Canonical Property</span></span>

  
  
<span data-ttu-id="57591-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57591-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57591-105">Contiene una lista de las estructuras de [MAPIUID](mapiuid.md) que identifican secciones de perfil adicionales para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="57591-105">Contains a list of [MAPIUID](mapiuid.md) structures that identify additional profile sections for the message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57591-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="57591-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="57591-107">PR_SERVICE_EXTRA_UIDS</span><span class="sxs-lookup"><span data-stu-id="57591-107">PR_SERVICE_EXTRA_UIDS</span></span>  <br/> |
|<span data-ttu-id="57591-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="57591-108">Identifier:</span></span>  <br/> |<span data-ttu-id="57591-109">0x3D0D</span><span class="sxs-lookup"><span data-stu-id="57591-109">0x3D0D</span></span>  <br/> |
|<span data-ttu-id="57591-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="57591-110">Data type:</span></span>  <br/> |<span data-ttu-id="57591-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="57591-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="57591-112">Área:</span><span class="sxs-lookup"><span data-stu-id="57591-112">Area:</span></span>  <br/> |<span data-ttu-id="57591-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="57591-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57591-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57591-114">Remarks</span></span>

<span data-ttu-id="57591-115">Se pueden crear nuevas secciones de perfil para cada filtro de mensajes.</span><span class="sxs-lookup"><span data-stu-id="57591-115">New profile sections can be created for each message filter.</span></span> <span data-ttu-id="57591-116">Cuando la información sobre el servicio de mensajes se va a copiar a otro perfil, es importante copiar también las secciones de perfil adicionales para los filtros.</span><span class="sxs-lookup"><span data-stu-id="57591-116">When the information about the message service is to be copied to another profile, it is important to copy the additional profile sections for the filters as well.</span></span> <span data-ttu-id="57591-117">Un proveedor de servicios que usa secciones de perfil adicionales puede almacenar las estructuras **MAPIUID** de esas secciones de perfil en **PR_SERVICE_EXTRA_UIDS**, lo que permite a MAPI copiar la información adicional del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="57591-117">A service provider that uses additional profile sections can store the **MAPIUID** structures of those profile sections in **PR_SERVICE_EXTRA_UIDS**, which allows MAPI to copy the additional message service information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="57591-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="57591-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="57591-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="57591-119">Header files</span></span>

<span data-ttu-id="57591-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="57591-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="57591-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="57591-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="57591-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="57591-122">Mapitags.h</span></span>
  
> <span data-ttu-id="57591-123">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="57591-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="57591-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="57591-124">See also</span></span>



[<span data-ttu-id="57591-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="57591-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="57591-126">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="57591-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="57591-127">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="57591-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="57591-128">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="57591-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

