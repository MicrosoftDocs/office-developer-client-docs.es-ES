---
title: Propiedad canónica PidTagViewDescriptorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewDescriptorName
api_type:
- COM
ms.assetid: 1e689ee4-9e89-4328-beb9-05c80a6544a0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 55d838661dcbe0efb604e6a623a434f9ae87512e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567786"
---
# <a name="pidtagviewdescriptorname-canonical-property"></a><span data-ttu-id="b3f2c-103">Propiedad canónica PidTagViewDescriptorName</span><span class="sxs-lookup"><span data-stu-id="b3f2c-103">PidTagViewDescriptorName Canonical Property</span></span>

  
  
<span data-ttu-id="b3f2c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3f2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3f2c-105">Contiene el nombre de un descriptor de vista.</span><span class="sxs-lookup"><span data-stu-id="b3f2c-105">Contains the name of a view descriptor.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b3f2c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b3f2c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b3f2c-107">PR_VD_NAME, PR_VD_NAME_A, PR_VD_NAME_W</span><span class="sxs-lookup"><span data-stu-id="b3f2c-107">PR_VD_NAME, PR_VD_NAME_A, PR_VD_NAME_W</span></span>  <br/> |
|<span data-ttu-id="b3f2c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b3f2c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b3f2c-109">0x7006</span><span class="sxs-lookup"><span data-stu-id="b3f2c-109">0x7006</span></span>  <br/> |
|<span data-ttu-id="b3f2c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b3f2c-110">Data type:</span></span>  <br/> |<span data-ttu-id="b3f2c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b3f2c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b3f2c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b3f2c-112">Area:</span></span>  <br/> |<span data-ttu-id="b3f2c-113">Mensaje definido por la clase transmisible</span><span class="sxs-lookup"><span data-stu-id="b3f2c-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3f2c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b3f2c-114">Remarks</span></span>

<span data-ttu-id="b3f2c-115">Estas propiedades se deben establecer en una cadena no vacía para un mensaje de carpeta asociar información (FAI) que contiene las definiciones de vista.</span><span class="sxs-lookup"><span data-stu-id="b3f2c-115">These properties must be set to a non-empty string for a Folder Associate Information (FAI) message that contains view definitions.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b3f2c-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3f2c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b3f2c-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b3f2c-117">Protocol specifications</span></span>

<span data-ttu-id="b3f2c-118">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b3f2c-118">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b3f2c-119">Especifica la ubicación y las propiedades de datos de configuración de cliente y servidor, como las listas de categoría compartida y horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="b3f2c-119">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b3f2c-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b3f2c-120">Header files</span></span>

<span data-ttu-id="b3f2c-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b3f2c-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="b3f2c-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b3f2c-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="b3f2c-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b3f2c-123">Mapitags.h</span></span>
  
> <span data-ttu-id="b3f2c-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b3f2c-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b3f2c-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="b3f2c-125">See also</span></span>



[<span data-ttu-id="b3f2c-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b3f2c-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b3f2c-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b3f2c-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b3f2c-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b3f2c-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b3f2c-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b3f2c-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

