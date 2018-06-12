---
title: Propiedad canónico PidTagIpmSubtreeEntryId
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 9635c06ffa5638e370312e3b2b29e0c98161a766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819651"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="9b545-103">Propiedad canónico PidTagIpmSubtreeEntryId</span><span class="sxs-lookup"><span data-stu-id="9b545-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="9b545-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9b545-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9b545-105">Contiene el identificador de entrada de la raíz del subárbol de la carpeta de mensajes interpersonales (IPM) en el árbol de carpetas del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9b545-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b545-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9b545-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9b545-107">PR_IPM_SUBTREE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9b545-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="9b545-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9b545-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9b545-109">0x35E0</span><span class="sxs-lookup"><span data-stu-id="9b545-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="9b545-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9b545-110">Data type:</span></span>  <br/> |<span data-ttu-id="9b545-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9b545-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9b545-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9b545-112">Area:</span></span>  <br/> |<span data-ttu-id="9b545-113">Carpeta</span><span class="sxs-lookup"><span data-stu-id="9b545-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b545-114">Notas</span><span class="sxs-lookup"><span data-stu-id="9b545-114">Remarks</span></span>

<span data-ttu-id="9b545-115">Esta propiedad representa la raíz de la jerarquía IPM.</span><span class="sxs-lookup"><span data-stu-id="9b545-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="9b545-116">Los clientes IPM no deben mostrar todas las carpetas que no son las subcarpetas de la carpeta representada por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9b545-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9b545-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b545-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9b545-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9b545-118">Header files</span></span>

<span data-ttu-id="9b545-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9b545-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b545-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9b545-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="9b545-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9b545-121">Mapitags.h</span></span>
  
> <span data-ttu-id="9b545-122">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9b545-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b545-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="9b545-123">See also</span></span>



[<span data-ttu-id="9b545-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9b545-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b545-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9b545-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b545-126">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="9b545-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b545-127">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9b545-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

