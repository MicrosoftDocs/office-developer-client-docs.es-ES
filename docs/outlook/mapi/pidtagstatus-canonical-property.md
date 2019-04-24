---
title: Propiedad canónica PidTagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278795"
---
# <a name="pidtagstatus-canonical-property"></a><span data-ttu-id="e2fdb-103">Propiedad canónica PidTagStatus</span><span class="sxs-lookup"><span data-stu-id="e2fdb-103">PidTagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="e2fdb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2fdb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2fdb-105">Contiene una máscara de bits de 32 bits de marcadores que definen el estado de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-105">Contains a 32-bit bitmask of flags that define folder status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2fdb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e2fdb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2fdb-107">PR_STATUS</span><span class="sxs-lookup"><span data-stu-id="e2fdb-107">PR_STATUS</span></span>  <br/> |
|<span data-ttu-id="e2fdb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e2fdb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2fdb-109">0x360B</span><span class="sxs-lookup"><span data-stu-id="e2fdb-109">0x360B</span></span>  <br/> |
|<span data-ttu-id="e2fdb-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e2fdb-110">Data type:</span></span>  <br/> |<span data-ttu-id="e2fdb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e2fdb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e2fdb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e2fdb-112">Area:</span></span>  <br/> |<span data-ttu-id="e2fdb-113">Contenedor de MAPI</span><span class="sxs-lookup"><span data-stu-id="e2fdb-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2fdb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2fdb-114">Remarks</span></span>

<span data-ttu-id="e2fdb-115">Esta propiedad para Folders es análoga a la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-115">This property for folders is analogous to the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property for messages.</span></span> <span data-ttu-id="e2fdb-116">Sus indicadores se proporcionan solo para la aplicación cliente y no afectan al almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-116">Its flags are provided for the client application only and do not affect the message store.</span></span> <span data-ttu-id="e2fdb-117">Los clientes pueden usar u omitir esta configuración.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-117">Clients can use or ignore these settings.</span></span> <span data-ttu-id="e2fdb-118">El cliente también puede definir sus propios valores para los bits definible por el cliente de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-118">The client can also define its own values for the client-definable bits of this property.</span></span>
  
<span data-ttu-id="e2fdb-119">Se pueden establecer uno o varios de los siguientes indicadores para la máscara de la máscara:</span><span class="sxs-lookup"><span data-stu-id="e2fdb-119">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="e2fdb-120">FLDSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="e2fdb-120">FLDSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="e2fdb-121">La carpeta se marca para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-121">The folder is marked for deletion.</span></span> <span data-ttu-id="e2fdb-122">La aplicación cliente establece esta marca.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-122">The client application sets this flag.</span></span>
    
<span data-ttu-id="e2fdb-123">FLDSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="e2fdb-123">FLDSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="e2fdb-124">La carpeta está oculta.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-124">The folder is hidden.</span></span>
    
<span data-ttu-id="e2fdb-125">FLDSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="e2fdb-125">FLDSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="e2fdb-126">La carpeta aparece resaltada, por ejemplo, en inverso de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-126">The folder is highlighted, for example, shown in reverse video.</span></span>
    
<span data-ttu-id="e2fdb-127">FLDSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="e2fdb-127">FLDSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="e2fdb-128">La carpeta se etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-128">The folder is tagged.</span></span>
    
<span data-ttu-id="e2fdb-129">Los proveedores de almacenamiento de mensajes establecen esta propiedad en una carpeta en uno o varios de estos valores y los clientes interpretan el estado según corresponda para sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-129">Message store providers set this property on a folder to one or more of these values and clients interpret the status as appropriate for their applications.</span></span> <span data-ttu-id="e2fdb-130">Por ejemplo, un cliente puede usar el estado de la carpeta para diferenciar visualmente las carpetas de una tabla de jerarquías y mostrar las carpetas que tienen el mismo estado de la misma forma.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-130">For example, a client can use the folder status to visually differentiate between folders in a hierarchy table, displaying folders with the same status in the same way.</span></span> <span data-ttu-id="e2fdb-131">Las carpetas reSaltadas se pueden mostrar en vídeo inverso, las carpetas con etiquetas y las carpetas marcadas para eliminación pueden mostrarse con un icono significativo y las carpetas ocultas se pueden ocultar.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-131">Highlighted folders can be shown in reverse video, tagged folders and folders marked for deletion can be shown with a meaningful icon, and hidden folders can be concealed.</span></span>
  
<span data-ttu-id="e2fdb-132">Los bits 16 a 31 ("0x10000" a "0x80000000") de esta propiedad están disponibles para su uso por parte de la aplicación cliente IPM.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-132">Bits 16 through 31 ("0x10000" through "0x80000000") of this property are available for use by the IPM client application.</span></span> <span data-ttu-id="e2fdb-133">El resto de los bits están reservados para su uso por parte de MAPI; los que no están definidos en la lista anterior deben establecerse inicialmente en cero y no han sido modificados.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-133">All other bits are reserved for use by MAPI; those not defined in the preceding list should be initially set to zero and not altered.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e2fdb-134">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2fdb-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2fdb-135">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e2fdb-135">Protocol specifications</span></span>

<span data-ttu-id="e2fdb-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2fdb-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2fdb-137">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2fdb-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2fdb-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2fdb-139">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-139">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2fdb-140">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e2fdb-140">Header files</span></span>

<span data-ttu-id="e2fdb-141">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e2fdb-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2fdb-142">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="e2fdb-143">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e2fdb-143">Mapitags.h</span></span>
  
> <span data-ttu-id="e2fdb-144">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e2fdb-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2fdb-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2fdb-145">See also</span></span>



[<span data-ttu-id="e2fdb-146">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e2fdb-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2fdb-147">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="e2fdb-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2fdb-148">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e2fdb-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2fdb-149">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e2fdb-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

