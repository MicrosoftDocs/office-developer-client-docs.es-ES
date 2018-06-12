---
title: Propiedad canónico PidTagRoamingDatatypes
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: d8b4df2dbb0d7fd2edeb82222f333c11c5f71987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820121"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a><span data-ttu-id="63873-103">Propiedad canónico PidTagRoamingDatatypes</span><span class="sxs-lookup"><span data-stu-id="63873-103">PidTagRoamingDatatypes Canonical Property</span></span>

  
  
<span data-ttu-id="63873-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63873-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63873-105">Contiene una máscara de bits que indica qué secuencia de propiedades que existen en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="63873-105">Contains a bitmask that indicates which stream properties exist on the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63873-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="63873-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63873-107">PR_ROAMING_DATATYPES</span><span class="sxs-lookup"><span data-stu-id="63873-107">PR_ROAMING_DATATYPES</span></span>  <br/> |
|<span data-ttu-id="63873-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="63873-108">Identifier:</span></span>  <br/> |<span data-ttu-id="63873-109">0x7C06</span><span class="sxs-lookup"><span data-stu-id="63873-109">0x7C06</span></span>  <br/> |
|<span data-ttu-id="63873-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="63873-110">Data type:</span></span>  <br/> |<span data-ttu-id="63873-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="63873-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="63873-112">Área:</span><span class="sxs-lookup"><span data-stu-id="63873-112">Area:</span></span>  <br/> |<span data-ttu-id="63873-113">Configuración</span><span class="sxs-lookup"><span data-stu-id="63873-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63873-114">Notas</span><span class="sxs-lookup"><span data-stu-id="63873-114">Remarks</span></span>

<span data-ttu-id="63873-115">Esta propiedad debe establecerse en uno o varios de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="63873-115">This property must be set to one or more of the following values:</span></span>
  
|<span data-ttu-id="63873-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="63873-116">**Value**</span></span>|<span data-ttu-id="63873-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63873-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="63873-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="63873-118">0x00000002</span></span>  <br/> |<span data-ttu-id="63873-119">Indica que el mensaje de la carpeta asociada información (FAI) debe contener una secuencia de diccionario, serializa en un esquema XML fijo y almacena en la propiedad **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="63873-119">Indicates that the Folder Associated Information (FAI) message should contain a Dictionary stream, serialized into a fixed XML schema and stored in the **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) property.</span></span> <span data-ttu-id="63873-120">Si el mensaje FAI no contiene una secuencia de diccionario, la aplicación debe tratar el diccionario como no tener ninguna entrada.</span><span class="sxs-lookup"><span data-stu-id="63873-120">If the FAI message does not contain a Dictionary stream, the application must treat the Dictionary as having no entries.</span></span>  <br/> |
|<span data-ttu-id="63873-121">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="63873-121">0x00000004</span></span>  <br/> |<span data-ttu-id="63873-122">Indica que el mensaje FAI debe contener una secuencia XML que se almacena en la propiedad **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) que utiliza un esquema XML arbitrario.</span><span class="sxs-lookup"><span data-stu-id="63873-122">Indicates that the FAI message must contain an XML stream stored in the **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) property that uses an arbitrary XML schema.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="63873-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="63873-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63873-124">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="63873-124">Protocol specifications</span></span>

<span data-ttu-id="63873-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63873-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63873-126">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="63873-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="63873-127">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63873-127">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63873-128">Especifica la ubicación y las propiedades de datos de configuración de cliente y servidor, como las listas de categoría compartida y horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="63873-128">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63873-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="63873-129">Header files</span></span>

<span data-ttu-id="63873-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63873-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="63873-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="63873-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="63873-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="63873-132">Mapitags.h</span></span>
  
> <span data-ttu-id="63873-133">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="63873-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63873-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="63873-134">See also</span></span>



[<span data-ttu-id="63873-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="63873-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63873-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="63873-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63873-137">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="63873-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63873-138">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="63873-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

