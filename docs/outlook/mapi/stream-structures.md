---
title: Estructuras de secuencia
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327443"
---
# <a name="stream-structures"></a>Estructuras de secuencia

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las definiciones de los campos definidos por el usuario de un elemento de Microsoft Outlook se almacenan en la propiedad [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) . El valor de esta propiedad es una secuencia binaria que contiene las definiciones de los campos definidos por el usuario y la configuración de enlace de datos para los campos integrados para el elemento de Outlook. En esta sección se proporciona información acerca de la estructura de la secuencia binaria, dividida en las siguientes estructuras de secuencias. 
  
> [!NOTE]
> Los nombres de estas estructuras de secuencia (por ejemplo, PropertyDefinition, FieldDefinition y SkipBlock) y sus elementos de datos no forman parte técnicamente de la interfaz de programación de la API de mensajería (MAPI) y se proporcionan aquí solo para la documentación. propósito de las estructuras de Stream reales. Los desarrolladores pueden etiquetar estas estructuras de secuencia y elementos de datos en sus aplicaciones según su elección. 
  
- [Estructura de la secuencia PropertyDefinition](propertydefinition-stream-structure.md)
    
- [Estructura de la secuencia FieldDefinition](fielddefinition-stream-structure.md)
    
- [Estructura de la secuencia SkipBlock](skipblock-stream-structure.md)
    
- [Estructura de la secuencia FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
    
- [Estructura de la secuencia PackedAnsiString](packedansistring-stream-structure.md)
    
- [Estructura de la secuencia PackedUnicodeString](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Vea también



[Campos y elementos de Outlook](outlook-items-and-fields.md)
  
[Agregar una definición para un nuevo campo definido por el usuario](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Ejemplo de secuencia PropertyDefinition](propertydefinition-stream-sample.md)

