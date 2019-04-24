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
# <a name="pidtaganr-canonical-property"></a><span data-ttu-id="6c013-103">Propiedad canónica PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="6c013-103">PidTagAnr Canonical Property</span></span>

  
  
<span data-ttu-id="6c013-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c013-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c013-105">Contiene un valor de tipo String que se usa en una restricción de propiedad en una tabla de contenido del contenedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="6c013-105">Contains a string value for use in a property restriction on an address book container contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6c013-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6c013-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c013-107">PR_ANR, PR_ANR_A, PR_ANR_W</span><span class="sxs-lookup"><span data-stu-id="6c013-107">PR_ANR, PR_ANR_A, PR_ANR_W</span></span>  <br/> |
|<span data-ttu-id="6c013-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6c013-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6c013-109">0x360C</span><span class="sxs-lookup"><span data-stu-id="6c013-109">0x360C</span></span>  <br/> |
|<span data-ttu-id="6c013-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6c013-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c013-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="6c013-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="6c013-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6c013-112">Area:</span></span>  <br/> |<span data-ttu-id="6c013-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="6c013-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c013-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c013-114">Remarks</span></span>

<span data-ttu-id="6c013-115">Estas propiedades no pertenecen a ningún objeto; la proporcionan los proveedores de libreta de direcciones en las estructuras [SPropertyRestriction](spropertyrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="6c013-115">These properties do not belong to any object; it is furnished by address book providers in [SPropertyRestriction](spropertyrestriction.md) structures.</span></span> <span data-ttu-id="6c013-116">Esta propiedad contiene una cadena de resolución de nombres ambiguos (ANR) que puede probarse con una tabla de contenido de un contenedor de libreta de direcciones para buscar los destinatarios de mensajes correspondientes.</span><span class="sxs-lookup"><span data-stu-id="6c013-116">This property contains an ambiguous name resolution (ANR) string that can be tested against an address book container's contents table to find corresponding message recipients.</span></span> 
  
<span data-ttu-id="6c013-117">Los proveedores de la libreta de direcciones coinciden con el valor de **PR_ANR** y las propiedades asociadas con todas las entradas de la tabla de contenido, utilizando un algoritmo de coincidencia definido por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="6c013-117">Address book providers match the value of **PR_ANR** and associated properties against every entry in the contents table, using a provider-defined matching algorithm.</span></span> <span data-ttu-id="6c013-118">La columna o columnas que se usan en esta coincidencia las elige el proveedor como parte del algoritmo.</span><span class="sxs-lookup"><span data-stu-id="6c013-118">The column or columns that are used in this match are chosen by the provider as part of the algorithm.</span></span> <span data-ttu-id="6c013-119">La columna **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) es la que se usa con más frecuencia; la columna **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) también es útil cuando contiene el nombre de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="6c013-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column is the most commonly used; the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) column is also useful when it contains the user's email name.</span></span> 
  
<span data-ttu-id="6c013-120">Para obtener más información acerca de la resolución de nombres ambiguos, consulte restricciones de la [Libreta de direcciones](address-book-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="6c013-120">For more information on ambiguous name resolution, see [Address Book Restrictions](address-book-restrictions.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6c013-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c013-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c013-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6c013-122">Protocol specifications</span></span>

<span data-ttu-id="6c013-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c013-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c013-124">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6c013-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c013-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c013-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c013-126">Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="6c013-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c013-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6c013-127">Header files</span></span>

<span data-ttu-id="6c013-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6c013-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c013-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6c013-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="6c013-130">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6c013-130">Mapitags.h</span></span>
  
> <span data-ttu-id="6c013-131">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="6c013-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c013-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c013-132">See also</span></span>



[<span data-ttu-id="6c013-133">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="6c013-133">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="6c013-134">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="6c013-134">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="6c013-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6c013-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c013-136">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="6c013-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c013-137">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6c013-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c013-138">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="6c013-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

