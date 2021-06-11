---
title: Outlook Elementos y campos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b40752d4a5f445368752ad4caf5c919f6e0ce27b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409121"
---
# <a name="outlook-items-and-fields"></a>Outlook Elementos y campos

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook proporciona tipos de elementos especializados para su funcionalidad (por ejemplo, elementos de correo, citas, contactos, tareas y notas). Outlook proporciona campos estándar para cada tipo de elemento, comúnmente denominados campos integrados. Outlook también permite a los usuarios crear campos personalizados, comúnmente denominados campos definidos por el usuario. Cada campo está asociado con un tipo de datos y un valor. Ejemplos de tipos de datos **son Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords** y **Text**. Los usuarios pueden definir campos personalizados mediante el Diseñador de formularios en Outlook.
  
En el nivel de programación, cada elemento está representado por un [objeto IMessage.](imessageimapiprop.md) Cada campo definido por el usuario está asociado con una definición de campo y un valor. 
  
### <a name="field-definition"></a>Definición de campo

Una definición de campo incluye el nombre, el tipo de datos y otra información sobre el campo. Para cada elemento, Outlook las definiciones de todos los campos definidos por el usuario en la propiedad [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) del objeto **IMessage** correspondiente. La **propiedad PidLidPropertyDefinitionStream** contiene una secuencia binaria conocida como [PropertyDefinition](propertydefinition-stream-structure.md) que contiene las definiciones de campo. Para obtener más información acerca de las estructuras de secuencia para definiciones de campo, vea [Stream Structures](stream-structures.md).
  
### <a name="field-value"></a>Valor de campo

Cada campo definido por el usuario de un elemento tiene un valor almacenado en una propiedad con nombre correspondiente. Esa propiedad con nombre está en el PS_PUBLIC_STRINGS de propiedades y tiene una cadena de caracteres Unicode como el nombre de la propiedad. El tipo de datos de la propiedad corresponde al tipo del campo. Si la propiedad no está presente en el objeto **IMessage,** Outlook supone un valor predeterminado razonable para la propiedad. Por ejemplo, para un tipo de cadena, Outlook supone una cadena vacía si la propiedad no está presente. 
  
## <a name="see-also"></a>Vea también



[Agregar una definición para un nuevo User-Defined campo](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Ejemplo de secuencia PropertyDefinition](propertydefinition-stream-sample.md)
  
[Estructuras de secuencias](stream-structures.md)
  
[Estructura de secuencia PropertyDefinition](propertydefinition-stream-structure.md)
  
[Estructura de secuencia FieldDefinition](fielddefinition-stream-structure.md)
  
[Estructura de secuencias SkipBlock](skipblock-stream-structure.md)
  
[Estructura de secuencias FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
  
[Estructura de secuencias PackedAnsiString](packedansistring-stream-structure.md)
  
[Estructura de secuencias PackedUnicodeString](packedunicodestring-stream-structure.md)

