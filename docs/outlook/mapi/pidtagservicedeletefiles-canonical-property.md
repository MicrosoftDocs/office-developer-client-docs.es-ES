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
ms.openlocfilehash: 8f90d72e842df62c19c5aeeaf6c398c5db469560
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820298"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a><span data-ttu-id="5bcd9-103">Propiedad canónica PidTagServiceDeleteFiles</span><span class="sxs-lookup"><span data-stu-id="5bcd9-103">PidTagServiceDeleteFiles Canonical Property</span></span>

  
  
<span data-ttu-id="5bcd9-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5bcd9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5bcd9-105">Contiene una lista de nombres de archivo que se va a eliminar cuando se desinstala el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="5bcd9-105">Contains a list of filenames that are to be deleted when the message service is uninstalled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5bcd9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5bcd9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5bcd9-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span><span class="sxs-lookup"><span data-stu-id="5bcd9-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span></span>  <br/> |
|<span data-ttu-id="5bcd9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5bcd9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5bcd9-109">0x3D10</span><span class="sxs-lookup"><span data-stu-id="5bcd9-109">0x3D10</span></span>  <br/> |
|<span data-ttu-id="5bcd9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5bcd9-110">Data type:</span></span>  <br/> |<span data-ttu-id="5bcd9-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5bcd9-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5bcd9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5bcd9-112">Area:</span></span>  <br/> |<span data-ttu-id="5bcd9-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="5bcd9-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bcd9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5bcd9-114">Remarks</span></span>

<span data-ttu-id="5bcd9-115">Los nombres de archivo en la lista de contenidos en estas propiedades se eliminan del equipo cuando se usa el panel de control para desinstalar el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="5bcd9-115">The filenames in the list contained in these properties are deleted from the computer when using the control panel to uninstall the message service.</span></span> <span data-ttu-id="5bcd9-116">No incluir en la lista de cualquier archivo DLL que es compatible con varios servicios de mensaje o servicios adicionales de mensaje podrían quitarse sin darse cuenta.</span><span class="sxs-lookup"><span data-stu-id="5bcd9-116">Do not include in the list any DLL that supports multiple message services, or additional message services could be inadvertently removed.</span></span>
  
<span data-ttu-id="5bcd9-117">MAPI sólo funciona con los nombres de archivo y otras cadenas pasan a ella, en el juego de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="5bcd9-117">MAPI works only with filenames, and other strings passed to it, in the ANSI character set.</span></span> <span data-ttu-id="5bcd9-118">Las aplicaciones que usan nombres de archivo en un juego de caracteres OEM deben convertirlos a ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="5bcd9-118">Applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5bcd9-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5bcd9-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5bcd9-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5bcd9-120">Header files</span></span>

<span data-ttu-id="5bcd9-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5bcd9-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="5bcd9-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5bcd9-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="5bcd9-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5bcd9-123">Mapitags.h</span></span>
  
> <span data-ttu-id="5bcd9-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5bcd9-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bcd9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bcd9-125">See also</span></span>



[<span data-ttu-id="5bcd9-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5bcd9-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5bcd9-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5bcd9-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5bcd9-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5bcd9-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5bcd9-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5bcd9-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

