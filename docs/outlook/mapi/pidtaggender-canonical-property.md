---
title: Propiedad canónica PidTagGender
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGender
api_type:
- HeaderDef
ms.assetid: a79a139a-6813-49f6-b622-bb66d62c4462
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1c2089eee731fea8c80d8811f6b2e9f3c75ad1cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570530"
---
# <a name="pidtaggender-canonical-property"></a><span data-ttu-id="edcb5-103">Propiedad canónica PidTagGender</span><span class="sxs-lookup"><span data-stu-id="edcb5-103">PidTagGender Canonical Property</span></span>

  
  
<span data-ttu-id="edcb5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edcb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edcb5-105">Contiene el género del usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="edcb5-105">Contains the gender of the messaging user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edcb5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="edcb5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="edcb5-107">PR_GENDER</span><span class="sxs-lookup"><span data-stu-id="edcb5-107">PR_GENDER</span></span>  <br/> |
|<span data-ttu-id="edcb5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="edcb5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="edcb5-109">0x3A4D</span><span class="sxs-lookup"><span data-stu-id="edcb5-109">0x3A4D</span></span>  <br/> |
|<span data-ttu-id="edcb5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="edcb5-110">Data type:</span></span>  <br/> |<span data-ttu-id="edcb5-111">PT_I2</span><span class="sxs-lookup"><span data-stu-id="edcb5-111">PT_I2</span></span>  <br/> |
|<span data-ttu-id="edcb5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="edcb5-112">Area:</span></span>  <br/> |<span data-ttu-id="edcb5-113">Usuario de correo MAPI</span><span class="sxs-lookup"><span data-stu-id="edcb5-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edcb5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edcb5-114">Remarks</span></span>

<span data-ttu-id="edcb5-115">Esta propiedad proporciona acceso a información sobre un usuario de mensajería e identificación y el contenido es.</span><span class="sxs-lookup"><span data-stu-id="edcb5-115">This property provides identification and access information about a messaging user and the content is.</span></span> <span data-ttu-id="edcb5-116">El contenido es definido por el usuario de mensajería y organización de mensajería del usuario.</span><span class="sxs-lookup"><span data-stu-id="edcb5-116">The content is defined by the messaging user and the messaging user's organization.</span></span> 
  
<span data-ttu-id="edcb5-117">Los valores posibles para esta propiedad se definen en la enumeración género.</span><span class="sxs-lookup"><span data-stu-id="edcb5-117">The possible values for this property are defined in the gender enumeration.</span></span> <span data-ttu-id="edcb5-118">Aparecen en la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="edcb5-118">They are listed as follows:</span></span>
  
|<span data-ttu-id="edcb5-119">**Enumeración de género**</span><span class="sxs-lookup"><span data-stu-id="edcb5-119">**Gender enumeration**</span></span>|<span data-ttu-id="edcb5-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="edcb5-120">**Value**</span></span>|<span data-ttu-id="edcb5-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="edcb5-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="edcb5-122">genderUnspecified</span><span class="sxs-lookup"><span data-stu-id="edcb5-122">genderUnspecified</span></span>  <br/> |<span data-ttu-id="edcb5-123">0x0000</span><span class="sxs-lookup"><span data-stu-id="edcb5-123">0x0000</span></span>  <br/> |<span data-ttu-id="edcb5-124">No se especifica el sexo del contacto.</span><span class="sxs-lookup"><span data-stu-id="edcb5-124">The contact's gender is unspecified.</span></span>  <br/> |
|<span data-ttu-id="edcb5-125">genderFemale</span><span class="sxs-lookup"><span data-stu-id="edcb5-125">genderFemale</span></span>  <br/> |<span data-ttu-id="edcb5-126">0 x 0001</span><span class="sxs-lookup"><span data-stu-id="edcb5-126">0x0001</span></span>  <br/> |<span data-ttu-id="edcb5-127">El contacto está femenino.</span><span class="sxs-lookup"><span data-stu-id="edcb5-127">The contact is female.</span></span>  <br/> |
|<span data-ttu-id="edcb5-128">genderMale</span><span class="sxs-lookup"><span data-stu-id="edcb5-128">genderMale</span></span>  <br/> |<span data-ttu-id="edcb5-129">0x0002</span><span class="sxs-lookup"><span data-stu-id="edcb5-129">0x0002</span></span>  <br/> |<span data-ttu-id="edcb5-130">El contacto está masculino.</span><span class="sxs-lookup"><span data-stu-id="edcb5-130">The contact is male.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="edcb5-131">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="edcb5-131">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="edcb5-132">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="edcb5-132">Protocol specifications</span></span>

<span data-ttu-id="edcb5-133">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edcb5-133">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edcb5-134">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="edcb5-134">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="edcb5-135">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edcb5-135">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edcb5-136">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="edcb5-136">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="edcb5-137">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edcb5-137">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edcb5-138">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="edcb5-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="edcb5-139">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="edcb5-139">Header files</span></span>

<span data-ttu-id="edcb5-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="edcb5-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="edcb5-141">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="edcb5-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="edcb5-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="edcb5-142">Mapitags.h</span></span>
  
> <span data-ttu-id="edcb5-143">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="edcb5-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edcb5-144">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="edcb5-144">See also</span></span>



[<span data-ttu-id="edcb5-145">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="edcb5-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="edcb5-146">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="edcb5-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="edcb5-147">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="edcb5-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="edcb5-148">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="edcb5-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

