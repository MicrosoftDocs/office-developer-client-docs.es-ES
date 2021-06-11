---
title: Propiedad canónica PidTagResourcePath
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 32d150e508f5c208e15d5ee5f0b8c800a1e597f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429862"
---
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="1c467-103">Propiedad canónica PidTagResourcePath</span><span class="sxs-lookup"><span data-stu-id="1c467-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="1c467-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c467-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c467-105">Contiene una ruta de acceso al servidor del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="1c467-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1c467-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1c467-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c467-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span><span class="sxs-lookup"><span data-stu-id="1c467-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="1c467-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1c467-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1c467-109">0x3E07</span><span class="sxs-lookup"><span data-stu-id="1c467-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="1c467-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1c467-110">Data type:</span></span>  <br/> |<span data-ttu-id="1c467-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1c467-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1c467-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1c467-112">Area:</span></span>  <br/> |<span data-ttu-id="1c467-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="1c467-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c467-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c467-114">Remarks</span></span>

<span data-ttu-id="1c467-115">La ruta de acceso contenida en estas propiedades representa la ruta de acceso sugerida donde el usuario puede encontrar recursos.</span><span class="sxs-lookup"><span data-stu-id="1c467-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="1c467-116">La definición de estas propiedades es específica del proveedor.</span><span class="sxs-lookup"><span data-stu-id="1c467-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="1c467-117">Por ejemplo, una aplicación de programación usa estas propiedades para especificar la ubicación sugerida para sus archivos de aplicación de programación.</span><span class="sxs-lookup"><span data-stu-id="1c467-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="1c467-118">El perfil de usuario de mensajería proporciona estas propiedades para que una aplicación cliente no tenga que solicitar al usuario de mensajería una ruta de acceso de red o una letra de unidad de red.</span><span class="sxs-lookup"><span data-stu-id="1c467-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="1c467-119">MAPI solo funciona con nombres de archivo en el conjunto de caracteres del American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1c467-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="1c467-120">Las aplicaciones que usan nombres de archivo en un juego de caracteres del fabricante de equipos originales (OEM) deben convertirlos en ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="1c467-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1c467-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c467-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1c467-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1c467-122">Header files</span></span>

<span data-ttu-id="1c467-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c467-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c467-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1c467-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="1c467-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1c467-125">Mapitags.h</span></span>
  
> <span data-ttu-id="1c467-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1c467-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c467-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c467-127">See also</span></span>



[<span data-ttu-id="1c467-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1c467-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c467-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1c467-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c467-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1c467-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c467-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="1c467-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

