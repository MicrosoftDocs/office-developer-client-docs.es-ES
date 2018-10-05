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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386421"
---
# <a name="pidtagdisplayname-canonical-property"></a><span data-ttu-id="a1661-103">Propiedad canónica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="a1661-103">PidTagDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="a1661-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1661-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1661-105">Contiene el nombre para mostrar para un determinado objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="a1661-105">Contains the display name for a given MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1661-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a1661-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1661-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="a1661-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="a1661-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a1661-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a1661-109">0x3001</span><span class="sxs-lookup"><span data-stu-id="a1661-109">0x3001</span></span>  <br/> |
|<span data-ttu-id="a1661-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a1661-110">Data type:</span></span>  <br/> |<span data-ttu-id="a1661-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a1661-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a1661-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a1661-112">Area:</span></span>  <br/> |<span data-ttu-id="a1661-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="a1661-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1661-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a1661-114">Remarks</span></span>

<span data-ttu-id="a1661-115">Las carpetas requieren las subcarpetas del mismo nivel que los nombres de presentación únicos.</span><span class="sxs-lookup"><span data-stu-id="a1661-115">Folders require sibling subfolders to have unique display names.</span></span> <span data-ttu-id="a1661-116">Por ejemplo, si una carpeta contiene dos subcarpetas, las dos subcarpetas no pueden usar el mismo valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="a1661-116">For example, if a folder contains two subfolders, the two subfolders cannot use the same value for this property.</span></span> <span data-ttu-id="a1661-117">Esta restricción no se aplica a otros contenedores, como libretas de direcciones y listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="a1661-117">This restriction does not apply to other containers, such as address books and distribution lists.</span></span> 
  
<span data-ttu-id="a1661-118">Proveedores de servicios deben establecer el valor de esta propiedad para que contenga tanto la información de configuración y tipo de proveedor.</span><span class="sxs-lookup"><span data-stu-id="a1661-118">Service providers should set the value of this property so that it contains both the provider type and configuration information.</span></span> <span data-ttu-id="a1661-119">La información adicional ayuda a distinguir entre instancias de los proveedores del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="a1661-119">The additional information helps to distinguish between instances of providers of the same type.</span></span> <span data-ttu-id="a1661-120">Sin configurar proveedores deben usar una cadena que asigna el proveedor.</span><span class="sxs-lookup"><span data-stu-id="a1661-120">Unconfigured providers should use a string that names the provider.</span></span> <span data-ttu-id="a1661-121">Configurado los proveedores deben usar la misma cadena seguida de una cadena distintiva entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="a1661-121">Configured providers should use the same string followed by a distinguishing string in parentheses.</span></span> <span data-ttu-id="a1661-122">Por ejemplo, un proveedor de almacén de mensajes no configurado puede establecer estas propiedades:</span><span class="sxs-lookup"><span data-stu-id="a1661-122">For example, an unconfigured message store provider might set these properties to:</span></span> 
  
<span data-ttu-id="a1661-123">Almacén de información personal</span><span class="sxs-lookup"><span data-stu-id="a1661-123">Personal Information Store</span></span>
  
<span data-ttu-id="a1661-124">La versión configurada, a continuación, puede establecer estas propiedades:</span><span class="sxs-lookup"><span data-stu-id="a1661-124">The configured version could then set these properties to:</span></span> 
  
<span data-ttu-id="a1661-125">Almacén de información personal (6 de febrero de 1998)</span><span class="sxs-lookup"><span data-stu-id="a1661-125">Personal Information Store (February 6, 1998)</span></span>
  
<span data-ttu-id="a1661-126">Para los objetos de estado, estas propiedades contienen el nombre del componente que se puede mostrar la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a1661-126">For status objects, these properties contain the name of the component that can be displayed by the user interface.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a1661-127">Punto y coma no se puede usar dentro de nombres de los destinatarios de mensajería MAPI.</span><span class="sxs-lookup"><span data-stu-id="a1661-127">Semicolons cannot be used within recipient names in MAPI messaging.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a1661-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1661-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1661-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a1661-129">Protocol specifications</span></span>

<span data-ttu-id="a1661-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1661-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1661-131">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a1661-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a1661-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1661-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1661-133">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a1661-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="a1661-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1661-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1661-135">Controla las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a1661-135">Handles folder operations.</span></span>
    
<span data-ttu-id="a1661-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1661-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1661-137">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="a1661-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="a1661-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1661-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1661-139">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="a1661-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="a1661-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1661-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1661-141">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a1661-141">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="a1661-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1661-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1661-143">Extiende el protocolo WebDAV que especifica cómo solicitar y establecer el descriptor de seguridad de Exchange a través de los métodos de WebDAV.</span><span class="sxs-lookup"><span data-stu-id="a1661-143">Extends the WebDAV protocol that specifies how to request and set the Exchange security descriptor via WebDAV methods.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1661-144">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a1661-144">Header files</span></span>

<span data-ttu-id="a1661-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1661-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1661-146">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a1661-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="a1661-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a1661-147">Mapitags.h</span></span>
  
> <span data-ttu-id="a1661-148">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a1661-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1661-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1661-149">See also</span></span>



[<span data-ttu-id="a1661-150">Propiedad canónica PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="a1661-150">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="a1661-151">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a1661-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1661-152">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a1661-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1661-153">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a1661-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1661-154">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="a1661-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

