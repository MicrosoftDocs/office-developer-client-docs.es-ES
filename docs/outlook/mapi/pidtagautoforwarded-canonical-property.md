---
title: Propiedad canónica PidTagAutoForwarded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAutoForwarded
api_type:
- HeaderDef
ms.assetid: 1ba40cc2-ba27-4d75-9682-c536cf3a0d58
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 25d1bb121df6470f5038a2106587e3f5b37f6bb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326617"
---
# <a name="pidtagautoforwarded-canonical-property"></a><span data-ttu-id="69816-103">Propiedad canónica PidTagAutoForwarded</span><span class="sxs-lookup"><span data-stu-id="69816-103">PidTagAutoForwarded Canonical Property</span></span>

  
  
<span data-ttu-id="69816-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69816-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69816-105">Contiene TRUE si el cliente solicita un campo de encabezado X-MS-Exchange-Organization-AutoForwarded.</span><span class="sxs-lookup"><span data-stu-id="69816-105">Contains TRUE if the client requests an X-MS-Exchange-Organization-AutoForwarded header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69816-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="69816-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69816-107">PR_AUTO_FORWARDED</span><span class="sxs-lookup"><span data-stu-id="69816-107">PR_AUTO_FORWARDED</span></span>  <br/> |
|<span data-ttu-id="69816-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="69816-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69816-109">0x0005</span><span class="sxs-lookup"><span data-stu-id="69816-109">0x0005</span></span>  <br/> |
|<span data-ttu-id="69816-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="69816-110">Data type:</span></span>  <br/> |<span data-ttu-id="69816-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="69816-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="69816-112">Área:</span><span class="sxs-lookup"><span data-stu-id="69816-112">Area:</span></span>  <br/> |<span data-ttu-id="69816-113">Informes generales</span><span class="sxs-lookup"><span data-stu-id="69816-113">General reporting</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69816-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69816-114">Remarks</span></span>

<span data-ttu-id="69816-115">Si esta propiedad se establece en FALSE o no se usa, no se creará ningún campo de encabezado X-MS-Exchange-Organization-AutoForwarded.</span><span class="sxs-lookup"><span data-stu-id="69816-115">If this property is set to FALSE or not used, no X-MS-Exchange-Organization-AutoForwarded header field will be created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="69816-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="69816-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69816-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="69816-117">Protocol specifications</span></span>

<span data-ttu-id="69816-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69816-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69816-119">Define cada propiedad que se usa en los objetos descritos por documentos con prefijo MS-OXO.</span><span class="sxs-lookup"><span data-stu-id="69816-119">Defines each property that is used in the objects that are described by MS-OXO-prefixed documents.</span></span>
    
<span data-ttu-id="69816-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69816-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69816-121">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="69816-121">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69816-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="69816-122">Header files</span></span>

<span data-ttu-id="69816-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69816-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="69816-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="69816-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="69816-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="69816-125">Mapitags.h</span></span>
  
> <span data-ttu-id="69816-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="69816-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69816-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="69816-127">See also</span></span>



[<span data-ttu-id="69816-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="69816-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69816-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="69816-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69816-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="69816-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69816-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="69816-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

