---
title: Propiedad canónica PidTagExpiryNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryNumber
api_type:
- HeaderDef
ms.assetid: 644e8d3d-1792-4417-95a1-e978d0e6cd8e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da90347f5aacdb2fcac8547eddd5b89a0a44820d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385826"
---
# <a name="pidtagexpirynumber-canonical-property"></a><span data-ttu-id="74f28-103">Propiedad canónica PidTagExpiryNumber</span><span class="sxs-lookup"><span data-stu-id="74f28-103">PidTagExpiryNumber Canonical Property</span></span>

  
  
<span data-ttu-id="74f28-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74f28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74f28-105">Define el tiempo de envío de caducidad junto con la propiedad **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="74f28-105">Defines the expiry send time in conjunction with the **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74f28-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="74f28-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74f28-107">PR_EXPIRY_NUMBER</span><span class="sxs-lookup"><span data-stu-id="74f28-107">PR_EXPIRY_NUMBER</span></span>  <br/> |
|<span data-ttu-id="74f28-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="74f28-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74f28-109">0x3FED</span><span class="sxs-lookup"><span data-stu-id="74f28-109">0x3FED</span></span>  <br/> |
|<span data-ttu-id="74f28-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="74f28-110">Data type:</span></span>  <br/> |<span data-ttu-id="74f28-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="74f28-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="74f28-112">Área:</span><span class="sxs-lookup"><span data-stu-id="74f28-112">Area:</span></span>  <br/> |<span data-ttu-id="74f28-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="74f28-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74f28-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74f28-114">Remarks</span></span>

<span data-ttu-id="74f28-115">Valor de esta propiedad debe establecerse entre 0 y 999 ambos inclusive, si está presente.</span><span class="sxs-lookup"><span data-stu-id="74f28-115">This property's value must be set between 0 and 999 inclusive, if it is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="74f28-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="74f28-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74f28-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="74f28-117">Protocol specifications</span></span>

<span data-ttu-id="74f28-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74f28-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74f28-119">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="74f28-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="74f28-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="74f28-120">Header files</span></span>

<span data-ttu-id="74f28-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74f28-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="74f28-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="74f28-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="74f28-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="74f28-123">Mapitags.h</span></span>
  
> <span data-ttu-id="74f28-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="74f28-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74f28-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="74f28-125">See also</span></span>



[<span data-ttu-id="74f28-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="74f28-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74f28-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="74f28-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74f28-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="74f28-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74f28-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="74f28-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

