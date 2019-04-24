---
title: Propiedad canónica PidTagProviderDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDisplay
api_type:
- COM
ms.assetid: 62e96db8-4c3e-4f73-b695-99eb4b2396fd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 58db944720817491420f2bcb1774e51e3842b4a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286470"
---
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="9f088-103">Propiedad canónica PidTagProviderDisplay</span><span class="sxs-lookup"><span data-stu-id="9f088-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="9f088-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f088-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f088-105">Contiene el nombre para mostrar definido por el proveedor para un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="9f088-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f088-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9f088-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f088-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="9f088-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="9f088-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9f088-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9f088-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="9f088-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="9f088-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9f088-110">Data type:</span></span>  <br/> |<span data-ttu-id="9f088-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9f088-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9f088-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9f088-112">Area:</span></span>  <br/> |<span data-ttu-id="9f088-113">Common MAPI</span><span class="sxs-lookup"><span data-stu-id="9f088-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f088-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f088-114">Remarks</span></span>

<span data-ttu-id="9f088-115">Estas propiedades y **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) se definen solo en secciones de perfil pertenecientes a proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="9f088-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="9f088-116">Deben estar presentes en MAPISVC. INF.</span><span class="sxs-lookup"><span data-stu-id="9f088-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9f088-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f088-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9f088-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9f088-118">Header files</span></span>

<span data-ttu-id="9f088-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9f088-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f088-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9f088-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="9f088-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9f088-121">Mapitags.h</span></span>
  
> <span data-ttu-id="9f088-122">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9f088-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f088-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f088-123">See also</span></span>



[<span data-ttu-id="9f088-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9f088-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f088-125">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="9f088-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f088-126">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9f088-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f088-127">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9f088-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

