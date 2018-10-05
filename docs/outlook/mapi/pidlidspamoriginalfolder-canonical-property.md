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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387849"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a><span data-ttu-id="c52e7-103">Propiedad canónica PidLidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="c52e7-103">PidLidSpamOriginalFolder Canonical Property</span></span>

  
  
<span data-ttu-id="c52e7-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c52e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c52e7-105">Indica qué carpeta un mensaje estaba en antes de que se ha filtrado en la carpeta de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="c52e7-105">Indicates which folder a message was in before it was filtered into the junk email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c52e7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c52e7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c52e7-107">dispidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="c52e7-107">dispidSpamOriginalFolder</span></span>  <br/> |
|<span data-ttu-id="c52e7-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="c52e7-108">Property set:</span></span>  <br/> |<span data-ttu-id="c52e7-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c52e7-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c52e7-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="c52e7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c52e7-111">0x0000859C</span><span class="sxs-lookup"><span data-stu-id="c52e7-111">0x0000859C</span></span>  <br/> |
|<span data-ttu-id="c52e7-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c52e7-112">Data type:</span></span>  <br/> |<span data-ttu-id="c52e7-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c52e7-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c52e7-114">Área:</span><span class="sxs-lookup"><span data-stu-id="c52e7-114">Area:</span></span>  <br/> |<span data-ttu-id="c52e7-115">Spam</span><span class="sxs-lookup"><span data-stu-id="c52e7-115">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c52e7-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c52e7-116">Remarks</span></span>

<span data-ttu-id="c52e7-117">El valor de esta propiedad es la **propiedad EntryID** de la carpeta que contenía el mensaje antes de que se ha movido.</span><span class="sxs-lookup"><span data-stu-id="c52e7-117">The value of this property is the **EntryID** of the folder that contained the message before it was moved.</span></span> <span data-ttu-id="c52e7-118">Esta propiedad debe establecerse cuando se marca un mensaje como correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="c52e7-118">This property should be set when a message is marked as spam.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c52e7-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c52e7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c52e7-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c52e7-120">Protocol specifications</span></span>

<span data-ttu-id="c52e7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c52e7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c52e7-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c52e7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c52e7-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c52e7-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c52e7-124">Permite la manipulación de las listas Permitir o bloquear y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="c52e7-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c52e7-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c52e7-125">Header files</span></span>

<span data-ttu-id="c52e7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c52e7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c52e7-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c52e7-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c52e7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c52e7-128">See also</span></span>



[<span data-ttu-id="c52e7-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c52e7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c52e7-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c52e7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c52e7-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c52e7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c52e7-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c52e7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

