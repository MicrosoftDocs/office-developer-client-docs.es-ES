---
title: Propiedad canónica PidTagAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressType
api_type:
- HeaderDef
ms.assetid: 986719d2-8837-46b4-8d04-c24508f5e19a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6051d3403cede21fa4aebdb6ca561dd3efb46771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360091"
---
# <a name="pidtagaddresstype-canonical-property"></a><span data-ttu-id="05fa4-103">Propiedad canónica PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="05fa4-103">PidTagAddressType Canonical Property</span></span>

<span data-ttu-id="05fa4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05fa4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05fa4-105">Contiene el tipo de dirección de correo electrónico del usuario de mensajería, como SMTP.</span><span class="sxs-lookup"><span data-stu-id="05fa4-105">Contains the messaging user's email address type, such as SMTP.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05fa4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="05fa4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05fa4-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="05fa4-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="05fa4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="05fa4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="05fa4-109">0x3002</span><span class="sxs-lookup"><span data-stu-id="05fa4-109">0x3002</span></span>  <br/> |
|<span data-ttu-id="05fa4-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="05fa4-110">Data type:</span></span>  <br/> |<span data-ttu-id="05fa4-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="05fa4-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="05fa4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="05fa4-112">Area:</span></span>  <br/> |<span data-ttu-id="05fa4-113">Address</span><span class="sxs-lookup"><span data-stu-id="05fa4-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05fa4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="05fa4-114">Remarks</span></span>

<span data-ttu-id="05fa4-115">Estas propiedades son ejemplos de las propiedades de dirección base comunes a todos los usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="05fa4-115">These properties are examples of the base address properties common to all messaging users.</span></span> <span data-ttu-id="05fa4-116">Especifica qué sistema de mensajería mapi usa para controlar un mensaje determinado.</span><span class="sxs-lookup"><span data-stu-id="05fa4-116">It specifies which messaging system MAPI uses to handle a given message.</span></span>
  
<span data-ttu-id="05fa4-117">Esta propiedad también determina el formato de la cadena de dirección **en el PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="05fa4-117">This property also determines the format of the address string in the **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="05fa4-118">La cadena que proporciona puede contener solo los caracteres alfabéticos en mayúsculas de la A a la Z y los números del 0 al 9.</span><span class="sxs-lookup"><span data-stu-id="05fa4-118">The string it provides can contain only the uppercase alphabetic characters from A through Z and the numbers from 0 through 9.</span></span>
  
<span data-ttu-id="05fa4-119">Entre los ejemplos válidos de la cadena se incluyen:</span><span class="sxs-lookup"><span data-stu-id="05fa4-119">Valid examples for the string include:</span></span> 
  
```cpp
FAX
MHS
PROFS
SMTP
X400

```

## <a name="related-resources"></a><span data-ttu-id="05fa4-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="05fa4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="05fa4-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="05fa4-121">Protocol specifications</span></span>

<span data-ttu-id="05fa4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05fa4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05fa4-123">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="05fa4-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="05fa4-124">[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05fa4-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05fa4-125">Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="05fa4-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="05fa4-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05fa4-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05fa4-127">Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="05fa4-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="05fa4-128">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05fa4-128">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05fa4-129">Controla las comunicaciones de un cliente con un servidor de interfaz de proveedor de servicios de nombres (NSPI).</span><span class="sxs-lookup"><span data-stu-id="05fa4-129">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="05fa4-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05fa4-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05fa4-131">Define las estructuras de datos básicas que se usan en operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="05fa4-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="05fa4-132">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05fa4-132">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05fa4-133">Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="05fa4-133">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="05fa4-134">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05fa4-134">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05fa4-135">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="05fa4-135">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="05fa4-136">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05fa4-136">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05fa4-137">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="05fa4-137">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="05fa4-138">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05fa4-138">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05fa4-139">Especifica las operaciones permitidas para los objetos principales del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="05fa4-139">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="05fa4-140">[[MS-OJOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05fa4-140">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05fa4-141">Especifica las propiedades y operaciones permitidas para las plantillas de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="05fa4-141">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="05fa4-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05fa4-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05fa4-143">Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="05fa4-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="05fa4-144">[[MS-OJORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05fa4-144">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05fa4-145">Manipula los mensajes de correo electrónico entrantes en un servidor.</span><span class="sxs-lookup"><span data-stu-id="05fa4-145">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="05fa4-146">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05fa4-146">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05fa4-147">Especifica las propiedades y las operaciones para manipular una configuración de lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="05fa4-147">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="05fa4-148">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="05fa4-148">Header files</span></span>

<span data-ttu-id="05fa4-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05fa4-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="05fa4-150">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="05fa4-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="05fa4-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="05fa4-151">Mapitags.h</span></span>
  
> <span data-ttu-id="05fa4-152">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="05fa4-152">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05fa4-153">Consulte también</span><span class="sxs-lookup"><span data-stu-id="05fa4-153">See also</span></span>



[<span data-ttu-id="05fa4-154">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="05fa4-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05fa4-155">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="05fa4-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05fa4-156">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="05fa4-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05fa4-157">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="05fa4-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
  
[<span data-ttu-id="05fa4-158">Tipos de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="05fa4-158">MAPI Address Types</span></span>](mapi-address-types.md)

