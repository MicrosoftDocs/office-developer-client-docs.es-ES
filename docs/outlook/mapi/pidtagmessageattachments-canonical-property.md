---
title: Propiedad canónico PidTagMessageAttachments
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 5b76a73a0fde8f4531b99a58646b927724162e81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819713"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="dc2d1-103">Propiedad canónico PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="dc2d1-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="dc2d1-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc2d1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc2d1-105">Contiene una tabla de las restricciones que se pueden aplicar a una tabla de contenido para buscar todos los mensajes que contienen los subobjetos de datos adjuntos que cumplen las restricciones.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain attachment subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc2d1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="dc2d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc2d1-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="dc2d1-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="dc2d1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dc2d1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dc2d1-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="dc2d1-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="dc2d1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="dc2d1-110">Data type:</span></span>  <br/> |<span data-ttu-id="dc2d1-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="dc2d1-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="dc2d1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dc2d1-112">Area:</span></span>  <br/> |<span data-ttu-id="dc2d1-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="dc2d1-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc2d1-114">Notas</span><span class="sxs-lookup"><span data-stu-id="dc2d1-114">Remarks</span></span>

<span data-ttu-id="dc2d1-115">Esta propiedad puede ser en las operaciones de [IMAPIProp::CopyTo](imapiprop-copyto.md) incluyen o excluyen de operaciones de [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="dc2d1-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="dc2d1-116">Como una propiedad de tipo pt Object, no se correctamente puede recuperar mediante el método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="dc2d1-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="dc2d1-117">El método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , que solicita el identificador de interfaz **IID_IMAPITable** debe tener acceso a su contenido.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="dc2d1-118">Proveedores de servicios deben identificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si se establece, pero es posible que, opcionalmente, identificarlo o no, si no está establecido.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="dc2d1-119">Para recuperar el contenido de la tabla, una aplicación de cliente debe llamar al método de [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) .</span><span class="sxs-lookup"><span data-stu-id="dc2d1-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="dc2d1-120">For more information, see [Tablas de datos adjuntos](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="dc2d1-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="dc2d1-121">Esta propiedad se puede utilizar para la restricción de subobjetos mediante la especificación de la estructura de [SSubRestriction](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="dc2d1-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="dc2d1-122">Esto permite que el cliente limitar la vista de un contenedor para los mensajes con datos adjuntos de la reunión criterios dados.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="dc2d1-123">Un mensaje se califica para ver si hay al menos una fila en su tabla de datos adjuntos, es decir, un dato adjunto, satisface la restricción de subobjetos.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dc2d1-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc2d1-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dc2d1-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="dc2d1-125">Protocol specifications</span></span>

<span data-ttu-id="dc2d1-126">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2d1-126">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc2d1-127">Define las estructuras de datos básicos que se usan en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="dc2d1-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2d1-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc2d1-129">Define las estructuras de datos básicos que se usan en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="dc2d1-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2d1-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc2d1-131">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dc2d1-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="dc2d1-132">Header files</span></span>

<span data-ttu-id="dc2d1-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc2d1-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc2d1-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="dc2d1-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dc2d1-135">Mapitags.h</span></span>
  
> <span data-ttu-id="dc2d1-136">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc2d1-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="dc2d1-137">See also</span></span>



[<span data-ttu-id="dc2d1-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dc2d1-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc2d1-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="dc2d1-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc2d1-140">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="dc2d1-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc2d1-141">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="dc2d1-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

