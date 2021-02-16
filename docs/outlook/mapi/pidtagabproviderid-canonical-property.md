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
ms.openlocfilehash: 820df61ec23e2dd1459582e5a7bb35ad9525e0b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422246"
---
# <a name="pidtagabproviderid-canonical-property"></a><span data-ttu-id="4b6de-103">Propiedad canónica PidTagAbProviderId</span><span class="sxs-lookup"><span data-stu-id="4b6de-103">PidTagAbProviderId Canonical Property</span></span>

  
  
<span data-ttu-id="4b6de-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b6de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b6de-105">Contiene la estructura [MAPIUID](mapiuid.md) de un proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4b6de-105">Contains an address book provider's [MAPIUID](mapiuid.md) structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b6de-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4b6de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b6de-107">PR_AB_PROVIDER_ID</span><span class="sxs-lookup"><span data-stu-id="4b6de-107">PR_AB_PROVIDER_ID</span></span>  <br/> |
|<span data-ttu-id="4b6de-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4b6de-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4b6de-109">0x3615</span><span class="sxs-lookup"><span data-stu-id="4b6de-109">0x3615</span></span>  <br/> |
|<span data-ttu-id="4b6de-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4b6de-110">Data type:</span></span>  <br/> |<span data-ttu-id="4b6de-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4b6de-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4b6de-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4b6de-112">Area:</span></span>  <br/> |<span data-ttu-id="4b6de-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="4b6de-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b6de-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b6de-114">Remarks</span></span>

<span data-ttu-id="4b6de-115">La **estructura MAPIUID** identifica qué proveedor de libreta de direcciones proporciona este contenedor en particular en la jerarquía de contenedores.</span><span class="sxs-lookup"><span data-stu-id="4b6de-115">The **MAPIUID** structure identifies which address book provider supplies this particular container in the container hierarchy.</span></span> <span data-ttu-id="4b6de-116">El valor es único para cada proveedor.</span><span class="sxs-lookup"><span data-stu-id="4b6de-116">The value is unique to each provider.</span></span> 
  
<span data-ttu-id="4b6de-117">Un proveedor de libreta de direcciones puede proporcionar más de un identificador.</span><span class="sxs-lookup"><span data-stu-id="4b6de-117">An address book provider can provide more than one identifier.</span></span> <span data-ttu-id="4b6de-118">Por ejemplo, un proveedor que proporciona dos contenedores diferentes puede publicar **en PR_AB_PROVIDER_ID** identificadores únicos para cada contenedor.</span><span class="sxs-lookup"><span data-stu-id="4b6de-118">For example, a provider that supplies two different containers can publish in **PR_AB_PROVIDER_ID** unique identifiers for each container.</span></span> 
  
 <span data-ttu-id="4b6de-119">**PR_AB_PROVIDER_ID** es análogo a la **propiedad PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para los almacenes de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4b6de-119">**PR_AB_PROVIDER_ID** is analogous to the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for message stores.</span></span> <span data-ttu-id="4b6de-120">Las aplicaciones cliente pueden usar **PR_AB_PROVIDER_ID** para buscar filas relacionadas en una tabla de jerarquía de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4b6de-120">Client applications can use **PR_AB_PROVIDER_ID** to find related rows in an address book hierarchy table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4b6de-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b6de-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4b6de-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4b6de-122">Header files</span></span>

<span data-ttu-id="4b6de-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4b6de-123">Mapitags.h</span></span>
  
> <span data-ttu-id="4b6de-124">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="4b6de-124">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="4b6de-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b6de-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b6de-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4b6de-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b6de-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4b6de-127">See also</span></span>



[<span data-ttu-id="4b6de-128">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="4b6de-128">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="4b6de-129">Propiedad canónica PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="4b6de-129">PidTagStoreProvider Canonical Property</span></span>](pidtagstoreprovider-canonical-property.md)


[<span data-ttu-id="4b6de-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="4b6de-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b6de-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4b6de-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b6de-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4b6de-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

