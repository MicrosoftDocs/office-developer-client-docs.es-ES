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
ms.openlocfilehash: 6d461c88e96a3f749595b3e071737107480472aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819853"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a><span data-ttu-id="510bc-103">Propiedad canónica PidTagOriginalSensitivity</span><span class="sxs-lookup"><span data-stu-id="510bc-103">PidTagOriginalSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="510bc-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="510bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="510bc-105">Contiene el valor de sensibilidad asignado por el remitente de la primera versión de un mensaje, es decir, el mensaje antes de que se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="510bc-105">Contains the sensitivity value assigned by the sender of the first version of a message that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="510bc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="510bc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="510bc-107">PR_ORIGINAL_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="510bc-107">PR_ORIGINAL_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="510bc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="510bc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="510bc-109">0x002E</span><span class="sxs-lookup"><span data-stu-id="510bc-109">0x002E</span></span>  <br/> |
|<span data-ttu-id="510bc-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="510bc-110">Data type:</span></span>  <br/> |<span data-ttu-id="510bc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="510bc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="510bc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="510bc-112">Area:</span></span>  <br/> |<span data-ttu-id="510bc-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="510bc-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="510bc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="510bc-114">Remarks</span></span>

<span data-ttu-id="510bc-115">Una aplicación de cliente debe establecer esta propiedad en el mismo valor tal y como se envió la propiedad **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) cuando el mensaje es el primero.</span><span class="sxs-lookup"><span data-stu-id="510bc-115">A client application should set this property to the same value as the **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) property when the message is first submitted.</span></span> <span data-ttu-id="510bc-116">Nunca debe cambiarse posteriormente.</span><span class="sxs-lookup"><span data-stu-id="510bc-116">It should never be changed subsequently.</span></span>
  
<span data-ttu-id="510bc-117">Esta propiedad se usa en el proveedor de transporte para proteger la confidencialidad en los movimientos copiados.</span><span class="sxs-lookup"><span data-stu-id="510bc-117">This property is used by the transport provider to protect the sensitivity on copied entries.</span></span> <span data-ttu-id="510bc-118">Permite a él, por ejemplo, para bloquear la modificación del texto del mensaje original en un avance de o responder a un mensaje que se marcó originalmente **SENSITIVITY_PRIVATE**.</span><span class="sxs-lookup"><span data-stu-id="510bc-118">It enables it, for example, to block modification of the original message text in a forward of or reply to a message that was originally marked **SENSITIVITY_PRIVATE**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="510bc-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="510bc-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="510bc-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="510bc-120">Protocol specifications</span></span>

<span data-ttu-id="510bc-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="510bc-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="510bc-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="510bc-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="510bc-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="510bc-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="510bc-124">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="510bc-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="510bc-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="510bc-125">Header files</span></span>

<span data-ttu-id="510bc-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="510bc-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="510bc-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="510bc-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="510bc-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="510bc-128">Mapitags.h</span></span>
  
> <span data-ttu-id="510bc-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="510bc-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="510bc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="510bc-130">See also</span></span>



[<span data-ttu-id="510bc-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="510bc-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="510bc-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="510bc-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="510bc-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="510bc-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="510bc-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="510bc-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

