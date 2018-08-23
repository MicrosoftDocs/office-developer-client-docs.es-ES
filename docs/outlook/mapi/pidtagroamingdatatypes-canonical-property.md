---
title: Propiedad canónica PidTagRoamingDatatypes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2b29f47191bc1f12653ddcc4e78dd8b3401f0480
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587645"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a><span data-ttu-id="f6097-103">Propiedad canónica PidTagRoamingDatatypes</span><span class="sxs-lookup"><span data-stu-id="f6097-103">PidTagRoamingDatatypes Canonical Property</span></span>

  
  
<span data-ttu-id="f6097-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6097-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6097-105">Contiene una máscara de bits que indica qué secuencia de propiedades que existen en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f6097-105">Contains a bitmask that indicates which stream properties exist on the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f6097-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f6097-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6097-107">PR_ROAMING_DATATYPES</span><span class="sxs-lookup"><span data-stu-id="f6097-107">PR_ROAMING_DATATYPES</span></span>  <br/> |
|<span data-ttu-id="f6097-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f6097-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f6097-109">0x7C06</span><span class="sxs-lookup"><span data-stu-id="f6097-109">0x7C06</span></span>  <br/> |
|<span data-ttu-id="f6097-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f6097-110">Data type:</span></span>  <br/> |<span data-ttu-id="f6097-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f6097-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f6097-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f6097-112">Area:</span></span>  <br/> |<span data-ttu-id="f6097-113">Configuración</span><span class="sxs-lookup"><span data-stu-id="f6097-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6097-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f6097-114">Remarks</span></span>

<span data-ttu-id="f6097-115">Esta propiedad debe establecerse en uno o varios de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="f6097-115">This property must be set to one or more of the following values:</span></span>
  
|<span data-ttu-id="f6097-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f6097-116">**Value**</span></span>|<span data-ttu-id="f6097-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f6097-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f6097-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f6097-118">0x00000002</span></span>  <br/> |<span data-ttu-id="f6097-119">Indica que el mensaje de la carpeta asociada información (FAI) debe contener una secuencia de diccionario, serializa en un esquema XML fijo y almacena en la propiedad **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f6097-119">Indicates that the Folder Associated Information (FAI) message should contain a Dictionary stream, serialized into a fixed XML schema and stored in the **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) property.</span></span> <span data-ttu-id="f6097-120">Si el mensaje FAI no contiene una secuencia de diccionario, la aplicación debe tratar el diccionario como no tener ninguna entrada.</span><span class="sxs-lookup"><span data-stu-id="f6097-120">If the FAI message does not contain a Dictionary stream, the application must treat the Dictionary as having no entries.</span></span>  <br/> |
|<span data-ttu-id="f6097-121">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="f6097-121">0x00000004</span></span>  <br/> |<span data-ttu-id="f6097-122">Indica que el mensaje FAI debe contener una secuencia XML que se almacena en la propiedad **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) que utiliza un esquema XML arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f6097-122">Indicates that the FAI message must contain an XML stream stored in the **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) property that uses an arbitrary XML schema.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f6097-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6097-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f6097-124">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f6097-124">Protocol specifications</span></span>

<span data-ttu-id="f6097-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6097-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6097-126">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f6097-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f6097-127">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6097-127">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6097-128">Especifica la ubicación y las propiedades de datos de configuración de cliente y servidor, como las listas de categoría compartida y horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f6097-128">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f6097-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f6097-129">Header files</span></span>

<span data-ttu-id="f6097-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6097-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6097-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f6097-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="f6097-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f6097-132">Mapitags.h</span></span>
  
> <span data-ttu-id="f6097-133">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="f6097-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6097-134">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f6097-134">See also</span></span>



[<span data-ttu-id="f6097-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f6097-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6097-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f6097-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6097-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f6097-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6097-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f6097-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

