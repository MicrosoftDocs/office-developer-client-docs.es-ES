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
ms.openlocfilehash: 28c269db15d0c0a81950a61ee9e6629ad067b789
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819580"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a><span data-ttu-id="2c744-103">Propiedad canónica PidTagIdentitySearchKey</span><span class="sxs-lookup"><span data-stu-id="2c744-103">PidTagIdentitySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="2c744-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c744-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c744-105">Contiene la clave de búsqueda para la identidad de un proveedor de servicios, tal como se define dentro de un sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="2c744-105">Contains the search key for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2c744-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2c744-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c744-107">PR_IDENTITY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="2c744-107">PR_IDENTITY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="2c744-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2c744-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2c744-109">0x3E05</span><span class="sxs-lookup"><span data-stu-id="2c744-109">0x3E05</span></span>  <br/> |
|<span data-ttu-id="2c744-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2c744-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c744-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2c744-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2c744-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2c744-112">Area:</span></span>  <br/> |<span data-ttu-id="2c744-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="2c744-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c744-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c744-114">Remarks</span></span>

<span data-ttu-id="2c744-115">Esta propiedad no aparece como una propiedad en cualquier objeto sino sólo como una columna de una tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="2c744-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="2c744-116">Forma parte de la identidad de la exposición de la fila de la tabla de estado de proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="2c744-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="2c744-117">Identidad del proveedor normalmente hace referencia a su cuenta en el servidor, pero puede hacer referencia a cualquier representación que el proveedor define dentro del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="2c744-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="2c744-118">Debe proporcionar un proveedor de servicios de suministro de cualquiera de las propiedades de identidad todos ellos.</span><span class="sxs-lookup"><span data-stu-id="2c744-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="2c744-119">Los proveedores que pertenecen al mismo servicio de mensajes deben exponer los mismos valores para las propiedades de identidad.</span><span class="sxs-lookup"><span data-stu-id="2c744-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2c744-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c744-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2c744-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2c744-121">Header files</span></span>

<span data-ttu-id="2c744-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c744-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c744-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2c744-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c744-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2c744-124">Mapitags.h</span></span>
  
> <span data-ttu-id="2c744-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2c744-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c744-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c744-126">See also</span></span>



[<span data-ttu-id="2c744-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="2c744-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="2c744-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2c744-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c744-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2c744-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c744-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2c744-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c744-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="2c744-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

