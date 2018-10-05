---
title: Propiedad canónica PidTagLastModificationTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dea709b457e28efef62718fc388621e01c4eb5bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387331"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a><span data-ttu-id="cd5c6-103">Propiedad canónica PidTagLastModificationTime</span><span class="sxs-lookup"><span data-stu-id="cd5c6-103">PidTagLastModificationTime Canonical Property</span></span>

  
  
<span data-ttu-id="cd5c6-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd5c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd5c6-105">Contiene la fecha y hora de última modificación de el objeto o subobjetos.</span><span class="sxs-lookup"><span data-stu-id="cd5c6-105">Contains the date and time when the object or subobject was last modified.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd5c6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cd5c6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd5c6-107">PR_LAST_MODIFICATION_TIME</span><span class="sxs-lookup"><span data-stu-id="cd5c6-107">PR_LAST_MODIFICATION_TIME</span></span>  <br/> |
|<span data-ttu-id="cd5c6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cd5c6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cd5c6-109">0x3008</span><span class="sxs-lookup"><span data-stu-id="cd5c6-109">0x3008</span></span>  <br/> |
|<span data-ttu-id="cd5c6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cd5c6-110">Data type:</span></span>  <br/> |<span data-ttu-id="cd5c6-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="cd5c6-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="cd5c6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cd5c6-112">Area:</span></span>  <br/> |<span data-ttu-id="cd5c6-113">Hora del mensaje</span><span class="sxs-lookup"><span data-stu-id="cd5c6-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd5c6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd5c6-114">Remarks</span></span>

<span data-ttu-id="cd5c6-115">Esta propiedad se establece inicialmente en el mismo valor que la propiedad **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cd5c6-115">This property is initially set to the same value as the **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) property.</span></span> <span data-ttu-id="cd5c6-116">Datos adjuntos subobjetos actualizarlo, según sea necesario mediante la copia de la hora de última modificación mantenida por el sistema de archivos nativo.</span><span class="sxs-lookup"><span data-stu-id="cd5c6-116">Attachment subobjects can update it as necessary by copying the last modification time maintained by the native file system.</span></span> <span data-ttu-id="cd5c6-117">Una aplicación cliente puede establecer esta propiedad hasta la primera llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="cd5c6-117">A client application can set this property until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="cd5c6-118">En el proveedor debe actualizar **PR_LAST_MODIFICATION_TIME** durante cada llamada **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="cd5c6-118">From then on the provider should update **PR_LAST_MODIFICATION_TIME** during every **IMAPIProp::SaveChanges** call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cd5c6-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cd5c6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cd5c6-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="cd5c6-120">Protocol specifications</span></span>

<span data-ttu-id="cd5c6-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd5c6-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd5c6-122">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="cd5c6-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="cd5c6-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd5c6-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd5c6-124">Controla la sincronización de datos de objeto mensajería entre un servidor y un cliente.</span><span class="sxs-lookup"><span data-stu-id="cd5c6-124">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="cd5c6-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd5c6-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd5c6-126">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="cd5c6-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cd5c6-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cd5c6-127">Header files</span></span>

<span data-ttu-id="cd5c6-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd5c6-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd5c6-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cd5c6-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="cd5c6-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cd5c6-130">Mapitags.h</span></span>
  
> <span data-ttu-id="cd5c6-131">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="cd5c6-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd5c6-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd5c6-132">See also</span></span>



[<span data-ttu-id="cd5c6-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cd5c6-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd5c6-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="cd5c6-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd5c6-135">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cd5c6-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd5c6-136">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="cd5c6-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

