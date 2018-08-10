---
title: Estructura de la secuencia de PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 289227ee171c2325cad0ed321dab4f635a0ca724
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820467"
---
# <a name="propertydefinition-stream-structure"></a>Estructura de la secuencia de PropertyDefinition

**Hace referencia a**: Outlook 
  
Una estructura de secuencia PropertyDefinition es una matriz de estructuras de secuencia [FieldDefinition](fielddefinition-stream-structure.md) que contienen definiciones para todos los campos definidos por el usuario en un elemento de Microsoft Outlook y la configuración de enlace de datos para algunos campos integrados. 
  
Se puede manipular mediante programación la estructura de la secuencia de PropertyDefinition. Sin embargo, puede lograr resultados similares mediante el Diseñador de formularios de Outlook y, en particular, el cuadro de diálogo **Propiedades de** cuadro para un control enlazado a datos. 
  
Las definiciones de campo en una estructura de secuencia PropertyDefinition pueden ser uno de los dos formatos: PropDefV1 y PropDefV2. Outlook admite PropDefV1 y PropDefV2. Todas las definiciones de campo en una estructura de secuencia PropertyDefinition único deben ser del mismo formato. Para obtener más información acerca de cómo PropDefV1 y PropDefV2 difieren, vea [FieldDefinition secuencia de estructura](fielddefinition-stream-structure.md).
  
Elementos de datos en esta secuencia se almacenan en orden de bytes little-endian, inmediatamente después de entre sí en el orden especificado a continuación.
  
- Versión: WORD (2 bytes), el formato de las definiciones de campo en el PropertyDefinition en secuencia de estructura. En la siguiente tabla se muestra los valores posibles.
    
    |**Valor**|**Descripción**|
    |:-----|:-----|
    |0x0102  <br/> |Formato es PropDefV1.  <br/> |
    |0x0103  <br/> |Formato es PropDefV2.  <br/> |
   
- FieldDefinitionCount: DWORD (4 bytes), el número de definiciones de campo en esta secuencia. Éste es el recuento de elementos de matriz en el elemento de datos de FieldDefinitions.
    
- FieldDefinitions: Una matriz de estructuras de secuencia FieldDefinition. El recuento de esta matriz es igual al elemento de datos de FieldDefinitionCount.
    
## <a name="see-also"></a>Vea también

- [Campos y elementos de Outlook](outlook-items-and-fields.md)
- [Agregar una definición para un nuevo campo definido por el usuario](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [Ejemplo de flujo PropertyDefinition](propertydefinition-stream-sample.md)
- [Estructuras de secuencia](stream-structures.md)

