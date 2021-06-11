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
ms.openlocfilehash: 7dddca6a17b07047d1447a57347fbe47a04471e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331321"
---
# <a name="pidlidsmartnoattach-canonical-property"></a><span data-ttu-id="2852e-103">Propiedad canónica PidLidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="2852e-103">PidLidSmartNoAttach Canonical Property</span></span>

  
  
<span data-ttu-id="2852e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2852e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2852e-105">Representa si los datos adjuntos de un mensaje se consideran ocultos.</span><span class="sxs-lookup"><span data-stu-id="2852e-105">Represents whether the attachments on a message are considered as hidden.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2852e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2852e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2852e-107">dispidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="2852e-107">dispidSmartNoAttach</span></span>  <br/> |
|<span data-ttu-id="2852e-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="2852e-108">Property set:</span></span>  <br/> |<span data-ttu-id="2852e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="2852e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="2852e-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="2852e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2852e-111">0x00008514</span><span class="sxs-lookup"><span data-stu-id="2852e-111">0x00008514</span></span>  <br/> |
|<span data-ttu-id="2852e-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2852e-112">Data type:</span></span>  <br/> |<span data-ttu-id="2852e-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2852e-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2852e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="2852e-114">Area:</span></span>  <br/> |<span data-ttu-id="2852e-115">Configuración en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="2852e-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2852e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2852e-116">Remarks</span></span>

<span data-ttu-id="2852e-117">Esta propiedad es TRUE si los datos adjuntos del mensaje se consideran ocultos.</span><span class="sxs-lookup"><span data-stu-id="2852e-117">This property is TRUE if the attachments of the message are considered as hidden.</span></span>
  
<span data-ttu-id="2852e-118">Indica si el objeto de mensaje no tiene datos adjuntos visibles del usuario final.</span><span class="sxs-lookup"><span data-stu-id="2852e-118">It indicates whether the message object has no end-user visible attachments.</span></span> <span data-ttu-id="2852e-119">Esta propiedad puede estar sin conjunto; si es así, se supone un valor predeterminado de FALSE.</span><span class="sxs-lookup"><span data-stu-id="2852e-119">This property may be unset; if so, a default value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2852e-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2852e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2852e-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="2852e-121">Protocol specifications</span></span>

<span data-ttu-id="2852e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2852e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2852e-123">Proporciona la definición del conjunto de propiedades y las referencias a las Exchange Server de protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="2852e-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2852e-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2852e-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2852e-125">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="2852e-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2852e-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2852e-126">Header files</span></span>

<span data-ttu-id="2852e-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2852e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="2852e-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2852e-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2852e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2852e-129">See also</span></span>



[<span data-ttu-id="2852e-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2852e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2852e-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2852e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2852e-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2852e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2852e-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2852e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

