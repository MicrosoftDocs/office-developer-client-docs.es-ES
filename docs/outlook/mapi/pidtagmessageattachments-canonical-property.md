---
title: Propiedad canónica PidTagMessageAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageAttachments
api_type:
- HeaderDef
ms.assetid: 85762771-b823-4227-9a7b-75b6ac280b2d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 975f52e6ea0ca7a469a027565f845f9dc0f9c2cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342570"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="85494-103">Propiedad canónica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="85494-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="85494-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85494-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85494-105">Contiene una tabla de datos adjuntos de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="85494-105">Contains a table of attachments for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85494-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="85494-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="85494-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="85494-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="85494-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="85494-108">Identifier:</span></span>  <br/> |<span data-ttu-id="85494-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="85494-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="85494-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="85494-110">Data type:</span></span>  <br/> |<span data-ttu-id="85494-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="85494-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="85494-112">Área:</span><span class="sxs-lookup"><span data-stu-id="85494-112">Area:</span></span>  <br/> |<span data-ttu-id="85494-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="85494-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85494-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="85494-114">Remarks</span></span>

<span data-ttu-id="85494-115">Esta propiedad se puede excluir en las operaciones de [IMAPIProp:: CopyTo](imapiprop-copyto.md) o incluirse en las operaciones de [IMAPIProp:: CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="85494-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="85494-116">Como una propiedad de tipo PT Object, el método [IMAPIProp:: GetProps](imapiprop-getprops.md) no puede recuperarlo correctamente.</span><span class="sxs-lookup"><span data-stu-id="85494-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="85494-117">Debe obtener acceso a su contenido mediante el método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , lo que solicita el identificador de interfaz **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="85494-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="85494-118">Los proveedores de servicios deben informar al método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) si está establecido, pero, opcionalmente, puede informar de él o no si no se ha establecido.</span><span class="sxs-lookup"><span data-stu-id="85494-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="85494-119">Para recuperar el contenido de la tabla, una aplicación cliente debe llamar al método [IMessage:: GetAttachmentTable](imessage-getattachmenttable.md) .</span><span class="sxs-lookup"><span data-stu-id="85494-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="85494-120">For more information, see [Tablas de datos adjuntos](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="85494-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="85494-121">Esta propiedad se puede usar para la restricción de subobjeto al especificarla en la estructura [SSubRestriction](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="85494-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="85494-122">Esto permite al cliente limitar la vista de un contenedor a los mensajes con datos adjuntos que cumplan los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="85494-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="85494-123">Un mensaje es apto para ver si al menos una fila de la tabla de datos adjuntos, es decir, un dato adjunto, cumple la restricción de subobjeto.</span><span class="sxs-lookup"><span data-stu-id="85494-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="85494-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="85494-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="85494-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="85494-125">Protocol specifications</span></span>

<span data-ttu-id="85494-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85494-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85494-127">Define las estructuras de datos básicas que se usan en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="85494-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="85494-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85494-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85494-129">Define las estructuras de datos básicas que se usan en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="85494-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="85494-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85494-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85494-131">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="85494-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="85494-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="85494-132">Header files</span></span>

<span data-ttu-id="85494-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="85494-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="85494-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="85494-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="85494-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="85494-135">Mapitags.h</span></span>
  
> <span data-ttu-id="85494-136">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="85494-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="85494-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="85494-137">See also</span></span>



[<span data-ttu-id="85494-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="85494-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="85494-139">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="85494-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="85494-140">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="85494-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="85494-141">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="85494-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

