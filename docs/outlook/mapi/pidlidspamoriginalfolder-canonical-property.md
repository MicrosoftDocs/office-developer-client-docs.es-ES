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
# <a name="pidlidspamoriginalfolder-canonical-property"></a><span data-ttu-id="1c14a-103">Propiedad canónica PidLidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="1c14a-103">PidLidSpamOriginalFolder Canonical Property</span></span>

  
  
<span data-ttu-id="1c14a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c14a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c14a-105">Indica la carpeta en la que se encontraba un mensaje antes de que se filtrara en la carpeta de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="1c14a-105">Indicates which folder a message was in before it was filtered into the junk email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1c14a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1c14a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c14a-107">dispidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="1c14a-107">dispidSpamOriginalFolder</span></span>  <br/> |
|<span data-ttu-id="1c14a-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="1c14a-108">Property set:</span></span>  <br/> |<span data-ttu-id="1c14a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="1c14a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="1c14a-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="1c14a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1c14a-111">0x0000859C</span><span class="sxs-lookup"><span data-stu-id="1c14a-111">0x0000859C</span></span>  <br/> |
|<span data-ttu-id="1c14a-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1c14a-112">Data type:</span></span>  <br/> |<span data-ttu-id="1c14a-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1c14a-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1c14a-114">Área:</span><span class="sxs-lookup"><span data-stu-id="1c14a-114">Area:</span></span>  <br/> |<span data-ttu-id="1c14a-115">Correo no deseado</span><span class="sxs-lookup"><span data-stu-id="1c14a-115">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c14a-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c14a-116">Remarks</span></span>

<span data-ttu-id="1c14a-117">El valor de esta propiedad es el **EntryID** de la carpeta que contenía el mensaje antes de que se moviera.</span><span class="sxs-lookup"><span data-stu-id="1c14a-117">The value of this property is the **EntryID** of the folder that contained the message before it was moved.</span></span> <span data-ttu-id="1c14a-118">Esta propiedad debe establecerse cuando un mensaje se marca como correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="1c14a-118">This property should be set when a message is marked as spam.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1c14a-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c14a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1c14a-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1c14a-120">Protocol specifications</span></span>

<span data-ttu-id="1c14a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c14a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c14a-122">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1c14a-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1c14a-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c14a-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c14a-124">Habilita el control de las listas de permitidos y bloqueados y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="1c14a-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1c14a-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1c14a-125">Header files</span></span>

<span data-ttu-id="1c14a-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1c14a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c14a-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1c14a-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c14a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c14a-128">See also</span></span>



[<span data-ttu-id="1c14a-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1c14a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c14a-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="1c14a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c14a-131">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1c14a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c14a-132">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="1c14a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

