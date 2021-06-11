---
title: Propiedad canónica PidTagSubfolders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubfolders
api_type:
- COM
ms.assetid: b456b07b-4d83-46bf-a305-4f322ea7dbd1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8de14542c0d2a4e6d95fb4258697b827f82b8d06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339252"
---
# <a name="pidtagsubfolders-canonical-property"></a><span data-ttu-id="2370d-103">Propiedad canónica PidTagSubfolders</span><span class="sxs-lookup"><span data-stu-id="2370d-103">PidTagSubfolders Canonical Property</span></span>

  
  
<span data-ttu-id="2370d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2370d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2370d-105">Contiene TRUE si una carpeta contiene subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="2370d-105">Contains TRUE if a folder contains subfolders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2370d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2370d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2370d-107">PR_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="2370d-107">PR_SUBFOLDERS</span></span>  <br/> |
|<span data-ttu-id="2370d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2370d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2370d-109">0x360A</span><span class="sxs-lookup"><span data-stu-id="2370d-109">0x360A</span></span>  <br/> |
|<span data-ttu-id="2370d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2370d-110">Data type:</span></span>  <br/> |<span data-ttu-id="2370d-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2370d-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2370d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2370d-112">Area:</span></span>  <br/> |<span data-ttu-id="2370d-113">Contenedor MAPI</span><span class="sxs-lookup"><span data-stu-id="2370d-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2370d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2370d-114">Remarks</span></span>

<span data-ttu-id="2370d-115">Los almacenes de mensajes deben proporcionar esta propiedad para todas las carpetas.</span><span class="sxs-lookup"><span data-stu-id="2370d-115">Message stores must supply this property for all folders.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2370d-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2370d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2370d-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="2370d-117">Protocol specifications</span></span>

<span data-ttu-id="2370d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2370d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2370d-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="2370d-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2370d-120">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2370d-120">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2370d-121">Controla las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="2370d-121">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2370d-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2370d-122">Header files</span></span>

<span data-ttu-id="2370d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2370d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="2370d-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2370d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="2370d-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2370d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="2370d-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2370d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2370d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2370d-127">See also</span></span>



[<span data-ttu-id="2370d-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2370d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2370d-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2370d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2370d-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2370d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2370d-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2370d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

