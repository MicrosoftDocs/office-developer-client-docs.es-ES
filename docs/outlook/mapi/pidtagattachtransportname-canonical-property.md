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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400519"
---
# <a name="pidtagattachtransportname-canonical-property"></a><span data-ttu-id="260c1-103">Propiedad canónica PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="260c1-103">PidTagAttachTransportName Canonical Property</span></span>

  
  
<span data-ttu-id="260c1-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="260c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="260c1-105">Contiene el nombre de un archivo de datos adjuntos modificado para que se puede asociar con mensajes TNEF.</span><span class="sxs-lookup"><span data-stu-id="260c1-105">Contains the name of an attachment file modified so that it can be associated with TNEF messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="260c1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="260c1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="260c1-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="260c1-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="260c1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="260c1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="260c1-109">0x370C</span><span class="sxs-lookup"><span data-stu-id="260c1-109">0x370C</span></span>  <br/> |
|<span data-ttu-id="260c1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="260c1-110">Data type:</span></span>  <br/> |<span data-ttu-id="260c1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="260c1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="260c1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="260c1-112">Area:</span></span>  <br/> |<span data-ttu-id="260c1-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="260c1-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="260c1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="260c1-114">Remarks</span></span>

<span data-ttu-id="260c1-115">TNEF y el proveedor de transporte usan estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="260c1-115">TNEF and the transport provider use these properties.</span></span> <span data-ttu-id="260c1-116">Normalmente, no están disponibles para las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="260c1-116">They are usually not available to client applications.</span></span> 
  
<span data-ttu-id="260c1-117">Estas propiedades se usan con frecuencia por TNEF cuando el sistema de mensajería subyacente no es compatible con los nombres de archivo proporcionado.</span><span class="sxs-lookup"><span data-stu-id="260c1-117">These properties are commonly used by TNEF when the underlying messaging system does not support the supplied filenames.</span></span> <span data-ttu-id="260c1-118">Por ejemplo, se utilizan cuando el usuario asocia a varios archivos con el mismo nombre, como archivos de cinco denominado CONFIG. PREDETERMINADO DEL SISTEMA</span><span class="sxs-lookup"><span data-stu-id="260c1-118">For example, they are used when the user attaches multiple files with the same name, such as five files named CONFIG.SYS.</span></span> <span data-ttu-id="260c1-119">El proveedor de transporte debe modificar los nombres para asegurarse de que son únicos.</span><span class="sxs-lookup"><span data-stu-id="260c1-119">The transport provider must modify the names to make sure they are unique.</span></span> <span data-ttu-id="260c1-120">Cada nombre modificado aparece en su adjunto **PR_ATTACH_TRANSPORT_NAME** y propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="260c1-120">Each modified name appears in its attachment's **PR_ATTACH_TRANSPORT_NAME** and associated properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="260c1-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="260c1-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="260c1-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="260c1-122">Protocol specifications</span></span>

<span data-ttu-id="260c1-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="260c1-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="260c1-124">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="260c1-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="260c1-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="260c1-125">Header files</span></span>

<span data-ttu-id="260c1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="260c1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="260c1-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="260c1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="260c1-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="260c1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="260c1-129">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="260c1-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="260c1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="260c1-130">See also</span></span>



[<span data-ttu-id="260c1-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="260c1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="260c1-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="260c1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="260c1-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="260c1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="260c1-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="260c1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

