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
ms.openlocfilehash: 972df747e0ee459996b9b4da5732be1490fbd08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417129"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a><span data-ttu-id="f7fbf-103">Propiedad canónica PidTagConversionWithLossProhibited</span><span class="sxs-lookup"><span data-stu-id="f7fbf-103">PidTagConversionWithLossProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="f7fbf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7fbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7fbf-105">Contiene TRUE si se prohíbe a un agente de transferencia de mensajes (MTA) realizar conversiones de texto de mensajes que pierdan información.</span><span class="sxs-lookup"><span data-stu-id="f7fbf-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making message text conversions that lose information.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7fbf-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f7fbf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7fbf-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="f7fbf-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="f7fbf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f7fbf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7fbf-109">0x000D</span><span class="sxs-lookup"><span data-stu-id="f7fbf-109">0x000D</span></span>  <br/> |
|<span data-ttu-id="f7fbf-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f7fbf-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7fbf-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f7fbf-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f7fbf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f7fbf-112">Area:</span></span>  <br/> |<span data-ttu-id="f7fbf-113">Configuración general</span><span class="sxs-lookup"><span data-stu-id="f7fbf-113">General configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7fbf-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f7fbf-114">Remarks</span></span>

<span data-ttu-id="f7fbf-115">Un ejemplo del tipo de conversión prohibido es la asignación de "pérdida" de Unicode (dos bytes por carácter) a un conjunto de caracteres de un solo byte.</span><span class="sxs-lookup"><span data-stu-id="f7fbf-115">An example of the type of conversion being prohibited is the "lossy" mapping from Unicode (two bytes per character) to a single-byte character set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f7fbf-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7fbf-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f7fbf-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f7fbf-117">Header files</span></span>

<span data-ttu-id="f7fbf-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7fbf-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7fbf-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f7fbf-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7fbf-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f7fbf-120">Mapitags.h</span></span>
  
> <span data-ttu-id="f7fbf-121">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f7fbf-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7fbf-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7fbf-122">See also</span></span>



[<span data-ttu-id="f7fbf-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f7fbf-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7fbf-124">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="f7fbf-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7fbf-125">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f7fbf-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7fbf-126">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f7fbf-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

