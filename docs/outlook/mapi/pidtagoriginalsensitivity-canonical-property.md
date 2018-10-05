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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390082"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a><span data-ttu-id="09039-103">Propiedad canónica PidTagOriginalSensitivity</span><span class="sxs-lookup"><span data-stu-id="09039-103">PidTagOriginalSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="09039-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09039-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09039-105">Contiene el valor de sensibilidad asignado por el remitente de la primera versión de un mensaje, es decir, el mensaje antes de que se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="09039-105">Contains the sensitivity value assigned by the sender of the first version of a message that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="09039-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="09039-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="09039-107">PR_ORIGINAL_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="09039-107">PR_ORIGINAL_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="09039-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="09039-108">Identifier:</span></span>  <br/> |<span data-ttu-id="09039-109">0x002E</span><span class="sxs-lookup"><span data-stu-id="09039-109">0x002E</span></span>  <br/> |
|<span data-ttu-id="09039-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="09039-110">Data type:</span></span>  <br/> |<span data-ttu-id="09039-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="09039-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="09039-112">Área:</span><span class="sxs-lookup"><span data-stu-id="09039-112">Area:</span></span>  <br/> |<span data-ttu-id="09039-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="09039-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09039-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09039-114">Remarks</span></span>

<span data-ttu-id="09039-115">Una aplicación de cliente debe establecer esta propiedad en el mismo valor tal y como se envió la propiedad **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) cuando el mensaje es el primero.</span><span class="sxs-lookup"><span data-stu-id="09039-115">A client application should set this property to the same value as the **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) property when the message is first submitted.</span></span> <span data-ttu-id="09039-116">Nunca debe cambiarse posteriormente.</span><span class="sxs-lookup"><span data-stu-id="09039-116">It should never be changed subsequently.</span></span>
  
<span data-ttu-id="09039-117">Esta propiedad se usa en el proveedor de transporte para proteger la confidencialidad en los movimientos copiados.</span><span class="sxs-lookup"><span data-stu-id="09039-117">This property is used by the transport provider to protect the sensitivity on copied entries.</span></span> <span data-ttu-id="09039-118">Permite a él, por ejemplo, para bloquear la modificación del texto del mensaje original en un avance de o responder a un mensaje que se marcó originalmente **SENSITIVITY_PRIVATE**.</span><span class="sxs-lookup"><span data-stu-id="09039-118">It enables it, for example, to block modification of the original message text in a forward of or reply to a message that was originally marked **SENSITIVITY_PRIVATE**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="09039-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="09039-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="09039-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="09039-120">Protocol specifications</span></span>

<span data-ttu-id="09039-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09039-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09039-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="09039-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="09039-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09039-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09039-124">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="09039-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="09039-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="09039-125">Header files</span></span>

<span data-ttu-id="09039-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="09039-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="09039-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="09039-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="09039-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="09039-128">Mapitags.h</span></span>
  
> <span data-ttu-id="09039-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="09039-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="09039-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="09039-130">See also</span></span>



[<span data-ttu-id="09039-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="09039-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="09039-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="09039-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="09039-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="09039-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="09039-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="09039-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

