---
title: Propiedad canónica PidTagCommonViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCommonViewsEntryId
api_type:
- HeaderDef
ms.assetid: cd9e6a46-2112-4663-891e-5e57b22c0950
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e22b8905901f16606614ac918896f3afe0093752
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437346"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a><span data-ttu-id="ba1ac-103">Propiedad canónica PidTagCommonViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="ba1ac-103">PidTagCommonViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="ba1ac-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba1ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba1ac-105">Contiene el identificador de entrada de la carpeta vista común predefinida.</span><span class="sxs-lookup"><span data-stu-id="ba1ac-105">Contains the entry identifier of the predefined common view folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba1ac-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ba1ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ba1ac-107">PR_COMMON_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ba1ac-107">PR_COMMON_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="ba1ac-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ba1ac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ba1ac-109">0x35E6</span><span class="sxs-lookup"><span data-stu-id="ba1ac-109">0x35E6</span></span>  <br/> |
|<span data-ttu-id="ba1ac-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ba1ac-110">Data type:</span></span>  <br/> |<span data-ttu-id="ba1ac-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ba1ac-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ba1ac-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ba1ac-112">Area:</span></span>  <br/> |<span data-ttu-id="ba1ac-113">Aplicación de Outlook</span><span class="sxs-lookup"><span data-stu-id="ba1ac-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba1ac-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ba1ac-114">Remarks</span></span>

<span data-ttu-id="ba1ac-115">La carpeta vista común contiene un conjunto predefinido de especificadores de vista estándar, mientras que la carpeta de vista contiene los especificadores definidos por un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ba1ac-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="ba1ac-116">Estas carpetas, que no están visibles en la jerarquía de mensajes interpersonales (IPM), pueden contener muchos especificadores de vista, cada uno de los cuales se almacena como un mensaje.</span><span class="sxs-lookup"><span data-stu-id="ba1ac-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="ba1ac-117">Una aplicación cliente puede optar por combinar los dos conjuntos de especificadores y hacer que estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="ba1ac-117">A client application can choose to merge the two sets of specifiers and make them both available.</span></span> 
  
<span data-ttu-id="ba1ac-118">Para obtener más información acerca de las vistas, consulte [View folders](mapi-view-folders.md).</span><span class="sxs-lookup"><span data-stu-id="ba1ac-118">For more information on views, see [View Folders](mapi-view-folders.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ba1ac-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba1ac-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ba1ac-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ba1ac-120">Header files</span></span>

<span data-ttu-id="ba1ac-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ba1ac-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="ba1ac-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ba1ac-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="ba1ac-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ba1ac-123">Mapitags.h</span></span>
  
> <span data-ttu-id="ba1ac-124">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ba1ac-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ba1ac-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="ba1ac-125">See also</span></span>



[<span data-ttu-id="ba1ac-126">Propiedad canónica PidTagDefaultViewEntryId</span><span class="sxs-lookup"><span data-stu-id="ba1ac-126">PidTagDefaultViewEntryId Canonical Property</span></span>](pidtagdefaultviewentryid-canonical-property.md)
  
[<span data-ttu-id="ba1ac-127">Propiedad canónica PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="ba1ac-127">PidTagViewsEntryId Canonical Property</span></span>](pidtagviewsentryid-canonical-property.md)


[<span data-ttu-id="ba1ac-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ba1ac-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ba1ac-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="ba1ac-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ba1ac-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ba1ac-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ba1ac-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ba1ac-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

