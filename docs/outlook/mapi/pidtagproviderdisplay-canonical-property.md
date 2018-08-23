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
ms.openlocfilehash: 9a37382cda1a96025f950d941f83fb5b6a0497bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565504"
---
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="4d0e1-103">Propiedad canónica PidTagProviderDisplay</span><span class="sxs-lookup"><span data-stu-id="4d0e1-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="4d0e1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d0e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d0e1-105">Contiene el nombre para mostrar definido por el proveedor para un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="4d0e1-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d0e1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4d0e1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d0e1-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="4d0e1-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="4d0e1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4d0e1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4d0e1-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="4d0e1-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="4d0e1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4d0e1-110">Data type:</span></span>  <br/> |<span data-ttu-id="4d0e1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4d0e1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4d0e1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4d0e1-112">Area:</span></span>  <br/> |<span data-ttu-id="4d0e1-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="4d0e1-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d0e1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d0e1-114">Remarks</span></span>

<span data-ttu-id="4d0e1-115">Estas propiedades y **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) sólo se definen en las secciones de perfil que pertenecen a los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="4d0e1-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="4d0e1-116">Deben estar presentes en MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="4d0e1-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4d0e1-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d0e1-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4d0e1-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4d0e1-118">Header files</span></span>

<span data-ttu-id="4d0e1-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d0e1-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d0e1-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4d0e1-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4d0e1-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4d0e1-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4d0e1-122">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4d0e1-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d0e1-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="4d0e1-123">See also</span></span>



[<span data-ttu-id="4d0e1-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4d0e1-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d0e1-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4d0e1-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d0e1-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4d0e1-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d0e1-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="4d0e1-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

