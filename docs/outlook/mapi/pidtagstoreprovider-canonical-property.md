---
title: Propiedad canónica PidTagStoreProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412054"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="376d2-103">Propiedad canónica PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="376d2-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="376d2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="376d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="376d2-105">Contiene una estructura [MAPIUID](mapiuid.md) definida por el proveedor que indica el tipo del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="376d2-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="376d2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="376d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="376d2-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="376d2-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="376d2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="376d2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="376d2-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="376d2-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="376d2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="376d2-110">Data type:</span></span>  <br/> |<span data-ttu-id="376d2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="376d2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="376d2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="376d2-112">Area:</span></span>  <br/> |<span data-ttu-id="376d2-113">Propiedades de id.</span><span class="sxs-lookup"><span data-stu-id="376d2-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="376d2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="376d2-114">Remarks</span></span>

<span data-ttu-id="376d2-115">La [estructura MAPIUID](mapiuid.md) identifica el tipo de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="376d2-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="376d2-116">El valor lo calculan los proveedores de almacén de mensajes en objetos de almacén de mensajes y es único para cada proveedor.</span><span class="sxs-lookup"><span data-stu-id="376d2-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="376d2-117">Normalmente se usa para examinar la tabla de almacén de mensajes para buscar un almacén del tipo deseado, como carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="376d2-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="376d2-118">Esta propiedad es análoga a la **propiedad PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) para las libretas de direcciones.</span><span class="sxs-lookup"><span data-stu-id="376d2-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="376d2-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="376d2-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="376d2-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="376d2-120">Header files</span></span>

<span data-ttu-id="376d2-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="376d2-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="376d2-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="376d2-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="376d2-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="376d2-123">Mapitags.h</span></span>
  
> <span data-ttu-id="376d2-124">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="376d2-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="376d2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="376d2-125">See also</span></span>



[<span data-ttu-id="376d2-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="376d2-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="376d2-127">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="376d2-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="376d2-128">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="376d2-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="376d2-129">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="376d2-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

