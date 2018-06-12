---
title: Propiedad canónico PidLidCleanGlobalObjectId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: a784c91a04cce572c8e30085b1760c28296a1d53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818615"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a><span data-ttu-id="2c6a5-103">Propiedad canónico PidLidCleanGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="2c6a5-103">PidLidCleanGlobalObjectId Canonical Property</span></span>

  
  
<span data-ttu-id="2c6a5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c6a5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c6a5-105">Especifica la limpieza global **ObjectID**.</span><span class="sxs-lookup"><span data-stu-id="2c6a5-105">Specifies the clean global **ObjectID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c6a5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2c6a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c6a5-107">dispidCleanGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="2c6a5-107">dispidCleanGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="2c6a5-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="2c6a5-108">Property set:</span></span>  <br/> |<span data-ttu-id="2c6a5-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="2c6a5-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="2c6a5-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="2c6a5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2c6a5-111">0 x 00000023</span><span class="sxs-lookup"><span data-stu-id="2c6a5-111">0x00000023</span></span>  <br/> |
|<span data-ttu-id="2c6a5-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2c6a5-112">Data type:</span></span>  <br/> |<span data-ttu-id="2c6a5-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2c6a5-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2c6a5-114">Área:</span><span class="sxs-lookup"><span data-stu-id="2c6a5-114">Area:</span></span>  <br/> |<span data-ttu-id="2c6a5-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="2c6a5-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c6a5-116">Notas</span><span class="sxs-lookup"><span data-stu-id="2c6a5-116">Remarks</span></span>

<span data-ttu-id="2c6a5-117">El formato de esta propiedad es el mismo que el de **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2c6a5-117">The format of this property is the same as that of **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span></span> <span data-ttu-id="2c6a5-118">El valor de esta propiedad debe ser igual que el valor de **LID_GLOBAL_OBJID**, excepto la YH, IL, M, y campos de D deben ser cero.</span><span class="sxs-lookup"><span data-stu-id="2c6a5-118">The value of this property must be equal to the value of **LID_GLOBAL_OBJID**, except the YH, YL, M, and D fields must be zero.</span></span> <span data-ttu-id="2c6a5-119">Todos los objetos que hacen referencia a una instancia de una serie periódica (incluida una instancia huérfana), así como la serie periódica propiamente dicha, tendrá el mismo valor para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2c6a5-119">All objects that refer to an Instance of a recurring series (including an orphan instance), as well as the recurring series itself, will have the same value for this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2c6a5-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c6a5-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c6a5-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="2c6a5-121">Protocol specifications</span></span>

<span data-ttu-id="2c6a5-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c6a5-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c6a5-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="2c6a5-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2c6a5-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c6a5-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c6a5-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c6a5-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c6a5-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2c6a5-126">Header files</span></span>

<span data-ttu-id="2c6a5-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c6a5-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c6a5-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2c6a5-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c6a5-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="2c6a5-129">See also</span></span>



[<span data-ttu-id="2c6a5-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2c6a5-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c6a5-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2c6a5-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c6a5-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="2c6a5-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c6a5-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2c6a5-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

