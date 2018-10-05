---
title: Propiedad canónica PidLidPropertyDefinitionStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPropertyDefinitionStream
api_type:
- COM
ms.assetid: ead35049-e60e-4b46-bf12-f73d77cd36b2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b5ddb87111cfb0039cb1150338945615bbd5afc5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393274"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a><span data-ttu-id="e761f-103">Propiedad canónica PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="e761f-103">PidLidPropertyDefinitionStream Canonical Property</span></span>

  
  
<span data-ttu-id="e761f-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e761f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e761f-105">Representa las definiciones de campos definidos por el usuario y la configuración de enlace de datos de los campos integrados de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e761f-105">Represents definitions of user-defined fields and data-binding settings of built-in fields of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e761f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e761f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e761f-107">dispidPropDefStream</span><span class="sxs-lookup"><span data-stu-id="e761f-107">dispidPropDefStream</span></span>  <br/> |
|<span data-ttu-id="e761f-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e761f-108">Property set:</span></span>  <br/> |<span data-ttu-id="e761f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e761f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e761f-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="e761f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e761f-111">0x00008540</span><span class="sxs-lookup"><span data-stu-id="e761f-111">0x00008540</span></span>  <br/> |
|<span data-ttu-id="e761f-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e761f-112">Data type:</span></span>  <br/> |<span data-ttu-id="e761f-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e761f-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e761f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e761f-114">Area:</span></span>  <br/> |<span data-ttu-id="e761f-115">Configuración de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="e761f-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e761f-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e761f-116">Remarks</span></span>

<span data-ttu-id="e761f-117">El valor de la propiedad **PidLidPropertyDefinitionStream** se guarda como parte de la definición de formulario personalizado para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e761f-117">The value of the **PidLidPropertyDefinitionStream** property is saved as part of the custom form definition for the message.</span></span> 
  
<span data-ttu-id="e761f-118">El valor de esta propiedad es una secuencia binaria.</span><span class="sxs-lookup"><span data-stu-id="e761f-118">The value of this property is a binary stream.</span></span> <span data-ttu-id="e761f-119">Para obtener información sobre la estructura de esta secuencia, vea [Estructura de secuencia de PropertyDefinition](propertydefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="e761f-119">For information on the structure of this stream, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e761f-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e761f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e761f-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e761f-121">Protocol specifications</span></span>

<span data-ttu-id="e761f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e761f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e761f-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e761f-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e761f-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e761f-124">Header files</span></span>

<span data-ttu-id="e761f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e761f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e761f-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e761f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e761f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e761f-127">See also</span></span>



[<span data-ttu-id="e761f-128">Campos y elementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="e761f-128">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="e761f-129">Agregar una definición para un nuevo campo definido por el usuario</span><span class="sxs-lookup"><span data-stu-id="e761f-129">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="e761f-130">Ejemplo de flujo PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="e761f-130">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="e761f-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e761f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e761f-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e761f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e761f-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e761f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e761f-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e761f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

