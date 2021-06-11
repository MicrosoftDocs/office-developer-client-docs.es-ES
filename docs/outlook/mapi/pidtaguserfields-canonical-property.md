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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360743"
---
# <a name="pidtaguserfields-canonical-property"></a>Propiedad canónica PidTagUserFields

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre, el tipo de datos y otra información sobre un campo definido por el usuario.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_USERFIELDS  <br/> |
|Identificador:  <br/> |0x36E3  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Carpeta MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Para cada elemento, Outlook las definiciones de todos los campos definidos por el usuario en la propiedad [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) del objeto **IMessage** correspondiente. La **propiedad PidLidPropertyDefinitionStream** contiene una secuencia binaria conocida como [PropertyDefinition](propertydefinition-stream-structure.md), que contiene las definiciones de campo. Para obtener más información acerca de las estructuras de secuencia para definiciones de campo, vea [Stream Structures](stream-structures.md).
  
Para cada carpeta, Outlook almacena las definiciones de todos los campos definidos por el usuario en esa carpeta en la propiedad **PidTagUserFields** de un mensaje asociado de la clase de mensaje IPC.MS. REN. USERFIELDS: cada carpeta que se supone no contiene más de un mensaje de esta clase en su tabla de contenido asociada. 
  
> [!NOTE]
> Es posible que el conjunto de campos definidos por el usuario de una carpeta no coincida necesariamente con los conjuntos de campos definidos por el usuario en cada uno de sus elementos. 
  
El conjunto de campos definidos por el usuario en una carpeta se muestra en varios lugares de la interfaz de usuario de Outlook, como el Seleccionador de campos de la carpeta. La propiedad **PidTagUserFields** del mensaje contiene una secuencia binaria, **FolderUserFields**, que contiene las definiciones de campo de carpeta. Para obtener más información acerca de las estructuras de secuencia para definiciones de campo de carpeta, vea [Folder Fields Stream Structures](folder-fields-stream-structures.md) y [folderUserFields Stream Sample](folderuserfields-stream-sample.md).
  
## <a name="section-heading"></a>Título de sección

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Outlook Elementos y campos](outlook-items-and-fields.md)
  
[Agregar una definición para un nuevo User-Defined campo](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Ejemplo de secuencia PropertyDefinition](propertydefinition-stream-sample.md)
  
[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

