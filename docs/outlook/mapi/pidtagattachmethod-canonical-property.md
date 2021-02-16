---
title: Propiedad canónica PidTagAttachMethod
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: 'Last modified: September 07, 2016'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327261"
---
# <a name="pidtagattachmethod-canonical-property"></a><span data-ttu-id="7fe28-103">Propiedad canónica PidTagAttachMethod</span><span class="sxs-lookup"><span data-stu-id="7fe28-103">PidTagAttachMethod Canonical Property</span></span>

 
  
<span data-ttu-id="7fe28-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fe28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fe28-105">Contiene una constante definida por MAPI que representa la forma en que se puede tener acceso al contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7fe28-105">Contains a MAPI-defined constant representing the way the contents of an attachment can be accessed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7fe28-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7fe28-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7fe28-107">PR_ATTACH_METHOD</span><span class="sxs-lookup"><span data-stu-id="7fe28-107">PR_ATTACH_METHOD</span></span>  <br/> |
|<span data-ttu-id="7fe28-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7fe28-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7fe28-109">0x3705</span><span class="sxs-lookup"><span data-stu-id="7fe28-109">0x3705</span></span>  <br/> |
|<span data-ttu-id="7fe28-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7fe28-110">Data type:</span></span>  <br/> |<span data-ttu-id="7fe28-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7fe28-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7fe28-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7fe28-112">Area:</span></span>  <br/> |<span data-ttu-id="7fe28-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="7fe28-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fe28-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7fe28-114">Remarks</span></span>

<span data-ttu-id="7fe28-115">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="7fe28-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="7fe28-116">NO_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="7fe28-116">NO_ATTACHMENT</span></span> 
  
> <span data-ttu-id="7fe28-117">Los datos adjuntos se han creado.</span><span class="sxs-lookup"><span data-stu-id="7fe28-117">The attachment has just been created.</span></span> 
    
<span data-ttu-id="7fe28-118">ATTACH_BY_VALUE</span><span class="sxs-lookup"><span data-stu-id="7fe28-118">ATTACH_BY_VALUE</span></span> 
  
> <span data-ttu-id="7fe28-119">La **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) contiene los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7fe28-119">The **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property contains the attachment data.</span></span> 
    
<span data-ttu-id="7fe28-120">ATTACH_BY_REFERENCE</span><span class="sxs-lookup"><span data-stu-id="7fe28-120">ATTACH_BY_REFERENCE</span></span> 
  
> <span data-ttu-id="7fe28-121">La **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) o **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) contiene una ruta de acceso completa que identifica los datos adjuntos a los destinatarios con acceso a un servidor de archivos común.</span><span class="sxs-lookup"><span data-stu-id="7fe28-121">The **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) or **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) property contains a fully-qualified path identifying the attachment to recipients with access to a common file server.</span></span> 
    
<span data-ttu-id="7fe28-122">ATTACH_BY_REF_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="7fe28-122">ATTACH_BY_REF_RESOLVE</span></span> 
  
> <span data-ttu-id="7fe28-123">La **PR_ATTACH_PATHNAME** o **PR_ATTACH_LONG_PATHNAME** contiene una ruta de acceso completa que identifica los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7fe28-123">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="7fe28-124">ATTACH_BY_REF_ONLY</span><span class="sxs-lookup"><span data-stu-id="7fe28-124">ATTACH_BY_REF_ONLY</span></span> 
  
> <span data-ttu-id="7fe28-125">La **PR_ATTACH_PATHNAME** o **PR_ATTACH_LONG_PATHNAME** contiene una ruta de acceso completa que identifica los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7fe28-125">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="7fe28-126">ATTACH_EMBEDDED_MSG</span><span class="sxs-lookup"><span data-stu-id="7fe28-126">ATTACH_EMBEDDED_MSG</span></span> 
  
> <span data-ttu-id="7fe28-127">La **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) contiene un objeto incrustado que admite la **interfaz IMessage.**</span><span class="sxs-lookup"><span data-stu-id="7fe28-127">The **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property contains an embedded object that supports the **IMessage** interface.</span></span> 
    
