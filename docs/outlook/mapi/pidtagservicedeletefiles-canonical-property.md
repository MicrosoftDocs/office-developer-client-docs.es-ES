---
title: Propiedad canónica PidTagServiceDeleteFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da01385f83d9af9ad02eeb2fed08e3bc22d4df84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436828"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a><span data-ttu-id="c1660-103">Propiedad canónica PidTagServiceDeleteFiles</span><span class="sxs-lookup"><span data-stu-id="c1660-103">PidTagServiceDeleteFiles Canonical Property</span></span>

  
  
<span data-ttu-id="c1660-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1660-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1660-105">Contiene una lista de nombres de archivo que se eliminarán cuando se desinstale el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c1660-105">Contains a list of filenames that are to be deleted when the message service is uninstalled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1660-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c1660-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c1660-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span><span class="sxs-lookup"><span data-stu-id="c1660-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span></span>  <br/> |
|<span data-ttu-id="c1660-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c1660-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c1660-109">0x3D10</span><span class="sxs-lookup"><span data-stu-id="c1660-109">0x3D10</span></span>  <br/> |
|<span data-ttu-id="c1660-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c1660-110">Data type:</span></span>  <br/> |<span data-ttu-id="c1660-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c1660-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c1660-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c1660-112">Area:</span></span>  <br/> |<span data-ttu-id="c1660-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="c1660-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1660-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1660-114">Remarks</span></span>

<span data-ttu-id="c1660-115">Los nombres de archivo de la lista contenida en estas propiedades se eliminan del equipo cuando se usa el panel de control para desinstalar el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c1660-115">The filenames in the list contained in these properties are deleted from the computer when using the control panel to uninstall the message service.</span></span> <span data-ttu-id="c1660-116">No incluya en la lista ninguna DLL que admita varios servicios de mensajes o que se puedan quitar accidentalmente servicios de mensajes adicionales.</span><span class="sxs-lookup"><span data-stu-id="c1660-116">Do not include in the list any DLL that supports multiple message services, or additional message services could be inadvertently removed.</span></span>
  
<span data-ttu-id="c1660-117">MAPI sólo funciona con nombres de archivo y otras cadenas pasadas en el juego de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="c1660-117">MAPI works only with filenames, and other strings passed to it, in the ANSI character set.</span></span> <span data-ttu-id="c1660-118">Las aplicaciones que usan nombres de archivo en un juego de caracteres OEM deben convertirlos en ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="c1660-118">Applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c1660-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1660-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c1660-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c1660-120">Header files</span></span>

<span data-ttu-id="c1660-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c1660-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="c1660-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c1660-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="c1660-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c1660-123">Mapitags.h</span></span>
  
> <span data-ttu-id="c1660-124">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c1660-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1660-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c1660-125">See also</span></span>



[<span data-ttu-id="c1660-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c1660-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c1660-127">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="c1660-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c1660-128">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c1660-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c1660-129">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c1660-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

