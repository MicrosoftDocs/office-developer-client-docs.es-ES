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
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341114"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a><span data-ttu-id="f0ac6-103">Propiedad canónica PidTagRecipientReassignmentProhibited</span><span class="sxs-lookup"><span data-stu-id="f0ac6-103">PidTagRecipientReassignmentProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="f0ac6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0ac6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0ac6-105">Especifica si se prohíbe agregar destinatarios adicionales, cuando se reenvía el mensaje, para el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f0ac6-105">Specifies whether adding additional recipients, when forwarding the message, is prohibited for the email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f0ac6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f0ac6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f0ac6-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="f0ac6-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="f0ac6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f0ac6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f0ac6-109">0x002B</span><span class="sxs-lookup"><span data-stu-id="f0ac6-109">0x002B</span></span>  <br/> |
|<span data-ttu-id="f0ac6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f0ac6-110">Data type:</span></span>  <br/> |<span data-ttu-id="f0ac6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f0ac6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f0ac6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f0ac6-112">Area:</span></span>  <br/> |<span data-ttu-id="f0ac6-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="f0ac6-113">MAPI Envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0ac6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f0ac6-114">Remarks</span></span>

<span data-ttu-id="f0ac6-115">Esta propiedad se establece en función del valor de **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f0ac6-115">This property is set based on the email message's **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) value.</span></span> <span data-ttu-id="f0ac6-116">Si **PR_SENSITIVITY** se establece en "0x00000000" (normal) o "0x00000003" (confidencial), esta propiedad debe establecerse en "0x00" o no existir, lo que significa que se pueden agregar destinatarios adicionales o distintos al mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f0ac6-116">If **PR_SENSITIVITY** is set to "0x00000000" (normal) or "0x00000003" (confidential), this property must be set to "0x00" or absent meaning that adding additional or different recipients to the email message is allowed.</span></span> <span data-ttu-id="f0ac6-117">Si el **PR_SENSITIVITY** del objeto de correo electrónico se establece en "0x00000001" (personal) o "0x00000002" (privado), esta propiedad se debe establecer "0x01" para evitar que se agreguen destinatarios adicionales o distintos de este correo electrónico a través del reenvío.</span><span class="sxs-lookup"><span data-stu-id="f0ac6-117">If the email object's **PR_SENSITIVITY** is set to "0x00000001" (personal) or "0x00000002" (private), this property must be set "0x01" to prevent adding additional or different recipients of this email through forwarding.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f0ac6-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0ac6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f0ac6-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f0ac6-119">Protocol specifications</span></span>

<span data-ttu-id="f0ac6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0ac6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0ac6-121">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f0ac6-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f0ac6-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0ac6-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0ac6-123">Especifica las propiedades y operaciones que se admiten en los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f0ac6-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f0ac6-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f0ac6-124">Header files</span></span>

<span data-ttu-id="f0ac6-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f0ac6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f0ac6-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f0ac6-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f0ac6-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f0ac6-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f0ac6-128">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="f0ac6-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0ac6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0ac6-129">See also</span></span>



[<span data-ttu-id="f0ac6-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f0ac6-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f0ac6-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f0ac6-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f0ac6-132">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f0ac6-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f0ac6-133">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f0ac6-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

