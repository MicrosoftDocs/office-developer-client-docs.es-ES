---
title: Propiedad canónica PidLidAddressBookProviderEmailList
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9f73720860aa0ec54289f25a553bb00bfbe76b6a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581051"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="a5170-103">Propiedad canónica PidLidAddressBookProviderEmailList</span><span class="sxs-lookup"><span data-stu-id="a5170-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="a5170-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5170-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5170-105">Especifica qué propiedades de dirección electrónica se establecen en el contacto.</span><span class="sxs-lookup"><span data-stu-id="a5170-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5170-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a5170-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5170-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="a5170-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="a5170-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="a5170-108">Property set:</span></span>  <br/> |<span data-ttu-id="a5170-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="a5170-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="a5170-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="a5170-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a5170-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="a5170-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="a5170-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a5170-112">Data type:</span></span>  <br/> |<span data-ttu-id="a5170-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="a5170-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="a5170-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a5170-114">Area:</span></span>  <br/> |<span data-ttu-id="a5170-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="a5170-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5170-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5170-116">Remarks</span></span>

<span data-ttu-id="a5170-117">Cada valor PT_LONG en esta propiedad debe ser único en la propiedad y debe establecerse en uno de los valores en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a5170-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="a5170-118">Si se establece esta propiedad, también se debe establecer la propiedad **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a5170-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="a5170-119">Estas dos propiedades se deben mantener sincronizadas con cada una de las demás.</span><span class="sxs-lookup"><span data-stu-id="a5170-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="a5170-120">Por ejemplo, si uno de los valores de **dispidABPEmailList** es "0 x 00000000" y, a continuación, **dispidABPArrayType** debe haber establecido el bit "0 x 00000001".</span><span class="sxs-lookup"><span data-stu-id="a5170-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="a5170-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a5170-121">**Value**</span></span>|<span data-ttu-id="a5170-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a5170-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a5170-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5170-123">0x00000000</span></span>  <br/> |<span data-ttu-id="a5170-124">Correo electrónico1 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="a5170-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="a5170-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a5170-125">0x00000001</span></span>  <br/> |<span data-ttu-id="a5170-126">Correo electrónico 2 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="a5170-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="a5170-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a5170-127">0x00000002</span></span>  <br/> |<span data-ttu-id="a5170-128">Correo electrónico 3 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="a5170-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="a5170-129">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="a5170-129">0x00000003</span></span>  <br/> |<span data-ttu-id="a5170-130">Fax del trabajo se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="a5170-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="a5170-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="a5170-131">0x00000004</span></span>  <br/> |<span data-ttu-id="a5170-132">Fax del domicilio particular se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="a5170-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="a5170-133">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="a5170-133">0x00000005</span></span>  <br/> |<span data-ttu-id="a5170-134">Fax principal se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="a5170-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a5170-135">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5170-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5170-136">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a5170-136">Protocol specifications</span></span>

<span data-ttu-id="a5170-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5170-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5170-138">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a5170-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5170-139">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5170-139">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5170-140">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="a5170-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5170-141">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a5170-141">Header files</span></span>

<span data-ttu-id="a5170-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5170-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5170-143">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a5170-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5170-144">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a5170-144">See also</span></span>



[<span data-ttu-id="a5170-145">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a5170-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5170-146">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a5170-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5170-147">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a5170-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5170-148">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="a5170-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

