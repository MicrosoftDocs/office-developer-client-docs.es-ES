---
title: Propiedad canónico PidLidAddressBookProviderArrayType
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 3515d0f751cb6d8d0d427079691456519bac97dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818463"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a><span data-ttu-id="9f793-103">Propiedad canónico PidLidAddressBookProviderArrayType</span><span class="sxs-lookup"><span data-stu-id="9f793-103">PidLidAddressBookProviderArrayType Canonical Property</span></span>

  
  
<span data-ttu-id="9f793-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f793-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f793-105">Especifica el estado de las direcciones de presentación electrónica del contacto y representa un conjunto de indicadores de bits.</span><span class="sxs-lookup"><span data-stu-id="9f793-105">Specifies the state of the contact's electronic addresses and represents a set of bit flags.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f793-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9f793-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f793-107">dispidABPArrayType</span><span class="sxs-lookup"><span data-stu-id="9f793-107">dispidABPArrayType</span></span>  <br/> |
|<span data-ttu-id="9f793-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="9f793-108">Property set:</span></span>  <br/> |<span data-ttu-id="9f793-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="9f793-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="9f793-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="9f793-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9f793-111">0x00008029</span><span class="sxs-lookup"><span data-stu-id="9f793-111">0x00008029</span></span>  <br/> |
|<span data-ttu-id="9f793-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9f793-112">Data type:</span></span>  <br/> |<span data-ttu-id="9f793-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9f793-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9f793-114">Área:</span><span class="sxs-lookup"><span data-stu-id="9f793-114">Area:</span></span>  <br/> |<span data-ttu-id="9f793-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="9f793-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f793-116">Notas</span><span class="sxs-lookup"><span data-stu-id="9f793-116">Remarks</span></span>

<span data-ttu-id="9f793-117">El valor de la propiedad **dispidABPArrayType** debe ser una combinación de marcadores que especifican el estado del objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="9f793-117">The value of the **dispidABPArrayType** property must be a combination of flags that specify the state of the contact object.</span></span> <span data-ttu-id="9f793-118">Indicadores individuales se especifican en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="9f793-118">Individual flags are specified in the following table.</span></span> <span data-ttu-id="9f793-119">Si se establece esta propiedad, la propiedad **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) debe establecerse, así como.</span><span class="sxs-lookup"><span data-stu-id="9f793-119">If this property is set, the **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) property must be set, as well.</span></span> <span data-ttu-id="9f793-120">Estas dos propiedades se deben mantener sincronizadas con cada una de las demás.</span><span class="sxs-lookup"><span data-stu-id="9f793-120">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="9f793-121">Por ejemplo, si **dispidABPArrayType** tiene el bit "0 x 00000001 conjunto", uno de los valores de **dispidABPEmailList** debe ser "0 x 00000000".</span><span class="sxs-lookup"><span data-stu-id="9f793-121">For example, if **dispidABPArrayType** has the bit "0x00000001 set", one of the values of **dispidABPEmailList** must be "0x00000000".</span></span> 
  
|<span data-ttu-id="9f793-122">**Bit**</span><span class="sxs-lookup"><span data-stu-id="9f793-122">**Bit**</span></span>|<span data-ttu-id="9f793-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9f793-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9f793-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9f793-124">0x00000001</span></span>  <br/> |<span data-ttu-id="9f793-125">Correo electrónico1 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="9f793-125">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="9f793-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9f793-126">0x00000002</span></span>  <br/> |<span data-ttu-id="9f793-127">Correo electrónico 2 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="9f793-127">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="9f793-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="9f793-128">0x00000004</span></span>  <br/> |<span data-ttu-id="9f793-129">Correo electrónico 3 se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="9f793-129">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="9f793-130">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="9f793-130">0x00000008</span></span>  <br/> |<span data-ttu-id="9f793-131">Fax del trabajo se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="9f793-131">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="9f793-132">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="9f793-132">0x00000010</span></span>  <br/> |<span data-ttu-id="9f793-133">Fax del domicilio particular se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="9f793-133">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="9f793-134">0 x 00000020</span><span class="sxs-lookup"><span data-stu-id="9f793-134">0x00000020</span></span>  <br/> |<span data-ttu-id="9f793-135">Fax principal se define para el contacto.</span><span class="sxs-lookup"><span data-stu-id="9f793-135">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9f793-136">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f793-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9f793-137">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9f793-137">Protocol specifications</span></span>

<span data-ttu-id="9f793-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f793-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f793-139">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9f793-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9f793-140">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f793-140">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f793-141">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="9f793-141">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9f793-142">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9f793-142">Header files</span></span>

<span data-ttu-id="9f793-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9f793-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f793-144">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9f793-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f793-145">Ver también</span><span class="sxs-lookup"><span data-stu-id="9f793-145">See also</span></span>



[<span data-ttu-id="9f793-146">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9f793-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f793-147">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9f793-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f793-148">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="9f793-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f793-149">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9f793-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

