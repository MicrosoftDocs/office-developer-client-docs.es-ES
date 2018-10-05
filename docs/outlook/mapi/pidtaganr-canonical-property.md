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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400443"
---
# <a name="pidtaganr-canonical-property"></a><span data-ttu-id="bcfde-103">Propiedad canónica PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="bcfde-103">PidTagAnr Canonical Property</span></span>

  
  
<span data-ttu-id="bcfde-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcfde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcfde-105">Contiene un valor de cadena para su uso en una restricción de propiedad en una tabla de contenido de contenedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="bcfde-105">Contains a string value for use in a property restriction on an address book container contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bcfde-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="bcfde-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bcfde-107">PR_ANR, PR_ANR_A, PR_ANR_W</span><span class="sxs-lookup"><span data-stu-id="bcfde-107">PR_ANR, PR_ANR_A, PR_ANR_W</span></span>  <br/> |
|<span data-ttu-id="bcfde-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bcfde-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bcfde-109">0x360C</span><span class="sxs-lookup"><span data-stu-id="bcfde-109">0x360C</span></span>  <br/> |
|<span data-ttu-id="bcfde-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="bcfde-110">Data type:</span></span>  <br/> |<span data-ttu-id="bcfde-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="bcfde-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="bcfde-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bcfde-112">Area:</span></span>  <br/> |<span data-ttu-id="bcfde-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="bcfde-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcfde-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bcfde-114">Remarks</span></span>

<span data-ttu-id="bcfde-115">Estas propiedades no pertenecen a cualquier objeto; se está proporcionado por los proveedores de la libreta de direcciones en las estructuras de [SPropertyRestriction](spropertyrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="bcfde-115">These properties do not belong to any object; it is furnished by address book providers in [SPropertyRestriction](spropertyrestriction.md) structures.</span></span> <span data-ttu-id="bcfde-116">Esta propiedad contiene una cadena de nombre ambiguo resolución (ANR) que se puede probar en la tabla de contenido de un contenedor de la libreta de direcciones para buscar a destinatarios del mensaje correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bcfde-116">This property contains an ambiguous name resolution (ANR) string that can be tested against an address book container's contents table to find corresponding message recipients.</span></span> 
  
<span data-ttu-id="bcfde-117">Los proveedores de la libreta de direcciones coincide con el valor de **PR_ANR** y las propiedades asociadas con cada entrada en la tabla de contenido, mediante un algoritmo de coincidencia definidas por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="bcfde-117">Address book providers match the value of **PR_ANR** and associated properties against every entry in the contents table, using a provider-defined matching algorithm.</span></span> <span data-ttu-id="bcfde-118">La columna o columnas que se usan en esta coincidencia se elegida por el proveedor como parte del algoritmo.</span><span class="sxs-lookup"><span data-stu-id="bcfde-118">The column or columns that are used in this match are chosen by the provider as part of the algorithm.</span></span> <span data-ttu-id="bcfde-119">La columna de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) se utiliza con más frecuencia; la columna **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) también es útil cuando que contiene el nombre de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="bcfde-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column is the most commonly used; the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) column is also useful when it contains the user's email name.</span></span> 
  
<span data-ttu-id="bcfde-120">Para obtener más información sobre la resolución de nombres ambiguos, vea [Restricciones de la libreta de direcciones](address-book-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="bcfde-120">For more information on ambiguous name resolution, see [Address Book Restrictions](address-book-restrictions.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bcfde-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bcfde-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bcfde-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="bcfde-122">Protocol specifications</span></span>

<span data-ttu-id="bcfde-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcfde-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcfde-124">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="bcfde-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bcfde-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcfde-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcfde-126">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="bcfde-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bcfde-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="bcfde-127">Header files</span></span>

<span data-ttu-id="bcfde-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bcfde-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="bcfde-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="bcfde-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="bcfde-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bcfde-130">Mapitags.h</span></span>
  
> <span data-ttu-id="bcfde-131">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="bcfde-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcfde-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcfde-132">See also</span></span>



[<span data-ttu-id="bcfde-133">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="bcfde-133">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="bcfde-134">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="bcfde-134">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="bcfde-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bcfde-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bcfde-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="bcfde-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bcfde-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="bcfde-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bcfde-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="bcfde-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

