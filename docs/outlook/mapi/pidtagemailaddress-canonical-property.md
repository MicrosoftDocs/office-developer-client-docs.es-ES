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
# <a name="pidtagemailaddress-canonical-property"></a><span data-ttu-id="dddb8-103">Propiedad canónica PidTagEmailAddress</span><span class="sxs-lookup"><span data-stu-id="dddb8-103">PidTagEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="dddb8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dddb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dddb8-105">Contiene la dirección de correo electrónico del usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="dddb8-105">Contains the messaging user's email address.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dddb8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="dddb8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dddb8-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="dddb8-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="dddb8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dddb8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dddb8-109">0x3003</span><span class="sxs-lookup"><span data-stu-id="dddb8-109">0x3003</span></span>  <br/> |
|<span data-ttu-id="dddb8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="dddb8-110">Data type:</span></span>  <br/> |<span data-ttu-id="dddb8-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dddb8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dddb8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dddb8-112">Area:</span></span>  <br/> |<span data-ttu-id="dddb8-113">Common MAPI</span><span class="sxs-lookup"><span data-stu-id="dddb8-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dddb8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dddb8-114">Remarks</span></span>

<span data-ttu-id="dddb8-115">Estas propiedades son ejemplos de las propiedades de dirección base para todos los usuarios de la mensajería.</span><span class="sxs-lookup"><span data-stu-id="dddb8-115">These properties are examples of the base address properties for all messaging users.</span></span> <span data-ttu-id="dddb8-116">Se trata de una cadena terminada en NULL cuyo formato solo tiene significado para el sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="dddb8-116">It is a null-terminated string whose format has meaning only for the underlying messaging system.</span></span> 
  
<span data-ttu-id="dddb8-117">Estas propiedades se usan junto con las propiedades **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) y **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) en la dirección de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="dddb8-117">These properties are used in conjunction with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) properties in addressing messages.</span></span> <span data-ttu-id="dddb8-118">El formato de la cadena está cualificado por **PR_ADDRTYPE**.</span><span class="sxs-lookup"><span data-stu-id="dddb8-118">The string format is qualified by **PR_ADDRTYPE**.</span></span> 
  
<span data-ttu-id="dddb8-119">Los valores válidos para esta propiedad son:</span><span class="sxs-lookup"><span data-stu-id="dddb8-119">Valid values for this property include:</span></span> 
  
```cpp
network/postoffice/user 
Bruce@XYZZY.COM 
/c=US/a=att/p=Microsoft/o=Finance/ou=Purchasing/s=Furthur/g=Joe 
 
```

## <a name="related-resources"></a><span data-ttu-id="dddb8-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dddb8-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dddb8-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="dddb8-121">Protocol specifications</span></span>

<span data-ttu-id="dddb8-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dddb8-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dddb8-123">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="dddb8-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dddb8-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dddb8-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dddb8-125">Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="dddb8-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="dddb8-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dddb8-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dddb8-127">Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="dddb8-127">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dddb8-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="dddb8-128">Header files</span></span>

<span data-ttu-id="dddb8-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dddb8-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="dddb8-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="dddb8-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="dddb8-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="dddb8-131">Mapitags.h</span></span>
  
> <span data-ttu-id="dddb8-132">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="dddb8-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dddb8-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="dddb8-133">See also</span></span>



[<span data-ttu-id="dddb8-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dddb8-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dddb8-135">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="dddb8-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dddb8-136">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="dddb8-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dddb8-137">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="dddb8-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

