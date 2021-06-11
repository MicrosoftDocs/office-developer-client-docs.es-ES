---
title: Propiedad canónica PidTagViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7d261ac0e9aaf36f2333b04b45edfaf8e24fa30d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427314"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="2453d-103">Propiedad canónica PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="2453d-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="2453d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2453d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2453d-105">Contiene el identificador de entrada de la carpeta Vistas definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2453d-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2453d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2453d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2453d-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2453d-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="2453d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2453d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2453d-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="2453d-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="2453d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2453d-110">Data type:</span></span>  <br/> |<span data-ttu-id="2453d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2453d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2453d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2453d-112">Area:</span></span>  <br/> |<span data-ttu-id="2453d-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="2453d-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2453d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2453d-114">Remarks</span></span>

<span data-ttu-id="2453d-115">La carpeta de vista común contiene un conjunto predefinido de especificadores de vista estándar, mientras que la carpeta de vista contiene especificadores definidos por un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="2453d-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="2453d-116">Estas carpetas, que no están visibles en la jerarquía de mensajes interpersonales (IPM), pueden contener muchos especificadores de vista, cada uno almacenado como mensaje.</span><span class="sxs-lookup"><span data-stu-id="2453d-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="2453d-117">La aplicación cliente puede elegir combinar los dos conjuntos de especificadores y hacer que ambos estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="2453d-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2453d-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2453d-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2453d-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2453d-119">Header files</span></span>

<span data-ttu-id="2453d-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2453d-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="2453d-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2453d-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="2453d-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2453d-122">Mapitags.h</span></span>
  
> <span data-ttu-id="2453d-123">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2453d-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2453d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="2453d-124">See also</span></span>



[<span data-ttu-id="2453d-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2453d-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2453d-126">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2453d-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2453d-127">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2453d-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2453d-128">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2453d-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

