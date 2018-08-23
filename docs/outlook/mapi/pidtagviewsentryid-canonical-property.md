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
ms.openlocfilehash: 73ed7213ea2bd5079458ccc237b65590f06e8d53
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586266"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="86dec-103">Propiedad canónica PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="86dec-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="86dec-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86dec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86dec-105">Contiene el identificador de entrada de la carpeta de las vistas definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="86dec-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86dec-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="86dec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="86dec-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="86dec-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="86dec-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="86dec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="86dec-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="86dec-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="86dec-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="86dec-110">Data type:</span></span>  <br/> |<span data-ttu-id="86dec-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="86dec-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="86dec-112">Área:</span><span class="sxs-lookup"><span data-stu-id="86dec-112">Area:</span></span>  <br/> |<span data-ttu-id="86dec-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="86dec-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86dec-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86dec-114">Remarks</span></span>

<span data-ttu-id="86dec-115">La carpeta de vista comunes contiene un conjunto predefinido de especificadores de vista estándar, mientras que la carpeta de la vista contiene especificadores definidos por un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="86dec-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="86dec-116">Estas carpetas, que no están visibles en la jerarquía de mensajes interpersonales (IPM), pueden contener muchos especificadores de vista, cada uno de ellos que se almacene como un mensaje.</span><span class="sxs-lookup"><span data-stu-id="86dec-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="86dec-117">La aplicación cliente puede elegir combinar los dos conjuntos de especificadores y que estén ambos disponibles.</span><span class="sxs-lookup"><span data-stu-id="86dec-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="86dec-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="86dec-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="86dec-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="86dec-119">Header files</span></span>

<span data-ttu-id="86dec-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86dec-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="86dec-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="86dec-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="86dec-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="86dec-122">Mapitags.h</span></span>
  
> <span data-ttu-id="86dec-123">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="86dec-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86dec-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="86dec-124">See also</span></span>



[<span data-ttu-id="86dec-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="86dec-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="86dec-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="86dec-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="86dec-127">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="86dec-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="86dec-128">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="86dec-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

