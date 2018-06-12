---
title: Propiedad canónico PidTagViewsEntryId
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 1980e3bd815b370f125f4449dd7b7f340a7dcb9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820411"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="c927b-103">Propiedad canónico PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="c927b-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c927b-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c927b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c927b-105">Contiene el identificador de entrada de la carpeta de las vistas definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c927b-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c927b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c927b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c927b-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c927b-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c927b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c927b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c927b-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="c927b-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="c927b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c927b-110">Data type:</span></span>  <br/> |<span data-ttu-id="c927b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c927b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c927b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c927b-112">Area:</span></span>  <br/> |<span data-ttu-id="c927b-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="c927b-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c927b-114">Notas</span><span class="sxs-lookup"><span data-stu-id="c927b-114">Remarks</span></span>

<span data-ttu-id="c927b-115">La carpeta de vista comunes contiene un conjunto predefinido de especificadores de vista estándar, mientras que la carpeta de la vista contiene especificadores definidos por un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="c927b-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="c927b-116">Estas carpetas, que no están visibles en la jerarquía de mensajes interpersonales (IPM), pueden contener muchos especificadores de vista, cada uno de ellos que se almacene como un mensaje.</span><span class="sxs-lookup"><span data-stu-id="c927b-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="c927b-117">La aplicación cliente puede elegir combinar los dos conjuntos de especificadores y que estén ambos disponibles.</span><span class="sxs-lookup"><span data-stu-id="c927b-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c927b-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c927b-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c927b-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c927b-119">Header files</span></span>

<span data-ttu-id="c927b-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c927b-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="c927b-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c927b-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="c927b-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c927b-122">Mapitags.h</span></span>
  
> <span data-ttu-id="c927b-123">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c927b-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c927b-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="c927b-124">See also</span></span>



[<span data-ttu-id="c927b-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c927b-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c927b-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c927b-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c927b-127">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="c927b-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c927b-128">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c927b-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

