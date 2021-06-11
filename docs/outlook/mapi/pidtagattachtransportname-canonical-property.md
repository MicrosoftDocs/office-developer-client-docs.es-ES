---
title: Propiedad canónica PidTagAttachTransportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bd3a22bf55d03f3a9f06bf5c19650407bcc5627d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361071"
---
# <a name="pidtagattachtransportname-canonical-property"></a><span data-ttu-id="178c8-103">Propiedad canónica PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="178c8-103">PidTagAttachTransportName Canonical Property</span></span>

  
  
<span data-ttu-id="178c8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="178c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="178c8-105">Contiene el nombre de un archivo adjunto modificado para que se pueda asociar a mensajes TNEF.</span><span class="sxs-lookup"><span data-stu-id="178c8-105">Contains the name of an attachment file modified so that it can be associated with TNEF messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="178c8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="178c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="178c8-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="178c8-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="178c8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="178c8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="178c8-109">0x370C</span><span class="sxs-lookup"><span data-stu-id="178c8-109">0x370C</span></span>  <br/> |
|<span data-ttu-id="178c8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="178c8-110">Data type:</span></span>  <br/> |<span data-ttu-id="178c8-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="178c8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="178c8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="178c8-112">Area:</span></span>  <br/> |<span data-ttu-id="178c8-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="178c8-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="178c8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="178c8-114">Remarks</span></span>

<span data-ttu-id="178c8-115">TNEF y el proveedor de transporte usan estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="178c8-115">TNEF and the transport provider use these properties.</span></span> <span data-ttu-id="178c8-116">Por lo general, no están disponibles para las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="178c8-116">They are usually not available to client applications.</span></span> 
  
<span data-ttu-id="178c8-117">TNEF usa normalmente estas propiedades cuando el sistema de mensajería subyacente no admite los nombres de archivo proporcionados.</span><span class="sxs-lookup"><span data-stu-id="178c8-117">These properties are commonly used by TNEF when the underlying messaging system does not support the supplied filenames.</span></span> <span data-ttu-id="178c8-118">Por ejemplo, se usan cuando el usuario adjunta varios archivos con el mismo nombre, como cinco archivos denominados CONFIG.SYS.</span><span class="sxs-lookup"><span data-stu-id="178c8-118">For example, they are used when the user attaches multiple files with the same name, such as five files named CONFIG.SYS.</span></span> <span data-ttu-id="178c8-119">El proveedor de transporte debe modificar los nombres para asegurarse de que son únicos.</span><span class="sxs-lookup"><span data-stu-id="178c8-119">The transport provider must modify the names to make sure they are unique.</span></span> <span data-ttu-id="178c8-120">Cada nombre modificado aparece en las propiedades **asociadas** PR_ATTACH_TRANSPORT_NAME datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="178c8-120">Each modified name appears in its attachment's **PR_ATTACH_TRANSPORT_NAME** and associated properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="178c8-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="178c8-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="178c8-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="178c8-122">Protocol specifications</span></span>

<span data-ttu-id="178c8-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="178c8-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="178c8-124">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="178c8-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="178c8-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="178c8-125">Header files</span></span>

<span data-ttu-id="178c8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="178c8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="178c8-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="178c8-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="178c8-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="178c8-128">Mapitags.h</span></span>
  
> <span data-ttu-id="178c8-129">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="178c8-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="178c8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="178c8-130">See also</span></span>



[<span data-ttu-id="178c8-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="178c8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="178c8-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="178c8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="178c8-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="178c8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="178c8-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="178c8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

