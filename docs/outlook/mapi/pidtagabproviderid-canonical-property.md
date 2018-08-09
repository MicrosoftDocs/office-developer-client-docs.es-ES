---
title: Propiedad canónica PidTagAbProviderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 84a2d5517d405ac6deb61f7c4679d6816e802404
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819155"
---
# <a name="pidtagabproviderid-canonical-property"></a><span data-ttu-id="2a228-103">Propiedad canónica PidTagAbProviderId</span><span class="sxs-lookup"><span data-stu-id="2a228-103">PidTagAbProviderId Canonical Property</span></span>

  
  
<span data-ttu-id="2a228-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2a228-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2a228-105">Contiene la estructura [MAPIUID](mapiuid.md) de un proveedor libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="2a228-105">Contains an address book provider's [MAPIUID](mapiuid.md) structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a228-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2a228-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a228-107">PR_AB_PROVIDER_ID</span><span class="sxs-lookup"><span data-stu-id="2a228-107">PR_AB_PROVIDER_ID</span></span>  <br/> |
|<span data-ttu-id="2a228-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2a228-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2a228-109">0x3615</span><span class="sxs-lookup"><span data-stu-id="2a228-109">0x3615</span></span>  <br/> |
|<span data-ttu-id="2a228-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2a228-110">Data type:</span></span>  <br/> |<span data-ttu-id="2a228-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2a228-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2a228-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2a228-112">Area:</span></span>  <br/> |<span data-ttu-id="2a228-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="2a228-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a228-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a228-114">Remarks</span></span>

<span data-ttu-id="2a228-115">La estructura **MAPIUID** identifica qué proveedor de libreta de direcciones proporciona este contenedor determinado en la jerarquía del contenedor.</span><span class="sxs-lookup"><span data-stu-id="2a228-115">The **MAPIUID** structure identifies which address book provider supplies this particular container in the container hierarchy.</span></span> <span data-ttu-id="2a228-116">El valor es único para cada proveedor.</span><span class="sxs-lookup"><span data-stu-id="2a228-116">The value is unique to each provider.</span></span> 
  
<span data-ttu-id="2a228-117">Un proveedor de la libreta de direcciones puede proporcionar más de un identificador.</span><span class="sxs-lookup"><span data-stu-id="2a228-117">An address book provider can provide more than one identifier.</span></span> <span data-ttu-id="2a228-118">Por ejemplo, un proveedor que suministran los dos contenedores diferentes puede publicar en **PR_AB_PROVIDER_ID** identificadores únicos para cada contenedor.</span><span class="sxs-lookup"><span data-stu-id="2a228-118">For example, a provider that supplies two different containers can publish in **PR_AB_PROVIDER_ID** unique identifiers for each container.</span></span> 
  
 <span data-ttu-id="2a228-119">**PR_AB_PROVIDER_ID** es análoga a la propiedad **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para los almacenes de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2a228-119">**PR_AB_PROVIDER_ID** is analogous to the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for message stores.</span></span> <span data-ttu-id="2a228-120">Las aplicaciones de cliente pueden usar **PR_AB_PROVIDER_ID** para buscar filas relacionadas en una tabla de jerarquías de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="2a228-120">Client applications can use **PR_AB_PROVIDER_ID** to find related rows in an address book hierarchy table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2a228-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a228-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2a228-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2a228-122">Header files</span></span>

<span data-ttu-id="2a228-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2a228-123">Mapitags.h</span></span>
  
> <span data-ttu-id="2a228-124">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="2a228-124">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="2a228-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a228-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a228-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2a228-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a228-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a228-127">See also</span></span>



[<span data-ttu-id="2a228-128">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="2a228-128">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="2a228-129">Propiedad canónica PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="2a228-129">PidTagStoreProvider Canonical Property</span></span>](pidtagstoreprovider-canonical-property.md)


[<span data-ttu-id="2a228-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2a228-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a228-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2a228-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a228-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="2a228-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

