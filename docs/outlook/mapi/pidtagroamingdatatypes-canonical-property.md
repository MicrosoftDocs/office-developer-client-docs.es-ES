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
ms.openlocfilehash: fe5528f7605412d0cfd4b4b914e9b221c715e1b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359559"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a><span data-ttu-id="832ea-103">Propiedad canónica PidTagRoamingDatatypes</span><span class="sxs-lookup"><span data-stu-id="832ea-103">PidTagRoamingDatatypes Canonical Property</span></span>

  
  
<span data-ttu-id="832ea-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="832ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="832ea-105">Contiene una máscara de bits que indica qué propiedades de secuencia existen en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="832ea-105">Contains a bitmask that indicates which stream properties exist on the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="832ea-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="832ea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="832ea-107">PR_ROAMING_DATATYPES</span><span class="sxs-lookup"><span data-stu-id="832ea-107">PR_ROAMING_DATATYPES</span></span>  <br/> |
|<span data-ttu-id="832ea-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="832ea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="832ea-109">0x7C06</span><span class="sxs-lookup"><span data-stu-id="832ea-109">0x7C06</span></span>  <br/> |
|<span data-ttu-id="832ea-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="832ea-110">Data type:</span></span>  <br/> |<span data-ttu-id="832ea-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="832ea-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="832ea-112">Área:</span><span class="sxs-lookup"><span data-stu-id="832ea-112">Area:</span></span>  <br/> |<span data-ttu-id="832ea-113">Configuración</span><span class="sxs-lookup"><span data-stu-id="832ea-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="832ea-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="832ea-114">Remarks</span></span>

<span data-ttu-id="832ea-115">Esta propiedad debe establecerse en uno o varios de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="832ea-115">This property must be set to one or more of the following values:</span></span>
  
|<span data-ttu-id="832ea-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="832ea-116">**Value**</span></span>|<span data-ttu-id="832ea-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="832ea-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="832ea-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="832ea-118">0x00000002</span></span>  <br/> |<span data-ttu-id="832ea-119">Indica que el mensaje de información asociada a carpetas (FAI) debe contener una secuencia Dictionary, serializada en un esquema XML fijo y almacenada en la propiedad **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="832ea-119">Indicates that the Folder Associated Information (FAI) message should contain a Dictionary stream, serialized into a fixed XML schema and stored in the **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) property.</span></span> <span data-ttu-id="832ea-120">Si el mensaje FAI no contiene una secuencia Dictionary, la aplicación debe tratar dictionary como que no tiene entradas.</span><span class="sxs-lookup"><span data-stu-id="832ea-120">If the FAI message does not contain a Dictionary stream, the application must treat the Dictionary as having no entries.</span></span>  <br/> |
|<span data-ttu-id="832ea-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="832ea-121">0x00000004</span></span>  <br/> |<span data-ttu-id="832ea-122">Indica que el mensaje FAI debe contener una secuencia XML almacenada en la propiedad **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) que usa un esquema XML arbitrario.</span><span class="sxs-lookup"><span data-stu-id="832ea-122">Indicates that the FAI message must contain an XML stream stored in the **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) property that uses an arbitrary XML schema.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="832ea-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="832ea-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="832ea-124">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="832ea-124">Protocol specifications</span></span>

<span data-ttu-id="832ea-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="832ea-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="832ea-126">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="832ea-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="832ea-127">[[MS-OCFGCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="832ea-127">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="832ea-128">Especifica la ubicación y las propiedades de los datos de configuración de cliente y servidor, como listas de categorías compartidas y horas laborables.</span><span class="sxs-lookup"><span data-stu-id="832ea-128">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="832ea-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="832ea-129">Header files</span></span>

<span data-ttu-id="832ea-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="832ea-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="832ea-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="832ea-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="832ea-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="832ea-132">Mapitags.h</span></span>
  
> <span data-ttu-id="832ea-133">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="832ea-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="832ea-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="832ea-134">See also</span></span>



[<span data-ttu-id="832ea-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="832ea-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="832ea-136">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="832ea-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="832ea-137">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="832ea-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="832ea-138">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="832ea-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

