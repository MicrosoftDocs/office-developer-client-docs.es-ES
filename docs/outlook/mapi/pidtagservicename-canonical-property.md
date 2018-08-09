---
title: Propiedad canónica PidTagServiceName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 260a35af11b76b1867c693723c1a7fa8133082fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820290"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="8275c-103">Propiedad canónica PidTagServiceName</span><span class="sxs-lookup"><span data-stu-id="8275c-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="8275c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8275c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8275c-105">Contiene el nombre de un servicio de mensajes como conjunto por el usuario en el archivo MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="8275c-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8275c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8275c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8275c-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="8275c-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="8275c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8275c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8275c-109">0x3D09</span><span class="sxs-lookup"><span data-stu-id="8275c-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="8275c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8275c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8275c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8275c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8275c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8275c-112">Area:</span></span>  <br/> |<span data-ttu-id="8275c-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="8275c-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8275c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8275c-114">Remarks</span></span>

<span data-ttu-id="8275c-115">El nombre de estas propiedades es específico para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8275c-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="8275c-116">Se trata de la sección [Services] en MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="8275c-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="8275c-117">Estas propiedades aparecen como una columna en la tabla de servicios de mensaje y se pueden usar para filtrar los servicios.</span><span class="sxs-lookup"><span data-stu-id="8275c-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="8275c-118">Debido a que se usa para identificar y filtrar los servicios, el valor no debe estar adaptado.</span><span class="sxs-lookup"><span data-stu-id="8275c-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8275c-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8275c-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8275c-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8275c-120">Header files</span></span>

<span data-ttu-id="8275c-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8275c-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="8275c-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8275c-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="8275c-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8275c-123">Mapitags.h</span></span>
  
> <span data-ttu-id="8275c-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8275c-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8275c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8275c-125">See also</span></span>



[<span data-ttu-id="8275c-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8275c-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8275c-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8275c-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8275c-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8275c-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8275c-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8275c-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

