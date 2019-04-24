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
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a><span data-ttu-id="4b6ca-103">Propiedad canónica PidTagDefaultPostMessageClass</span><span class="sxs-lookup"><span data-stu-id="4b6ca-103">PidTagDefaultPostMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="4b6ca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b6ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b6ca-105">Contiene el nombre de una clase de mensaje de formulario personalizado.</span><span class="sxs-lookup"><span data-stu-id="4b6ca-105">Contains the name of a custom form Message class.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4b6ca-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4b6ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b6ca-107">PR_DEF_POST_MSGCLASS</span><span class="sxs-lookup"><span data-stu-id="4b6ca-107">PR_DEF_POST_MSGCLASS</span></span>  <br/> |
|<span data-ttu-id="4b6ca-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4b6ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4b6ca-109">0x36E5</span><span class="sxs-lookup"><span data-stu-id="4b6ca-109">0x36E5</span></span>  <br/> |
|<span data-ttu-id="4b6ca-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4b6ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="4b6ca-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="4b6ca-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="4b6ca-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4b6ca-112">Area:</span></span>  <br/> |<span data-ttu-id="4b6ca-113">Contenedor de MAPI</span><span class="sxs-lookup"><span data-stu-id="4b6ca-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b6ca-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b6ca-114">Remarks</span></span>

<span data-ttu-id="4b6ca-115">Si esta propiedad se establece en una carpeta, el valor debe contener exactamente la clase de mensaje base (por ejemplo, "IPM. Contact "para una carpeta de contactos o" IPM. Cita "para una carpeta de calendario) o empezar por la clase de mensaje base (por ejemplo," IPM. Contact. mi contacto ").</span><span class="sxs-lookup"><span data-stu-id="4b6ca-115">If this property is set on a folder, the value must contain either exactly the base message class (for example, "IPM.Contact" for a contacts folder or "IPM.Appointment" for a calendar folder), or begin with the base message class (for example, "IPM.Contact.MyContact").</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4b6ca-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b6ca-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4b6ca-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4b6ca-117">Protocol specifications</span></span>

<span data-ttu-id="4b6ca-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b6ca-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b6ca-119">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4b6ca-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4b6ca-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b6ca-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b6ca-121">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="4b6ca-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4b6ca-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4b6ca-122">Header files</span></span>

<span data-ttu-id="4b6ca-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4b6ca-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b6ca-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4b6ca-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="4b6ca-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4b6ca-125">Mapitags.h</span></span>
  
> <span data-ttu-id="4b6ca-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4b6ca-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b6ca-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b6ca-127">See also</span></span>



[<span data-ttu-id="4b6ca-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4b6ca-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4b6ca-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="4b6ca-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b6ca-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4b6ca-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b6ca-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4b6ca-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

