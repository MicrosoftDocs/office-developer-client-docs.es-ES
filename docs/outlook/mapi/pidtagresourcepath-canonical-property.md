---
title: Propiedad canónico PidTagResourcePath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: d7385ea403e7ea45c97f6fd98e422ad7eb762c4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820112"
---
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="2b0e5-103">Propiedad canónico PidTagResourcePath</span><span class="sxs-lookup"><span data-stu-id="2b0e5-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="2b0e5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2b0e5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2b0e5-105">Contiene una ruta de acceso al servidor del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="2b0e5-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2b0e5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2b0e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b0e5-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span><span class="sxs-lookup"><span data-stu-id="2b0e5-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="2b0e5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2b0e5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2b0e5-109">0x3E07</span><span class="sxs-lookup"><span data-stu-id="2b0e5-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="2b0e5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2b0e5-110">Data type:</span></span>  <br/> |<span data-ttu-id="2b0e5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2b0e5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2b0e5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2b0e5-112">Area:</span></span>  <br/> |<span data-ttu-id="2b0e5-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="2b0e5-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b0e5-114">Notas</span><span class="sxs-lookup"><span data-stu-id="2b0e5-114">Remarks</span></span>

<span data-ttu-id="2b0e5-115">La ruta de acceso contenida en estas propiedades representa la ruta de acceso sugerida donde el usuario puede encontrar recursos.</span><span class="sxs-lookup"><span data-stu-id="2b0e5-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="2b0e5-116">La definición de estas propiedades es específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="2b0e5-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="2b0e5-117">Por ejemplo, una aplicación de programación usa estas propiedades para especificar la ubicación sugerida para sus archivos de aplicación de programación.</span><span class="sxs-lookup"><span data-stu-id="2b0e5-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="2b0e5-118">El perfil de usuario de mensajería proporciona estas propiedades como una comodidad para que una aplicación cliente no tiene que solicitar al usuario de mensajería de una ruta de acceso de red o la letra de la unidad de red.</span><span class="sxs-lookup"><span data-stu-id="2b0e5-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="2b0e5-119">MAPI sólo funciona con los nombres de archivo en el juego de caracteres estadounidense National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2b0e5-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="2b0e5-120">Las aplicaciones que usan nombres de archivo en un juego de caracteres del fabricante de equipos originales (OEM) deben convertirlos a ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="2b0e5-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2b0e5-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b0e5-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2b0e5-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2b0e5-122">Header files</span></span>

<span data-ttu-id="2b0e5-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b0e5-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b0e5-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2b0e5-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="2b0e5-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2b0e5-125">Mapitags.h</span></span>
  
> <span data-ttu-id="2b0e5-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2b0e5-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b0e5-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="2b0e5-127">See also</span></span>



[<span data-ttu-id="2b0e5-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2b0e5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b0e5-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2b0e5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b0e5-130">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="2b0e5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b0e5-131">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2b0e5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

