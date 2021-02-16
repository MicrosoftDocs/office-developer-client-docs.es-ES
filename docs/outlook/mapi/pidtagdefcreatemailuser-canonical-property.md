---
title: Propiedad canónica PidTagDefCreateMailuser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cd09c85e4f44bbea29807d72a273ccf6980ca6df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407483"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="73648-103">Propiedad canónica PidTagDefCreateMailuser</span><span class="sxs-lookup"><span data-stu-id="73648-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="73648-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73648-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73648-105">Contiene el identificador de entrada de plantilla para un objeto de usuario de mensajería predeterminado.</span><span class="sxs-lookup"><span data-stu-id="73648-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73648-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="73648-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="73648-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="73648-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="73648-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="73648-108">Identifier:</span></span>  <br/> |<span data-ttu-id="73648-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="73648-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="73648-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="73648-110">Data type:</span></span>  <br/> |<span data-ttu-id="73648-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="73648-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="73648-112">Área:</span><span class="sxs-lookup"><span data-stu-id="73648-112">Area:</span></span>  <br/> |<span data-ttu-id="73648-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="73648-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73648-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73648-114">Remarks</span></span>

<span data-ttu-id="73648-115">Las aplicaciones cliente usan esta propiedad para crear un objeto de usuario de mensajería dentro de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="73648-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="73648-116">La compatibilidad con la creación de entradas es opcional para contenedores de libreta de direcciones; aquellos que no lo admiten no son necesarios para exponer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="73648-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="73648-117">Esta propiedad especifica una entrada que puede aparecer en la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) para los usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="73648-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="73648-118">Después de obtener el identificador, el cliente lo usa en una llamada al método [IABContainer::CreateEntry.](iabcontainer-createentry.md)</span><span class="sxs-lookup"><span data-stu-id="73648-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="73648-119">La entrada representa la plantilla para el usuario de mensajería predeterminado.</span><span class="sxs-lookup"><span data-stu-id="73648-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="73648-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="73648-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="73648-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="73648-121">Header files</span></span>

<span data-ttu-id="73648-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73648-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="73648-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="73648-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="73648-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="73648-124">Mapitags.h</span></span>
  
> <span data-ttu-id="73648-125">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="73648-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="73648-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="73648-126">See also</span></span>



[<span data-ttu-id="73648-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="73648-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="73648-128">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="73648-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="73648-129">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="73648-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="73648-130">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="73648-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

