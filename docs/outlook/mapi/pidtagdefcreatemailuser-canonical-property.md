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
ms.openlocfilehash: 21fdff2aa713905a27a3d0cc5545ceb59f030378
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586861"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="8b08b-103">Propiedad canónica PidTagDefCreateMailuser</span><span class="sxs-lookup"><span data-stu-id="8b08b-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="8b08b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b08b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b08b-105">Contiene el identificador de entrada de plantilla para un objeto de usuario de mensajería de manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8b08b-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b08b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8b08b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b08b-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="8b08b-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="8b08b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8b08b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b08b-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="8b08b-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="8b08b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8b08b-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b08b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8b08b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8b08b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8b08b-112">Area:</span></span>  <br/> |<span data-ttu-id="8b08b-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="8b08b-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b08b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8b08b-114">Remarks</span></span>

<span data-ttu-id="8b08b-115">Las aplicaciones cliente usan esta propiedad para crear un objeto de usuario de mensajería dentro de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="8b08b-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="8b08b-116">Soporte técnico de la creación de entrada es opcional para los contenedores de la libreta de direcciones; aquellas que no lo admiten no se requieren para exponer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="8b08b-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="8b08b-117">Esta propiedad especifica una entrada que puede aparecer en la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) para los usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="8b08b-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="8b08b-118">Después de obtener el identificador, el cliente la utiliza en una llamada al método [IABContainer::CreateEntry](iabcontainer-createentry.md) .</span><span class="sxs-lookup"><span data-stu-id="8b08b-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="8b08b-119">La entrada representa la plantilla para el usuario de mensajería de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8b08b-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8b08b-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b08b-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8b08b-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8b08b-121">Header files</span></span>

<span data-ttu-id="8b08b-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b08b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b08b-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8b08b-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b08b-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8b08b-124">Mapitags.h</span></span>
  
> <span data-ttu-id="8b08b-125">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="8b08b-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b08b-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8b08b-126">See also</span></span>



[<span data-ttu-id="8b08b-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8b08b-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b08b-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8b08b-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b08b-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8b08b-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b08b-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8b08b-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

