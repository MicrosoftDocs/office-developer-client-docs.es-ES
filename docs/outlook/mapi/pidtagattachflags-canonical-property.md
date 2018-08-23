---
title: Propiedad canónica PidTagAttachFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bf92e62dc572a81b6e0aab4cb1b0fc8afe97800d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573099"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="496e0-103">Propiedad canónica PidTagAttachFlags</span><span class="sxs-lookup"><span data-stu-id="496e0-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="496e0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="496e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="496e0-105">Contiene una máscara de bits de indicadores para los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="496e0-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="496e0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="496e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="496e0-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="496e0-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="496e0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="496e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="496e0-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="496e0-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="496e0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="496e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="496e0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="496e0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="496e0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="496e0-112">Area:</span></span>  <br/> |<span data-ttu-id="496e0-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="496e0-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="496e0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="496e0-114">Remarks</span></span>

<span data-ttu-id="496e0-115">Esta propiedad se utiliza para compatibilidad con MHTML.</span><span class="sxs-lookup"><span data-stu-id="496e0-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="496e0-116">La máscara de bits **PR_ATTACH_FLAGS** se pueden establecer uno o varios de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="496e0-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="496e0-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="496e0-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="496e0-118">Indica que este archivo adjunto no está disponible para las aplicaciones de representación de HTML y se debe omitir en Extensiones multipropósito extensiones de correo Internet (MIME) de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="496e0-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="496e0-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="496e0-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="496e0-120">Indica que este archivo adjunto no está disponible para las aplicaciones de representación en formato de texto enriquecido (RTF) y se debe omitir por MAPI.</span><span class="sxs-lookup"><span data-stu-id="496e0-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="496e0-121">Si la propiedad **PR_ATTACH_FLAGS** es cero o está ausente, los datos adjuntos están que va a procesar todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="496e0-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="496e0-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="496e0-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="496e0-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="496e0-123">Protocol specifications</span></span>

<span data-ttu-id="496e0-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="496e0-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="496e0-125">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="496e0-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="496e0-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="496e0-126">Header files</span></span>

<span data-ttu-id="496e0-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="496e0-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="496e0-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="496e0-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="496e0-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="496e0-129">Mapitags.h</span></span>
  
> <span data-ttu-id="496e0-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="496e0-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="496e0-131">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="496e0-131">See also</span></span>



[<span data-ttu-id="496e0-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="496e0-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="496e0-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="496e0-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="496e0-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="496e0-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="496e0-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="496e0-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

