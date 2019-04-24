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
ms.openlocfilehash: b8ce3898ac021bc6eec2af6220889d71ff5a18dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316159"
---
# <a name="pidtaggender-canonical-property"></a><span data-ttu-id="1cc4d-103">Propiedad canónica PidTagGender</span><span class="sxs-lookup"><span data-stu-id="1cc4d-103">PidTagGender Canonical Property</span></span>

  
  
<span data-ttu-id="1cc4d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cc4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cc4d-105">Contiene el género del usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="1cc4d-105">Contains the gender of the messaging user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1cc4d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1cc4d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1cc4d-107">PR_GENDER</span><span class="sxs-lookup"><span data-stu-id="1cc4d-107">PR_GENDER</span></span>  <br/> |
|<span data-ttu-id="1cc4d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1cc4d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1cc4d-109">0x3A4D</span><span class="sxs-lookup"><span data-stu-id="1cc4d-109">0x3A4D</span></span>  <br/> |
|<span data-ttu-id="1cc4d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1cc4d-110">Data type:</span></span>  <br/> |<span data-ttu-id="1cc4d-111">PT_I2</span><span class="sxs-lookup"><span data-stu-id="1cc4d-111">PT_I2</span></span>  <br/> |
|<span data-ttu-id="1cc4d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1cc4d-112">Area:</span></span>  <br/> |<span data-ttu-id="1cc4d-113">Usuario de correo MAPI</span><span class="sxs-lookup"><span data-stu-id="1cc4d-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cc4d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1cc4d-114">Remarks</span></span>

<span data-ttu-id="1cc4d-115">Esta propiedad proporciona información de identificación y acceso sobre un usuario de mensajería y el contenido es.</span><span class="sxs-lookup"><span data-stu-id="1cc4d-115">This property provides identification and access information about a messaging user and the content is.</span></span> <span data-ttu-id="1cc4d-116">El contenido lo define el usuario de mensajería y la organización del usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="1cc4d-116">The content is defined by the messaging user and the messaging user's organization.</span></span> 
  
<span data-ttu-id="1cc4d-117">Los valores posibles para esta propiedad se definen en la enumeración Gender.</span><span class="sxs-lookup"><span data-stu-id="1cc4d-117">The possible values for this property are defined in the gender enumeration.</span></span> <span data-ttu-id="1cc4d-118">Aparecen de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1cc4d-118">They are listed as follows:</span></span>
  
|<span data-ttu-id="1cc4d-119">**Enumeración Gender**</span><span class="sxs-lookup"><span data-stu-id="1cc4d-119">**Gender enumeration**</span></span>|<span data-ttu-id="1cc4d-120">**Value**</span><span class="sxs-lookup"><span data-stu-id="1cc4d-120">**Value**</span></span>|<span data-ttu-id="1cc4d-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1cc4d-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1cc4d-122">genderUnspecified</span><span class="sxs-lookup"><span data-stu-id="1cc4d-122">genderUnspecified</span></span>  <br/> |<span data-ttu-id="1cc4d-123">0x0000</span><span class="sxs-lookup"><span data-stu-id="1cc4d-123">0x0000</span></span>  <br/> |<span data-ttu-id="1cc4d-124">No se ha especificado el sexo del contacto.</span><span class="sxs-lookup"><span data-stu-id="1cc4d-124">The contact's gender is unspecified.</span></span>  <br/> |
|<span data-ttu-id="1cc4d-125">genderFemale</span><span class="sxs-lookup"><span data-stu-id="1cc4d-125">genderFemale</span></span>  <br/> |<span data-ttu-id="1cc4d-126">0x0001</span><span class="sxs-lookup"><span data-stu-id="1cc4d-126">0x0001</span></span>  <br/> |<span data-ttu-id="1cc4d-127">El contacto es hembra.</span><span class="sxs-lookup"><span data-stu-id="1cc4d-127">The contact is female.</span></span>  <br/> |
|<span data-ttu-id="1cc4d-128">genderMale</span><span class="sxs-lookup"><span data-stu-id="1cc4d-128">genderMale</span></span>  <br/> |<span data-ttu-id="1cc4d-129">0x0002</span><span class="sxs-lookup"><span data-stu-id="1cc4d-129">0x0002</span></span>  <br/> |<span data-ttu-id="1cc4d-130">El contacto es macho.</span><span class="sxs-lookup"><span data-stu-id="1cc4d-130">The contact is male.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1cc4d-131">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1cc4d-131">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1cc4d-132">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1cc4d-132">Protocol specifications</span></span>

<span data-ttu-id="1cc4d-133">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cc4d-133">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cc4d-134">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1cc4d-134">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1cc4d-135">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cc4d-135">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cc4d-136">Especifica las propiedades y operaciones que se admiten para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="1cc4d-136">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="1cc4d-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cc4d-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cc4d-138">Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="1cc4d-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1cc4d-139">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1cc4d-139">Header files</span></span>

<span data-ttu-id="1cc4d-140">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1cc4d-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="1cc4d-141">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1cc4d-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="1cc4d-142">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="1cc4d-142">Mapitags.h</span></span>
  
> <span data-ttu-id="1cc4d-143">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1cc4d-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1cc4d-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cc4d-144">See also</span></span>



[<span data-ttu-id="1cc4d-145">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1cc4d-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1cc4d-146">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="1cc4d-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1cc4d-147">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1cc4d-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1cc4d-148">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="1cc4d-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

