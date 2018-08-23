---
title: Propiedad canónica PidTagConversionWithLossProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e5d9261a9f33d77d52cfd6e448e69a2c1e8df415
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585237"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a><span data-ttu-id="71331-103">Propiedad canónica PidTagConversionWithLossProhibited</span><span class="sxs-lookup"><span data-stu-id="71331-103">PidTagConversionWithLossProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="71331-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71331-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71331-105">Contiene TRUE si un agente de transferencia de mensajes (MTA) se prohíbe realizar las conversiones de texto que se pierdan la información de mensaje.</span><span class="sxs-lookup"><span data-stu-id="71331-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making message text conversions that lose information.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71331-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="71331-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="71331-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="71331-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="71331-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="71331-108">Identifier:</span></span>  <br/> |<span data-ttu-id="71331-109">0x000D</span><span class="sxs-lookup"><span data-stu-id="71331-109">0x000D</span></span>  <br/> |
|<span data-ttu-id="71331-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="71331-110">Data type:</span></span>  <br/> |<span data-ttu-id="71331-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="71331-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="71331-112">Área:</span><span class="sxs-lookup"><span data-stu-id="71331-112">Area:</span></span>  <br/> |<span data-ttu-id="71331-113">Configuración general</span><span class="sxs-lookup"><span data-stu-id="71331-113">General configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71331-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="71331-114">Remarks</span></span>

<span data-ttu-id="71331-115">Un ejemplo del tipo de conversión que se está prohibido es la asignación "con pérdida" de Unicode (dos bytes por carácter) a un conjunto de caracteres de un byte.</span><span class="sxs-lookup"><span data-stu-id="71331-115">An example of the type of conversion being prohibited is the "lossy" mapping from Unicode (two bytes per character) to a single-byte character set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="71331-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="71331-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="71331-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="71331-117">Header files</span></span>

<span data-ttu-id="71331-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71331-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="71331-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="71331-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="71331-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="71331-120">Mapitags.h</span></span>
  
> <span data-ttu-id="71331-121">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="71331-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71331-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="71331-122">See also</span></span>



[<span data-ttu-id="71331-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="71331-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="71331-124">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="71331-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="71331-125">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="71331-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="71331-126">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="71331-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

