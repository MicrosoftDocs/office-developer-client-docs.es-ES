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
ms.openlocfilehash: 4666a5837c9f9f2ceb209088929aa3d343eb02f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819505"
---
# <a name="pidtagexpirytime-canonical-property"></a><span data-ttu-id="7c1ed-103">Propiedad canónica PidTagExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7c1ed-103">PidTagExpiryTime Canonical Property</span></span>

  
  
<span data-ttu-id="7c1ed-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c1ed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c1ed-105">Contiene la fecha y la hora cuando el sistema de mensajería puede invalidar el contenido de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="7c1ed-105">Contains the date and time when the messaging system can invalidate the content of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c1ed-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7c1ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c1ed-107">PR_EXPIRY_TIME</span><span class="sxs-lookup"><span data-stu-id="7c1ed-107">PR_EXPIRY_TIME</span></span>  <br/> |
|<span data-ttu-id="7c1ed-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7c1ed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c1ed-109">0x0015</span><span class="sxs-lookup"><span data-stu-id="7c1ed-109">0x0015</span></span>  <br/> |
|<span data-ttu-id="7c1ed-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7c1ed-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c1ed-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7c1ed-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7c1ed-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7c1ed-112">Area:</span></span>  <br/> |<span data-ttu-id="7c1ed-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="7c1ed-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c1ed-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7c1ed-114">Remarks</span></span>

<span data-ttu-id="7c1ed-115">Esta propiedad se utiliza para dirigir que el sistema de mensajería en el tratamiento de entrega mensajes interpersonales.</span><span class="sxs-lookup"><span data-stu-id="7c1ed-115">This property is used to direct the messaging system in handling delivered interpersonal messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7c1ed-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c1ed-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7c1ed-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7c1ed-117">Protocol specifications</span></span>

<span data-ttu-id="7c1ed-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c1ed-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c1ed-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7c1ed-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7c1ed-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c1ed-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c1ed-121">Especifica las propiedades y operaciones que se permiten en mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7c1ed-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c1ed-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7c1ed-122">Header files</span></span>

<span data-ttu-id="7c1ed-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c1ed-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c1ed-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7c1ed-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c1ed-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7c1ed-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7c1ed-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7c1ed-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c1ed-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c1ed-127">See also</span></span>



[<span data-ttu-id="7c1ed-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7c1ed-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c1ed-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="7c1ed-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c1ed-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7c1ed-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c1ed-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="7c1ed-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

