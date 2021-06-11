---
title: Propiedad canónica PidTagRuleProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 19889a1f48a6088f0d5ad224f7e9189b112622fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280608"
---
# <a name="pidtagruleprovider-canonical-property"></a><span data-ttu-id="d09d7-103">Propiedad canónica PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="d09d7-103">PidTagRuleProvider Canonical Property</span></span>

  
  
<span data-ttu-id="d09d7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d09d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d09d7-105">Contiene el nombre de la aplicación que establece una regla.</span><span class="sxs-lookup"><span data-stu-id="d09d7-105">Contains the name of the application that sets a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d09d7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d09d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d09d7-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span><span class="sxs-lookup"><span data-stu-id="d09d7-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span></span>  <br/> |
|<span data-ttu-id="d09d7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d09d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d09d7-109">0x6681</span><span class="sxs-lookup"><span data-stu-id="d09d7-109">0x6681</span></span>  <br/> |
|<span data-ttu-id="d09d7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d09d7-110">Data type:</span></span>  <br/> |<span data-ttu-id="d09d7-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d09d7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d09d7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d09d7-112">Area:</span></span>  <br/> |<span data-ttu-id="d09d7-113">Reglas del lado servidor</span><span class="sxs-lookup"><span data-stu-id="d09d7-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d09d7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d09d7-114">Remarks</span></span>

<span data-ttu-id="d09d7-115">Las acciones diferidas necesitan estas propiedades para identificar el código que debe interpretar y ejecutar la acción de regla.</span><span class="sxs-lookup"><span data-stu-id="d09d7-115">Deferred actions need these properties to identify the code that must interpret and execute the rule action.</span></span>
  
<span data-ttu-id="d09d7-116">Las reglas almacenadas en buzones y carpetas están asociadas con la aplicación que los posee mediante una cadena de proveedor de reglas.</span><span class="sxs-lookup"><span data-stu-id="d09d7-116">Rules stored on mailboxes and folders are associated with the application that owns them by a rule provider string.</span></span> <span data-ttu-id="d09d7-117">Un proveedor de reglas establece y controla las reglas de una tabla de reglas.</span><span class="sxs-lookup"><span data-stu-id="d09d7-117">A rule provider sets and handles rules in a rule table.</span></span> <span data-ttu-id="d09d7-118">También proporciona un medio para controlar las acciones diferidas si se establecen dichas reglas.</span><span class="sxs-lookup"><span data-stu-id="d09d7-118">It also provides a means of handling any deferred actions if such rules are set.</span></span> <span data-ttu-id="d09d7-119">Las acciones diferidas las crea implícitamente el almacén de información.</span><span class="sxs-lookup"><span data-stu-id="d09d7-119">Deferred actions are created implicitly by the information store.</span></span> <span data-ttu-id="d09d7-120">Para operaciones de movimiento o copia en un almacén diferente, si un proveedor establece una regla de acción diferida, debe proporcionar un controlador para realizar la acción cuando se desencadena la regla y se crea una acción diferida.</span><span class="sxs-lookup"><span data-stu-id="d09d7-120">For move or copy operations to a different store, if a provider sets a deferred action rule, it must provide a handler to perform the action when the rule is fired and a deferred action is created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d09d7-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d09d7-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d09d7-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="d09d7-122">Protocol specifications</span></span>

<span data-ttu-id="d09d7-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d09d7-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d09d7-124">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="d09d7-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d09d7-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d09d7-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d09d7-126">Manipula los mensajes de correo electrónico entrantes en un servidor.</span><span class="sxs-lookup"><span data-stu-id="d09d7-126">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d09d7-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d09d7-127">Header files</span></span>

<span data-ttu-id="d09d7-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d09d7-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="d09d7-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d09d7-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="d09d7-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d09d7-130">Mapitags.h</span></span>
  
> <span data-ttu-id="d09d7-131">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d09d7-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d09d7-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d09d7-132">See also</span></span>



[<span data-ttu-id="d09d7-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d09d7-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d09d7-134">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d09d7-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d09d7-135">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d09d7-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d09d7-136">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="d09d7-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

