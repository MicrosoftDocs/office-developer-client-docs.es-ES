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
ms.openlocfilehash: 053ec531f69ff7734872466b7a661beff3177b2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348485"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="37e35-103">Propiedad canónica PidLidAddressBookProviderEmailList</span><span class="sxs-lookup"><span data-stu-id="37e35-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="37e35-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37e35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37e35-105">Especifica qué propiedades de la dirección electrónica se establecen en el contacto.</span><span class="sxs-lookup"><span data-stu-id="37e35-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37e35-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="37e35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37e35-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="37e35-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="37e35-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="37e35-108">Property set:</span></span>  <br/> |<span data-ttu-id="37e35-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="37e35-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="37e35-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="37e35-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="37e35-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="37e35-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="37e35-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="37e35-112">Data type:</span></span>  <br/> |<span data-ttu-id="37e35-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="37e35-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="37e35-114">Área:</span><span class="sxs-lookup"><span data-stu-id="37e35-114">Area:</span></span>  <br/> |<span data-ttu-id="37e35-115">Contact</span><span class="sxs-lookup"><span data-stu-id="37e35-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37e35-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37e35-116">Remarks</span></span>

<span data-ttu-id="37e35-117">Cada valor PT_LONG de esta propiedad debe ser único en la propiedad y debe establecerse en uno de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="37e35-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="37e35-118">Si se establece esta propiedad, también se debe establecer la propiedad **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="37e35-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="37e35-119">Estas dos propiedades deben mantenerse sincronizadas entre sí.</span><span class="sxs-lookup"><span data-stu-id="37e35-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="37e35-120">Por ejemplo, si uno de los valores de **dispidABPEmailList** es "0x00000000", **dispidABPArrayType** debe tener establecido el bit "0x00000001".</span><span class="sxs-lookup"><span data-stu-id="37e35-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="37e35-121">**Value**</span><span class="sxs-lookup"><span data-stu-id="37e35-121">**Value**</span></span>|<span data-ttu-id="37e35-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37e35-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37e35-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37e35-123">0x00000000</span></span>  <br/> |<span data-ttu-id="37e35-124">Email1 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="37e35-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="37e35-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="37e35-125">0x00000001</span></span>  <br/> |<span data-ttu-id="37e35-126">Email2 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="37e35-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="37e35-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="37e35-127">0x00000002</span></span>  <br/> |<span data-ttu-id="37e35-128">Email3 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="37e35-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="37e35-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="37e35-129">0x00000003</span></span>  <br/> |<span data-ttu-id="37e35-130">El fax comercial se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="37e35-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="37e35-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="37e35-131">0x00000004</span></span>  <br/> |<span data-ttu-id="37e35-132">El fax particular se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="37e35-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="37e35-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="37e35-133">0x00000005</span></span>  <br/> |<span data-ttu-id="37e35-134">Se ha definido el fax principal para el contacto.</span><span class="sxs-lookup"><span data-stu-id="37e35-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="37e35-135">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="37e35-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="37e35-136">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="37e35-136">Protocol specifications</span></span>

<span data-ttu-id="37e35-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37e35-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37e35-138">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="37e35-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="37e35-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37e35-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37e35-140">Especifica las propiedades y operaciones que se admiten para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="37e35-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="37e35-141">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="37e35-141">Header files</span></span>

<span data-ttu-id="37e35-142">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="37e35-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="37e35-143">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="37e35-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37e35-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="37e35-144">See also</span></span>



[<span data-ttu-id="37e35-145">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="37e35-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37e35-146">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="37e35-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37e35-147">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="37e35-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37e35-148">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="37e35-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

