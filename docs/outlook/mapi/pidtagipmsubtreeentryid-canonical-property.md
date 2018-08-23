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
ms.openlocfilehash: ade74b13811445c39c73f778b6de49b67b59093b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587561"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="682f0-103">Propiedad canónica PidTagIpmSubtreeEntryId</span><span class="sxs-lookup"><span data-stu-id="682f0-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="682f0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="682f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="682f0-105">Contiene el identificador de entrada de la raíz del subárbol de la carpeta de mensajes interpersonales (IPM) en el árbol de carpetas del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="682f0-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="682f0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="682f0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="682f0-107">PR_IPM_SUBTREE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="682f0-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="682f0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="682f0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="682f0-109">0x35E0</span><span class="sxs-lookup"><span data-stu-id="682f0-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="682f0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="682f0-110">Data type:</span></span>  <br/> |<span data-ttu-id="682f0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="682f0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="682f0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="682f0-112">Area:</span></span>  <br/> |<span data-ttu-id="682f0-113">Folder</span><span class="sxs-lookup"><span data-stu-id="682f0-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="682f0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="682f0-114">Remarks</span></span>

<span data-ttu-id="682f0-115">Esta propiedad representa la raíz de la jerarquía IPM.</span><span class="sxs-lookup"><span data-stu-id="682f0-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="682f0-116">Los clientes IPM no deben mostrar todas las carpetas que no son las subcarpetas de la carpeta representada por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="682f0-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="682f0-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="682f0-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="682f0-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="682f0-118">Header files</span></span>

<span data-ttu-id="682f0-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="682f0-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="682f0-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="682f0-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="682f0-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="682f0-121">Mapitags.h</span></span>
  
> <span data-ttu-id="682f0-122">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="682f0-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="682f0-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="682f0-123">See also</span></span>



[<span data-ttu-id="682f0-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="682f0-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="682f0-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="682f0-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="682f0-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="682f0-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="682f0-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="682f0-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

