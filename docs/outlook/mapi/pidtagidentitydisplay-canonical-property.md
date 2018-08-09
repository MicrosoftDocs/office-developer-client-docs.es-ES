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
ms.openlocfilehash: b88fc54f1db26277d8a8d5e54fcff0ae164b0eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819600"
---
# <a name="pidtagidentitydisplay-canonical-property"></a><span data-ttu-id="96fd5-103">Propiedad canónica PidTagIdentityDisplay</span><span class="sxs-lookup"><span data-stu-id="96fd5-103">PidTagIdentityDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="96fd5-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="96fd5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="96fd5-105">Contiene el nombre para mostrar para la identidad de un proveedor de servicios, tal como se define dentro de un sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="96fd5-105">Contains the display name for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96fd5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="96fd5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96fd5-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="96fd5-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="96fd5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="96fd5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="96fd5-109">0x3E00</span><span class="sxs-lookup"><span data-stu-id="96fd5-109">0x3E00</span></span>  <br/> |
|<span data-ttu-id="96fd5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="96fd5-110">Data type:</span></span>  <br/> |<span data-ttu-id="96fd5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="96fd5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="96fd5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="96fd5-112">Area:</span></span>  <br/> |<span data-ttu-id="96fd5-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="96fd5-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96fd5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96fd5-114">Remarks</span></span>

<span data-ttu-id="96fd5-115">Estas propiedades no aparecen como propiedades en cualquier objeto, pero sólo como una columna de una tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="96fd5-115">These properties do not appear as properties on any object but only as a column in a status table.</span></span> <span data-ttu-id="96fd5-116">Forma parte de la identidad de la exposición de la fila de la tabla de estado de proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="96fd5-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="96fd5-117">Identidad del proveedor normalmente hace referencia a su cuenta en el servidor, pero puede hacer referencia a cualquier representación que el proveedor define dentro del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="96fd5-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="96fd5-118">Debe proporcionar un proveedor de servicios de suministro de cualquiera de las propiedades de identidad todos ellos.</span><span class="sxs-lookup"><span data-stu-id="96fd5-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="96fd5-119">Los proveedores que pertenecen al mismo servicio de mensajes deben exponer los mismos valores para las propiedades de identidad.</span><span class="sxs-lookup"><span data-stu-id="96fd5-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="96fd5-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="96fd5-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="96fd5-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="96fd5-121">Header files</span></span>

<span data-ttu-id="96fd5-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96fd5-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="96fd5-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="96fd5-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="96fd5-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="96fd5-124">Mapitags.h</span></span>
  
> <span data-ttu-id="96fd5-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="96fd5-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96fd5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="96fd5-126">See also</span></span>



[<span data-ttu-id="96fd5-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="96fd5-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="96fd5-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="96fd5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96fd5-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="96fd5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96fd5-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="96fd5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96fd5-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="96fd5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

