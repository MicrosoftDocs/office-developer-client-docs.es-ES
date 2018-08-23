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
ms.openlocfilehash: 12226039457782162eb74a19713fa77936332f80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565147"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a><span data-ttu-id="ccc6e-103">Propiedad canónica PidTagIdentitySearchKey</span><span class="sxs-lookup"><span data-stu-id="ccc6e-103">PidTagIdentitySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="ccc6e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccc6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccc6e-105">Contiene la clave de búsqueda para la identidad de un proveedor de servicios, tal como se define dentro de un sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ccc6e-105">Contains the search key for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ccc6e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ccc6e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ccc6e-107">PR_IDENTITY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="ccc6e-107">PR_IDENTITY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="ccc6e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ccc6e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ccc6e-109">0x3E05</span><span class="sxs-lookup"><span data-stu-id="ccc6e-109">0x3E05</span></span>  <br/> |
|<span data-ttu-id="ccc6e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ccc6e-110">Data type:</span></span>  <br/> |<span data-ttu-id="ccc6e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ccc6e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ccc6e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ccc6e-112">Area:</span></span>  <br/> |<span data-ttu-id="ccc6e-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="ccc6e-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ccc6e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ccc6e-114">Remarks</span></span>

<span data-ttu-id="ccc6e-115">Esta propiedad no aparece como una propiedad en cualquier objeto sino sólo como una columna de una tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="ccc6e-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="ccc6e-116">Forma parte de la identidad de la exposición de la fila de la tabla de estado de proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="ccc6e-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="ccc6e-117">Identidad del proveedor normalmente hace referencia a su cuenta en el servidor, pero puede hacer referencia a cualquier representación que el proveedor define dentro del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ccc6e-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="ccc6e-118">Debe proporcionar un proveedor de servicios de suministro de cualquiera de las propiedades de identidad todos ellos.</span><span class="sxs-lookup"><span data-stu-id="ccc6e-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="ccc6e-119">Los proveedores que pertenecen al mismo servicio de mensajes deben exponer los mismos valores para las propiedades de identidad.</span><span class="sxs-lookup"><span data-stu-id="ccc6e-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ccc6e-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ccc6e-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ccc6e-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ccc6e-121">Header files</span></span>

<span data-ttu-id="ccc6e-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ccc6e-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="ccc6e-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ccc6e-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="ccc6e-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ccc6e-124">Mapitags.h</span></span>
  
> <span data-ttu-id="ccc6e-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ccc6e-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ccc6e-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ccc6e-126">See also</span></span>



[<span data-ttu-id="ccc6e-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="ccc6e-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="ccc6e-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ccc6e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ccc6e-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="ccc6e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ccc6e-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ccc6e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ccc6e-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="ccc6e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

