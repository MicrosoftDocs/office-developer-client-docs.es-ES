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
ms.openlocfilehash: a00abec7627eb12e23e7b76f5d0900514d710ffb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593098"
---
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="f6377-103">Propiedad canónica PidTagResourcePath</span><span class="sxs-lookup"><span data-stu-id="f6377-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="f6377-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6377-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6377-105">Contiene una ruta de acceso al servidor del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="f6377-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f6377-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f6377-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6377-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span><span class="sxs-lookup"><span data-stu-id="f6377-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="f6377-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f6377-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f6377-109">0x3E07</span><span class="sxs-lookup"><span data-stu-id="f6377-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="f6377-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f6377-110">Data type:</span></span>  <br/> |<span data-ttu-id="f6377-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f6377-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f6377-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f6377-112">Area:</span></span>  <br/> |<span data-ttu-id="f6377-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="f6377-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6377-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f6377-114">Remarks</span></span>

<span data-ttu-id="f6377-115">La ruta de acceso contenida en estas propiedades representa la ruta de acceso sugerida donde el usuario puede encontrar recursos.</span><span class="sxs-lookup"><span data-stu-id="f6377-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="f6377-116">La definición de estas propiedades es específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f6377-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="f6377-117">Por ejemplo, una aplicación de programación usa estas propiedades para especificar la ubicación sugerida para sus archivos de aplicación de programación.</span><span class="sxs-lookup"><span data-stu-id="f6377-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="f6377-118">El perfil de usuario de mensajería proporciona estas propiedades como una comodidad para que una aplicación cliente no tiene que solicitar al usuario de mensajería de una ruta de acceso de red o la letra de la unidad de red.</span><span class="sxs-lookup"><span data-stu-id="f6377-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="f6377-119">MAPI sólo funciona con los nombres de archivo en el juego de caracteres estadounidense National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f6377-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="f6377-120">Las aplicaciones que usan nombres de archivo en un juego de caracteres del fabricante de equipos originales (OEM) deben convertirlos a ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="f6377-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f6377-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6377-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f6377-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f6377-122">Header files</span></span>

<span data-ttu-id="f6377-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6377-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6377-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f6377-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f6377-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f6377-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f6377-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f6377-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6377-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f6377-127">See also</span></span>



[<span data-ttu-id="f6377-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f6377-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6377-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f6377-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6377-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f6377-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6377-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f6377-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

