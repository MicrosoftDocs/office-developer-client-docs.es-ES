---
title: Propiedad canónica PidTagPstPathHint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6415ddcec2823192967b8869b46b22b58b08ba5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437311"
---
# <a name="pidtagpstpathhint-canonical-property"></a><span data-ttu-id="896be-103">Propiedad canónica PidTagPstPathHint</span><span class="sxs-lookup"><span data-stu-id="896be-103">PidTagPstPathHint Canonical Property</span></span>

  
  
<span data-ttu-id="896be-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="896be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="896be-105">Proporciona el nombre de tabla de almacenamiento personal (archivo .pst), que el usuario puede editar, para el cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="896be-105">Provides the personal storage table (.pst file) name, which the user can edit, for the configuration dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="896be-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="896be-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="896be-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span><span class="sxs-lookup"><span data-stu-id="896be-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span></span>  <br/> |
|<span data-ttu-id="896be-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="896be-108">Identifier:</span></span>  <br/> |<span data-ttu-id="896be-109">0x6771</span><span class="sxs-lookup"><span data-stu-id="896be-109">0x6771</span></span>  <br/> |
|<span data-ttu-id="896be-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="896be-110">Data type:</span></span>  <br/> |<span data-ttu-id="896be-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="896be-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="896be-112">Área:</span><span class="sxs-lookup"><span data-stu-id="896be-112">Area:</span></span>  <br/> |<span data-ttu-id="896be-113">Tabla de almacenamiento personal (.pst) interna</span><span class="sxs-lookup"><span data-stu-id="896be-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="896be-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="896be-114">Remarks</span></span>

<span data-ttu-id="896be-115">Si **en su lugar se** usa la propiedad PR_PST_PATH ([PidTagPstPath](pidtagpstpath-canonical-property.md)), se abrirá el cuadro de diálogo de configuración, pero el usuario no podrá editar la ruta de acceso ni muchas otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="896be-115">If the **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) property is used instead, the configuration dialog box will open, but the user will not be allowed to edit the path and many other properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="896be-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="896be-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="896be-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="896be-117">Protocol specifications</span></span>

<span data-ttu-id="896be-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="896be-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="896be-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="896be-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="896be-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="896be-120">Header files</span></span>

<span data-ttu-id="896be-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="896be-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="896be-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="896be-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="896be-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="896be-123">Mapitags.h</span></span>
  
> <span data-ttu-id="896be-124">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="896be-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="896be-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="896be-125">See also</span></span>



[<span data-ttu-id="896be-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="896be-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="896be-127">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="896be-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="896be-128">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="896be-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="896be-129">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="896be-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

