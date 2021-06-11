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
ms.openlocfilehash: 2c771f1d97305271b70102c148e62f30512974fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432474"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="219f5-103">Propiedad canónica PidTagServiceEntryName</span><span class="sxs-lookup"><span data-stu-id="219f5-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="219f5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="219f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="219f5-105">Contiene el nombre de la función de punto de entrada para la configuración de un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="219f5-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="219f5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="219f5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="219f5-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="219f5-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="219f5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="219f5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="219f5-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="219f5-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="219f5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="219f5-110">Data type:</span></span>  <br/> |<span data-ttu-id="219f5-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="219f5-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="219f5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="219f5-112">Area:</span></span>  <br/> |<span data-ttu-id="219f5-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="219f5-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="219f5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="219f5-114">Remarks</span></span>

<span data-ttu-id="219f5-115">Se recomienda que los implementadores del servicio de mensajes proporcionen un punto de entrada de servicio de mensajes, pero no es necesario el punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="219f5-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="219f5-116">Sin embargo, el punto de entrada solo debe proporcionarse si existen las propiedades de configuración relacionadas.</span><span class="sxs-lookup"><span data-stu-id="219f5-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="219f5-117">Si estas propiedades no existen, MAPI supone que no se proporciona ningún punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="219f5-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="219f5-118">La biblioteca de vínculos dinámicos (DLL) en la que aparece la función de punto de entrada se denomina mediante la propiedad **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="219f5-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="219f5-119">Para obtener más información sobre los puntos de entrada del servicio de mensajes, vea [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="219f5-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="219f5-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="219f5-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="219f5-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="219f5-121">Header files</span></span>

<span data-ttu-id="219f5-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="219f5-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="219f5-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="219f5-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="219f5-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="219f5-124">Mapitags.h</span></span>
  
> <span data-ttu-id="219f5-125">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="219f5-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="219f5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="219f5-126">See also</span></span>



[<span data-ttu-id="219f5-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="219f5-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="219f5-128">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="219f5-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="219f5-129">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="219f5-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="219f5-130">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="219f5-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

