---
title: Propiedad canónica PidTagIpmSubtreeEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSubtreeEntryId
api_type:
- HeaderDef
ms.assetid: 5763fc78-5192-4162-be27-4aadc7ed65bc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 815685696dfc93bb6241f608ca0157e87e758e7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327877"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="4e833-103">Propiedad canónica PidTagIpmSubtreeEntryId</span><span class="sxs-lookup"><span data-stu-id="4e833-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="4e833-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e833-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e833-105">Contiene el identificador de entrada de la raíz del subárbol de carpetas de mensajes interpersonales (IPM) en el árbol de carpetas del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4e833-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e833-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4e833-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e833-107">PR_IPM_SUBTREE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4e833-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="4e833-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4e833-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4e833-109">0x35E0</span><span class="sxs-lookup"><span data-stu-id="4e833-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="4e833-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4e833-110">Data type:</span></span>  <br/> |<span data-ttu-id="4e833-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4e833-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4e833-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4e833-112">Area:</span></span>  <br/> |<span data-ttu-id="4e833-113">Folder</span><span class="sxs-lookup"><span data-stu-id="4e833-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e833-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e833-114">Remarks</span></span>

<span data-ttu-id="4e833-115">Esta propiedad representa la raíz de la jerarquía de IPM.</span><span class="sxs-lookup"><span data-stu-id="4e833-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="4e833-116">Los clientes IPM no deben mostrar ninguna carpeta que no sea una subcarpeta de la carpeta representada por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4e833-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4e833-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e833-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4e833-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4e833-118">Header files</span></span>

<span data-ttu-id="4e833-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4e833-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e833-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4e833-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4e833-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4e833-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4e833-122">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4e833-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e833-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e833-123">See also</span></span>



[<span data-ttu-id="4e833-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4e833-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e833-125">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="4e833-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e833-126">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4e833-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e833-127">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4e833-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

