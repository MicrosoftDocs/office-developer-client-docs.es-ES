---
title: Propiedad canónica PidTagMappingSignature
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342554"
---
# <a name="pidtagmappingsignature-canonical-property"></a><span data-ttu-id="90edb-103">Propiedad canónica PidTagMappingSignature</span><span class="sxs-lookup"><span data-stu-id="90edb-103">PidTagMappingSignature Canonical Property</span></span>

  
  
<span data-ttu-id="90edb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90edb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90edb-105">Contiene la firma de asignación de las propiedades con nombre de un objeto MAPI en particular.</span><span class="sxs-lookup"><span data-stu-id="90edb-105">Contains the mapping signature for named properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="90edb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="90edb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90edb-107">PR_MAPPING_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="90edb-107">PR_MAPPING_SIGNATURE</span></span>  <br/> |
|<span data-ttu-id="90edb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="90edb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90edb-109">0x0FF8</span><span class="sxs-lookup"><span data-stu-id="90edb-109">0x0FF8</span></span>  <br/> |
|<span data-ttu-id="90edb-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="90edb-110">Data type:</span></span>  <br/> |<span data-ttu-id="90edb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="90edb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="90edb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="90edb-112">Area:</span></span>  <br/> |<span data-ttu-id="90edb-113">Varios</span><span class="sxs-lookup"><span data-stu-id="90edb-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90edb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="90edb-114">Remarks</span></span>

<span data-ttu-id="90edb-115">Se recomienda que los objetos que tienen propiedades con nombre expongan esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="90edb-115">It is recommended that objects having named properties expose this property.</span></span> <span data-ttu-id="90edb-116">Una aplicación cliente debe comprobar la propiedad **PR_MAPPING_SIGNATURE** de ambos objetos cuando se copian propiedades con nombre de un objeto a otro.</span><span class="sxs-lookup"><span data-stu-id="90edb-116">A client application should check the **PR_MAPPING_SIGNATURE** property of both objects when copying named properties from one object to another.</span></span> <span data-ttu-id="90edb-117">El uso de esta propiedad puede minimizar la conversión entre los nombres y los identificadores de las propiedades que se han copiado.</span><span class="sxs-lookup"><span data-stu-id="90edb-117">Use of this property can minimize translating between copied properties' names and identifiers.</span></span> 
  
<span data-ttu-id="90edb-118">Si esta propiedad no existe para un objeto MAPI determinado, el objeto tiene su propia asignación única de nombres e identificadores.</span><span class="sxs-lookup"><span data-stu-id="90edb-118">If this property does not exist for a given MAPI object, then the object has its own unique mapping of names and identifiers.</span></span> <span data-ttu-id="90edb-119">En este caso, el cliente debe llamar al método [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) en el objeto de origen y, a continuación, al método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) en el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="90edb-119">In this case the client must call the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method on the source object and then the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method on the destination object.</span></span> 
  
<span data-ttu-id="90edb-120">Cuando dos objetos tienen el mismo valor **PR_MAPPING_SIGNATURE** , no es necesario que el cliente traduzca el nombre Identifier e Identifier a Name.</span><span class="sxs-lookup"><span data-stu-id="90edb-120">When two objects have the same **PR_MAPPING_SIGNATURE** value, the client does not need to translate name to identifier and identifier to name.</span></span> <span data-ttu-id="90edb-121">El cliente simplemente puede llamar al método [IMAPIProp:: GetProps](imapiprop-getprops.md) en el origen y, a continuación, al método [IMAPIProp:: SetProps](imapiprop-setprops.md) en el destino.</span><span class="sxs-lookup"><span data-stu-id="90edb-121">The client can simply call the [IMAPIProp::GetProps](imapiprop-getprops.md) method on the source and then the [IMAPIProp::SetProps](imapiprop-setprops.md) method on the destination.</span></span> <span data-ttu-id="90edb-122">Esto es conveniente para los clientes que realizan copias personalizadas de propiedades con nombre y para proveedores que implementan los métodos [IMAPIProp:: CopyTo](imapiprop-copyto.md) y [IMAPIProp:: CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="90edb-122">This is convenient for clients that perform custom copying of named properties, and for providers implementing the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) methods.</span></span> 
  
<span data-ttu-id="90edb-123">Para obtener más información acerca de las propiedades con nombre y la asignación de nombres e identificadores, consulte [MAPI con nombre de propiedades](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="90edb-123">For more information on named properties and mapping of names and identifiers, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="90edb-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="90edb-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90edb-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="90edb-125">Protocol specifications</span></span>

<span data-ttu-id="90edb-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90edb-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90edb-127">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="90edb-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="90edb-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90edb-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90edb-129">Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="90edb-129">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90edb-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="90edb-130">Header files</span></span>

<span data-ttu-id="90edb-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="90edb-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="90edb-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="90edb-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="90edb-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="90edb-133">Mapitags.h</span></span>
  
> <span data-ttu-id="90edb-134">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="90edb-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90edb-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="90edb-135">See also</span></span>



[<span data-ttu-id="90edb-136">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="90edb-136">MAPINAMEID</span></span>](mapinameid.md)


[<span data-ttu-id="90edb-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="90edb-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90edb-138">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="90edb-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90edb-139">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="90edb-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90edb-140">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="90edb-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

