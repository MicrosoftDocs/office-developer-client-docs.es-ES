---
title: Propiedad canónica PidTagDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayName
api_type:
- HeaderDef
ms.assetid: bd094e00-5c60-4bb3-9a45-b943fab52876
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 834141fe3e57fde5e6404776e0ad5ce3b438450e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360805"
---
# <a name="pidtagdisplayname-canonical-property"></a><span data-ttu-id="8bac2-103">Propiedad canónica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="8bac2-103">PidTagDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="8bac2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bac2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bac2-105">Contiene el nombre para mostrar de un objeto MAPI determinado.</span><span class="sxs-lookup"><span data-stu-id="8bac2-105">Contains the display name for a given MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8bac2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8bac2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8bac2-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="8bac2-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="8bac2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8bac2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8bac2-109">0x3001</span><span class="sxs-lookup"><span data-stu-id="8bac2-109">0x3001</span></span>  <br/> |
|<span data-ttu-id="8bac2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8bac2-110">Data type:</span></span>  <br/> |<span data-ttu-id="8bac2-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8bac2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8bac2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8bac2-112">Area:</span></span>  <br/> |<span data-ttu-id="8bac2-113">MAPI común</span><span class="sxs-lookup"><span data-stu-id="8bac2-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8bac2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8bac2-114">Remarks</span></span>

<span data-ttu-id="8bac2-115">Las carpetas requieren subcarpetas del mismo nivel para tener nombres para mostrar únicos.</span><span class="sxs-lookup"><span data-stu-id="8bac2-115">Folders require sibling subfolders to have unique display names.</span></span> <span data-ttu-id="8bac2-116">Por ejemplo, si una carpeta contiene dos subcarpetas, las dos subcarpetas no pueden usar el mismo valor para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="8bac2-116">For example, if a folder contains two subfolders, the two subfolders cannot use the same value for this property.</span></span> <span data-ttu-id="8bac2-117">Esta restricción no se aplica a otros contenedores, como libretas de direcciones y listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="8bac2-117">This restriction does not apply to other containers, such as address books and distribution lists.</span></span> 
  
<span data-ttu-id="8bac2-118">Los proveedores de servicios deben establecer el valor de esta propiedad para que contenga tanto el tipo de proveedor como la información de configuración.</span><span class="sxs-lookup"><span data-stu-id="8bac2-118">Service providers should set the value of this property so that it contains both the provider type and configuration information.</span></span> <span data-ttu-id="8bac2-119">La información adicional ayuda a distinguir entre instancias de proveedores del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="8bac2-119">The additional information helps to distinguish between instances of providers of the same type.</span></span> <span data-ttu-id="8bac2-120">Los proveedores no configurados deben usar una cadena que nombra al proveedor.</span><span class="sxs-lookup"><span data-stu-id="8bac2-120">Unconfigured providers should use a string that names the provider.</span></span> <span data-ttu-id="8bac2-121">Los proveedores configurados deben usar la misma cadena seguida de una cadena distintiva entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="8bac2-121">Configured providers should use the same string followed by a distinguishing string in parentheses.</span></span> <span data-ttu-id="8bac2-122">Por ejemplo, un proveedor de almacén de mensajes no configurado puede establecer estas propiedades en:</span><span class="sxs-lookup"><span data-stu-id="8bac2-122">For example, an unconfigured message store provider might set these properties to:</span></span> 
  
<span data-ttu-id="8bac2-123">Almacén de información personal</span><span class="sxs-lookup"><span data-stu-id="8bac2-123">Personal Information Store</span></span>
  
<span data-ttu-id="8bac2-124">A continuación, la versión configurada podría establecer estas propiedades en:</span><span class="sxs-lookup"><span data-stu-id="8bac2-124">The configured version could then set these properties to:</span></span> 
  
<span data-ttu-id="8bac2-125">Almacén de información personal (6 de febrero de 1998)</span><span class="sxs-lookup"><span data-stu-id="8bac2-125">Personal Information Store (February 6, 1998)</span></span>
  
<span data-ttu-id="8bac2-126">Para los objetos de estado, estas propiedades contienen el nombre del componente que puede mostrar la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8bac2-126">For status objects, these properties contain the name of the component that can be displayed by the user interface.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8bac2-127">Los puntos y coma no se pueden usar dentro de los nombres de destinatarios en la mensajería MAPI.</span><span class="sxs-lookup"><span data-stu-id="8bac2-127">Semicolons cannot be used within recipient names in MAPI messaging.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8bac2-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bac2-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8bac2-129">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="8bac2-129">Protocol specifications</span></span>

<span data-ttu-id="8bac2-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bac2-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bac2-131">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="8bac2-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8bac2-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bac2-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bac2-133">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="8bac2-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="8bac2-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bac2-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bac2-135">Controla las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="8bac2-135">Handles folder operations.</span></span>
    
<span data-ttu-id="8bac2-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bac2-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bac2-137">Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="8bac2-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="8bac2-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bac2-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bac2-139">Especifica las propiedades y las operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="8bac2-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="8bac2-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bac2-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bac2-141">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8bac2-141">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="8bac2-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bac2-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bac2-143">Amplía el protocolo WebDAV que especifica cómo solicitar y establecer el descriptor de seguridad Exchange mediante métodos WebDAV.</span><span class="sxs-lookup"><span data-stu-id="8bac2-143">Extends the WebDAV protocol that specifies how to request and set the Exchange security descriptor via WebDAV methods.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8bac2-144">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8bac2-144">Header files</span></span>

<span data-ttu-id="8bac2-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8bac2-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="8bac2-146">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8bac2-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="8bac2-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8bac2-147">Mapitags.h</span></span>
  
> <span data-ttu-id="8bac2-148">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8bac2-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8bac2-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bac2-149">See also</span></span>



[<span data-ttu-id="8bac2-150">Propiedad canónica PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="8bac2-150">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="8bac2-151">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8bac2-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8bac2-152">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8bac2-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8bac2-153">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8bac2-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8bac2-154">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8bac2-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

