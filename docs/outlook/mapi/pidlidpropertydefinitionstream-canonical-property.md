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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315942"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a><span data-ttu-id="24ce9-103">Propiedad canónica PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="24ce9-103">PidLidPropertyDefinitionStream Canonical Property</span></span>

  
  
<span data-ttu-id="24ce9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24ce9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24ce9-105">Representa las definiciones de campos definidos por el usuario y la configuración de enlace de datos de los campos integrados de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="24ce9-105">Represents definitions of user-defined fields and data-binding settings of built-in fields of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="24ce9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="24ce9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24ce9-107">dispidPropDefStream</span><span class="sxs-lookup"><span data-stu-id="24ce9-107">dispidPropDefStream</span></span>  <br/> |
|<span data-ttu-id="24ce9-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="24ce9-108">Property set:</span></span>  <br/> |<span data-ttu-id="24ce9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="24ce9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="24ce9-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="24ce9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="24ce9-111">0x00008540</span><span class="sxs-lookup"><span data-stu-id="24ce9-111">0x00008540</span></span>  <br/> |
|<span data-ttu-id="24ce9-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="24ce9-112">Data type:</span></span>  <br/> |<span data-ttu-id="24ce9-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="24ce9-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="24ce9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="24ce9-114">Area:</span></span>  <br/> |<span data-ttu-id="24ce9-115">Configuración en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="24ce9-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24ce9-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="24ce9-116">Remarks</span></span>

<span data-ttu-id="24ce9-117">El valor de la **propiedad PidLidPropertyDefinitionStream** se guarda como parte de la definición de formulario personalizada del mensaje.</span><span class="sxs-lookup"><span data-stu-id="24ce9-117">The value of the **PidLidPropertyDefinitionStream** property is saved as part of the custom form definition for the message.</span></span> 
  
<span data-ttu-id="24ce9-118">El valor de esta propiedad es una secuencia binaria.</span><span class="sxs-lookup"><span data-stu-id="24ce9-118">The value of this property is a binary stream.</span></span> <span data-ttu-id="24ce9-119">Para obtener información sobre la estructura de esta secuencia, vea [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="24ce9-119">For information on the structure of this stream, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="24ce9-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="24ce9-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="24ce9-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="24ce9-121">Protocol specifications</span></span>

<span data-ttu-id="24ce9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24ce9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24ce9-123">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="24ce9-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="24ce9-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="24ce9-124">Header files</span></span>

<span data-ttu-id="24ce9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24ce9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="24ce9-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="24ce9-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24ce9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="24ce9-127">See also</span></span>



[<span data-ttu-id="24ce9-128">Outlook Elementos y campos</span><span class="sxs-lookup"><span data-stu-id="24ce9-128">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="24ce9-129">Agregar una definición para un nuevo User-Defined campo</span><span class="sxs-lookup"><span data-stu-id="24ce9-129">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="24ce9-130">Ejemplo de secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="24ce9-130">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="24ce9-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="24ce9-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24ce9-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="24ce9-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24ce9-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="24ce9-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24ce9-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="24ce9-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

