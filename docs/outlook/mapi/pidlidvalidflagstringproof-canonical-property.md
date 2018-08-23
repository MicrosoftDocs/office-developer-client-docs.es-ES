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
ms.openlocfilehash: efbbffe184e965caae84db54383e1431dfb1a569
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585825"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="e2cfc-103">Propiedad canónica PidLidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="e2cfc-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="e2cfc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2cfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2cfc-105">Valida si el valor de la propiedad **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) se estableció por un agente que conoce el valor de la propiedad **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e2cfc-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2cfc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e2cfc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2cfc-107">dispidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="e2cfc-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="e2cfc-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e2cfc-108">Property set:</span></span>  <br/> |<span data-ttu-id="e2cfc-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e2cfc-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e2cfc-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="e2cfc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e2cfc-111">0x000085BF</span><span class="sxs-lookup"><span data-stu-id="e2cfc-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="e2cfc-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e2cfc-112">Data type:</span></span>  <br/> |<span data-ttu-id="e2cfc-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e2cfc-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e2cfc-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e2cfc-114">Area:</span></span>  <br/> |<span data-ttu-id="e2cfc-115">Task</span><span class="sxs-lookup"><span data-stu-id="e2cfc-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2cfc-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2cfc-116">Remarks</span></span>

<span data-ttu-id="e2cfc-117">En los objetos que no se puedan enviar (correo recibido y objetos que no sean de correo), los clientes deben establecer este valor en el valor de **PR_MESSAGE_DELIVERY_TIME** al modificar **dispidRequest**.</span><span class="sxs-lookup"><span data-stu-id="e2cfc-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="e2cfc-118">Dado que no se puede predecir el valor de **PR_MESSAGE_DELIVERY_TIME** por el remitente, si el valor de esta propiedad es igual al valor de **PR_MESSAGE_DELIVERY_TIME**, es razonablemente seguro de que el valor de **dispidRequest** no lo hizo se originan desde el remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e2cfc-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="e2cfc-119">Un cliente puede decidir cómo presentar el valor de **dispidRequest** para el usuario final en función del resultado de esta comparación con arreglo a la directiva de seguridad específicos del cliente.</span><span class="sxs-lookup"><span data-stu-id="e2cfc-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="e2cfc-120">Si se omite el valor de **dispidRequest** debido a la presencia de un valor para **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), debe ignorarse esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e2cfc-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e2cfc-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2cfc-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2cfc-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e2cfc-122">Protocol specifications</span></span>

<span data-ttu-id="e2cfc-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2cfc-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2cfc-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e2cfc-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2cfc-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2cfc-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2cfc-126">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="e2cfc-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2cfc-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e2cfc-127">Header files</span></span>

<span data-ttu-id="e2cfc-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2cfc-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2cfc-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e2cfc-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2cfc-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e2cfc-130">See also</span></span>



[<span data-ttu-id="e2cfc-131">Propiedad canónica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="e2cfc-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="e2cfc-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e2cfc-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2cfc-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e2cfc-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2cfc-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e2cfc-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2cfc-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e2cfc-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

