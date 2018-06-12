---
title: Propiedad canónico PidTagAutoForwarded
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 8303a60ee0d61a56c79fadf471bc6111fcbde7d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819264"
---
# <a name="pidtagautoforwarded-canonical-property"></a><span data-ttu-id="b6b94-103">Propiedad canónico PidTagAutoForwarded</span><span class="sxs-lookup"><span data-stu-id="b6b94-103">PidTagAutoForwarded Canonical Property</span></span>

  
  
<span data-ttu-id="b6b94-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6b94-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6b94-105">Contiene TRUE si el cliente solicita un campo de encabezado X-MS-Exchange-organización-AutoForwarded.</span><span class="sxs-lookup"><span data-stu-id="b6b94-105">Contains TRUE if the client requests an X-MS-Exchange-Organization-AutoForwarded header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6b94-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b6b94-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6b94-107">PR_AUTO_FORWARDED</span><span class="sxs-lookup"><span data-stu-id="b6b94-107">PR_AUTO_FORWARDED</span></span>  <br/> |
|<span data-ttu-id="b6b94-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b6b94-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6b94-109">0x0005</span><span class="sxs-lookup"><span data-stu-id="b6b94-109">0x0005</span></span>  <br/> |
|<span data-ttu-id="b6b94-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b6b94-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6b94-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b6b94-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b6b94-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b6b94-112">Area:</span></span>  <br/> |<span data-ttu-id="b6b94-113">Informe de errores general</span><span class="sxs-lookup"><span data-stu-id="b6b94-113">General reporting</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6b94-114">Notas</span><span class="sxs-lookup"><span data-stu-id="b6b94-114">Remarks</span></span>

<span data-ttu-id="b6b94-115">Si esta propiedad está establecida en FALSE o no se utilizan, no se creará ningún campo de encabezado X-MS-Exchange-organización-AutoForwarded.</span><span class="sxs-lookup"><span data-stu-id="b6b94-115">If this property is set to FALSE or not used, no X-MS-Exchange-Organization-AutoForwarded header field will be created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b6b94-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6b94-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b6b94-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b6b94-117">Protocol specifications</span></span>

<span data-ttu-id="b6b94-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6b94-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6b94-119">Define cada propiedad que se usa en los objetos que se describen en los documentos como prefijo MS-Oxobenc.</span><span class="sxs-lookup"><span data-stu-id="b6b94-119">Defines each property that is used in the objects that are described by MS-OXO-prefixed documents.</span></span>
    
<span data-ttu-id="b6b94-120">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6b94-120">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6b94-121">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b6b94-121">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b6b94-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b6b94-122">Header files</span></span>

<span data-ttu-id="b6b94-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6b94-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6b94-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b6b94-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6b94-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b6b94-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b6b94-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b6b94-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6b94-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="b6b94-127">See also</span></span>



[<span data-ttu-id="b6b94-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b6b94-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6b94-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b6b94-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6b94-130">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="b6b94-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6b94-131">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b6b94-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

