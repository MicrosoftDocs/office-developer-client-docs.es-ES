---
title: Propiedad canónico PidTagServiceExtraUids
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 71f802014200d4b767c346c14df53f1193d44b0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820291"
---
# <a name="pidtagserviceextrauids-canonical-property"></a><span data-ttu-id="a1f9e-103">Propiedad canónico PidTagServiceExtraUids</span><span class="sxs-lookup"><span data-stu-id="a1f9e-103">PidTagServiceExtraUids Canonical Property</span></span>

  
  
<span data-ttu-id="a1f9e-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a1f9e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a1f9e-105">Contiene una lista de las estructuras [MAPIUID](mapiuid.md) que identifican las secciones de perfil adicional para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a1f9e-105">Contains a list of [MAPIUID](mapiuid.md) structures that identify additional profile sections for the message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1f9e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a1f9e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1f9e-107">PR_SERVICE_EXTRA_UIDS</span><span class="sxs-lookup"><span data-stu-id="a1f9e-107">PR_SERVICE_EXTRA_UIDS</span></span>  <br/> |
|<span data-ttu-id="a1f9e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a1f9e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a1f9e-109">0x3D0D</span><span class="sxs-lookup"><span data-stu-id="a1f9e-109">0x3D0D</span></span>  <br/> |
|<span data-ttu-id="a1f9e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a1f9e-110">Data type:</span></span>  <br/> |<span data-ttu-id="a1f9e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a1f9e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a1f9e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a1f9e-112">Area:</span></span>  <br/> |<span data-ttu-id="a1f9e-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="a1f9e-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1f9e-114">Notas</span><span class="sxs-lookup"><span data-stu-id="a1f9e-114">Remarks</span></span>

<span data-ttu-id="a1f9e-115">Para cada filtro de mensaje, se pueden crear nuevas secciones de perfil.</span><span class="sxs-lookup"><span data-stu-id="a1f9e-115">New profile sections can be created for each message filter.</span></span> <span data-ttu-id="a1f9e-116">Cuando la información sobre el servicio de mensajes se va a copiar a otro perfil, es importante copiar las secciones de perfil adicional para así como los filtros.</span><span class="sxs-lookup"><span data-stu-id="a1f9e-116">When the information about the message service is to be copied to another profile, it is important to copy the additional profile sections for the filters as well.</span></span> <span data-ttu-id="a1f9e-117">Un proveedor de servicio que usa las secciones de perfil adicional puede almacenar las estructuras **MAPIUID** de esas secciones de perfil en **PR_SERVICE_EXTRA_UIDS**, que permite la MAPI copiar la información de servicio de mensajes adicionales.</span><span class="sxs-lookup"><span data-stu-id="a1f9e-117">A service provider that uses additional profile sections can store the **MAPIUID** structures of those profile sections in **PR_SERVICE_EXTRA_UIDS**, which allows MAPI to copy the additional message service information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a1f9e-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1f9e-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a1f9e-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a1f9e-119">Header files</span></span>

<span data-ttu-id="a1f9e-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1f9e-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1f9e-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a1f9e-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="a1f9e-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a1f9e-122">Mapitags.h</span></span>
  
> <span data-ttu-id="a1f9e-123">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a1f9e-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1f9e-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="a1f9e-124">See also</span></span>



[<span data-ttu-id="a1f9e-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a1f9e-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1f9e-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a1f9e-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1f9e-127">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="a1f9e-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1f9e-128">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a1f9e-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

