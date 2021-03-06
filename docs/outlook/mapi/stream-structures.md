---
title: Estructuras de secuencias
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407826"
---
# <a name="stream-structures"></a>Estructuras de secuencias

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las definiciones de campos definidos por el usuario de un elemento Outlook microsoft se almacenan en la [propiedad PidLidPropertyDefinitionStream.](pidlidpropertydefinitionstream-canonical-property.md) El valor de esta propiedad es una secuencia binaria que contiene definiciones de campos definidos por el usuario y opciones de enlace de datos para los campos integrados para el Outlook elemento. En esta sección se proporciona información sobre la estructura de la secuencia binaria, desglosada en las siguientes estructuras de secuencia. 
  
> [!NOTE]
> Los nombres de estas estructuras de secuencia (por ejemplo, PropertyDefinition, FieldDefinition y SkipBlock) y sus elementos de datos no forman parte técnicamente de la interfaz de programación de la API de mensajería (MAPI) y se proporcionan aquí solo con fines de documentación de las estructuras de secuencias reales. Los desarrolladores pueden etiquetar estas estructuras de secuencia y los elementos de datos en sus aplicaciones según lo elijan. 
  
- [Estructura de secuencia PropertyDefinition](propertydefinition-stream-structure.md)
    
- [Estructura de secuencia FieldDefinition](fielddefinition-stream-structure.md)
    
- [Estructura de secuencias SkipBlock](skipblock-stream-structure.md)
    
- [Estructura de secuencias FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
    
- [Estructura de secuencias PackedAnsiString](packedansistring-stream-structure.md)
    
- [Estructura de secuencias PackedUnicodeString](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Vea también



[Outlook Elementos y campos](outlook-items-and-fields.md)
  
[Agregar una definición para un nuevo User-Defined campo](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Ejemplo de secuencia PropertyDefinition](propertydefinition-stream-sample.md)

