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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335423"
---
# <a name="pidtagruleproviderdata-canonical-property"></a><span data-ttu-id="a4d0a-103">Propiedad canónica PidTagRuleProviderData</span><span class="sxs-lookup"><span data-stu-id="a4d0a-103">PidTagRuleProviderData Canonical Property</span></span>

  
  
<span data-ttu-id="a4d0a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4d0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4d0a-105">Una propiedad opaca que el cliente establece para el uso exclusivo del cliente.</span><span class="sxs-lookup"><span data-stu-id="a4d0a-105">An opaque property that the client sets for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4d0a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a4d0a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a4d0a-107">PR_RULE_PROVIDER_DATA</span><span class="sxs-lookup"><span data-stu-id="a4d0a-107">PR_RULE_PROVIDER_DATA</span></span>  <br/> |
|<span data-ttu-id="a4d0a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a4d0a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a4d0a-109">0x6684</span><span class="sxs-lookup"><span data-stu-id="a4d0a-109">0x6684</span></span>  <br/> |
|<span data-ttu-id="a4d0a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a4d0a-110">Data type:</span></span>  <br/> |<span data-ttu-id="a4d0a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a4d0a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a4d0a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a4d0a-112">Area:</span></span>  <br/> |<span data-ttu-id="a4d0a-113">Reglas del lado servidor</span><span class="sxs-lookup"><span data-stu-id="a4d0a-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4d0a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4d0a-114">Remarks</span></span>

<span data-ttu-id="a4d0a-115">El servidor debe conservar el valor de esta propiedad si lo estableció el cliente, pero debe omitir su contenido durante la evaluación y el procesamiento de la regla.</span><span class="sxs-lookup"><span data-stu-id="a4d0a-115">The server must preserve the value of this property if it was set by the client but must ignore its contents during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a4d0a-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4d0a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a4d0a-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="a4d0a-117">Protocol specifications</span></span>

<span data-ttu-id="a4d0a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4d0a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4d0a-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="a4d0a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a4d0a-120">[[MS-OJORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4d0a-120">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4d0a-121">Manipula los mensajes de correo electrónico entrantes en un servidor.</span><span class="sxs-lookup"><span data-stu-id="a4d0a-121">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a4d0a-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a4d0a-122">Header files</span></span>

<span data-ttu-id="a4d0a-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a4d0a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a4d0a-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a4d0a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a4d0a-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a4d0a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a4d0a-126">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="a4d0a-126">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a4d0a-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a4d0a-127">See also</span></span>



[<span data-ttu-id="a4d0a-128">Propiedad canónica PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="a4d0a-128">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="a4d0a-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a4d0a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a4d0a-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="a4d0a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a4d0a-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a4d0a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a4d0a-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="a4d0a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

