---
title: Propiedad canónica PidTagExpiryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryTime
api_type:
- HeaderDef
ms.assetid: 6e4d4ee9-c6b1-4987-b02e-684c2af3d21c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8d6fa58e61dde30292487c95fb8a74d568a3bbeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316376"
---
# <a name="pidtagexpirytime-canonical-property"></a><span data-ttu-id="fcdb8-103">Propiedad canónica PidTagExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fcdb8-103">PidTagExpiryTime Canonical Property</span></span>

  
  
<span data-ttu-id="fcdb8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcdb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcdb8-105">Contiene la fecha y la hora en que el sistema de mensajería puede invalidar el contenido de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-105">Contains the date and time when the messaging system can invalidate the content of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcdb8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fcdb8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fcdb8-107">PR_EXPIRY_TIME</span><span class="sxs-lookup"><span data-stu-id="fcdb8-107">PR_EXPIRY_TIME</span></span>  <br/> |
|<span data-ttu-id="fcdb8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fcdb8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fcdb8-109">0x0015</span><span class="sxs-lookup"><span data-stu-id="fcdb8-109">0x0015</span></span>  <br/> |
|<span data-ttu-id="fcdb8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fcdb8-110">Data type:</span></span>  <br/> |<span data-ttu-id="fcdb8-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="fcdb8-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="fcdb8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fcdb8-112">Area:</span></span>  <br/> |<span data-ttu-id="fcdb8-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="fcdb8-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fcdb8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fcdb8-114">Remarks</span></span>

<span data-ttu-id="fcdb8-115">Esta propiedad se usa para dirigir al sistema de mensajería en el tratamiento de los mensajes interpersonales entregados.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-115">This property is used to direct the messaging system in handling delivered interpersonal messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fcdb8-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fcdb8-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fcdb8-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="fcdb8-117">Protocol specifications</span></span>

<span data-ttu-id="fcdb8-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcdb8-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcdb8-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fcdb8-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcdb8-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcdb8-121">Especifica las propiedades y operaciones permitidas en los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fcdb8-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fcdb8-122">Header files</span></span>

<span data-ttu-id="fcdb8-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fcdb8-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="fcdb8-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="fcdb8-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fcdb8-125">Mapitags.h</span></span>
  
> <span data-ttu-id="fcdb8-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fcdb8-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fcdb8-127">See also</span></span>



[<span data-ttu-id="fcdb8-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fcdb8-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fcdb8-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="fcdb8-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fcdb8-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fcdb8-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fcdb8-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="fcdb8-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

