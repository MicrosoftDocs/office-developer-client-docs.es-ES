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
ms.openlocfilehash: 02d2c30fede7e554910a1bedb01b79c488447bb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595359"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="2b80e-103">Propiedad canónica PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="2b80e-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="2b80e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b80e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b80e-105">Contiene una estructura [MAPIUID](mapiuid.md) definida por el proveedor que indica el tipo del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2b80e-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b80e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2b80e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b80e-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="2b80e-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="2b80e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2b80e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2b80e-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="2b80e-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="2b80e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2b80e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2b80e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2b80e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2b80e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2b80e-112">Area:</span></span>  <br/> |<span data-ttu-id="2b80e-113">Propiedades de Id.</span><span class="sxs-lookup"><span data-stu-id="2b80e-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b80e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b80e-114">Remarks</span></span>

<span data-ttu-id="2b80e-115">La estructura [MAPIUID](mapiuid.md) identifica el tipo de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2b80e-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="2b80e-116">El valor se calcula mediante los proveedores de almacén de mensajes en los objetos de almacén de mensajes y es único para cada proveedor.</span><span class="sxs-lookup"><span data-stu-id="2b80e-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="2b80e-117">Normalmente se usa para la exploración a través de la tabla de almacenamiento de mensajes para buscar un almacén del tipo que desee, como las carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="2b80e-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="2b80e-118">Esta propiedad es análoga a la propiedad **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) de libretas de direcciones.</span><span class="sxs-lookup"><span data-stu-id="2b80e-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2b80e-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b80e-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2b80e-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2b80e-120">Header files</span></span>

<span data-ttu-id="2b80e-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b80e-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b80e-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2b80e-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="2b80e-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2b80e-123">Mapitags.h</span></span>
  
> <span data-ttu-id="2b80e-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2b80e-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b80e-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="2b80e-125">See also</span></span>



[<span data-ttu-id="2b80e-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2b80e-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b80e-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2b80e-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b80e-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2b80e-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b80e-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="2b80e-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

