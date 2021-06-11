---
title: Propiedad canónica PidTagAttachmentContactPhoto
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentContactPhoto
api_type:
- HeaderDef
ms.assetid: ea5b77b7-8440-4e54-abd2-c475138c8f63
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5d61289349306b763d13a9a2111c2cd02ff3937e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345769"
---
# <a name="pidtagattachmentcontactphoto-canonical-property"></a><span data-ttu-id="f842f-103">Propiedad canónica PidTagAttachmentContactPhoto</span><span class="sxs-lookup"><span data-stu-id="f842f-103">PidTagAttachmentContactPhoto Canonical Property</span></span>

  
  
<span data-ttu-id="f842f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f842f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f842f-105">Indica la existencia de datos adjuntos de una foto para un contacto.</span><span class="sxs-lookup"><span data-stu-id="f842f-105">Indicates the existence of a photo attachment for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f842f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f842f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f842f-107">PR_ATTACHMENT_CONTACTPHOTO</span><span class="sxs-lookup"><span data-stu-id="f842f-107">PR_ATTACHMENT_CONTACTPHOTO</span></span>  <br/> |
|<span data-ttu-id="f842f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f842f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f842f-109">0x7FFF</span><span class="sxs-lookup"><span data-stu-id="f842f-109">0x7FFF</span></span>  <br/> |
|<span data-ttu-id="f842f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f842f-110">Data type:</span></span>  <br/> |<span data-ttu-id="f842f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f842f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f842f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f842f-112">Area:</span></span>  <br/> |<span data-ttu-id="f842f-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="f842f-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f842f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f842f-114">Remarks</span></span>

<span data-ttu-id="f842f-115">El valor de esta propiedad debe establecerse en TRUE y solo debe haber un dato adjunto en un objeto Contact determinado.</span><span class="sxs-lookup"><span data-stu-id="f842f-115">This property's value must be set to TRUE, and there should only be one attachment on a given Contact object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f842f-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f842f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f842f-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="f842f-117">Protocol specifications</span></span>

<span data-ttu-id="f842f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f842f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f842f-119">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="f842f-119">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f842f-120">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f842f-120">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f842f-121">Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="f842f-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f842f-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f842f-122">Header files</span></span>

<span data-ttu-id="f842f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f842f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f842f-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f842f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f842f-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f842f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f842f-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f842f-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f842f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f842f-127">See also</span></span>



[<span data-ttu-id="f842f-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f842f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f842f-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="f842f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f842f-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f842f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f842f-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f842f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

