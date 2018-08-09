---
title: Propiedad canónica PidTagProfileName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6ecd84e4ffa0959a037574998b5ff12d8f539c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819951"
---
# <a name="pidtagprofilename-canonical-property"></a><span data-ttu-id="35ad1-103">Propiedad canónica PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="35ad1-103">PidTagProfileName Canonical Property</span></span>

  
  
<span data-ttu-id="35ad1-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35ad1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35ad1-105">Contiene el nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="35ad1-105">Contains the name of the profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35ad1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="35ad1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35ad1-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="35ad1-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="35ad1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="35ad1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35ad1-109">0x3D12</span><span class="sxs-lookup"><span data-stu-id="35ad1-109">0x3D12</span></span>  <br/> |
|<span data-ttu-id="35ad1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="35ad1-110">Data type:</span></span>  <br/> |<span data-ttu-id="35ad1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="35ad1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="35ad1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="35ad1-112">Area:</span></span>  <br/> |<span data-ttu-id="35ad1-113">Configuración de perfiles de MAPI</span><span class="sxs-lookup"><span data-stu-id="35ad1-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35ad1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="35ad1-114">Remarks</span></span>

<span data-ttu-id="35ad1-115">Estas propiedades se calculan por los proveedores de servicio.</span><span class="sxs-lookup"><span data-stu-id="35ad1-115">These properties are computed by service providers.</span></span> <span data-ttu-id="35ad1-116">Implementación de un proveedor de la función de **entrada de servicio** puede usar estas propiedades para descubrir el nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="35ad1-116">A provider's implementation of the **ServiceEntry** function can use these properties to discover the profile name.</span></span> 
  
<span data-ttu-id="35ad1-117">Aplicaciones cliente pueden utilizar estas propiedades como una alternativa cómoda a obtener el nombre del perfil mediante el examen de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en la fila de tabla de estado del subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="35ad1-117">Client applications can use these properties as a convenient alternative to obtaining the profile name by examining the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MAPI subsystem's status table row.</span></span>
  
<span data-ttu-id="35ad1-118">Estas propiedades no pueden ser únicas a través del tiempo, por ejemplo donde se elimina y más adelante vuelve a crear con el mismo nombre de un perfil.</span><span class="sxs-lookup"><span data-stu-id="35ad1-118">These properties may not be unique across time, for example where a profile is deleted and later recreated with the same name.</span></span> <span data-ttu-id="35ad1-119">MAPI proporciona una propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) totalmente única en una sección de perfil codificado de forma rígida denominada **MUID_PROFILE_INSTANCE.**</span><span class="sxs-lookup"><span data-stu-id="35ad1-119">MAPI furnishes a totally unique **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property in a hard-coded profile section called **MUID_PROFILE_INSTANCE.**</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="35ad1-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="35ad1-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="35ad1-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="35ad1-121">Header files</span></span>

<span data-ttu-id="35ad1-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35ad1-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="35ad1-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="35ad1-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="35ad1-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="35ad1-124">Mapitags.h</span></span>
  
> <span data-ttu-id="35ad1-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="35ad1-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35ad1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="35ad1-126">See also</span></span>



[<span data-ttu-id="35ad1-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="35ad1-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35ad1-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="35ad1-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35ad1-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="35ad1-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35ad1-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="35ad1-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

