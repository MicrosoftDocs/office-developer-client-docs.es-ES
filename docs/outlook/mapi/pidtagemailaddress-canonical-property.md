---
title: Propiedad canónica PidTagEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmailAddress
api_type:
- HeaderDef
ms.assetid: bbd1e187-172e-4612-9efe-7c8e52967dfe
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: efcb72d872836adce544f3a90cf093de1f3713a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338643"
---
# <a name="pidtagemailaddress-canonical-property"></a><span data-ttu-id="fb0c2-103">Propiedad canónica PidTagEmailAddress</span><span class="sxs-lookup"><span data-stu-id="fb0c2-103">PidTagEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="fb0c2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb0c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb0c2-105">Contiene la dirección de correo electrónico del usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="fb0c2-105">Contains the messaging user's email address.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb0c2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fb0c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fb0c2-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="fb0c2-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="fb0c2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fb0c2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fb0c2-109">0x3003</span><span class="sxs-lookup"><span data-stu-id="fb0c2-109">0x3003</span></span>  <br/> |
|<span data-ttu-id="fb0c2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fb0c2-110">Data type:</span></span>  <br/> |<span data-ttu-id="fb0c2-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fb0c2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fb0c2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fb0c2-112">Area:</span></span>  <br/> |<span data-ttu-id="fb0c2-113">MAPI común</span><span class="sxs-lookup"><span data-stu-id="fb0c2-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb0c2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb0c2-114">Remarks</span></span>

<span data-ttu-id="fb0c2-115">Estas propiedades son ejemplos de las propiedades de dirección base para todos los usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="fb0c2-115">These properties are examples of the base address properties for all messaging users.</span></span> <span data-ttu-id="fb0c2-116">Es una cadena terminada en null cuyo formato solo tiene significado para el sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="fb0c2-116">It is a null-terminated string whose format has meaning only for the underlying messaging system.</span></span> 
  
<span data-ttu-id="fb0c2-117">Estas propiedades se usan junto con las propiedades **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) y **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) en el direccionamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="fb0c2-117">These properties are used in conjunction with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) properties in addressing messages.</span></span> <span data-ttu-id="fb0c2-118">El formato de cadena está calificado **por PR_ADDRTYPE**.</span><span class="sxs-lookup"><span data-stu-id="fb0c2-118">The string format is qualified by **PR_ADDRTYPE**.</span></span> 
  
<span data-ttu-id="fb0c2-119">Entre los valores válidos de esta propiedad se incluyen:</span><span class="sxs-lookup"><span data-stu-id="fb0c2-119">Valid values for this property include:</span></span> 
  
```cpp
network/postoffice/user 
Bruce@XYZZY.COM 
/c=US/a=att/p=Microsoft/o=Finance/ou=Purchasing/s=Furthur/g=Joe 
 
```

## <a name="related-resources"></a><span data-ttu-id="fb0c2-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fb0c2-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fb0c2-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="fb0c2-121">Protocol specifications</span></span>

<span data-ttu-id="fb0c2-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb0c2-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb0c2-123">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="fb0c2-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fb0c2-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb0c2-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb0c2-125">Especifica las propiedades y las operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="fb0c2-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="fb0c2-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb0c2-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb0c2-127">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="fb0c2-127">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fb0c2-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fb0c2-128">Header files</span></span>

<span data-ttu-id="fb0c2-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fb0c2-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="fb0c2-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fb0c2-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="fb0c2-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fb0c2-131">Mapitags.h</span></span>
  
> <span data-ttu-id="fb0c2-132">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fb0c2-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fb0c2-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb0c2-133">See also</span></span>



[<span data-ttu-id="fb0c2-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fb0c2-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fb0c2-135">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fb0c2-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fb0c2-136">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fb0c2-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fb0c2-137">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="fb0c2-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

