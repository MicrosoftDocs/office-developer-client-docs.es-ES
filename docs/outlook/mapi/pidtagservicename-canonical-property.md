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
ms.openlocfilehash: e5659113b1c6579913042ae0c8dfcd03e9802621
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359482"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="046d2-103">Propiedad canónica PidTagServiceName</span><span class="sxs-lookup"><span data-stu-id="046d2-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="046d2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="046d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="046d2-105">Contiene el nombre de un servicio de mensajes establecido por el usuario en el archivo MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="046d2-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="046d2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="046d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="046d2-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="046d2-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="046d2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="046d2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="046d2-109">0x3D09</span><span class="sxs-lookup"><span data-stu-id="046d2-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="046d2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="046d2-110">Data type:</span></span>  <br/> |<span data-ttu-id="046d2-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="046d2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="046d2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="046d2-112">Area:</span></span>  <br/> |<span data-ttu-id="046d2-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="046d2-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="046d2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="046d2-114">Remarks</span></span>

<span data-ttu-id="046d2-115">El nombre contenido en estas propiedades es específico del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="046d2-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="046d2-116">Procede de la sección [Services] del archivo MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="046d2-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="046d2-117">Estas propiedades aparecen como una columna en la tabla de servicio de mensajes y se pueden usar para filtrar servicios.</span><span class="sxs-lookup"><span data-stu-id="046d2-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="046d2-118">Dado que se usa para identificar y filtrar los servicios, el valor no debe estar localizado.</span><span class="sxs-lookup"><span data-stu-id="046d2-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="046d2-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="046d2-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="046d2-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="046d2-120">Header files</span></span>

<span data-ttu-id="046d2-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="046d2-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="046d2-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="046d2-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="046d2-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="046d2-123">Mapitags.h</span></span>
  
> <span data-ttu-id="046d2-124">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="046d2-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="046d2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="046d2-125">See also</span></span>



[<span data-ttu-id="046d2-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="046d2-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="046d2-127">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="046d2-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="046d2-128">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="046d2-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="046d2-129">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="046d2-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

