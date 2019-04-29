---
title: Estructura de la secuencia PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 479339762867aa778bc8bc8baa1f21f6bc34b441
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438592"
---
# <a name="propertydefinition-stream-structure"></a>Estructura de la secuencia PropertyDefinition

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una estructura de secuencia PropertyDefinition es una matriz de estructuras de secuencia [FieldDefinition](fielddefinition-stream-structure.md) que contiene definiciones para todos los campos definidos por el usuario en un elemento de Microsoft Outlook y la configuración de enlace de datos para algunos campos integrados. 
  
Puede manipular mediante programación la estructura de la secuencia PropertyDefinition. Sin embargo, puede obtener resultados similares mediante el diseñador de formularios de Outlook y, en concreto, el cuadro de diálogo **propiedades** de un control enlazado a datos. 
  
Las definiciones de campo en una estructura de secuencia PropertyDefinition puede tener uno de estos dos formatos: PropDefV1 y PropDefV2. Outlook admite tanto PropDefV1 como PropDefV2. Todas las definiciones de campo en una única estructura de secuencia PropertyDefinition deben tener el mismo formato. Para obtener más información sobre cómo difieren PropDefV1 y PropDefV2, consulte [FieldDefinition estructura](fielddefinition-stream-structure.md)de la secuencia.
  
Los elementos de datos de esta secuencia se almacenan en el orden de bytes Little-endian, inmediatamente a continuación entre sí en el orden especificado a continuación.
  
- Versión: WORD (2 bytes), el formato de las definiciones de campo de la estructura de secuencia PropertyDefinition. En la siguiente tabla se muestran los valores posibles.
    
    |**Valor**|**Descripción**|
    |:-----|:-----|
    |0x0102  <br/> |El formato es PropDefV1.  <br/> |
    |0x0103  <br/> |El formato es PropDefV2.  <br/> |
   
- FieldDefinitionCount: DWORD (4 bytes), el número de definiciones de campo en esta secuencia. Se trata del número de elementos de matriz en el elemento de datos FieldDefinitions.
    
- FieldDefinitions: una matriz de estructuras de secuencia FieldDefinition. El recuento de esta matriz es igual al elemento de datos FieldDefinitionCount.
    
## <a name="see-also"></a>Ver también

- [Campos y elementos de Outlook](outlook-items-and-fields.md)
- [Agregar una definición para un nuevo campo definido por el usuario](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [Ejemplo de secuencia PropertyDefinition](propertydefinition-stream-sample.md)
- [Estructuras de secuencia](stream-structures.md)

