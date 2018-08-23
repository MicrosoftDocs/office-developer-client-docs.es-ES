---
title: Propiedad canónica PidTagStoreRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreRecordKey
api_type:
- COM
ms.assetid: 27347302-bd52-4f62-98f1-6c37f9a66463
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 08527f3325742eb7c48f11c2ed7d08f71fa3e972
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592713"
---
# <a name="pidtagstorerecordkey-canonical-property"></a><span data-ttu-id="33b16-103">Propiedad canónica PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="33b16-103">PidTagStoreRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="33b16-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33b16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33b16-105">Contiene el identificador único de binario comparable (clave de registro) del almacén de mensajes en el que reside un objeto.</span><span class="sxs-lookup"><span data-stu-id="33b16-105">Contains the unique binary-comparable identifier (record key) of the message store in which an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33b16-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="33b16-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33b16-107">PR_STORE_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="33b16-107">PR_STORE_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="33b16-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="33b16-108">Identifier:</span></span>  <br/> |<span data-ttu-id="33b16-109">0x0FFA</span><span class="sxs-lookup"><span data-stu-id="33b16-109">0x0FFA</span></span>  <br/> |
|<span data-ttu-id="33b16-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="33b16-110">Data type:</span></span>  <br/> |<span data-ttu-id="33b16-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="33b16-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="33b16-112">Área:</span><span class="sxs-lookup"><span data-stu-id="33b16-112">Area:</span></span>  <br/> |<span data-ttu-id="33b16-113">Propiedades de Id.</span><span class="sxs-lookup"><span data-stu-id="33b16-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33b16-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="33b16-114">Remarks</span></span>

<span data-ttu-id="33b16-115">Para un almacén de mensajes, esta propiedad es idéntica a la propiedad de **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) del almacén.</span><span class="sxs-lookup"><span data-stu-id="33b16-115">For a message store, this property is identical to the store's own **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="33b16-116">La relación entre esta propiedad y **PR_RECORD_KEY** es la misma que la relación entre **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) y la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="33b16-116">The relationship between this property and **PR_RECORD_KEY** is the same as the relationship between **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="33b16-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="33b16-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33b16-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="33b16-118">Protocol specifications</span></span>

<span data-ttu-id="33b16-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33b16-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33b16-120">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="33b16-120">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="33b16-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33b16-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33b16-122">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="33b16-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33b16-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="33b16-123">Header files</span></span>

<span data-ttu-id="33b16-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33b16-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="33b16-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="33b16-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="33b16-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="33b16-126">Mapitags.h</span></span>
  
> <span data-ttu-id="33b16-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="33b16-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33b16-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="33b16-128">See also</span></span>



[<span data-ttu-id="33b16-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="33b16-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33b16-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="33b16-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33b16-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="33b16-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33b16-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="33b16-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

