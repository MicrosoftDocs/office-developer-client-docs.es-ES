---
title: Propiedad canónica PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326127"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a><span data-ttu-id="f5a89-103">Propiedad canónica PidTagAddressBookHierarchicalRootDepartment</span><span class="sxs-lookup"><span data-stu-id="f5a89-103">PidTagAddressBookHierarchicalRootDepartment</span></span>

  
  
<span data-ttu-id="f5a89-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5a89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="f5a89-105">Contiene el nombre distintivo (DN) de la raíz jerárquica de la dirección (HAB).</span><span class="sxs-lookup"><span data-stu-id="f5a89-105">Contains the distinguished name (DN) of the hierarchical address root (HAB).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f5a89-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f5a89-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5a89-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span><span class="sxs-lookup"><span data-stu-id="f5a89-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span></span>  <br/> |
|<span data-ttu-id="f5a89-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="f5a89-108">Property set:</span></span>  <br/> |<span data-ttu-id="f5a89-109">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="f5a89-109">Address Book</span></span>  <br/> |
|<span data-ttu-id="f5a89-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f5a89-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f5a89-111">0x8C98</span><span class="sxs-lookup"><span data-stu-id="f5a89-111">0x8C98</span></span>  <br/> |
|<span data-ttu-id="f5a89-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f5a89-112">Data type:</span></span>  <br/> |<span data-ttu-id="f5a89-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="f5a89-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="f5a89-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f5a89-114">Area:</span></span>  <br/> |<span data-ttu-id="f5a89-115">Libreta de direcciones de Exchange</span><span class="sxs-lookup"><span data-stu-id="f5a89-115">Exchange Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5a89-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f5a89-116">Remarks</span></span>

<span data-ttu-id="f5a89-117">Se trata de una propiedad del contenedor de la lista global de direcciones (GAL) y representa el nombre distintivo de la raíz jerárquica de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f5a89-117">This is a property on the global address list (GAL) container and represents the distinguished name of the hierarchical address root.</span></span> <span data-ttu-id="f5a89-118">Esta propiedad solo está presente en la libreta de direcciones sin conexión y nunca en los Servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="f5a89-118">This property is only present in the offline address book and never in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="f5a89-119">Los autores de llamadas deben MAPI_CACHE_ONLY a la llamada GetProps para evitar una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="f5a89-119">Callers should pass MAPI_CACHE_ONLY to the GetProps call to avoid a remote procedure call.</span></span> <span data-ttu-id="f5a89-120">Si no está presente, los autores de llamadas deben usar PR_EMS_AB_HAB_ROOT_DEPARTMENT, que es de tipo PT_OBJECT, para encontrar el departamento raíz.</span><span class="sxs-lookup"><span data-stu-id="f5a89-120">If this is not present, callers should use PR_EMS_AB_HAB_ROOT_DEPARTMENT, which is of type PT_OBJECT, to find the root department.</span></span> 
  
<span data-ttu-id="f5a89-121">Una vez que se obtiene el departamento raíz, puede tener un tipo de objeto MAPI_MAILUSER o MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="f5a89-121">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="f5a89-122">Si el tipo de objeto MAPI_DISTLIST, se está empleando el nuevo esquema.</span><span class="sxs-lookup"><span data-stu-id="f5a89-122">If the object type is MAPI_DISTLIST, the new schema is being employed.</span></span> <span data-ttu-id="f5a89-123">Si el tipo de objeto MAPI_MAILUSER, se está empleando el esquema anterior.</span><span class="sxs-lookup"><span data-stu-id="f5a89-123">If the object type is MAPI_MAILUSER, the previous schema is being employed.</span></span> 
  
- <span data-ttu-id="f5a89-124">Microsoft Office Outlook 2007 Service Pack 2 admite ambos esquemas.</span><span class="sxs-lookup"><span data-stu-id="f5a89-124">Microsoft Office Outlook 2007 Service Pack 2 supports both schemas.</span></span> 
    
- <span data-ttu-id="f5a89-125">Microsoft Outlook 2010 y Microsoft Outlook 2013 admiten el nuevo esquema.</span><span class="sxs-lookup"><span data-stu-id="f5a89-125">Microsoft Outlook 2010 and Microsoft Outlook 2013 support the new schema.</span></span>
    
<span data-ttu-id="f5a89-126">En el nuevo esquema, todos los grupos departamentales también son listas de distribución y son de tipo MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="f5a89-126">In the new schema, all departmental groups are also distribution lists and are of type MAPI_DISTLIST.</span></span> <span data-ttu-id="f5a89-127">Los miembros de los grupos departamentales y los departamentos dentro de los grupos departamentales se obtienen mediante PR_EMS_AB_MEMBER, exactamente igual que los miembros de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="f5a89-127">Members of departmental groups, and departments within departmental groups are obtained by using PR_EMS_AB_MEMBER, exactly like distribution list members.</span></span>
  
<span data-ttu-id="f5a89-128">Una vez que se obtiene el departamento raíz, puede tener un tipo de objeto MAPI_MAILUSER o MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="f5a89-128">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="f5a89-129">Si el tipo de objeto MAPI_DISTLIST, se usa el nuevo esquema.</span><span class="sxs-lookup"><span data-stu-id="f5a89-129">If the object type is MAPI_DISTLIST, the new schema is being used.</span></span> <span data-ttu-id="f5a89-130">Si el tipo de objeto MAPI_MAILUSER, se usa el esquema antiguo.</span><span class="sxs-lookup"><span data-stu-id="f5a89-130">If the object type is MAPI_MAILUSER, the old schema is being used.</span></span> 
  
<span data-ttu-id="f5a89-131">En el nuevo esquema, todos los grupos departamentales también son DLs y son de tipo MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="f5a89-131">In the new schema, all departmental groups are also DLs and are of type MAPI_DISTLIST.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f5a89-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5a89-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5a89-133">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="f5a89-133">Protocol specifications</span></span>

<span data-ttu-id="f5a89-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5a89-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5a89-135">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Microsoft Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="f5a89-135">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5a89-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f5a89-136">Header files</span></span>

<span data-ttu-id="f5a89-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5a89-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5a89-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f5a89-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5a89-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f5a89-139">See also</span></span>



[<span data-ttu-id="f5a89-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f5a89-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5a89-141">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f5a89-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5a89-142">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f5a89-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5a89-143">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f5a89-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

