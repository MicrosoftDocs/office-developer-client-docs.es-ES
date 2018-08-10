---
title: Estructuras de secuencia
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6ec44fe0dbf8e63b7bbc58da1ba6e20f8ff59d3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820775"
---
# <a name="stream-structures"></a>Estructuras de secuencia

  
  
**Hace referencia a**: Outlook 
  
Definiciones de campos definidos por el usuario de un elemento de Microsoft Outlook se almacenan en la propiedad [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) . El valor de esta propiedad es una secuencia binaria que contiene las definiciones de campos definidos por el usuario y la configuración de enlace de datos para los campos integrados para el elemento de Outlook. En esta sección se proporciona información acerca de la estructura de la secuencia binaria, desglosada en las siguientes estructuras de secuencia. 
  
> [!NOTE]
> Los nombres de estas estructuras de secuencia (por ejemplo, PropertyDefinition, FieldDefinition y SkipBlock) y sus elementos de datos no son técnicamente forman parte de la interfaz de programación de la API de mensajería (MAPI) y se proporcionan aquí sólo para la documentación con fines de las estructuras de la secuencia real. Los desarrolladores pueden etiquetar estos elementos de las estructuras y datos de secuencia en sus aplicaciones cuando lo prefieran. 
  
- [Muestra de la secuencia PropertyDefinition](propertydefinition-stream-structure.md)
    
- [Muestra de la secuencia FieldDefinition](fielddefinition-stream-structure.md)
    
- [Estructura de la secuencia SkipBlock](skipblock-stream-structure.md)
    
- [Estructura de la secuencia FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
    
- [Estructura de la secuencia PackedAnsiString](packedansistring-stream-structure.md)
    
- [Estructura de la secuencia PackedUnicodeString](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Vea también



[Campos y elementos de Outlook](outlook-items-and-fields.md)
  
[Agregar una definición para un nuevo campo definido por el usuario](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Ejemplo de flujo PropertyDefinition](propertydefinition-stream-sample.md)

