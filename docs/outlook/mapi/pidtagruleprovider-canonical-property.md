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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385980"
---
# <a name="pidtagruleprovider-canonical-property"></a><span data-ttu-id="0b673-103">Propiedad canónica PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="0b673-103">PidTagRuleProvider Canonical Property</span></span>

  
  
<span data-ttu-id="0b673-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b673-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b673-105">Contiene el nombre de la aplicación que establece una regla.</span><span class="sxs-lookup"><span data-stu-id="0b673-105">Contains the name of the application that sets a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0b673-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0b673-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b673-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A, PR_RULE_PROVIDER_W</span><span class="sxs-lookup"><span data-stu-id="0b673-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span></span>  <br/> |
|<span data-ttu-id="0b673-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0b673-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0b673-109">0x6681</span><span class="sxs-lookup"><span data-stu-id="0b673-109">0x6681</span></span>  <br/> |
|<span data-ttu-id="0b673-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0b673-110">Data type:</span></span>  <br/> |<span data-ttu-id="0b673-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0b673-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0b673-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0b673-112">Area:</span></span>  <br/> |<span data-ttu-id="0b673-113">Reglas del servidor</span><span class="sxs-lookup"><span data-stu-id="0b673-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b673-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b673-114">Remarks</span></span>

<span data-ttu-id="0b673-115">Aplaza necesidad de acciones estas propiedades para identificar el código que se deben interpretar y ejecutar la acción de regla.</span><span class="sxs-lookup"><span data-stu-id="0b673-115">Deferred actions need these properties to identify the code that must interpret and execute the rule action.</span></span>
  
<span data-ttu-id="0b673-116">Las reglas almacenadas en los buzones de correo y las carpetas están asociadas con la aplicación que es el propietario por una cadena de proveedor de la regla.</span><span class="sxs-lookup"><span data-stu-id="0b673-116">Rules stored on mailboxes and folders are associated with the application that owns them by a rule provider string.</span></span> <span data-ttu-id="0b673-117">Un proveedor de regla establece y administra las reglas en una tabla de reglas.</span><span class="sxs-lookup"><span data-stu-id="0b673-117">A rule provider sets and handles rules in a rule table.</span></span> <span data-ttu-id="0b673-118">También proporciona un medio de controlar todas las acciones diferidas si estas reglas están establecidas.</span><span class="sxs-lookup"><span data-stu-id="0b673-118">It also provides a means of handling any deferred actions if such rules are set.</span></span> <span data-ttu-id="0b673-119">Acciones diferidas se crean implícitamente por el almacén de información.</span><span class="sxs-lookup"><span data-stu-id="0b673-119">Deferred actions are created implicitly by the information store.</span></span> <span data-ttu-id="0b673-120">Para las operaciones de mover o copiar a un almacén diferente, si un proveedor establece una regla de acción aplazada, debe proporcionar un controlador para llevar a cabo la acción cuando se desencadena la regla y se crea una acción aplazada.</span><span class="sxs-lookup"><span data-stu-id="0b673-120">For move or copy operations to a different store, if a provider sets a deferred action rule, it must provide a handler to perform the action when the rule is fired and a deferred action is created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0b673-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b673-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b673-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0b673-122">Protocol specifications</span></span>

<span data-ttu-id="0b673-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b673-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b673-124">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0b673-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0b673-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b673-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b673-126">Manipula los mensajes de correo electrónico entrante en un servidor.</span><span class="sxs-lookup"><span data-stu-id="0b673-126">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b673-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0b673-127">Header files</span></span>

<span data-ttu-id="0b673-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b673-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b673-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0b673-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="0b673-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0b673-130">Mapitags.h</span></span>
  
> <span data-ttu-id="0b673-131">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0b673-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b673-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b673-132">See also</span></span>



[<span data-ttu-id="0b673-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0b673-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b673-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0b673-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b673-135">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0b673-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b673-136">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0b673-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

