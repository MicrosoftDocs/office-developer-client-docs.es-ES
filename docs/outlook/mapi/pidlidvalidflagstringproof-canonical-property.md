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
ms.openlocfilehash: dfe3b57c246e247eda365bed46af2e0f35f0e54b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315389"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="14a01-103">Propiedad canónica PidLidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="14a01-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="14a01-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14a01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14a01-105">Valida si el valor de la propiedad **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) lo estableció un agente que conocía el valor de la propiedad **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="14a01-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="14a01-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="14a01-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="14a01-107">dispidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="14a01-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="14a01-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="14a01-108">Property set:</span></span>  <br/> |<span data-ttu-id="14a01-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="14a01-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="14a01-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="14a01-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="14a01-111">0x000085BF</span><span class="sxs-lookup"><span data-stu-id="14a01-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="14a01-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="14a01-112">Data type:</span></span>  <br/> |<span data-ttu-id="14a01-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="14a01-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="14a01-114">Área:</span><span class="sxs-lookup"><span data-stu-id="14a01-114">Area:</span></span>  <br/> |<span data-ttu-id="14a01-115">Task</span><span class="sxs-lookup"><span data-stu-id="14a01-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14a01-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="14a01-116">Remarks</span></span>

<span data-ttu-id="14a01-117">En objetos no enviables (correo recibido y objetos que no son de correo), los clientes deben establecer este valor en el valor de **PR_MESSAGE_DELIVERY_TIME** al modificar **dispidRequest**.</span><span class="sxs-lookup"><span data-stu-id="14a01-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="14a01-118">Dado que el remitente no puede predecir el valor de **PR_MESSAGE_DELIVERY_TIME,** si el valor de esta propiedad es igual al valor de **PR_MESSAGE_DELIVERY_TIME**, es razonablemente seguro que el valor de **dispidRequest** no se originó en el remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="14a01-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="14a01-119">Un cliente puede decidir cómo presentar el valor de **dispidRequest** al usuario final en función del resultado de esta comparación de acuerdo con la directiva de seguridad específica del cliente.</span><span class="sxs-lookup"><span data-stu-id="14a01-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="14a01-120">Si se omite el valor **de dispidRequest** debido a la presencia de un valor para **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), esta propiedad debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="14a01-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="14a01-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="14a01-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="14a01-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="14a01-122">Protocol specifications</span></span>

<span data-ttu-id="14a01-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14a01-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14a01-124">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="14a01-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="14a01-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14a01-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14a01-126">Especifica las propiedades y operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="14a01-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="14a01-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="14a01-127">Header files</span></span>

<span data-ttu-id="14a01-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="14a01-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="14a01-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="14a01-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14a01-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="14a01-130">See also</span></span>



[<span data-ttu-id="14a01-131">Propiedad canónica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="14a01-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="14a01-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="14a01-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="14a01-133">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="14a01-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="14a01-134">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="14a01-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="14a01-135">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="14a01-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

