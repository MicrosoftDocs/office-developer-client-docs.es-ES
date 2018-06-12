---
title: Propiedad canónico PidLidAddressBookProviderEmailList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderEmailList
api_type:
- COM
ms.assetid: 9c0527ea-e922-4514-b913-d3520350c452
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 4eb2897c1834715f3d937ef7946998943b386aef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818488"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="e2360-103">Propiedad canónico PidLidAddressBookProviderEmailList</span><span class="sxs-lookup"><span data-stu-id="e2360-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="e2360-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2360-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2360-105">Especifica qué propiedades de dirección electrónica se establecen en el contacto.</span><span class="sxs-lookup"><span data-stu-id="e2360-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2360-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e2360-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2360-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="e2360-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="e2360-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e2360-108">Property set:</span></span>  <br/> |<span data-ttu-id="e2360-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="e2360-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="e2360-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="e2360-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e2360-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="e2360-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="e2360-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e2360-112">Data type:</span></span>  <br/> |<span data-ttu-id="e2360-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="e2360-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="e2360-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e2360-114">Area:</span></span>  <br/> |<span data-ttu-id="e2360-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="e2360-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2360-116">Notas</span><span class="sxs-lookup"><span data-stu-id="e2360-116">Remarks</span></span>

<span data-ttu-id="e2360-117">Cada valor PT_LONG en esta propiedad debe ser único en la propiedad y debe establecerse en uno de los valores en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e2360-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="e2360-118">Si se establece esta propiedad, también se debe establecer la propiedad **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e2360-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="e2360-119">Estas dos propiedades se deben mantener sincronizadas con cada una de las demás.</span><span class="sxs-lookup"><span data-stu-id="e2360-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="e2360-120">Por ejemplo, si uno de los valores de **dispidABPEmailList** es "0 x 00000000" y, a continuación, **dispidABPArrayType** debe haber establecido el bit "0 x 00000001".</span><span class="sxs-lookup"><span data-stu-id="e2360-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="e2360-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e2360-121">**Value**</span></span>|<span data-ttu-id="e2360-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e2360-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e2360-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2360-123">0x00000000</span></span>  <br/> |<span data-ttu-id="e2360-124">Correo electrónico1 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="e2360-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="e2360-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e2360-125">0x00000001</span></span>  <br/> |<span data-ttu-id="e2360-126">Correo electrónico 2 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="e2360-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="e2360-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e2360-127">0x00000002</span></span>  <br/> |<span data-ttu-id="e2360-128">Correo electrónico 3 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="e2360-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="e2360-129">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="e2360-129">0x00000003</span></span>  <br/> |<span data-ttu-id="e2360-130">Fax del trabajo se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="e2360-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="e2360-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="e2360-131">0x00000004</span></span>  <br/> |<span data-ttu-id="e2360-132">Fax del domicilio particular se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="e2360-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="e2360-133">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="e2360-133">0x00000005</span></span>  <br/> |<span data-ttu-id="e2360-134">Fax principal se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="e2360-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e2360-135">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2360-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2360-136">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e2360-136">Protocol specifications</span></span>

<span data-ttu-id="e2360-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2360-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2360-138">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e2360-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2360-139">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2360-139">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2360-140">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="e2360-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2360-141">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e2360-141">Header files</span></span>

<span data-ttu-id="e2360-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2360-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2360-143">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e2360-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2360-144">Ver también</span><span class="sxs-lookup"><span data-stu-id="e2360-144">See also</span></span>



[<span data-ttu-id="e2360-145">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e2360-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2360-146">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e2360-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2360-147">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="e2360-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2360-148">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e2360-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

