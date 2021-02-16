---
title: Propiedad canónica PidTagIdentitySearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentitySearchKey
api_type:
- HeaderDef
ms.assetid: 5fe55ba7-4ecd-4a43-ab5b-2ef595c2cdd9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5f5f5eaa41d6256bed69b2cd9a91208181d5bda1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423751"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a><span data-ttu-id="9507f-103">Propiedad canónica PidTagIdentitySearchKey</span><span class="sxs-lookup"><span data-stu-id="9507f-103">PidTagIdentitySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="9507f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9507f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9507f-105">Contiene la clave de búsqueda de la identidad de un proveedor de servicios tal como se define en un sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="9507f-105">Contains the search key for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9507f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9507f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9507f-107">PR_IDENTITY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="9507f-107">PR_IDENTITY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="9507f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9507f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9507f-109">0x3E05</span><span class="sxs-lookup"><span data-stu-id="9507f-109">0x3E05</span></span>  <br/> |
|<span data-ttu-id="9507f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9507f-110">Data type:</span></span>  <br/> |<span data-ttu-id="9507f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9507f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9507f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9507f-112">Area:</span></span>  <br/> |<span data-ttu-id="9507f-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="9507f-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9507f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9507f-114">Remarks</span></span>

<span data-ttu-id="9507f-115">Esta propiedad no aparece como una propiedad en ningún objeto, sino solo como una columna de una tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="9507f-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="9507f-116">Forma parte de la identidad del proveedor de servicios que expone la fila de la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="9507f-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="9507f-117">La identidad del proveedor suele hacer referencia a su cuenta en el servidor, pero puede hacer referencia a cualquier representación que el proveedor defina dentro del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="9507f-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="9507f-118">Un proveedor de servicios que proporciona cualquiera de las propiedades de identidad debe proporcionar todas ellas.</span><span class="sxs-lookup"><span data-stu-id="9507f-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="9507f-119">Los proveedores que pertenecen al mismo servicio de mensajes deben exponer los mismos valores para las propiedades de identidad.</span><span class="sxs-lookup"><span data-stu-id="9507f-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9507f-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9507f-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9507f-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9507f-121">Header files</span></span>

<span data-ttu-id="9507f-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9507f-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="9507f-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9507f-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="9507f-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9507f-124">Mapitags.h</span></span>
  
> <span data-ttu-id="9507f-125">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9507f-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9507f-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9507f-126">See also</span></span>



[<span data-ttu-id="9507f-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="9507f-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="9507f-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9507f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9507f-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="9507f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9507f-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9507f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9507f-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9507f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

