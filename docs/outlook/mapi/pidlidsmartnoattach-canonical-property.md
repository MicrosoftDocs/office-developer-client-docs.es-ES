---
title: Propiedad canónica PidLidSmartNoAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSmartNoAttach
api_type:
- COM
ms.assetid: 60299c1b-1b46-4c3a-8fb9-a2b4d3383aac
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 43e10652a7dccdf0da6592df0f9fc2daf5ea9bee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818920"
---
# <a name="pidlidsmartnoattach-canonical-property"></a><span data-ttu-id="72723-103">Propiedad canónica PidLidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="72723-103">PidLidSmartNoAttach Canonical Property</span></span>

  
  
<span data-ttu-id="72723-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72723-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72723-105">Indica si los datos adjuntos en un mensaje se consideran como ocultas.</span><span class="sxs-lookup"><span data-stu-id="72723-105">Represents whether the attachments on a message are considered as hidden.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72723-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="72723-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72723-107">dispidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="72723-107">dispidSmartNoAttach</span></span>  <br/> |
|<span data-ttu-id="72723-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="72723-108">Property set:</span></span>  <br/> |<span data-ttu-id="72723-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="72723-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="72723-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="72723-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="72723-111">0x00008514</span><span class="sxs-lookup"><span data-stu-id="72723-111">0x00008514</span></span>  <br/> |
|<span data-ttu-id="72723-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="72723-112">Data type:</span></span>  <br/> |<span data-ttu-id="72723-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="72723-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="72723-114">Área:</span><span class="sxs-lookup"><span data-stu-id="72723-114">Area:</span></span>  <br/> |<span data-ttu-id="72723-115">Configuración de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="72723-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72723-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="72723-116">Remarks</span></span>

<span data-ttu-id="72723-117">Esta propiedad es TRUE si los datos adjuntos del mensaje se consideran como ocultas.</span><span class="sxs-lookup"><span data-stu-id="72723-117">This property is TRUE if the attachments of the message are considered as hidden.</span></span>
  
<span data-ttu-id="72723-118">Indica si el objeto de mensaje no tiene los datos adjuntos visible para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="72723-118">It indicates whether the message object has no end-user visible attachments.</span></span> <span data-ttu-id="72723-119">Esta propiedad puede ser sin establecer; Si es así, se supone un valor predeterminado de FALSE.</span><span class="sxs-lookup"><span data-stu-id="72723-119">This property may be unset; if so, a default value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="72723-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="72723-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="72723-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="72723-121">Protocol specifications</span></span>

<span data-ttu-id="72723-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72723-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72723-123">Proporciona la definición del conjunto de propiedad y referencias a las especificaciones de protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="72723-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="72723-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72723-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72723-125">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="72723-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="72723-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="72723-126">Header files</span></span>

<span data-ttu-id="72723-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72723-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="72723-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="72723-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72723-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="72723-129">See also</span></span>



[<span data-ttu-id="72723-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="72723-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72723-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="72723-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72723-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="72723-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72723-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="72723-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

