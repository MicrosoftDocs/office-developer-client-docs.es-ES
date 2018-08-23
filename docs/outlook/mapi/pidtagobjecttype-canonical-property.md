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
ms.openlocfilehash: 8b2d435e132bf453cf41ec141d5a946bf54f9c66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591054"
---
# <a name="pidtagobjecttype-canonical-property"></a><span data-ttu-id="edd12-103">Propiedad canónica PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="edd12-103">PidTagObjectType Canonical Property</span></span>

  
  
<span data-ttu-id="edd12-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edd12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edd12-105">Contiene el tipo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="edd12-105">Contains the type of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="edd12-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="edd12-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="edd12-107">PR_OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="edd12-107">PR_OBJECT_TYPE</span></span>  <br/> |
|<span data-ttu-id="edd12-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="edd12-108">Identifier:</span></span>  <br/> |<span data-ttu-id="edd12-109">0x0FFE</span><span class="sxs-lookup"><span data-stu-id="edd12-109">0x0FFE</span></span>  <br/> |
|<span data-ttu-id="edd12-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="edd12-110">Data type:</span></span>  <br/> |<span data-ttu-id="edd12-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="edd12-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="edd12-112">Área:</span><span class="sxs-lookup"><span data-stu-id="edd12-112">Area:</span></span>  <br/> |<span data-ttu-id="edd12-113">Common</span><span class="sxs-lookup"><span data-stu-id="edd12-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edd12-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edd12-114">Remarks</span></span>

<span data-ttu-id="edd12-115">El tipo de objeto contenido en esta propiedad corresponde a la interfaz principal disponible para un objeto accesible a través de la interfaz de **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="edd12-115">The object type contained in this property corresponds to the primary interface available for an object accessible through the **OpenEntry** interface.</span></span> <span data-ttu-id="edd12-116">Normalmente, se obtiene mediante el parámetro _lpulObjType_ devuelto por el método **OpenEntry** apropiado de consultoría.</span><span class="sxs-lookup"><span data-stu-id="edd12-116">It is usually obtained by consulting the  _lpulObjType_ parameter returned by the appropriate **OpenEntry** method.</span></span> <span data-ttu-id="edd12-117">Cuando se obtiene la interfaz de otras maneras, llame a [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="edd12-117">When the interface is obtained in other ways, call [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the value for this property.</span></span> 
  
<span data-ttu-id="edd12-118">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="edd12-118">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="edd12-119">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="edd12-119">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="edd12-120">Objeto de contenedor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="edd12-120">Address book container object</span></span> 
    
<span data-ttu-id="edd12-121">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="edd12-121">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="edd12-122">Objeto de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="edd12-122">Address book object</span></span> 
    
<span data-ttu-id="edd12-123">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="edd12-123">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="edd12-124">Objeto de datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="edd12-124">Message attachment object</span></span> 
    
<span data-ttu-id="edd12-125">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="edd12-125">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="edd12-126">Objeto de lista de distribución</span><span class="sxs-lookup"><span data-stu-id="edd12-126">Distribution list object</span></span> 
    
<span data-ttu-id="edd12-127">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="edd12-127">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="edd12-128">Objeto Folder</span><span class="sxs-lookup"><span data-stu-id="edd12-128">Folder object</span></span> 
    
<span data-ttu-id="edd12-129">MAPI_FORMINFO</span><span class="sxs-lookup"><span data-stu-id="edd12-129">MAPI_FORMINFO</span></span> 
  
> <span data-ttu-id="edd12-130">Objeto de formulario</span><span class="sxs-lookup"><span data-stu-id="edd12-130">Form object</span></span> 
    
<span data-ttu-id="edd12-131">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="edd12-131">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="edd12-132">Objeto de usuario de mensajería</span><span class="sxs-lookup"><span data-stu-id="edd12-132">Messaging user object</span></span> 
    
<span data-ttu-id="edd12-133">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="edd12-133">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="edd12-134">Objeto Message</span><span class="sxs-lookup"><span data-stu-id="edd12-134">Message object</span></span> 
    
<span data-ttu-id="edd12-135">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="edd12-135">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="edd12-136">Objeto de sección de perfil</span><span class="sxs-lookup"><span data-stu-id="edd12-136">Profile section object</span></span> 
    
<span data-ttu-id="edd12-137">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="edd12-137">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="edd12-138">Objeto de sesión</span><span class="sxs-lookup"><span data-stu-id="edd12-138">Session object</span></span> 
    
<span data-ttu-id="edd12-139">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="edd12-139">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="edd12-140">Objeto de estado</span><span class="sxs-lookup"><span data-stu-id="edd12-140">Status object</span></span> 
    
<span data-ttu-id="edd12-141">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="edd12-141">MAPI_STORE</span></span> 
  
> <span data-ttu-id="edd12-142">Objeto de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="edd12-142">Message store object</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="edd12-143">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="edd12-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="edd12-144">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="edd12-144">Protocol specifications</span></span>

<span data-ttu-id="edd12-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd12-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd12-146">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="edd12-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="edd12-147">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd12-147">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd12-148">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="edd12-148">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="edd12-149">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd12-149">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd12-150">Administra las comunicaciones de un cliente con un servidor de la interfaz de proveedor de servicio de nombres (NSPI).</span><span class="sxs-lookup"><span data-stu-id="edd12-150">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="edd12-151">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd12-151">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd12-152">Controla las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="edd12-152">Handles folder operations.</span></span>
    
<span data-ttu-id="edd12-153">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd12-153">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd12-154">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="edd12-154">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="edd12-155">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd12-155">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd12-156">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="edd12-156">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="edd12-157">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd12-157">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd12-158">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="edd12-158">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="edd12-159">[[MS-OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd12-159">[[MS-OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd12-160">Especifica los formatos de archivo (OAB) de la libreta de direcciones sin conexión para la caché de objetos de la libreta de direcciones locales.</span><span class="sxs-lookup"><span data-stu-id="edd12-160">Specifies the offline address book (OAB) file formats for the local address book objects cache.</span></span>
    
<span data-ttu-id="edd12-161">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd12-161">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd12-162">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="edd12-162">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="edd12-163">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd12-163">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd12-164">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="edd12-164">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="edd12-165">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="edd12-165">Header files</span></span>

<span data-ttu-id="edd12-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="edd12-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="edd12-167">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="edd12-167">Provides data type definitions.</span></span>
    
<span data-ttu-id="edd12-168">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="edd12-168">Mapitags.h</span></span>
  
> <span data-ttu-id="edd12-169">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="edd12-169">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edd12-170">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="edd12-170">See also</span></span>



[<span data-ttu-id="edd12-171">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="edd12-171">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="edd12-172">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="edd12-172">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="edd12-173">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="edd12-173">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="edd12-174">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="edd12-174">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

