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
ms.openlocfilehash: 49c9b0a80f9bc3b45dfafa6f4e037fe55af289d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819237"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a><span data-ttu-id="180df-103">Propiedad canónica PidTagAddressBookHierarchicalRootDepartment</span><span class="sxs-lookup"><span data-stu-id="180df-103">PidTagAddressBookHierarchicalRootDepartment</span></span>

  
  
<span data-ttu-id="180df-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="180df-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="180df-105">Contiene el nombre distintivo (DN) de la raíz de direcciones jerárquicas (HAB).</span><span class="sxs-lookup"><span data-stu-id="180df-105">Contains the distinguished name (DN) of the hierarchical address root (HAB).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="180df-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="180df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="180df-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span><span class="sxs-lookup"><span data-stu-id="180df-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span></span>  <br/> |
|<span data-ttu-id="180df-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="180df-108">Property set:</span></span>  <br/> |<span data-ttu-id="180df-109">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="180df-109">Address Book</span></span>  <br/> |
|<span data-ttu-id="180df-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="180df-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="180df-111">0x8C98</span><span class="sxs-lookup"><span data-stu-id="180df-111">0x8C98</span></span>  <br/> |
|<span data-ttu-id="180df-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="180df-112">Data type:</span></span>  <br/> |<span data-ttu-id="180df-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="180df-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="180df-114">Área:</span><span class="sxs-lookup"><span data-stu-id="180df-114">Area:</span></span>  <br/> |<span data-ttu-id="180df-115">Libreta de direcciones de Exchange</span><span class="sxs-lookup"><span data-stu-id="180df-115">Exchange Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="180df-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="180df-116">Remarks</span></span>

<span data-ttu-id="180df-117">Esto es una propiedad en el contenedor de (GAL) de la lista global de direcciones y representa el nombre distintivo (DN) de la raíz de direcciones jerárquica.</span><span class="sxs-lookup"><span data-stu-id="180df-117">This is a property on the global address list (GAL) container and represents the distinguished name of the hierarchical address root.</span></span> <span data-ttu-id="180df-118">Esta propiedad sólo está presente en la libreta de direcciones sin conexión y nunca en los servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="180df-118">This property is only present in the offline address book and never in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="180df-119">Los llamadores deben pasar MAPI_CACHE_ONLY a la llamada GetProps para evitar una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="180df-119">Callers should pass MAPI_CACHE_ONLY to the GetProps call to avoid a remote procedure call.</span></span> <span data-ttu-id="180df-120">Si esto no está presente, los llamadores deben utilizar PR_EMS_AB_HAB_ROOT_DEPARTMENT, que es del tipo pt Object, para buscar el departamento de raíz.</span><span class="sxs-lookup"><span data-stu-id="180df-120">If this is not present, callers should use PR_EMS_AB_HAB_ROOT_DEPARTMENT, which is of type PT_OBJECT, to find the root department.</span></span> 
  
<span data-ttu-id="180df-121">Una vez obtenido el departamento de raíz, puede tener un tipo de objeto MAPI_MAILUSER o MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="180df-121">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="180df-122">Si el tipo de objeto es MAPI_DISTLIST, que se emplea el nuevo esquema.</span><span class="sxs-lookup"><span data-stu-id="180df-122">If the object type is MAPI_DISTLIST, the new schema is being employed.</span></span> <span data-ttu-id="180df-123">Si el tipo de objeto es MAPI_MAILUSER, que se emplea el esquema anterior.</span><span class="sxs-lookup"><span data-stu-id="180df-123">If the object type is MAPI_MAILUSER, the previous schema is being employed.</span></span> 
  
- <span data-ttu-id="180df-124">Microsoft Office Outlook 2007 Service Pack 2 es compatible con ambos esquemas.</span><span class="sxs-lookup"><span data-stu-id="180df-124">Microsoft Office Outlook 2007 Service Pack 2 supports both schemas.</span></span> 
    
- <span data-ttu-id="180df-125">Microsoft Outlook 2010 y Microsoft Outlook 2013 admiten el nuevo esquema.</span><span class="sxs-lookup"><span data-stu-id="180df-125">Microsoft Outlook 2010 and Microsoft Outlook 2013 support the new schema.</span></span>
    
<span data-ttu-id="180df-126">En el esquema de nuevo, todos los grupos departamentales también son listas de distribución y son de tipo MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="180df-126">In the new schema, all departmental groups are also distribution lists and are of type MAPI_DISTLIST.</span></span> <span data-ttu-id="180df-127">Los miembros de grupos departamentales y departamentos dentro de los grupos de departamentos se obtienen mediante PR_EMS_AB_MEMBER, exactamente igual que los miembros de lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="180df-127">Members of departmental groups, and departments within departmental groups are obtained by using PR_EMS_AB_MEMBER, exactly like distribution list members.</span></span>
  
<span data-ttu-id="180df-128">Una vez obtenido el departamento de raíz, puede tener un tipo de objeto MAPI_MAILUSER o MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="180df-128">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="180df-129">Si el tipo de objeto es MAPI_DISTLIST, se utiliza el esquema de nuevo.</span><span class="sxs-lookup"><span data-stu-id="180df-129">If the object type is MAPI_DISTLIST, the new schema is being used.</span></span> <span data-ttu-id="180df-130">Si el tipo de objeto es MAPI_MAILUSER, se utiliza el esquema de la antiguo.</span><span class="sxs-lookup"><span data-stu-id="180df-130">If the object type is MAPI_MAILUSER, the old schema is being used.</span></span> 
  
<span data-ttu-id="180df-131">En el esquema de nuevo, todos los grupos de departamentos también son listas de distribución y son de tipo MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="180df-131">In the new schema, all departmental groups are also DLs and are of type MAPI_DISTLIST.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="180df-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="180df-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="180df-133">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="180df-133">Protocol specifications</span></span>

<span data-ttu-id="180df-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="180df-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="180df-135">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="180df-135">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="180df-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="180df-136">Header files</span></span>

<span data-ttu-id="180df-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="180df-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="180df-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="180df-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="180df-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="180df-139">See also</span></span>



[<span data-ttu-id="180df-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="180df-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="180df-141">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="180df-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="180df-142">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="180df-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="180df-143">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="180df-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
