---
title: Propiedad canónica PidTagRuleUserFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleUserFlags
api_type:
- COM
ms.assetid: c5dfb21f-b35e-4521-bf2b-e3d03d98d75d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 235efce341e1870f0c33917f1c6d42b021727308
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321346"
---
# <a name="pidtagruleuserflags-canonical-property"></a><span data-ttu-id="4772b-103">Propiedad canónica PidTagRuleUserFlags</span><span class="sxs-lookup"><span data-stu-id="4772b-103">PidTagRuleUserFlags Canonical Property</span></span>

  
  
<span data-ttu-id="4772b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4772b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4772b-105">El cliente establece esta propiedad para el uso exclusivo del cliente.</span><span class="sxs-lookup"><span data-stu-id="4772b-105">This property is set by the client for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4772b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4772b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4772b-107">PR_RULE_USER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="4772b-107">PR_RULE_USER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="4772b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4772b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4772b-109">0x6678</span><span class="sxs-lookup"><span data-stu-id="4772b-109">0x6678</span></span>  <br/> |
|<span data-ttu-id="4772b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4772b-110">Data type:</span></span>  <br/> |<span data-ttu-id="4772b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4772b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4772b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4772b-112">Area:</span></span>  <br/> |<span data-ttu-id="4772b-113">Reglas del lado servidor</span><span class="sxs-lookup"><span data-stu-id="4772b-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4772b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4772b-114">Remarks</span></span>

<span data-ttu-id="4772b-115">El servidor debe conservar el valor de esta propiedad si lo estableció el cliente.</span><span class="sxs-lookup"><span data-stu-id="4772b-115">The server must preserve the value of this property if it was set by the client.</span></span> <span data-ttu-id="4772b-116">El servidor debe omitirlo durante la evaluación y el procesamiento de la regla.</span><span class="sxs-lookup"><span data-stu-id="4772b-116">The server must ignore it during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4772b-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4772b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4772b-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4772b-118">Protocol specifications</span></span>

<span data-ttu-id="4772b-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4772b-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4772b-120">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4772b-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4772b-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4772b-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4772b-122">Manipula los mensajes de correo electrónico entrantes en un servidor.</span><span class="sxs-lookup"><span data-stu-id="4772b-122">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4772b-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4772b-123">Header files</span></span>

<span data-ttu-id="4772b-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4772b-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4772b-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4772b-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4772b-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4772b-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4772b-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4772b-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4772b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4772b-128">See also</span></span>



[<span data-ttu-id="4772b-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4772b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4772b-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="4772b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4772b-131">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4772b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4772b-132">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4772b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