<span data-ttu-id="7fe28-128">ATTACH_OLE</span><span class="sxs-lookup"><span data-stu-id="7fe28-128">ATTACH_OLE</span></span> 
  
> <span data-ttu-id="7fe28-129">Los datos adjuntos son un objeto OLE incrustado.</span><span class="sxs-lookup"><span data-stu-id="7fe28-129">The attachment is an embedded OLE object.</span></span>
    
<span data-ttu-id="7fe28-130">ATTACH_BY_WEBREFERENCE</span><span class="sxs-lookup"><span data-stu-id="7fe28-130">ATTACH_BY_WEBREFERENCE</span></span> 
  
> <span data-ttu-id="7fe28-131">El contenido de los datos adjuntos no está en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="7fe28-131">The attachment content is not in the message.</span></span> 
    
<span data-ttu-id="7fe28-132">Cuando se crean, todos los objetos adjuntos tienen un **valor PR_ATTACH_METHOD** inicial de **NO_ATTACHMENT**.</span><span class="sxs-lookup"><span data-stu-id="7fe28-132">When created, all attachment objects have an initial **PR_ATTACH_METHOD** value of **NO_ATTACHMENT**.</span></span> 
  
<span data-ttu-id="7fe28-133">Las aplicaciones cliente y los proveedores de servicios solo son necesarios para admitir el método de datos adjuntos representado por **el ATTACH_BY_VALUE** cliente.</span><span class="sxs-lookup"><span data-stu-id="7fe28-133">Client applications and service providers are only required to support the attachment method represented by the **ATTACH_BY_VALUE** value.</span></span> <span data-ttu-id="7fe28-134">Los otros métodos de datos adjuntos son opcionales.</span><span class="sxs-lookup"><span data-stu-id="7fe28-134">The other attachment methods are optional.</span></span> <span data-ttu-id="7fe28-135">El almacén de mensajes no exige ninguna coherencia entre el valor de **PR_ATTACH_METHOD** y los valores de las otras propiedades de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7fe28-135">The message store does not enforce any consistency between the value of **PR_ATTACH_METHOD** and the values of the other attachment properties.</span></span> 
  
<span data-ttu-id="7fe28-136">Se recomiendan nombres de convención de nomenclatura universal (UNC)  para rutas de acceso completas, que se deben usar con ATTACH_BY_REFERENCE **y ATTACH_BY_REF_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="7fe28-136">Universal naming convention (UNC) names are recommended for fully-qualified paths, which should be used with **ATTACH_BY_REFERENCE** and **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="7fe28-137">Con **ATTACH_BY_REF_RESOLVE,** una ruta de acceso absoluta es más rápida, porque la cola MAPI convierte los datos adjuntos en **ATTACH_BY_VALUE**.</span><span class="sxs-lookup"><span data-stu-id="7fe28-137">With **ATTACH_BY_REF_RESOLVE**, an absolute path is faster, because the MAPI spooler converts the attachment to **ATTACH_BY_VALUE**.</span></span> 
  
<span data-ttu-id="7fe28-138">Si **ATTACH_BY_REFERENCE** está establecido, **PR_ATTACH_DATA_BIN** debe estar vacío.</span><span class="sxs-lookup"><span data-stu-id="7fe28-138">If **ATTACH_BY_REFERENCE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="7fe28-139">Una puerta de enlace saliente puede convertir ATTACH_BY_REFERENCE **datos** adjuntos en un ATTACH_BY_VALUE **adjuntos** copiando los datos adjuntos en la **PR_ATTACH_DATA_BIN** datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7fe28-139">An outbound gateway can turn an **ATTACH_BY_REFERENCE** attachment into an **ATTACH_BY_VALUE** attachment by copying the attachment data into the **PR_ATTACH_DATA_BIN** property.</span></span> 
  
