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
ms.openlocfilehash: 41d1a4abe79892fa1c9c8789e159a19645318497
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820134"
---
# <a name="pidtagroamingdictionary-canonical-property"></a><span data-ttu-id="73e36-103">Propiedad canónica PidTagRoamingDictionary</span><span class="sxs-lookup"><span data-stu-id="73e36-103">PidTagRoamingDictionary Canonical Property</span></span>

<span data-ttu-id="73e36-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73e36-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73e36-105">Contiene un documento XML que describe el diccionario de movilidad.</span><span class="sxs-lookup"><span data-stu-id="73e36-105">Contains an XML document that describes the roaming dictionary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="73e36-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="73e36-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="73e36-107">PR_ROAMING_DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="73e36-107">PR_ROAMING_DICTIONARY</span></span>  <br/> |
|<span data-ttu-id="73e36-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="73e36-108">Identifier:</span></span>  <br/> |<span data-ttu-id="73e36-109">0x7C07</span><span class="sxs-lookup"><span data-stu-id="73e36-109">0x7C07</span></span>  <br/> |
|<span data-ttu-id="73e36-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="73e36-110">Data type:</span></span>  <br/> |<span data-ttu-id="73e36-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="73e36-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="73e36-112">Área:</span><span class="sxs-lookup"><span data-stu-id="73e36-112">Area:</span></span>  <br/> |<span data-ttu-id="73e36-113">Configuración</span><span class="sxs-lookup"><span data-stu-id="73e36-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73e36-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73e36-114">Remarks</span></span>

<span data-ttu-id="73e36-115">Esta propiedad contiene un documento XML UNICODE que está usando la codificación UTF8.</span><span class="sxs-lookup"><span data-stu-id="73e36-115">This property contains a UNICODE XML document that is using UTF8 encoding.</span></span> <span data-ttu-id="73e36-116">Un mensaje con una secuencia de diccionario debe establecer esta propiedad con el esquema siguiente:</span><span class="sxs-lookup"><span data-stu-id="73e36-116">A message with a dictionary stream must set this property with the following schema:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?> 
<xs:schema targetNamespace="Dictionary.xsd" xmlns="Dictionary.xsd" xmlns:xs="http://www.w3.org/2001/XMLSchema"> 
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

<span data-ttu-id="73e36-117">El siguiente es un documento XML de ejemplo almacenado en esta propiedad en un mensaje de datos de configuración:</span><span class="sxs-lookup"><span data-stu-id="73e36-117">The following is a sample XML document stored in this property on a Configuration Data message:</span></span> 
  
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

## <a name="related-resources"></a><span data-ttu-id="73e36-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="73e36-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="73e36-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="73e36-119">Protocol specifications</span></span>

<span data-ttu-id="73e36-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73e36-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73e36-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="73e36-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="73e36-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73e36-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73e36-123">Especifica la ubicación y las propiedades de datos de configuración de cliente y servidor, como las listas de categoría compartida y horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="73e36-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="73e36-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="73e36-124">Header files</span></span>

<span data-ttu-id="73e36-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73e36-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="73e36-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="73e36-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="73e36-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="73e36-127">Mapitags.h</span></span>
  
> <span data-ttu-id="73e36-128">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="73e36-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="73e36-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="73e36-129">See also</span></span>



[<span data-ttu-id="73e36-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="73e36-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="73e36-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="73e36-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="73e36-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="73e36-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="73e36-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="73e36-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
