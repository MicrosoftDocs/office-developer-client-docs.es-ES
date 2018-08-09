---
title: Propiedad canónica PidLidValidFlagStringProof
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidValidFlagStringProof
api_type:
- COM
ms.assetid: e5a94968-7e84-4faf-8104-9ea36d35fa1a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 90f16f33e7e116e124384f9988c0c7dddaad2da5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819044"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="9fb22-103">Propiedad canónica PidLidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="9fb22-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="9fb22-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9fb22-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9fb22-105">Valida si el valor de la propiedad **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) se estableció por un agente que conoce el valor de la propiedad **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9fb22-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9fb22-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9fb22-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9fb22-107">dispidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="9fb22-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="9fb22-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="9fb22-108">Property set:</span></span>  <br/> |<span data-ttu-id="9fb22-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="9fb22-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9fb22-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="9fb22-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9fb22-111">0x000085BF</span><span class="sxs-lookup"><span data-stu-id="9fb22-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="9fb22-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9fb22-112">Data type:</span></span>  <br/> |<span data-ttu-id="9fb22-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="9fb22-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="9fb22-114">Área:</span><span class="sxs-lookup"><span data-stu-id="9fb22-114">Area:</span></span>  <br/> |<span data-ttu-id="9fb22-115">Task</span><span class="sxs-lookup"><span data-stu-id="9fb22-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fb22-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9fb22-116">Remarks</span></span>

<span data-ttu-id="9fb22-117">En los objetos que no se puedan enviar (correo recibido y objetos que no sean de correo), los clientes deben establecer este valor en el valor de **PR_MESSAGE_DELIVERY_TIME** al modificar **dispidRequest**.</span><span class="sxs-lookup"><span data-stu-id="9fb22-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="9fb22-118">Dado que no se puede predecir el valor de **PR_MESSAGE_DELIVERY_TIME** por el remitente, si el valor de esta propiedad es igual al valor de **PR_MESSAGE_DELIVERY_TIME**, es razonablemente seguro de que el valor de **dispidRequest** no lo hizo se originan desde el remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9fb22-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="9fb22-119">Un cliente puede decidir cómo presentar el valor de **dispidRequest** para el usuario final en función del resultado de esta comparación con arreglo a la directiva de seguridad específicos del cliente.</span><span class="sxs-lookup"><span data-stu-id="9fb22-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="9fb22-120">Si se omite el valor de **dispidRequest** debido a la presencia de un valor para **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), debe ignorarse esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9fb22-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9fb22-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9fb22-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9fb22-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9fb22-122">Protocol specifications</span></span>

<span data-ttu-id="9fb22-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9fb22-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9fb22-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9fb22-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9fb22-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9fb22-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9fb22-126">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="9fb22-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9fb22-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9fb22-127">Header files</span></span>

<span data-ttu-id="9fb22-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9fb22-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="9fb22-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9fb22-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9fb22-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fb22-130">See also</span></span>



[<span data-ttu-id="9fb22-131">Propiedad canónica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="9fb22-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="9fb22-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9fb22-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9fb22-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9fb22-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9fb22-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9fb22-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9fb22-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="9fb22-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

