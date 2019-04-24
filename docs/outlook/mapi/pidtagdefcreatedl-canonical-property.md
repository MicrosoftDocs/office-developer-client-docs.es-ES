---
title: Propiedad canónica PidTagDefCreateDl
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ff5d35104e9effc27c405b716cb61cf4643677b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359958"
---
# <a name="pidtagdefcreatedl-canonical-property"></a><span data-ttu-id="90730-103">Propiedad canónica PidTagDefCreateDl</span><span class="sxs-lookup"><span data-stu-id="90730-103">PidTagDefCreateDl Canonical Property</span></span>

  
  
<span data-ttu-id="90730-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90730-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90730-105">Contiene el identificador de la entrada de plantilla para una lista de distribución predeterminada.</span><span class="sxs-lookup"><span data-stu-id="90730-105">Contains the template entry identifier for a default distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="90730-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="90730-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90730-107">PR_DEF_CREATE_DL</span><span class="sxs-lookup"><span data-stu-id="90730-107">PR_DEF_CREATE_DL</span></span>  <br/> |
|<span data-ttu-id="90730-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="90730-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90730-109">0x3611</span><span class="sxs-lookup"><span data-stu-id="90730-109">0x3611</span></span>  <br/> |
|<span data-ttu-id="90730-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="90730-110">Data type:</span></span>  <br/> |<span data-ttu-id="90730-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="90730-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="90730-112">Área:</span><span class="sxs-lookup"><span data-stu-id="90730-112">Area:</span></span>  <br/> |<span data-ttu-id="90730-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="90730-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90730-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="90730-114">Remarks</span></span>

<span data-ttu-id="90730-115">Las aplicaciones cliente usan esta propiedad para crear una lista de distribución dentro de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="90730-115">Client applications use this property to create a distribution list within a container.</span></span> <span data-ttu-id="90730-116">La compatibilidad con la creación de entradas es opcional para los contenedores de la libreta de direcciones; los usuarios que no la admitan no necesitan exponer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="90730-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="90730-117">Esta propiedad especifica una entrada que puede aparecer en la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) de las listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="90730-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for distribution lists.</span></span> <span data-ttu-id="90730-118">Después de obtener el identificador, el cliente lo usa en una llamada al método [IABContainer:: CreateEntry](iabcontainer-createentry.md) .</span><span class="sxs-lookup"><span data-stu-id="90730-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="90730-119">La entrada representa la plantilla de la lista de distribución predeterminada.</span><span class="sxs-lookup"><span data-stu-id="90730-119">The entry represents the template for the default distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="90730-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="90730-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="90730-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="90730-121">Header files</span></span>

<span data-ttu-id="90730-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="90730-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="90730-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="90730-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="90730-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="90730-124">Mapitags.h</span></span>
  
> <span data-ttu-id="90730-125">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="90730-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90730-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="90730-126">See also</span></span>



[<span data-ttu-id="90730-127">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="90730-127">IABLogon::CompareEntryIDs</span></span>](iablogon-compareentryids.md)


[<span data-ttu-id="90730-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="90730-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90730-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="90730-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90730-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="90730-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90730-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="90730-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

