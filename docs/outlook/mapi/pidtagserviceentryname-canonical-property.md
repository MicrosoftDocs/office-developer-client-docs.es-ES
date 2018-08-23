---
title: Propiedad canónica PidTagServiceEntryName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3988596cc0b9c01d526354dabef3a6e7fdefc3b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583228"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="5d380-103">Propiedad canónica PidTagServiceEntryName</span><span class="sxs-lookup"><span data-stu-id="5d380-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="5d380-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d380-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d380-105">Contiene el nombre de la función de punto de entrada para la configuración de un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="5d380-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d380-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5d380-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d380-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="5d380-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="5d380-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5d380-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5d380-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="5d380-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="5d380-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5d380-110">Data type:</span></span>  <br/> |<span data-ttu-id="5d380-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="5d380-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="5d380-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5d380-112">Area:</span></span>  <br/> |<span data-ttu-id="5d380-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="5d380-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d380-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d380-114">Remarks</span></span>

<span data-ttu-id="5d380-115">Se recomienda que los implementadores de servicio de mensaje proporcionar un punto de entrada del servicio de mensaje, pero el punto de entrada no es necesario.</span><span class="sxs-lookup"><span data-stu-id="5d380-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="5d380-116">Sin embargo, se debe proporcionar el punto de entrada sólo si existen las propiedades de configuración relacionados.</span><span class="sxs-lookup"><span data-stu-id="5d380-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="5d380-117">Si no existen estas propiedades, MAPI se da por supuesto que no se proporciona ningún punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="5d380-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="5d380-118">La biblioteca de vínculos dinámicos (DLL) en el que aparece la función de punto de entrada denominada por la propiedad **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5d380-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="5d380-119">Para obtener más información sobre puntos de entrada del servicio de mensajes, vea [implementar una función de punto de entrada de proveedor de servicio](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="5d380-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5d380-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d380-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5d380-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5d380-121">Header files</span></span>

<span data-ttu-id="5d380-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d380-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d380-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5d380-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="5d380-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5d380-124">Mapitags.h</span></span>
  
> <span data-ttu-id="5d380-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5d380-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d380-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5d380-126">See also</span></span>



[<span data-ttu-id="5d380-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5d380-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d380-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5d380-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d380-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5d380-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d380-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5d380-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

