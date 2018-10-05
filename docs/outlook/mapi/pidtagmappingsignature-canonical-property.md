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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396228"
---
# <a name="pidtagmappingsignature-canonical-property"></a><span data-ttu-id="d3de2-103">Propiedad canónica PidTagMappingSignature</span><span class="sxs-lookup"><span data-stu-id="d3de2-103">PidTagMappingSignature Canonical Property</span></span>

  
  
<span data-ttu-id="d3de2-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3de2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3de2-105">Contiene la firma de asignación para propiedades con nombre de un determinado objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="d3de2-105">Contains the mapping signature for named properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3de2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d3de2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d3de2-107">PR_MAPPING_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="d3de2-107">PR_MAPPING_SIGNATURE</span></span>  <br/> |
|<span data-ttu-id="d3de2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d3de2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d3de2-109">0x0FF8</span><span class="sxs-lookup"><span data-stu-id="d3de2-109">0x0FF8</span></span>  <br/> |
|<span data-ttu-id="d3de2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d3de2-110">Data type:</span></span>  <br/> |<span data-ttu-id="d3de2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d3de2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d3de2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d3de2-112">Area:</span></span>  <br/> |<span data-ttu-id="d3de2-113">Varios</span><span class="sxs-lookup"><span data-stu-id="d3de2-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3de2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d3de2-114">Remarks</span></span>

<span data-ttu-id="d3de2-115">Se recomienda que objetos tener propiedades con nombre exponen esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d3de2-115">It is recommended that objects having named properties expose this property.</span></span> <span data-ttu-id="d3de2-116">Una aplicación cliente debe comprobar la propiedad **PR_MAPPING_SIGNATURE** de ambos objetos al copiar las propiedades de un objeto a otro con nombre.</span><span class="sxs-lookup"><span data-stu-id="d3de2-116">A client application should check the **PR_MAPPING_SIGNATURE** property of both objects when copying named properties from one object to another.</span></span> <span data-ttu-id="d3de2-117">Uso de esta propiedad puede minimizar la traducción entre nombres e identificadores de las propiedades copiadas.</span><span class="sxs-lookup"><span data-stu-id="d3de2-117">Use of this property can minimize translating between copied properties' names and identifiers.</span></span> 
  
<span data-ttu-id="d3de2-118">Si esta propiedad no existe para un determinado objeto MAPI, a continuación, el objeto tiene su propia asignación de nombres y los identificadores único.</span><span class="sxs-lookup"><span data-stu-id="d3de2-118">If this property does not exist for a given MAPI object, then the object has its own unique mapping of names and identifiers.</span></span> <span data-ttu-id="d3de2-119">En este caso el cliente debe llamar al método [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) en el objeto de origen y, a continuación, el método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) en el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="d3de2-119">In this case the client must call the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method on the source object and then the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method on the destination object.</span></span> 
  
<span data-ttu-id="d3de2-120">Cuando dos objetos tienen el mismo valor **PR_MAPPING_SIGNATURE** , el cliente no necesita traducir el nombre de identificador y el identificador para el nombre.</span><span class="sxs-lookup"><span data-stu-id="d3de2-120">When two objects have the same **PR_MAPPING_SIGNATURE** value, the client does not need to translate name to identifier and identifier to name.</span></span> <span data-ttu-id="d3de2-121">El cliente puede llamar simplemente al método [IMAPIProp::GetProps](imapiprop-getprops.md) en el origen y, a continuación, el método [IMAPIProp::SetProps](imapiprop-setprops.md) en el destino.</span><span class="sxs-lookup"><span data-stu-id="d3de2-121">The client can simply call the [IMAPIProp::GetProps](imapiprop-getprops.md) method on the source and then the [IMAPIProp::SetProps](imapiprop-setprops.md) method on the destination.</span></span> <span data-ttu-id="d3de2-122">Esto es conveniente para los clientes que realizan copiar personalizado de propiedades con nombre y para los proveedores que implementan los métodos [IMAPIProp::CopyTo](imapiprop-copyto.md) y [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="d3de2-122">This is convenient for clients that perform custom copying of named properties, and for providers implementing the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) methods.</span></span> 
  
<span data-ttu-id="d3de2-123">Para obtener más información sobre las propiedades con nombre y la asignación de nombres y los identificadores, consulte [Propiedades de nombre de MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d3de2-123">For more information on named properties and mapping of names and identifiers, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d3de2-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3de2-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d3de2-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d3de2-125">Protocol specifications</span></span>

<span data-ttu-id="d3de2-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3de2-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3de2-127">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d3de2-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d3de2-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3de2-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3de2-129">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="d3de2-129">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d3de2-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d3de2-130">Header files</span></span>

<span data-ttu-id="d3de2-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d3de2-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="d3de2-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d3de2-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="d3de2-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d3de2-133">Mapitags.h</span></span>
  
> <span data-ttu-id="d3de2-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d3de2-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d3de2-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3de2-135">See also</span></span>



[<span data-ttu-id="d3de2-136">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="d3de2-136">MAPINAMEID</span></span>](mapinameid.md)


[<span data-ttu-id="d3de2-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d3de2-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d3de2-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d3de2-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d3de2-139">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d3de2-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d3de2-140">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d3de2-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

