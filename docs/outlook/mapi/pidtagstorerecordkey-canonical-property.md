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
ms.openlocfilehash: d6f858a9f1d3d4620a86621e3f5ecb4ad4609691
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278734"
---
# <a name="pidtagstorerecordkey-canonical-property"></a><span data-ttu-id="91975-103">Propiedad canónica PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="91975-103">PidTagStoreRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="91975-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91975-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91975-105">Contiene el identificador único comparable binario (clave de registro) del almacén de mensajes en el que reside un objeto.</span><span class="sxs-lookup"><span data-stu-id="91975-105">Contains the unique binary-comparable identifier (record key) of the message store in which an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91975-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="91975-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91975-107">PR_STORE_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="91975-107">PR_STORE_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="91975-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="91975-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91975-109">0x0FFA</span><span class="sxs-lookup"><span data-stu-id="91975-109">0x0FFA</span></span>  <br/> |
|<span data-ttu-id="91975-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="91975-110">Data type:</span></span>  <br/> |<span data-ttu-id="91975-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="91975-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="91975-112">Área:</span><span class="sxs-lookup"><span data-stu-id="91975-112">Area:</span></span>  <br/> |<span data-ttu-id="91975-113">Propiedades de identificador</span><span class="sxs-lookup"><span data-stu-id="91975-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91975-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="91975-114">Remarks</span></span>

<span data-ttu-id="91975-115">Para un almacén de mensajes, esta propiedad es idéntica a la propiedad **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) del almacén.</span><span class="sxs-lookup"><span data-stu-id="91975-115">For a message store, this property is identical to the store's own **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="91975-116">La relación entre esta propiedad y **PR_RECORD_KEY** es la misma que la relación entre **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) y \*\*\*\* ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="91975-116">The relationship between this property and **PR_RECORD_KEY** is the same as the relationship between **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="91975-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="91975-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91975-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="91975-118">Protocol specifications</span></span>

<span data-ttu-id="91975-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91975-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91975-120">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="91975-120">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="91975-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91975-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91975-122">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="91975-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91975-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="91975-123">Header files</span></span>

<span data-ttu-id="91975-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="91975-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="91975-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="91975-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="91975-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="91975-126">Mapitags.h</span></span>
  
> <span data-ttu-id="91975-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="91975-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91975-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="91975-128">See also</span></span>



[<span data-ttu-id="91975-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="91975-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91975-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="91975-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91975-131">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="91975-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91975-132">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="91975-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

