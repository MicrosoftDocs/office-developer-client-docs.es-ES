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
ms.openlocfilehash: f7f764d95c2fc36ba6af617333cb47d266cd2aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818846"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a>Propiedad canónica PidLidPropertyDefinitionStream

  
  
**Hace referencia a**: Outlook 
  
Representa las definiciones de campos definidos por el usuario y la configuración de enlace de datos de los campos integrados de un mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidPropDefStream  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008540  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Configuración de tiempo de ejecución  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de la propiedad **PidLidPropertyDefinitionStream** se guarda como parte de la definición de formulario personalizado para el mensaje. 
  
El valor de esta propiedad es una secuencia binaria. Para obtener información sobre la estructura de esta secuencia, vea [Estructura de secuencia de PropertyDefinition](propertydefinition-stream-structure.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Campos y elementos de Outlook](outlook-items-and-fields.md)
  
[Agregar una definición para un nuevo campo definido por el usuario](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Ejemplo de flujo PropertyDefinition](propertydefinition-stream-sample.md)
  
[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

