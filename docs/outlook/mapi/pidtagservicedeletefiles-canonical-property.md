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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336403"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a><span data-ttu-id="1e40f-103">Propiedad canónica PidTagServiceDeleteFiles</span><span class="sxs-lookup"><span data-stu-id="1e40f-103">PidTagServiceDeleteFiles Canonical Property</span></span>

  
  
<span data-ttu-id="1e40f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e40f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e40f-105">Contiene una lista de nombres de archivo que se eliminarán cuando se desinstale el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1e40f-105">Contains a list of filenames that are to be deleted when the message service is uninstalled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e40f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1e40f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e40f-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span><span class="sxs-lookup"><span data-stu-id="1e40f-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span></span>  <br/> |
|<span data-ttu-id="1e40f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1e40f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e40f-109">0x3D10</span><span class="sxs-lookup"><span data-stu-id="1e40f-109">0x3D10</span></span>  <br/> |
|<span data-ttu-id="1e40f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1e40f-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e40f-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1e40f-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1e40f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1e40f-112">Area:</span></span>  <br/> |<span data-ttu-id="1e40f-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="1e40f-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e40f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e40f-114">Remarks</span></span>

<span data-ttu-id="1e40f-115">Los nombres de archivo de la lista que se encuentran en estas propiedades se eliminan del equipo cuando se usa el panel de control para desinstalar el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1e40f-115">The filenames in the list contained in these properties are deleted from the computer when using the control panel to uninstall the message service.</span></span> <span data-ttu-id="1e40f-116">No incluya en la lista ninguna DLL que admita varios servicios de mensajes o que se puedan quitar accidentalmente servicios de mensajes adicionales.</span><span class="sxs-lookup"><span data-stu-id="1e40f-116">Do not include in the list any DLL that supports multiple message services, or additional message services could be inadvertently removed.</span></span>
  
<span data-ttu-id="1e40f-117">MAPI solo funciona con nombres de archivo y otras cadenas que se le pasan, en el juego de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="1e40f-117">MAPI works only with filenames, and other strings passed to it, in the ANSI character set.</span></span> <span data-ttu-id="1e40f-118">Las aplicaciones que usan nombres de archivo en un conjunto de caracteres OEM deben convertirlos a ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="1e40f-118">Applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1e40f-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e40f-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1e40f-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1e40f-120">Header files</span></span>

<span data-ttu-id="1e40f-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1e40f-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e40f-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1e40f-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e40f-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="1e40f-123">Mapitags.h</span></span>
  
> <span data-ttu-id="1e40f-124">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1e40f-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e40f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e40f-125">See also</span></span>



[<span data-ttu-id="1e40f-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1e40f-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e40f-127">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="1e40f-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e40f-128">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1e40f-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e40f-129">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="1e40f-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

