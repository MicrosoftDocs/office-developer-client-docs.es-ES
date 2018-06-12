---
title: Propiedad canónico PidTagServiceEntryName
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 0d75616aaa6599709828d32393a316c642bc613b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820281"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="1f8db-103">Propiedad canónico PidTagServiceEntryName</span><span class="sxs-lookup"><span data-stu-id="1f8db-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="1f8db-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f8db-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f8db-105">Contiene el nombre de la función de punto de entrada para la configuración de un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1f8db-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f8db-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1f8db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f8db-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="1f8db-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="1f8db-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1f8db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f8db-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="1f8db-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="1f8db-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1f8db-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f8db-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="1f8db-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="1f8db-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1f8db-112">Area:</span></span>  <br/> |<span data-ttu-id="1f8db-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="1f8db-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f8db-114">Notas</span><span class="sxs-lookup"><span data-stu-id="1f8db-114">Remarks</span></span>

<span data-ttu-id="1f8db-115">Se recomienda que los implementadores de servicio de mensaje proporcionar un punto de entrada del servicio de mensaje, pero el punto de entrada no es necesario.</span><span class="sxs-lookup"><span data-stu-id="1f8db-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="1f8db-116">Sin embargo, se debe proporcionar el punto de entrada sólo si existen las propiedades de configuración relacionados.</span><span class="sxs-lookup"><span data-stu-id="1f8db-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="1f8db-117">Si no existen estas propiedades, MAPI se da por supuesto que no se proporciona ningún punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="1f8db-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="1f8db-118">La biblioteca de vínculos dinámicos (DLL) en el que aparece la función de punto de entrada denominada por la propiedad **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1f8db-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="1f8db-119">Para obtener más información sobre puntos de entrada del servicio de mensajes, vea [implementar una función de punto de entrada de proveedor de servicio](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="1f8db-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1f8db-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f8db-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1f8db-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1f8db-121">Header files</span></span>

<span data-ttu-id="1f8db-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f8db-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f8db-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1f8db-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f8db-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f8db-124">Mapitags.h</span></span>
  
> <span data-ttu-id="1f8db-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1f8db-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f8db-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="1f8db-126">See also</span></span>



[<span data-ttu-id="1f8db-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1f8db-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f8db-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1f8db-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f8db-129">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="1f8db-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f8db-130">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1f8db-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

