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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438963"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="0d47b-103">Propiedad canónica PidTagServiceName</span><span class="sxs-lookup"><span data-stu-id="0d47b-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="0d47b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d47b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d47b-105">Contiene el nombre de un servicio de mensajes establecido por el usuario en el archivo MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="0d47b-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d47b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0d47b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d47b-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="0d47b-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="0d47b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0d47b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0d47b-109">0x3D09</span><span class="sxs-lookup"><span data-stu-id="0d47b-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="0d47b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0d47b-110">Data type:</span></span>  <br/> |<span data-ttu-id="0d47b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0d47b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0d47b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0d47b-112">Area:</span></span>  <br/> |<span data-ttu-id="0d47b-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="0d47b-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d47b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d47b-114">Remarks</span></span>

<span data-ttu-id="0d47b-115">El nombre incluido en estas propiedades es específico del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0d47b-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="0d47b-116">Procede de la sección [Servicios] de MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="0d47b-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="0d47b-117">Estas propiedades aparecen como una columna en la tabla de servicio de mensajes y se pueden usar para filtrar servicios.</span><span class="sxs-lookup"><span data-stu-id="0d47b-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="0d47b-118">Dado que se usa para identificar y filtrar servicios, el valor no debe localizarse.</span><span class="sxs-lookup"><span data-stu-id="0d47b-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0d47b-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d47b-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0d47b-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0d47b-120">Header files</span></span>

<span data-ttu-id="0d47b-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d47b-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d47b-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0d47b-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="0d47b-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0d47b-123">Mapitags.h</span></span>
  
> <span data-ttu-id="0d47b-124">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0d47b-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d47b-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0d47b-125">See also</span></span>



[<span data-ttu-id="0d47b-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0d47b-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d47b-127">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="0d47b-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d47b-128">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0d47b-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d47b-129">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0d47b-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

