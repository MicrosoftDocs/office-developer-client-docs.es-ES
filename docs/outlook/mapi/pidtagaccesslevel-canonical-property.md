---
title: Propiedad canónica PidTagAccessLevel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccessLevel
api_type:
- HeaderDef
ms.assetid: 8f7119c7-ffc3-47cf-aa1b-b4e56bcc5a24
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5138f5d255f6a90d2891fe2cf5ce92513463fa31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332000"
---
# <a name="pidtagaccesslevel-canonical-property"></a><span data-ttu-id="04103-103">Propiedad canónica PidTagAccessLevel</span><span class="sxs-lookup"><span data-stu-id="04103-103">PidTagAccessLevel Canonical Property</span></span>

  
  
<span data-ttu-id="04103-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04103-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04103-105">Indica el nivel de acceso del cliente al objeto.</span><span class="sxs-lookup"><span data-stu-id="04103-105">Indicates the client's access level to the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="04103-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="04103-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="04103-107">PR_ACCESS_LEVEL</span><span class="sxs-lookup"><span data-stu-id="04103-107">PR_ACCESS_LEVEL</span></span>  <br/> |
|<span data-ttu-id="04103-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="04103-108">Identifier:</span></span>  <br/> |<span data-ttu-id="04103-109">0x0FF7</span><span class="sxs-lookup"><span data-stu-id="04103-109">0x0FF7</span></span>  <br/> |
|<span data-ttu-id="04103-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="04103-110">Data type:</span></span>  <br/> |<span data-ttu-id="04103-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="04103-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="04103-112">Área:</span><span class="sxs-lookup"><span data-stu-id="04103-112">Area:</span></span>  <br/> |<span data-ttu-id="04103-113">Propiedades del control de acceso</span><span class="sxs-lookup"><span data-stu-id="04103-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04103-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04103-114">Remarks</span></span>

<span data-ttu-id="04103-115">Esta propiedad es de solo lectura para el cliente.</span><span class="sxs-lookup"><span data-stu-id="04103-115">This property is read-only for the client.</span></span> <span data-ttu-id="04103-116">Debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="04103-116">It must be one of the following values:</span></span>
  
|<span data-ttu-id="04103-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="04103-117">**Value**</span></span>|<span data-ttu-id="04103-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="04103-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="04103-119">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04103-119">0x00000000</span></span>  <br/> |<span data-ttu-id="04103-120">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="04103-120">Read-Only</span></span>  <br/> |
|<span data-ttu-id="04103-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="04103-121">0x00000001</span></span>  <br/> |<span data-ttu-id="04103-122">Modify</span><span class="sxs-lookup"><span data-stu-id="04103-122">Modify</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="04103-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="04103-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="04103-124">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="04103-124">Protocol specifications</span></span>

<span data-ttu-id="04103-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04103-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04103-126">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="04103-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="04103-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04103-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04103-128">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="04103-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="04103-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="04103-129">Header files</span></span>

<span data-ttu-id="04103-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="04103-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="04103-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="04103-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="04103-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="04103-132">Mapitags.h</span></span>
  
> <span data-ttu-id="04103-133">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="04103-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04103-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="04103-134">See also</span></span>



[<span data-ttu-id="04103-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="04103-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="04103-136">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="04103-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="04103-137">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="04103-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="04103-138">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="04103-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

