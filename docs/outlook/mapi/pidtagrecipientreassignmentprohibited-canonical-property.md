---
title: Propiedad canónica PidTagRecipientReassignmentProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0176485ca9b84260176e3be8ec9c8f42cf755cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820045"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a><span data-ttu-id="9b785-103">Propiedad canónica PidTagRecipientReassignmentProhibited</span><span class="sxs-lookup"><span data-stu-id="9b785-103">PidTagRecipientReassignmentProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="9b785-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9b785-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9b785-105">Especifica si agregar destinatarios adicionales, al reenviar el mensaje, está prohibido para el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9b785-105">Specifies whether adding additional recipients, when forwarding the message, is prohibited for the email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9b785-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9b785-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9b785-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="9b785-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="9b785-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9b785-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9b785-109">0x002B</span><span class="sxs-lookup"><span data-stu-id="9b785-109">0x002B</span></span>  <br/> |
|<span data-ttu-id="9b785-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9b785-110">Data type:</span></span>  <br/> |<span data-ttu-id="9b785-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9b785-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9b785-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9b785-112">Area:</span></span>  <br/> |<span data-ttu-id="9b785-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="9b785-113">MAPI Envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b785-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b785-114">Remarks</span></span>

<span data-ttu-id="9b785-115">Esta propiedad se establece en función de valor de **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9b785-115">This property is set based on the email message's **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) value.</span></span> <span data-ttu-id="9b785-116">Si **PR_SENSITIVITY** está establecido en "0 x 00000000" (normal) o "0 x 00000003" (confidencial), esta propiedad se debe establecer en "0 x 00" o absent lo que significa que agregar destinatarios adicionales o diferentes para el mensaje de correo electrónico se permite.</span><span class="sxs-lookup"><span data-stu-id="9b785-116">If **PR_SENSITIVITY** is set to "0x00000000" (normal) or "0x00000003" (confidential), this property must be set to "0x00" or absent meaning that adding additional or different recipients to the email message is allowed.</span></span> <span data-ttu-id="9b785-117">Si el correo electrónico **PR_SENSITIVITY del objeto** se establece en "0 x 00000001" (personal) o "0 x 00000002" (privado), esta propiedad se debe establecer "0 x 01" para evitar que agregar destinatarios adicionales o diferentes de este correo electrónico a través de reenvío.</span><span class="sxs-lookup"><span data-stu-id="9b785-117">If the email object's **PR_SENSITIVITY** is set to "0x00000001" (personal) or "0x00000002" (private), this property must be set "0x01" to prevent adding additional or different recipients of this email through forwarding.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9b785-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b785-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9b785-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9b785-119">Protocol specifications</span></span>

<span data-ttu-id="9b785-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b785-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b785-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9b785-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9b785-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b785-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b785-123">Especifica las propiedades y operaciones que se permiten en mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9b785-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9b785-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9b785-124">Header files</span></span>

<span data-ttu-id="9b785-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9b785-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b785-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9b785-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="9b785-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9b785-127">Mapitags.h</span></span>
  
> <span data-ttu-id="9b785-128">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="9b785-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b785-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b785-129">See also</span></span>



[<span data-ttu-id="9b785-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9b785-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b785-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9b785-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b785-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9b785-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b785-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="9b785-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
