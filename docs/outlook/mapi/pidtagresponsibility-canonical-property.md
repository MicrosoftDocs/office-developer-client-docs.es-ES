---
title: Propiedad canónica PidTagResponsibility
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9dba26ab6948d7190521ff31a8732c4b058ab7c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820116"
---
# <a name="pidtagresponsibility-canonical-property"></a><span data-ttu-id="4123e-103">Propiedad canónica PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="4123e-103">PidTagResponsibility Canonical Property</span></span>

  
  
<span data-ttu-id="4123e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4123e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4123e-105">Contiene TRUE si algún proveedor de transporte ya ha aceptado la responsabilidad de entregar el mensaje a este destinatario y FALSE si la cola MAPI se considera que este proveedor de transporte debe aceptar responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="4123e-105">Contains TRUE if some transport provider has already accepted responsibility for delivering the message to this recipient, and FALSE if the MAPI spooler considers that this transport provider should accept responsibility.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4123e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4123e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4123e-107">PR_RESPONSIBILITY</span><span class="sxs-lookup"><span data-stu-id="4123e-107">PR_RESPONSIBILITY</span></span>  <br/> |
|<span data-ttu-id="4123e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4123e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4123e-109">0x0E0F</span><span class="sxs-lookup"><span data-stu-id="4123e-109">0x0E0F</span></span>  <br/> |
|<span data-ttu-id="4123e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4123e-110">Data type:</span></span>  <br/> |<span data-ttu-id="4123e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4123e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4123e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4123e-112">Area:</span></span>  <br/> |<span data-ttu-id="4123e-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="4123e-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4123e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4123e-114">Remarks</span></span>

<span data-ttu-id="4123e-115">Cuando la cola MAPI presenta un mensaje saliente a un proveedor de transporte, a través de [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), se establece esta propiedad en FALSE para todos los destinatarios para que la cola MAPI considera ese proveedor de transporte responsable y TRUE para todas las otros destinatarios.</span><span class="sxs-lookup"><span data-stu-id="4123e-115">When the MAPI spooler presents an outbound message to a transport provider, through [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), it sets this property to FALSE for all recipients for which the MAPI spooler considers that transport provider responsible, and TRUE for all other recipients.</span></span> <span data-ttu-id="4123e-116">El proveedor de transporte debe intentar controlar a todos los destinatarios con **PR_RESPONSIBILITY** establecida en FALSE.</span><span class="sxs-lookup"><span data-stu-id="4123e-116">The transport provider should attempt to handle all recipients with **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="4123e-117">Después de enviar correctamente, o la certeza con errores enviar a un destinatario, el proveedor de transporte debe establecer esta propiedad en TRUE en el mensaje de origen para indicar que ha aceptado la responsabilidad de ese destinatario.</span><span class="sxs-lookup"><span data-stu-id="4123e-117">After successfully sending, or conclusively failing to send, to a recipient, the transport provider should set this property to TRUE in the source message to indicate that it has accepted responsibility for that recipient.</span></span> 
  
<span data-ttu-id="4123e-118">Si, después de examinar a un destinatario, un proveedor de transporte decide que no se puede o no debería administrar, el proveedor de transporte debe dejar **PR_RESPONSIBILITY** conjunto en FALSE.</span><span class="sxs-lookup"><span data-stu-id="4123e-118">If, after examining a recipient, a transport provider decides that it cannot or should not handle it, the transport provider should leave **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="4123e-119">Otro proveedor de transporte que puede administrar a ese destinatario, a continuación, buscará la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="4123e-119">The MAPI spooler will then look for another transport provider that can handle that recipient.</span></span> <span data-ttu-id="4123e-120">En última instancia, la cola MAPI crea un informe de no entrega para todos los destinatarios para que ningún proveedor de transporte acepta responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="4123e-120">The MAPI spooler ultimately creates a nondelivery report for any recipients for which no transport provider accepts responsibility.</span></span> 
  
<span data-ttu-id="4123e-121">Si el proveedor de transporte intenta y no puede entregar el mensaje, debe llamar al método de [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para indicar a MAPI las razones para el error, por lo que MAPI puede generar un informe de no entrega.</span><span class="sxs-lookup"><span data-stu-id="4123e-121">If the transport provider attempts and fails to deliver the message, it should call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate to MAPI the reasons for the failure, so that MAPI can generate a nondelivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4123e-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4123e-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4123e-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4123e-123">Protocol specifications</span></span>

<span data-ttu-id="4123e-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4123e-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4123e-125">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4123e-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4123e-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4123e-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4123e-127">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="4123e-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4123e-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4123e-128">Header files</span></span>

<span data-ttu-id="4123e-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4123e-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="4123e-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4123e-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="4123e-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4123e-131">Mapitags.h</span></span>
  
> <span data-ttu-id="4123e-132">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4123e-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4123e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="4123e-133">See also</span></span>



[<span data-ttu-id="4123e-134">Propiedad can�nico de PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="4123e-134">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)


[<span data-ttu-id="4123e-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4123e-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4123e-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4123e-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4123e-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4123e-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4123e-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="4123e-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

