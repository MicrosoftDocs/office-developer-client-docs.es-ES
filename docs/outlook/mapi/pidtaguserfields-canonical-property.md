---
title: Propiedad canónica PidTagUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397432"
---
# <a name="pidtaguserfields-canonical-property"></a>Propiedad canónica PidTagUserFields

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre, tipo de datos y otra información acerca de un campo definido por el usuario.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_USERFIELDS  <br/> |
|Identificador:  <br/> |0x36E3  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Carpeta MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Para cada elemento, Outlook almacena las definiciones de todos los campos definidos por el usuario en la propiedad [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) del objeto **IMessage** correspondiente. La propiedad **PidLidPropertyDefinitionStream** contiene una secuencia binaria conocida como [PropertyDefinition](propertydefinition-stream-structure.md), que contiene las definiciones de campo. Para obtener más información acerca de las estructuras de secuencia para las definiciones de campo, vea [Estructuras de secuencia](stream-structures.md).
  
Para cada carpeta, Outlook almacena las definiciones de todos los campos definidos por el usuario en esa carpeta en la propiedad **PidTagUserFields** de un mensaje asociado de la clase de mensaje IPC.MS. REN. USERFIELDS - supone que cada carpeta para contener no más de un mensaje de esta clase en su tabla de contenido asociada. 
  
> [!NOTE]
> El conjunto de campos definidos por el usuario en una carpeta no es posible que necesariamente deben coincidir con los conjuntos de campos definidos por el usuario en cada uno de sus elementos. 
  
El conjunto de campos definidos por el usuario en una carpeta se muestra en diversos lugares de la interfaz de usuario de Outlook, como el selector de campos de la carpeta. La propiedad del mensaje **PidTagUserFields** contiene una secuencia binaria, **FolderUserFields**, que contiene las definiciones de campo de la carpeta. Para obtener más información acerca de las estructuras de secuencia para las definiciones de campo de carpeta, vea [Estructuras de secuencia de los campos de carpeta](folder-fields-stream-structures.md) y el [Ejemplo de secuencia de FolderUserFields](folderuserfields-stream-sample.md).
  
## <a name="section-heading"></a>Encabezado de sección

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
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

