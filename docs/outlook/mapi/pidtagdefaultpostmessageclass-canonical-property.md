---
title: Propiedad canónica PidTagDefaultPostMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultPostMessageClass
api_type:
- HeaderDef
ms.assetid: 231c288f-547b-4463-9442-1499661b925e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 538cc7cdc6dcb281beead6d06ff8644c534ed569
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819402"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a><span data-ttu-id="0bc0e-103">Propiedad canónica PidTagDefaultPostMessageClass</span><span class="sxs-lookup"><span data-stu-id="0bc0e-103">PidTagDefaultPostMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="0bc0e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0bc0e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0bc0e-105">Contiene el nombre de un clase de mensaje del formulario personalizado.</span><span class="sxs-lookup"><span data-stu-id="0bc0e-105">Contains the name of a custom form Message class.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0bc0e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0bc0e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0bc0e-107">PR_DEF_POST_MSGCLASS</span><span class="sxs-lookup"><span data-stu-id="0bc0e-107">PR_DEF_POST_MSGCLASS</span></span>  <br/> |
|<span data-ttu-id="0bc0e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0bc0e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0bc0e-109">0x36E5</span><span class="sxs-lookup"><span data-stu-id="0bc0e-109">0x36E5</span></span>  <br/> |
|<span data-ttu-id="0bc0e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0bc0e-110">Data type:</span></span>  <br/> |<span data-ttu-id="0bc0e-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="0bc0e-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="0bc0e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0bc0e-112">Area:</span></span>  <br/> |<span data-ttu-id="0bc0e-113">Contenedor MAPI</span><span class="sxs-lookup"><span data-stu-id="0bc0e-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bc0e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0bc0e-114">Remarks</span></span>

<span data-ttu-id="0bc0e-115">Si esta propiedad se establece en una carpeta, el valor debe contener exactamente con la clase base de mensaje (por ejemplo, "IPM. Contacto"para una carpeta de contactos o"IPM. Cita"para una carpeta de calendario), o comenzar con la clase de mensaje base (por ejemplo," IPM. Contact.MyContact").</span><span class="sxs-lookup"><span data-stu-id="0bc0e-115">If this property is set on a folder, the value must contain either exactly the base message class (for example, "IPM.Contact" for a contacts folder or "IPM.Appointment" for a calendar folder), or begin with the base message class (for example, "IPM.Contact.MyContact").</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0bc0e-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0bc0e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0bc0e-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0bc0e-117">Protocol specifications</span></span>

<span data-ttu-id="0bc0e-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bc0e-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bc0e-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0bc0e-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0bc0e-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bc0e-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bc0e-121">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="0bc0e-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0bc0e-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0bc0e-122">Header files</span></span>

<span data-ttu-id="0bc0e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0bc0e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="0bc0e-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0bc0e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="0bc0e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0bc0e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="0bc0e-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0bc0e-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0bc0e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bc0e-127">See also</span></span>



[<span data-ttu-id="0bc0e-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0bc0e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0bc0e-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0bc0e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0bc0e-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0bc0e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0bc0e-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0bc0e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

