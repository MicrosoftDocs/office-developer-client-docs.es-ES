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
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="8c7cc-103">Propiedad canónica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="8c7cc-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="8c7cc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c7cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c7cc-105">Contiene una tabla de datos adjuntos de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-105">Contains a table of attachments for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c7cc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8c7cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c7cc-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="8c7cc-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="8c7cc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8c7cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8c7cc-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="8c7cc-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="8c7cc-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8c7cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="8c7cc-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="8c7cc-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="8c7cc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8c7cc-112">Area:</span></span>  <br/> |<span data-ttu-id="8c7cc-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="8c7cc-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c7cc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c7cc-114">Remarks</span></span>

<span data-ttu-id="8c7cc-115">Esta propiedad puede excluirse en operaciones [IMAPIProp::CopyTo](imapiprop-copyto.md) o incluirse en [operaciones IMAPIProp::CopyProps.](imapiprop-copyprops.md)</span><span class="sxs-lookup"><span data-stu-id="8c7cc-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="8c7cc-116">Como propiedad de tipo PT_OBJECT, el método [IMAPIProp::GetProps](imapiprop-getprops.md) no puede recuperarla correctamente.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="8c7cc-117">El método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) debe tener acceso a su contenido, solicitando el **identificador IID_IMAPITable** interfaz.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="8c7cc-118">Los proveedores de servicios deben notificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si está establecido, pero opcionalmente pueden notificarlo o no si no está establecido.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="8c7cc-119">Para recuperar el contenido de la tabla, una aplicación cliente debe llamar al método [IMessage::GetAttachmentTable.](imessage-getattachmenttable.md)</span><span class="sxs-lookup"><span data-stu-id="8c7cc-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="8c7cc-120">For more information, see [Tablas de datos adjuntos](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8c7cc-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="8c7cc-121">Esta propiedad puede usarse para la restricción de subobjetos si se especifica en la estructura [SSubRestriction.](ssubrestriction.md)</span><span class="sxs-lookup"><span data-stu-id="8c7cc-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="8c7cc-122">Esto permite que el cliente limite la vista de un contenedor a los mensajes con datos adjuntos que cumplan determinados criterios.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="8c7cc-123">Un mensaje cumple los requisitos para ver si al menos una fila de la tabla de datos adjuntos, es decir, un dato adjunto, satisface la restricción del subobjeto.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8c7cc-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c7cc-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c7cc-125">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="8c7cc-125">Protocol specifications</span></span>

<span data-ttu-id="8c7cc-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c7cc-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c7cc-127">Define las estructuras de datos básicas que se usan en operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="8c7cc-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c7cc-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c7cc-129">Define las estructuras de datos básicas que se usan en operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="8c7cc-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c7cc-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c7cc-131">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c7cc-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8c7cc-132">Header files</span></span>

<span data-ttu-id="8c7cc-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c7cc-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c7cc-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="8c7cc-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8c7cc-135">Mapitags.h</span></span>
  
> <span data-ttu-id="8c7cc-136">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c7cc-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8c7cc-137">See also</span></span>



[<span data-ttu-id="8c7cc-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8c7cc-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c7cc-139">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="8c7cc-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c7cc-140">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8c7cc-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c7cc-141">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8c7cc-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

