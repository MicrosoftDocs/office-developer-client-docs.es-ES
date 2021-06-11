---
title: Propiedad canónica PidLidSpamOriginalFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSpamOriginalFolder
api_type:
- COM
ms.assetid: 45846fe3-7ab3-4019-98bb-fe615889c31c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 561008782e7c1ffb8bc71cf4e3bc17befe69bbca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331559"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a><span data-ttu-id="8ca52-103">Propiedad canónica PidLidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="8ca52-103">PidLidSpamOriginalFolder Canonical Property</span></span>

  
  
<span data-ttu-id="8ca52-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ca52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ca52-105">Indica en qué carpeta estaba un mensaje antes de filtrarlo a la carpeta de correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="8ca52-105">Indicates which folder a message was in before it was filtered into the junk email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ca52-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8ca52-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ca52-107">dispidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="8ca52-107">dispidSpamOriginalFolder</span></span>  <br/> |
|<span data-ttu-id="8ca52-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="8ca52-108">Property set:</span></span>  <br/> |<span data-ttu-id="8ca52-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="8ca52-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="8ca52-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="8ca52-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8ca52-111">0x0000859C</span><span class="sxs-lookup"><span data-stu-id="8ca52-111">0x0000859C</span></span>  <br/> |
|<span data-ttu-id="8ca52-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8ca52-112">Data type:</span></span>  <br/> |<span data-ttu-id="8ca52-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8ca52-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8ca52-114">Área:</span><span class="sxs-lookup"><span data-stu-id="8ca52-114">Area:</span></span>  <br/> |<span data-ttu-id="8ca52-115">Correo no deseado</span><span class="sxs-lookup"><span data-stu-id="8ca52-115">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ca52-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8ca52-116">Remarks</span></span>

<span data-ttu-id="8ca52-117">El valor de esta propiedad es **el EntryID** de la carpeta que contenía el mensaje antes de que se moviese.</span><span class="sxs-lookup"><span data-stu-id="8ca52-117">The value of this property is the **EntryID** of the folder that contained the message before it was moved.</span></span> <span data-ttu-id="8ca52-118">Esta propiedad debe establecerse cuando un mensaje se marca como correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="8ca52-118">This property should be set when a message is marked as spam.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8ca52-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ca52-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8ca52-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="8ca52-120">Protocol specifications</span></span>

<span data-ttu-id="8ca52-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ca52-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ca52-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="8ca52-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8ca52-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ca52-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ca52-124">Permite el control de listas de permitidos o bloqueados y la determinación de mensajes de correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="8ca52-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8ca52-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8ca52-125">Header files</span></span>

<span data-ttu-id="8ca52-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ca52-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ca52-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8ca52-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ca52-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ca52-128">See also</span></span>



[<span data-ttu-id="8ca52-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8ca52-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ca52-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8ca52-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ca52-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8ca52-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ca52-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8ca52-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

