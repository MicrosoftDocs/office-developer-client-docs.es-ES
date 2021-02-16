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
# <a name="pidlidpropertydefinitionstream-canonical-property"></a>Propiedad canónica PidLidPropertyDefinitionStream

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Representa las definiciones de campos definidos por el usuario y la configuración de enlace de datos de los campos integrados de un mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidPropDefStream  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008540  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Configuración en tiempo de ejecución  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de la **propiedad PidLidPropertyDefinitionStream** se guarda como parte de la definición de formulario personalizada para el mensaje. 
  
El valor de esta propiedad es una secuencia binaria. Para obtener información sobre la estructura de esta secuencia, vea [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Elementos y campos de Outlook](outlook-items-and-fields.md)
  
[Agregar una definición para un nuevo User-Defined campo](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Ejemplo de secuencia PropertyDefinition](propertydefinition-stream-sample.md)
  
[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

