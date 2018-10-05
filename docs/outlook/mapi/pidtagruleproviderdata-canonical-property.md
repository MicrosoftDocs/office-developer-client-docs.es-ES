---
title: Propiedad canónica PidTagRuleProviderData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e4d209c4f185ff253476beb04913e6a64884f9b6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388024"
---
# <a name="pidtagruleproviderdata-canonical-property"></a><span data-ttu-id="c84f5-103">Propiedad canónica PidTagRuleProviderData</span><span class="sxs-lookup"><span data-stu-id="c84f5-103">PidTagRuleProviderData Canonical Property</span></span>

  
  
<span data-ttu-id="c84f5-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c84f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c84f5-105">Una propiedad opaca que establece el cliente para el uso exclusivo del cliente.</span><span class="sxs-lookup"><span data-stu-id="c84f5-105">An opaque property that the client sets for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c84f5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c84f5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c84f5-107">PR_RULE_PROVIDER_DATA</span><span class="sxs-lookup"><span data-stu-id="c84f5-107">PR_RULE_PROVIDER_DATA</span></span>  <br/> |
|<span data-ttu-id="c84f5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c84f5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c84f5-109">0x6684</span><span class="sxs-lookup"><span data-stu-id="c84f5-109">0x6684</span></span>  <br/> |
|<span data-ttu-id="c84f5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c84f5-110">Data type:</span></span>  <br/> |<span data-ttu-id="c84f5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c84f5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c84f5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c84f5-112">Area:</span></span>  <br/> |<span data-ttu-id="c84f5-113">Reglas del servidor</span><span class="sxs-lookup"><span data-stu-id="c84f5-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c84f5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c84f5-114">Remarks</span></span>

<span data-ttu-id="c84f5-115">El servidor debe conservar el valor de esta propiedad si se ha definido por el cliente, pero debe tener en cuenta su contenido durante el procesamiento y evaluación de la regla.</span><span class="sxs-lookup"><span data-stu-id="c84f5-115">The server must preserve the value of this property if it was set by the client but must ignore its contents during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c84f5-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c84f5-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c84f5-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c84f5-117">Protocol specifications</span></span>

<span data-ttu-id="c84f5-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c84f5-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c84f5-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c84f5-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c84f5-120">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c84f5-120">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c84f5-121">Manipula los mensajes de correo electrónico entrante en un servidor.</span><span class="sxs-lookup"><span data-stu-id="c84f5-121">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c84f5-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c84f5-122">Header files</span></span>

<span data-ttu-id="c84f5-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c84f5-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c84f5-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c84f5-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c84f5-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c84f5-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c84f5-126">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="c84f5-126">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c84f5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c84f5-127">See also</span></span>



[<span data-ttu-id="c84f5-128">Propiedad canónica PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="c84f5-128">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="c84f5-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c84f5-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c84f5-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c84f5-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c84f5-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c84f5-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c84f5-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c84f5-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

