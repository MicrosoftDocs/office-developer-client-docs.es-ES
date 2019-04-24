---
title: Propiedad canónica PidTagIdentityDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityDisplay
api_type:
- HeaderDef
ms.assetid: ad9756c1-c1f9-4ab3-a58a-31e574dd9530
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d6e189f78dec2fc92f1804be93e7885b61734b03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327954"
---
# <a name="pidtagidentitydisplay-canonical-property"></a><span data-ttu-id="2e482-103">Propiedad canónica PidTagIdentityDisplay</span><span class="sxs-lookup"><span data-stu-id="2e482-103">PidTagIdentityDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="2e482-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e482-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e482-105">Contiene el nombre para mostrar de la identidad de un proveedor de servicios, tal como se define en un sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="2e482-105">Contains the display name for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e482-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2e482-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e482-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="2e482-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="2e482-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2e482-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2e482-109">0x3E00</span><span class="sxs-lookup"><span data-stu-id="2e482-109">0x3E00</span></span>  <br/> |
|<span data-ttu-id="2e482-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2e482-110">Data type:</span></span>  <br/> |<span data-ttu-id="2e482-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2e482-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2e482-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2e482-112">Area:</span></span>  <br/> |<span data-ttu-id="2e482-113">Estado de MAPI</span><span class="sxs-lookup"><span data-stu-id="2e482-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e482-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e482-114">Remarks</span></span>

<span data-ttu-id="2e482-115">Estas propiedades no aparecen como propiedades en ningún objeto, sino sólo como una columna en una tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="2e482-115">These properties do not appear as properties on any object but only as a column in a status table.</span></span> <span data-ttu-id="2e482-116">Forma parte de la identidad del proveedor de servicios que expone la fila de la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="2e482-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="2e482-117">La identidad del proveedor normalmente hace referencia a su cuenta en el servidor, pero puede hacer referencia a cualquier representación que el proveedor defina en el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="2e482-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="2e482-118">Un proveedor de servicios que proporcione cualquiera de las propiedades de identidad debe proporcionar todas ellas.</span><span class="sxs-lookup"><span data-stu-id="2e482-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="2e482-119">Los proveedores que pertenecen al mismo servicio de mensajes deben exponer los mismos valores para las propiedades de identidad.</span><span class="sxs-lookup"><span data-stu-id="2e482-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2e482-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e482-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2e482-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2e482-121">Header files</span></span>

<span data-ttu-id="2e482-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2e482-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e482-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2e482-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="2e482-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2e482-124">Mapitags.h</span></span>
  
> <span data-ttu-id="2e482-125">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2e482-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e482-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e482-126">See also</span></span>



[<span data-ttu-id="2e482-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="2e482-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="2e482-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2e482-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e482-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="2e482-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e482-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2e482-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e482-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2e482-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

