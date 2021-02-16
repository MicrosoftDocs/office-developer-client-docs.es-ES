---
title: Propiedad canónica PidLidUseTnef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 56f6e2355ee2e64cc766bafe27cd59454e210ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315424"
---
# <a name="pidlidusetnef-canonical-property"></a><span data-ttu-id="0221e-103">Propiedad canónica PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="0221e-103">PidLidUseTnef Canonical Property</span></span>

  
  
<span data-ttu-id="0221e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0221e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0221e-105">Especifica si el formato de encapsulamiento neutro para transporte (TNEF) debe incluirse en un mensaje cuando ese mensaje se convierte de MAPI a extensiones multipropósito al correo de Internet (MIME) o al formato smtp (Protocolo simple de transferencia de correo).</span><span class="sxs-lookup"><span data-stu-id="0221e-105">Specifies whether Transport Neutral Encapsulation Format (TNEF) should be included on a message when that message is converted from MAPI to Multipurpose Internet Mail Extensions (MIME) or Simple Mail Transfer Protocol (SMTP) format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0221e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0221e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0221e-107">dispidUseTNEF</span><span class="sxs-lookup"><span data-stu-id="0221e-107">dispidUseTNEF</span></span>  <br/> |
|<span data-ttu-id="0221e-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="0221e-108">Property set:</span></span>  <br/> |<span data-ttu-id="0221e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="0221e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="0221e-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0221e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0221e-111">0x00008582</span><span class="sxs-lookup"><span data-stu-id="0221e-111">0x00008582</span></span>  <br/> |
|<span data-ttu-id="0221e-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0221e-112">Data type:</span></span>  <br/> |<span data-ttu-id="0221e-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0221e-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0221e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0221e-114">Area:</span></span>  <br/> |<span data-ttu-id="0221e-115">Configuración en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="0221e-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0221e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0221e-116">Remarks</span></span>

<span data-ttu-id="0221e-117">Esta propiedad especifica si TNEF debe incluirse en un mensaje cuando ese mensaje se convierte de TNEF a formato MIME o SMTP.</span><span class="sxs-lookup"><span data-stu-id="0221e-117">This property specifies whether TNEF should be included on a message when that message is converted from TNEF to MIME or SMTP format.</span></span> <span data-ttu-id="0221e-118">Es posible que esta propiedad no esté presente y, si es así, TNEF no debe incluirse en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0221e-118">This property may be absent, and if so, TNEF must not be included on the message.</span></span>
  
<span data-ttu-id="0221e-119">Esta propiedad solo se aplica cuando el mensaje se envía desde una cuenta de correo POP3/SMTP y no se aplica cuando otros proveedores envían el mensaje, como Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0221e-119">This property only applies when the message is sent from a POP3/SMTP mail account and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span>
  
<span data-ttu-id="0221e-120">En determinadas circunstancias, como cuando se habilitan los botones de votación o se adjunta un objeto incrustado OLE a un mensaje, Outlook puede establecer esta propiedad para forzar el uso de TNEF.</span><span class="sxs-lookup"><span data-stu-id="0221e-120">Under certain circumstances, such as when voting buttons are enabled or an OLE embedded object is attached to a message, Outlook can set this property to force the use of TNEF.</span></span>
  
<span data-ttu-id="0221e-121">La **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) se puede usar para aplicar sólo texto sin formato, y no TNEF, al enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="0221e-121">The **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="0221e-122">Debido a que **PidLidUseTNEF** invalida la configuración en **PR_MSG_EDITOR_FORMAT**, una aplicación que desea forzar texto sin formato en un mensaje saliente también debe buscar **PidLidUseTNEF** y restablecerlo a FALSE.</span><span class="sxs-lookup"><span data-stu-id="0221e-122">Because **PidLidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**, an application that wants to force plain text on an outgoing message should also look for **PidLidUseTNEF** and reset it to FALSE.</span></span> <span data-ttu-id="0221e-123">Además, el complemento debe quitar las características de mensaje que requerían TNEF para evitar datos adjuntos inutilizables en el mensaje que finalmente se envía.</span><span class="sxs-lookup"><span data-stu-id="0221e-123">Additionally, the add-in must remove the message features that required TNEF to avoid unusable attachments on the message that is finally sent.</span></span> 
  
<span data-ttu-id="0221e-124">Use la **marca CCSF_USE_TNEF** al llamar a [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para convertir un mensaje MAPI saliente en una secuencia MIME también puede aplicar TNEF.</span><span class="sxs-lookup"><span data-stu-id="0221e-124">Use the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="0221e-125">Esto se aplica incluso si **pidLidUseTNEF** no está establecido.</span><span class="sxs-lookup"><span data-stu-id="0221e-125">This applies even if **PidLidUseTNEF** is not set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0221e-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0221e-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0221e-127">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="0221e-127">Protocol specifications</span></span>

<span data-ttu-id="0221e-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0221e-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0221e-129">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="0221e-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0221e-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0221e-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0221e-131">Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0221e-131">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="0221e-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0221e-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0221e-133">Codifica y descodifica objetos de mensaje y datos adjuntos a una representación de secuencia eficiente.</span><span class="sxs-lookup"><span data-stu-id="0221e-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0221e-134">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0221e-134">Header files</span></span>

<span data-ttu-id="0221e-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0221e-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="0221e-136">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0221e-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0221e-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0221e-137">See also</span></span>



[<span data-ttu-id="0221e-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0221e-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0221e-139">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="0221e-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0221e-140">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0221e-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0221e-141">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0221e-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

