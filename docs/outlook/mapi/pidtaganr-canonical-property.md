---
title: Propiedad canónica PidTagAnr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAnr
api_type:
- HeaderDef
ms.assetid: eca3d4ff-2e92-4d20-a498-98e0773c1962
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ce08ba971662b7f5060e6b24a6d2c5ee1a921d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327968"
---
# <a name="pidtaganr-canonical-property"></a><span data-ttu-id="4a2f4-103">Propiedad canónica PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="4a2f4-103">PidTagAnr Canonical Property</span></span>

  
  
<span data-ttu-id="4a2f4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a2f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a2f4-105">Contiene un valor de cadena para su uso en una restricción de propiedad en una tabla de contenido de contenedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4a2f4-105">Contains a string value for use in a property restriction on an address book container contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a2f4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4a2f4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a2f4-107">PR_ANR, PR_ANR_A, PR_ANR_W</span><span class="sxs-lookup"><span data-stu-id="4a2f4-107">PR_ANR, PR_ANR_A, PR_ANR_W</span></span>  <br/> |
|<span data-ttu-id="4a2f4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4a2f4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a2f4-109">0x360C</span><span class="sxs-lookup"><span data-stu-id="4a2f4-109">0x360C</span></span>  <br/> |
|<span data-ttu-id="4a2f4-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4a2f4-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a2f4-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="4a2f4-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="4a2f4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4a2f4-112">Area:</span></span>  <br/> |<span data-ttu-id="4a2f4-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="4a2f4-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a2f4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a2f4-114">Remarks</span></span>

<span data-ttu-id="4a2f4-115">Estas propiedades no pertenecen a ningún objeto; lo ofrecen los proveedores de libretas de direcciones en [estructuras SPropertyRestriction.](spropertyrestriction.md)</span><span class="sxs-lookup"><span data-stu-id="4a2f4-115">These properties do not belong to any object; it is furnished by address book providers in [SPropertyRestriction](spropertyrestriction.md) structures.</span></span> <span data-ttu-id="4a2f4-116">Esta propiedad contiene una cadena de resolución de nombres ambiguos (ANR) que se puede probar con la tabla de contenido de un contenedor de libreta de direcciones para buscar los destinatarios de mensajes correspondientes.</span><span class="sxs-lookup"><span data-stu-id="4a2f4-116">This property contains an ambiguous name resolution (ANR) string that can be tested against an address book container's contents table to find corresponding message recipients.</span></span> 
  
<span data-ttu-id="4a2f4-117">Los proveedores de libretas de direcciones coinciden con el valor de **PR_ANR** y las propiedades asociadas con cada entrada de la tabla de contenido, mediante un algoritmo de coincidencia definido por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="4a2f4-117">Address book providers match the value of **PR_ANR** and associated properties against every entry in the contents table, using a provider-defined matching algorithm.</span></span> <span data-ttu-id="4a2f4-118">El proveedor elige la columna o las columnas que se usan en esta coincidencia como parte del algoritmo.</span><span class="sxs-lookup"><span data-stu-id="4a2f4-118">The column or columns that are used in this match are chosen by the provider as part of the algorithm.</span></span> <span data-ttu-id="4a2f4-119">La **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) es la más usada; la **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) también es útil cuando contiene el nombre de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="4a2f4-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column is the most commonly used; the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) column is also useful when it contains the user's email name.</span></span> 
  
<span data-ttu-id="4a2f4-120">Para obtener más información sobre la resolución de nombres ambiguos, vea [Restricciones de la libreta de direcciones.](address-book-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="4a2f4-120">For more information on ambiguous name resolution, see [Address Book Restrictions](address-book-restrictions.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4a2f4-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a2f4-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a2f4-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="4a2f4-122">Protocol specifications</span></span>

<span data-ttu-id="4a2f4-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a2f4-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a2f4-124">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="4a2f4-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a2f4-125">[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a2f4-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a2f4-126">Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="4a2f4-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a2f4-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4a2f4-127">Header files</span></span>

<span data-ttu-id="4a2f4-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a2f4-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a2f4-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4a2f4-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a2f4-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4a2f4-130">Mapitags.h</span></span>
  
> <span data-ttu-id="4a2f4-131">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="4a2f4-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a2f4-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4a2f4-132">See also</span></span>



[<span data-ttu-id="4a2f4-133">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="4a2f4-133">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="4a2f4-134">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="4a2f4-134">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="4a2f4-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4a2f4-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a2f4-136">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="4a2f4-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a2f4-137">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4a2f4-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a2f4-138">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4a2f4-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

