---
title: Propiedad canónica PidTagObjectType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObjectType
api_type:
- HeaderDef
ms.assetid: 37da4ff5-300d-479f-a8b4-6fc36df997d9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b433db7cb157afbf8c3b506f2ed95b04b7b88564
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329228"
---
# <a name="pidtagobjecttype-canonical-property"></a><span data-ttu-id="e0158-103">Propiedad canónica PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="e0158-103">PidTagObjectType Canonical Property</span></span>

  
  
<span data-ttu-id="e0158-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0158-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0158-105">Contiene el tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="e0158-105">Contains the type of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0158-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e0158-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0158-107">PR_OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="e0158-107">PR_OBJECT_TYPE</span></span>  <br/> |
|<span data-ttu-id="e0158-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e0158-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e0158-109">0x0FFE</span><span class="sxs-lookup"><span data-stu-id="e0158-109">0x0FFE</span></span>  <br/> |
|<span data-ttu-id="e0158-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e0158-110">Data type:</span></span>  <br/> |<span data-ttu-id="e0158-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e0158-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e0158-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e0158-112">Area:</span></span>  <br/> |<span data-ttu-id="e0158-113">Común</span><span class="sxs-lookup"><span data-stu-id="e0158-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0158-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0158-114">Remarks</span></span>

<span data-ttu-id="e0158-115">El tipo de objeto contenido en esta propiedad corresponde a la interfaz principal disponible para un objeto accesible a través de la **interfaz OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="e0158-115">The object type contained in this property corresponds to the primary interface available for an object accessible through the **OpenEntry** interface.</span></span> <span data-ttu-id="e0158-116">Normalmente se obtiene consultando el parámetro  _lpulObjType_ devuelto por el método **OpenEntry** adecuado.</span><span class="sxs-lookup"><span data-stu-id="e0158-116">It is usually obtained by consulting the  _lpulObjType_ parameter returned by the appropriate **OpenEntry** method.</span></span> <span data-ttu-id="e0158-117">Cuando la interfaz se obtiene de otras maneras, llama a [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e0158-117">When the interface is obtained in other ways, call [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the value for this property.</span></span> 
  
<span data-ttu-id="e0158-118">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e0158-118">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="e0158-119">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="e0158-119">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="e0158-120">Objeto contenedor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="e0158-120">Address book container object</span></span> 
    
<span data-ttu-id="e0158-121">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="e0158-121">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="e0158-122">Objeto libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="e0158-122">Address book object</span></span> 
    
<span data-ttu-id="e0158-123">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="e0158-123">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="e0158-124">Objeto de datos adjuntos de mensaje</span><span class="sxs-lookup"><span data-stu-id="e0158-124">Message attachment object</span></span> 
    
<span data-ttu-id="e0158-125">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="e0158-125">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="e0158-126">Objeto de lista de distribución</span><span class="sxs-lookup"><span data-stu-id="e0158-126">Distribution list object</span></span> 
    
<span data-ttu-id="e0158-127">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="e0158-127">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="e0158-128">Objeto Folder</span><span class="sxs-lookup"><span data-stu-id="e0158-128">Folder object</span></span> 
    
<span data-ttu-id="e0158-129">MAPI_FORMINFO</span><span class="sxs-lookup"><span data-stu-id="e0158-129">MAPI_FORMINFO</span></span> 
  
> <span data-ttu-id="e0158-130">Form (objeto)</span><span class="sxs-lookup"><span data-stu-id="e0158-130">Form object</span></span> 
    
<span data-ttu-id="e0158-131">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="e0158-131">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="e0158-132">Objeto de usuario de mensajería</span><span class="sxs-lookup"><span data-stu-id="e0158-132">Messaging user object</span></span> 
    
<span data-ttu-id="e0158-133">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="e0158-133">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="e0158-134">Objeto Message</span><span class="sxs-lookup"><span data-stu-id="e0158-134">Message object</span></span> 
    
<span data-ttu-id="e0158-135">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="e0158-135">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="e0158-136">Objeto de sección Perfil</span><span class="sxs-lookup"><span data-stu-id="e0158-136">Profile section object</span></span> 
    
<span data-ttu-id="e0158-137">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="e0158-137">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="e0158-138">Session (objeto)</span><span class="sxs-lookup"><span data-stu-id="e0158-138">Session object</span></span> 
    
<span data-ttu-id="e0158-139">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="e0158-139">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="e0158-140">Status (objeto)</span><span class="sxs-lookup"><span data-stu-id="e0158-140">Status object</span></span> 
    
<span data-ttu-id="e0158-141">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="e0158-141">MAPI_STORE</span></span> 
  
> <span data-ttu-id="e0158-142">Objeto de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="e0158-142">Message store object</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="e0158-143">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0158-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0158-144">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="e0158-144">Protocol specifications</span></span>

<span data-ttu-id="e0158-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0158-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0158-146">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="e0158-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e0158-147">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0158-147">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0158-148">Especifica las propiedades y las operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="e0158-148">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="e0158-149">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0158-149">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0158-150">Controla las comunicaciones de un cliente con un servidor de interfaz de proveedor de servicios de nombres (NSPI).</span><span class="sxs-lookup"><span data-stu-id="e0158-150">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="e0158-151">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0158-151">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0158-152">Controla las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="e0158-152">Handles folder operations.</span></span>
    
<span data-ttu-id="e0158-153">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0158-153">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0158-154">Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="e0158-154">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e0158-155">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0158-155">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0158-156">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e0158-156">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="e0158-157">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0158-157">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0158-158">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e0158-158">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e0158-159">[[MS-OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0158-159">[[MS-OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0158-160">Especifica los formatos de archivo de libreta de direcciones sin conexión (OAB) para la memoria caché de objetos de libreta de direcciones local.</span><span class="sxs-lookup"><span data-stu-id="e0158-160">Specifies the offline address book (OAB) file formats for the local address book objects cache.</span></span>
    
<span data-ttu-id="e0158-161">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0158-161">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0158-162">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e0158-162">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="e0158-163">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0158-163">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0158-164">Especifica las propiedades y las operaciones para manipular una configuración de lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e0158-164">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e0158-165">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e0158-165">Header files</span></span>

<span data-ttu-id="e0158-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0158-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0158-167">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e0158-167">Provides data type definitions.</span></span>
    
<span data-ttu-id="e0158-168">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e0158-168">Mapitags.h</span></span>
  
> <span data-ttu-id="e0158-169">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="e0158-169">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0158-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0158-170">See also</span></span>



[<span data-ttu-id="e0158-171">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e0158-171">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0158-172">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e0158-172">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0158-173">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e0158-173">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0158-174">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e0158-174">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

