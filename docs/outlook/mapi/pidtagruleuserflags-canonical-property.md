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
ms.openlocfilehash: 8a44c88cbc971d9d5358fc6b24093e56e9565eb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820190"
---
# <a name="pidtagruleuserflags-canonical-property"></a><span data-ttu-id="210f6-103">Propiedad canónica PidTagRuleUserFlags</span><span class="sxs-lookup"><span data-stu-id="210f6-103">PidTagRuleUserFlags Canonical Property</span></span>

  
  
<span data-ttu-id="210f6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="210f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="210f6-105">Esta propiedad se establece por el cliente para el uso exclusivo del cliente.</span><span class="sxs-lookup"><span data-stu-id="210f6-105">This property is set by the client for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="210f6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="210f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="210f6-107">PR_RULE_USER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="210f6-107">PR_RULE_USER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="210f6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="210f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="210f6-109">0x6678</span><span class="sxs-lookup"><span data-stu-id="210f6-109">0x6678</span></span>  <br/> |
|<span data-ttu-id="210f6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="210f6-110">Data type:</span></span>  <br/> |<span data-ttu-id="210f6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="210f6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="210f6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="210f6-112">Area:</span></span>  <br/> |<span data-ttu-id="210f6-113">Reglas del servidor</span><span class="sxs-lookup"><span data-stu-id="210f6-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="210f6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="210f6-114">Remarks</span></span>

<span data-ttu-id="210f6-115">El servidor debe conservar el valor de esta propiedad si se ha definido por el cliente.</span><span class="sxs-lookup"><span data-stu-id="210f6-115">The server must preserve the value of this property if it was set by the client.</span></span> <span data-ttu-id="210f6-116">El servidor debe omitirlo durante el procesamiento y evaluación de la regla.</span><span class="sxs-lookup"><span data-stu-id="210f6-116">The server must ignore it during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="210f6-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="210f6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="210f6-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="210f6-118">Protocol specifications</span></span>

<span data-ttu-id="210f6-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="210f6-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="210f6-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="210f6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="210f6-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="210f6-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="210f6-122">Manipula los mensajes de correo electrónico entrante en un servidor.</span><span class="sxs-lookup"><span data-stu-id="210f6-122">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="210f6-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="210f6-123">Header files</span></span>

<span data-ttu-id="210f6-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="210f6-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="210f6-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="210f6-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="210f6-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="210f6-126">Mapitags.h</span></span>
  
> <span data-ttu-id="210f6-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="210f6-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="210f6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="210f6-128">See also</span></span>



[<span data-ttu-id="210f6-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="210f6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="210f6-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="210f6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="210f6-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="210f6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="210f6-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="210f6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