<span data-ttu-id="7fe28-140">Si **ATTACH_BY_REF_RESOLVE** se establece, **PR_ATTACH_DATA_BIN** debe estar vacío.</span><span class="sxs-lookup"><span data-stu-id="7fe28-140">If **ATTACH_BY_REF_RESOLVE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="7fe28-141">Cuando se envía el mensaje que ATTACH_BY_REF_RESOLVE **datos** adjuntos, la cola MAPI copia los datos adjuntos **en** una ATTACH_BY_VALUE datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7fe28-141">When the message that contains the **ATTACH_BY_REF_RESOLVE** attachment is sent, the MAPI spooler copies the attachment data into an **ATTACH_BY_VALUE** attachment.</span></span> <span data-ttu-id="7fe28-142">Este proceso de resolución coloca los datos adjuntos **en PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="7fe28-142">This resolution process places the attachment data in **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="7fe28-143">Si **ATTACH_BY_REF_ONLY** se establece, **PR_ATTACH_DATA_BIN** debe estar vacío y el sistema de mensajería nunca resuelve la referencia de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7fe28-143">If **ATTACH_BY_REF_ONLY** is set, **PR_ATTACH_DATA_BIN** must be empty, and the messaging system never resolves the attachment reference.</span></span> <span data-ttu-id="7fe28-144">Use este valor cuando desee enviar el vínculo, pero no los datos.</span><span class="sxs-lookup"><span data-stu-id="7fe28-144">Use this value when you want to send the link but not the data.</span></span> 
  
<span data-ttu-id="7fe28-145">Cuando el objeto OLE está en formato **IStorage** de OLE 2.0, se puede acceder a los datos a través **de PR_ATTACH_DATA_OBJ**.</span><span class="sxs-lookup"><span data-stu-id="7fe28-145">When the OLE object is in OLE 2.0 **IStorage** format, the data is accessible through **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="7fe28-146">Cuando el objeto OLE está en formato OLE 1.0 **OLESTREAM,** los datos son accesibles a través **PR_ATTACH_DATA_BIN** como **un IStream**.</span><span class="sxs-lookup"><span data-stu-id="7fe28-146">When the OLE object is in OLE 1.0 **OLESTREAM** format, the data is accessible through **PR_ATTACH_DATA_BIN** as an **IStream**.</span></span> <span data-ttu-id="7fe28-147">El tipo de la codificación OLE puede determinarse mediante **el PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7fe28-147">The type of the OLE encoding can be determined by the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) value.</span></span> 
  
<span data-ttu-id="7fe28-148">Para obtener más información sobre las interfaces y formatos OLE, vea la referencia *del programador de OLE.*</span><span class="sxs-lookup"><span data-stu-id="7fe28-148">For more information on OLE interfaces and formats, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7fe28-149">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7fe28-149">Remarks</span></span>

<span data-ttu-id="7fe28-150">Cuando el **PR_ATTACH_METHOD** está **ATTACH_BY_WEBREFERENCE,** el contenido de los datos adjuntos no está en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="7fe28-150">When the **PR_ATTACH_METHOD** is **ATTACH_BY_WEBREFERENCE**, the attachment content is not in the message.</span></span> <span data-ttu-id="7fe28-151">En su lugar, **PR_ATTACH_LONG_FILENAME** propiedad contiene una dirección URL absoluta para el contenido de datos adjuntos, que se almacena en línea.</span><span class="sxs-lookup"><span data-stu-id="7fe28-151">Instead, the **PR_ATTACH_LONG_FILENAME** property contains an absolute URL to the attachment content, which is stored online.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7fe28-152">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7fe28-152">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7fe28-153">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="7fe28-153">Protocol specifications</span></span>

<span data-ttu-id="7fe28-154">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fe28-154">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fe28-155">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7fe28-155">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7fe28-156">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7fe28-156">Header files</span></span>

<span data-ttu-id="7fe28-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7fe28-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="7fe28-158">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7fe28-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="7fe28-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7fe28-159">Mapitags.h</span></span>
  
> <span data-ttu-id="7fe28-160">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7fe28-160">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7fe28-161">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7fe28-161">See also</span></span>



[<span data-ttu-id="7fe28-162">Propiedad canónica PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="7fe28-162">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)


[<span data-ttu-id="7fe28-163">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7fe28-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7fe28-164">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="7fe28-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7fe28-165">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7fe28-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7fe28-166">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7fe28-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

