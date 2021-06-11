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
ms.openlocfilehash: 0ab904625d3a23462a4fedf3b64f49c54b34ad28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357907"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a><span data-ttu-id="d8e49-103">Propiedad canónica PidTagDefaultPostMessageClass</span><span class="sxs-lookup"><span data-stu-id="d8e49-103">PidTagDefaultPostMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="d8e49-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8e49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8e49-105">Contiene el nombre de una clase Message del formulario personalizado.</span><span class="sxs-lookup"><span data-stu-id="d8e49-105">Contains the name of a custom form Message class.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8e49-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d8e49-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d8e49-107">PR_DEF_POST_MSGCLASS</span><span class="sxs-lookup"><span data-stu-id="d8e49-107">PR_DEF_POST_MSGCLASS</span></span>  <br/> |
|<span data-ttu-id="d8e49-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d8e49-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d8e49-109">0x36E5</span><span class="sxs-lookup"><span data-stu-id="d8e49-109">0x36E5</span></span>  <br/> |
|<span data-ttu-id="d8e49-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d8e49-110">Data type:</span></span>  <br/> |<span data-ttu-id="d8e49-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="d8e49-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="d8e49-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d8e49-112">Area:</span></span>  <br/> |<span data-ttu-id="d8e49-113">Contenedor MAPI</span><span class="sxs-lookup"><span data-stu-id="d8e49-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8e49-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8e49-114">Remarks</span></span>

<span data-ttu-id="d8e49-115">Si esta propiedad se establece en una carpeta, el valor debe contener exactamente la clase de mensaje base (por ejemplo, "IPM. Contacto" para una carpeta de contactos o "IPM. Appointment" para una carpeta de calendario) o comenzar con la clase de mensaje base (por ejemplo, "IPM. Contact.MyContact").</span><span class="sxs-lookup"><span data-stu-id="d8e49-115">If this property is set on a folder, the value must contain either exactly the base message class (for example, "IPM.Contact" for a contacts folder or "IPM.Appointment" for a calendar folder), or begin with the base message class (for example, "IPM.Contact.MyContact").</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d8e49-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8e49-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d8e49-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="d8e49-117">Protocol specifications</span></span>

<span data-ttu-id="d8e49-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8e49-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8e49-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="d8e49-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d8e49-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8e49-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8e49-121">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="d8e49-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d8e49-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d8e49-122">Header files</span></span>

<span data-ttu-id="d8e49-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d8e49-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d8e49-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d8e49-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d8e49-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d8e49-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d8e49-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d8e49-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8e49-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8e49-127">See also</span></span>



[<span data-ttu-id="d8e49-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d8e49-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d8e49-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d8e49-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d8e49-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d8e49-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d8e49-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="d8e49-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

