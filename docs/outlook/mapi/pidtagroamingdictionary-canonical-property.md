---
title: Propiedad canónica PidTagRoamingDictionary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDictionary
api_type:
- COM
ms.assetid: 40b50181-f88c-40ee-b3d0-a36dd36c158e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4b2aa12b1b81dfd218781a839f5f84881763ef06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359552"
---
# <a name="pidtagroamingdictionary-canonical-property"></a><span data-ttu-id="cae81-103">Propiedad canónica PidTagRoamingDictionary</span><span class="sxs-lookup"><span data-stu-id="cae81-103">PidTagRoamingDictionary Canonical Property</span></span>

<span data-ttu-id="cae81-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cae81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cae81-105">Contiene un documento XML que describe el diccionario móvil.</span><span class="sxs-lookup"><span data-stu-id="cae81-105">Contains an XML document that describes the roaming dictionary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cae81-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cae81-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cae81-107">PR_ROAMING_DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="cae81-107">PR_ROAMING_DICTIONARY</span></span>  <br/> |
|<span data-ttu-id="cae81-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cae81-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cae81-109">0x7C07</span><span class="sxs-lookup"><span data-stu-id="cae81-109">0x7C07</span></span>  <br/> |
|<span data-ttu-id="cae81-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cae81-110">Data type:</span></span>  <br/> |<span data-ttu-id="cae81-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cae81-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cae81-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cae81-112">Area:</span></span>  <br/> |<span data-ttu-id="cae81-113">Configuración</span><span class="sxs-lookup"><span data-stu-id="cae81-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cae81-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cae81-114">Remarks</span></span>

<span data-ttu-id="cae81-115">Esta propiedad contiene un documento XML UNICODE que usa codificación UTF8.</span><span class="sxs-lookup"><span data-stu-id="cae81-115">This property contains a UNICODE XML document that is using UTF8 encoding.</span></span> <span data-ttu-id="cae81-116">Un mensaje con una secuencia de diccionario debe establecer esta propiedad con el esquema siguiente:</span><span class="sxs-lookup"><span data-stu-id="cae81-116">A message with a dictionary stream must set this property with the following schema:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?> 
<xs:schema targetNamespace="Dictionary.xsd" xmlns="Dictionary.xsd" xmlns:xs="https://www.w3.org/2001/XMLSchema"> 
   <xs:element name="UserConfiguration"> 
   <xs:complexType> 
   <xs:sequence> 
   <xs:element name="Info"> 
   <xs:complexType> 
   <xs:sequence /> 
   <xs:attribute name="version" type="VersionString"> 
   </xs:attribute> 
   </xs:complexType>
```

<span data-ttu-id="cae81-117">A continuación se muestra un documento XML de ejemplo almacenado en esta propiedad en un mensaje de datos de configuración:</span><span class="sxs-lookup"><span data-stu-id="cae81-117">The following is a sample XML document stored in this property on a Configuration Data message:</span></span> 
  
```xml
<?xml version="1.0"?> 
<UserConfiguration> 
<Info version="Outlook.12"/> 
<Data> <e k="18-piAutoProcess" v="3-True"/> 
<e k="18-piRemindDefault" v="9-15"/> 
<e k="18-piReminderUpgradeTime" v="9-212864507"/> 
<e k="18-OLPrefsVersion" v="9-1"/> 
</Data> 
</UserConfiguration>
```

## <a name="related-resources"></a><span data-ttu-id="cae81-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cae81-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cae81-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="cae81-119">Protocol specifications</span></span>

<span data-ttu-id="cae81-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cae81-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cae81-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="cae81-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cae81-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cae81-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cae81-123">Especifica la ubicación y las propiedades de los datos de configuración de cliente y servidor, como listas de categorías compartidas y horas laborables.</span><span class="sxs-lookup"><span data-stu-id="cae81-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cae81-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cae81-124">Header files</span></span>

<span data-ttu-id="cae81-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cae81-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="cae81-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cae81-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="cae81-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cae81-127">Mapitags.h</span></span>
  
> <span data-ttu-id="cae81-128">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="cae81-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cae81-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="cae81-129">See also</span></span>



[<span data-ttu-id="cae81-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cae81-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cae81-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="cae81-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cae81-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cae81-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cae81-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="cae81-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

