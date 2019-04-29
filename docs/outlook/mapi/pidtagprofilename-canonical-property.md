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
ms.openlocfilehash: 992b3a6a30e15d267ffeda11ec98c7b4aeacb2c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435652"
---
# <a name="pidtagprofilename-canonical-property"></a><span data-ttu-id="ee6a9-103">Propiedad canónica PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="ee6a9-103">PidTagProfileName Canonical Property</span></span>

  
  
<span data-ttu-id="ee6a9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee6a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee6a9-105">Contiene el nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="ee6a9-105">Contains the name of the profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee6a9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ee6a9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee6a9-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="ee6a9-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="ee6a9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ee6a9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee6a9-109">0x3D12</span><span class="sxs-lookup"><span data-stu-id="ee6a9-109">0x3D12</span></span>  <br/> |
|<span data-ttu-id="ee6a9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ee6a9-110">Data type:</span></span>  <br/> |<span data-ttu-id="ee6a9-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ee6a9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ee6a9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ee6a9-112">Area:</span></span>  <br/> |<span data-ttu-id="ee6a9-113">Configuración del perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="ee6a9-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee6a9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee6a9-114">Remarks</span></span>

<span data-ttu-id="ee6a9-115">Estas propiedades son calculadas por proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="ee6a9-115">These properties are computed by service providers.</span></span> <span data-ttu-id="ee6a9-116">La implementación de un proveedor de la función **ServiceEntry** puede usar estas propiedades para descubrir el nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="ee6a9-116">A provider's implementation of the **ServiceEntry** function can use these properties to discover the profile name.</span></span> 
  
<span data-ttu-id="ee6a9-117">Las aplicaciones cliente pueden usar estas propiedades como una alternativa cómoda para obtener el nombre del perfil mediante el examen de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en la fila de la tabla de estado del subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee6a9-117">Client applications can use these properties as a convenient alternative to obtaining the profile name by examining the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MAPI subsystem's status table row.</span></span>
  
<span data-ttu-id="ee6a9-118">Es posible que estas propiedades no sean únicas a lo largo del tiempo, por ejemplo, cuando se elimina un perfil y posteriormente se vuelve a crear con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="ee6a9-118">These properties may not be unique across time, for example where a profile is deleted and later recreated with the same name.</span></span> <span data-ttu-id="ee6a9-119">MAPI facilita una propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) totalmente única en una sección de perfil codificada de forma rígida denominada **MUID_PROFILE_INSTANCE.**</span><span class="sxs-lookup"><span data-stu-id="ee6a9-119">MAPI furnishes a totally unique **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property in a hard-coded profile section called **MUID_PROFILE_INSTANCE.**</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ee6a9-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee6a9-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ee6a9-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ee6a9-121">Header files</span></span>

<span data-ttu-id="ee6a9-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ee6a9-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee6a9-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ee6a9-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="ee6a9-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ee6a9-124">Mapitags.h</span></span>
  
> <span data-ttu-id="ee6a9-125">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ee6a9-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee6a9-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="ee6a9-126">See also</span></span>



[<span data-ttu-id="ee6a9-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ee6a9-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee6a9-128">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="ee6a9-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee6a9-129">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ee6a9-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee6a9-130">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ee6a9-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

