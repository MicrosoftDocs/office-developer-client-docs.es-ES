---
title: Propiedad canónica PidLidAddressBookProviderArrayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 68396f210aab465da9cec4a74a3c24cc4e8578a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348443"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a><span data-ttu-id="439eb-103">Propiedad canónica PidLidAddressBookProviderArrayType</span><span class="sxs-lookup"><span data-stu-id="439eb-103">PidLidAddressBookProviderArrayType Canonical Property</span></span>

  
  
<span data-ttu-id="439eb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="439eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="439eb-105">Especifica el estado de las direcciones electrónicas del contacto y representa un conjunto de marcas de bits.</span><span class="sxs-lookup"><span data-stu-id="439eb-105">Specifies the state of the contact's electronic addresses and represents a set of bit flags.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="439eb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="439eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="439eb-107">dispidABPArrayType</span><span class="sxs-lookup"><span data-stu-id="439eb-107">dispidABPArrayType</span></span>  <br/> |
|<span data-ttu-id="439eb-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="439eb-108">Property set:</span></span>  <br/> |<span data-ttu-id="439eb-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="439eb-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="439eb-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="439eb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="439eb-111">0x00008029</span><span class="sxs-lookup"><span data-stu-id="439eb-111">0x00008029</span></span>  <br/> |
|<span data-ttu-id="439eb-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="439eb-112">Data type:</span></span>  <br/> |<span data-ttu-id="439eb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="439eb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="439eb-114">Área:</span><span class="sxs-lookup"><span data-stu-id="439eb-114">Area:</span></span>  <br/> |<span data-ttu-id="439eb-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="439eb-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="439eb-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="439eb-116">Remarks</span></span>

<span data-ttu-id="439eb-117">El valor de la **propiedad dispidABPArrayType** debe ser una combinación de marcas que especifiquen el estado del objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="439eb-117">The value of the **dispidABPArrayType** property must be a combination of flags that specify the state of the contact object.</span></span> <span data-ttu-id="439eb-118">Las marcas individuales se especifican en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="439eb-118">Individual flags are specified in the following table.</span></span> <span data-ttu-id="439eb-119">Si se establece esta propiedad, también se debe establecer la propiedad **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="439eb-119">If this property is set, the **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) property must be set, as well.</span></span> <span data-ttu-id="439eb-120">Estas dos propiedades deben mantenerse sincronizadas entre sí.</span><span class="sxs-lookup"><span data-stu-id="439eb-120">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="439eb-121">Por ejemplo, si **dispidABPArrayType** tiene el bit "0x00000001 set", uno de los valores de **dispidABPEmailList** debe ser "0x00000000".</span><span class="sxs-lookup"><span data-stu-id="439eb-121">For example, if **dispidABPArrayType** has the bit "0x00000001 set", one of the values of **dispidABPEmailList** must be "0x00000000".</span></span> 
  
|<span data-ttu-id="439eb-122">**Bit**</span><span class="sxs-lookup"><span data-stu-id="439eb-122">**Bit**</span></span>|<span data-ttu-id="439eb-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="439eb-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="439eb-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="439eb-124">0x00000001</span></span>  <br/> |<span data-ttu-id="439eb-125">Email1 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="439eb-125">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="439eb-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="439eb-126">0x00000002</span></span>  <br/> |<span data-ttu-id="439eb-127">Email2 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="439eb-127">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="439eb-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="439eb-128">0x00000004</span></span>  <br/> |<span data-ttu-id="439eb-129">Email3 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="439eb-129">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="439eb-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="439eb-130">0x00000008</span></span>  <br/> |<span data-ttu-id="439eb-131">El fax de empresa se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="439eb-131">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="439eb-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="439eb-132">0x00000010</span></span>  <br/> |<span data-ttu-id="439eb-133">El fax principal se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="439eb-133">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="439eb-134">0x00000020</span><span class="sxs-lookup"><span data-stu-id="439eb-134">0x00000020</span></span>  <br/> |<span data-ttu-id="439eb-135">El fax principal se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="439eb-135">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="439eb-136">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="439eb-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="439eb-137">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="439eb-137">Protocol specifications</span></span>

<span data-ttu-id="439eb-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="439eb-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="439eb-139">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="439eb-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="439eb-140">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="439eb-140">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="439eb-141">Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="439eb-141">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="439eb-142">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="439eb-142">Header files</span></span>

<span data-ttu-id="439eb-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="439eb-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="439eb-144">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="439eb-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="439eb-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="439eb-145">See also</span></span>



[<span data-ttu-id="439eb-146">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="439eb-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="439eb-147">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="439eb-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="439eb-148">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="439eb-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="439eb-149">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="439eb-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

