---
title: Propiedad canónica PidTagRemoteValidateOk
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8b5c9e5bb2aa915d4b76d9998baaf504e7929b78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424227"
---
# <a name="pidtagremotevalidateok-canonical-property"></a><span data-ttu-id="54ce6-103">Propiedad canónica PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="54ce6-103">PidTagRemoteValidateOk Canonical Property</span></span>

  
  
<span data-ttu-id="54ce6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54ce6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54ce6-105">Esta propiedad contiene TRUE si el visor remoto puede llamar al [método IMAPIStatus::ValidateState.](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="54ce6-105">This property contains TRUE if the remote viewer is allowed to call the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54ce6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="54ce6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54ce6-107">PR_REMOTE_VALIDATE_OK</span><span class="sxs-lookup"><span data-stu-id="54ce6-107">PR_REMOTE_VALIDATE_OK</span></span>  <br/> |
|<span data-ttu-id="54ce6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="54ce6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="54ce6-109">0x3E0D</span><span class="sxs-lookup"><span data-stu-id="54ce6-109">0x3E0D</span></span>  <br/> |
|<span data-ttu-id="54ce6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="54ce6-110">Data type:</span></span>  <br/> |<span data-ttu-id="54ce6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="54ce6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="54ce6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="54ce6-112">Area:</span></span>  <br/> |<span data-ttu-id="54ce6-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="54ce6-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54ce6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54ce6-114">Remarks</span></span>

<span data-ttu-id="54ce6-115">Esta propiedad aparece en la tabla de estado y ofrece cierto control sobre el rendimiento del transporte.</span><span class="sxs-lookup"><span data-stu-id="54ce6-115">This property appears in the status table and offers some control over transport performance.</span></span> <span data-ttu-id="54ce6-116">Se puede considerar como otra forma de dirigir el visor remoto a inactivo.</span><span class="sxs-lookup"><span data-stu-id="54ce6-116">It can be considered as another way of directing the remote viewer to idle.</span></span> <span data-ttu-id="54ce6-117">Cuando se establece en TRUE, el visor remoto puede llamar a **IMAPIStatus::ValidateState** tantas veces como desee.</span><span class="sxs-lookup"><span data-stu-id="54ce6-117">When it is set to TRUE, the remote viewer can call **IMAPIStatus::ValidateState** as often as desired.</span></span> <span data-ttu-id="54ce6-118">Un valor FALSE indica que el visor remoto no puede realizar más llamadas.</span><span class="sxs-lookup"><span data-stu-id="54ce6-118">A value of FALSE indicates that the remote viewer cannot make any more calls.</span></span> 
  
<span data-ttu-id="54ce6-119">Normalmente, el proveedor de transporte establece esta propiedad dinámicamente, estableciendo el valor en FALSE para deshabilitar llamadas adicionales cuando el proveedor de transporte tiene una cantidad suficiente de procesamiento para realizar.</span><span class="sxs-lookup"><span data-stu-id="54ce6-119">The transport provider usually sets this property dynamically, by setting the value to FALSE to disable additional calls when the transport provider has a sufficient amount of processing to perform.</span></span> <span data-ttu-id="54ce6-120">Una vez terminado el proveedor de transporte, establece el valor en TRUE para permitir que la aplicación cliente realice más llamadas **IMAPIStatus::ValidateState.**</span><span class="sxs-lookup"><span data-stu-id="54ce6-120">When the transport provider is done, it then sets the value to TRUE to allow the client application to make further **IMAPIStatus::ValidateState** calls.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="54ce6-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="54ce6-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="54ce6-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="54ce6-122">Header files</span></span>

<span data-ttu-id="54ce6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54ce6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="54ce6-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="54ce6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="54ce6-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="54ce6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="54ce6-126">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="54ce6-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54ce6-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="54ce6-127">See also</span></span>



[<span data-ttu-id="54ce6-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="54ce6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54ce6-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="54ce6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54ce6-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="54ce6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54ce6-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="54ce6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

