---
title: Propiedad canónica PidTagOriginalSensitivity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSensitivity
api_type:
- COM
ms.assetid: 70a87cf8-2011-4669-90fd-2711c3352e30
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e712a4cc49541ee4330f479d7a03af323bdbc887
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341233"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a><span data-ttu-id="b3463-103">Propiedad canónica PidTagOriginalSensitivity</span><span class="sxs-lookup"><span data-stu-id="b3463-103">PidTagOriginalSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="b3463-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3463-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3463-105">Contiene el valor de confidencialidad asignado por el remitente de la primera versión de un mensaje, es decir, el mensaje antes de reenviarlo o responderlo.</span><span class="sxs-lookup"><span data-stu-id="b3463-105">Contains the sensitivity value assigned by the sender of the first version of a message that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b3463-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b3463-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b3463-107">PR_ORIGINAL_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="b3463-107">PR_ORIGINAL_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="b3463-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b3463-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b3463-109">0x002E</span><span class="sxs-lookup"><span data-stu-id="b3463-109">0x002E</span></span>  <br/> |
|<span data-ttu-id="b3463-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b3463-110">Data type:</span></span>  <br/> |<span data-ttu-id="b3463-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b3463-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b3463-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b3463-112">Area:</span></span>  <br/> |<span data-ttu-id="b3463-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="b3463-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3463-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b3463-114">Remarks</span></span>

<span data-ttu-id="b3463-115">Una aplicación cliente debe establecer esta propiedad en el mismo valor que la propiedad **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) cuando se envía el mensaje por primera vez.</span><span class="sxs-lookup"><span data-stu-id="b3463-115">A client application should set this property to the same value as the **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) property when the message is first submitted.</span></span> <span data-ttu-id="b3463-116">Nunca se debe cambiar posteriormente.</span><span class="sxs-lookup"><span data-stu-id="b3463-116">It should never be changed subsequently.</span></span>
  
<span data-ttu-id="b3463-117">El proveedor de transporte usa esta propiedad para proteger la confidencialidad de las entradas copiadas.</span><span class="sxs-lookup"><span data-stu-id="b3463-117">This property is used by the transport provider to protect the sensitivity on copied entries.</span></span> <span data-ttu-id="b3463-118">Le permite, por ejemplo, bloquear la modificación del texto del mensaje original al reenviar o responder a un mensaje que se marcó originalmente **como SENSITIVITY_PRIVATE**.</span><span class="sxs-lookup"><span data-stu-id="b3463-118">It enables it, for example, to block modification of the original message text in a forward of or reply to a message that was originally marked **SENSITIVITY_PRIVATE**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b3463-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3463-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b3463-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="b3463-120">Protocol specifications</span></span>

<span data-ttu-id="b3463-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b3463-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b3463-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="b3463-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b3463-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b3463-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b3463-124">Especifica las propiedades y operaciones permitidas en los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b3463-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b3463-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b3463-125">Header files</span></span>

<span data-ttu-id="b3463-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b3463-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b3463-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b3463-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b3463-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b3463-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b3463-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b3463-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b3463-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b3463-130">See also</span></span>



[<span data-ttu-id="b3463-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b3463-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b3463-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="b3463-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b3463-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b3463-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b3463-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="b3463-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

