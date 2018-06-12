---
title: Propiedad canónico PidTagAttachTransportName
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 6828a6436946de27020fa1177223955e07a08faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819261"
---
# <a name="pidtagattachtransportname-canonical-property"></a><span data-ttu-id="d0bd5-103">Propiedad canónico PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="d0bd5-103">PidTagAttachTransportName Canonical Property</span></span>

  
  
<span data-ttu-id="d0bd5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0bd5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0bd5-105">Contiene el nombre de un archivo de datos adjuntos modificado para que se puede asociar con mensajes TNEF.</span><span class="sxs-lookup"><span data-stu-id="d0bd5-105">Contains the name of an attachment file modified so that it can be associated with TNEF messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0bd5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d0bd5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0bd5-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="d0bd5-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="d0bd5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d0bd5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d0bd5-109">0x370C</span><span class="sxs-lookup"><span data-stu-id="d0bd5-109">0x370C</span></span>  <br/> |
|<span data-ttu-id="d0bd5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d0bd5-110">Data type:</span></span>  <br/> |<span data-ttu-id="d0bd5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d0bd5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d0bd5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d0bd5-112">Area:</span></span>  <br/> |<span data-ttu-id="d0bd5-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="d0bd5-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0bd5-114">Notas</span><span class="sxs-lookup"><span data-stu-id="d0bd5-114">Remarks</span></span>

<span data-ttu-id="d0bd5-115">TNEF y el proveedor de transporte usan estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d0bd5-115">TNEF and the transport provider use these properties.</span></span> <span data-ttu-id="d0bd5-116">Normalmente, no están disponibles para las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="d0bd5-116">They are usually not available to client applications.</span></span> 
  
<span data-ttu-id="d0bd5-117">Estas propiedades se usan con frecuencia por TNEF cuando el sistema de mensajería subyacente no es compatible con los nombres de archivo proporcionado.</span><span class="sxs-lookup"><span data-stu-id="d0bd5-117">These properties are commonly used by TNEF when the underlying messaging system does not support the supplied filenames.</span></span> <span data-ttu-id="d0bd5-118">Por ejemplo, se utilizan cuando el usuario asocia a varios archivos con el mismo nombre, como archivos de cinco denominado CONFIG. PREDETERMINADO DEL SISTEMA</span><span class="sxs-lookup"><span data-stu-id="d0bd5-118">For example, they are used when the user attaches multiple files with the same name, such as five files named CONFIG.SYS.</span></span> <span data-ttu-id="d0bd5-119">El proveedor de transporte debe modificar los nombres para asegurarse de que son únicos.</span><span class="sxs-lookup"><span data-stu-id="d0bd5-119">The transport provider must modify the names to make sure they are unique.</span></span> <span data-ttu-id="d0bd5-120">Cada nombre modificado aparece en su adjunto **PR_ATTACH_TRANSPORT_NAME** y propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="d0bd5-120">Each modified name appears in its attachment's **PR_ATTACH_TRANSPORT_NAME** and associated properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d0bd5-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0bd5-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d0bd5-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d0bd5-122">Protocol specifications</span></span>

<span data-ttu-id="d0bd5-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0bd5-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0bd5-124">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d0bd5-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d0bd5-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d0bd5-125">Header files</span></span>

<span data-ttu-id="d0bd5-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0bd5-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0bd5-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d0bd5-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d0bd5-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d0bd5-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d0bd5-129">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="d0bd5-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0bd5-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="d0bd5-130">See also</span></span>



[<span data-ttu-id="d0bd5-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d0bd5-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0bd5-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d0bd5-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0bd5-133">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="d0bd5-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0bd5-134">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d0bd5-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

