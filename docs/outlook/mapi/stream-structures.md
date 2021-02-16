---
title: Estructuras de flujo
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
# <a name="stream-structures"></a>Estructuras de flujo

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las definiciones de campos definidos por el usuario de un elemento de Microsoft Outlook se almacenan en la [propiedad PidLidPropertyDefinitionStream.](pidlidpropertydefinitionstream-canonical-property.md) El valor de esta propiedad es una secuencia binaria que contiene definiciones de campos definidos por el usuario y configuraciones de enlace de datos para los campos integrados para el elemento de Outlook. En esta sección se proporciona información acerca de la estructura de la secuencia binaria, desglosada en las siguientes estructuras de secuencia. 
  
> [!NOTE]
> Los nombres de estas estructuras de secuencia (por ejemplo, PropertyDefinition, FieldDefinition y SkipBlock) y sus elementos de datos no forman parte técnicamente de la interfaz de programación de la API de mensajería (MAPI) y se proporcionan aquí solo con fines de documentación de las estructuras de secuencias reales. Los desarrolladores pueden etiquetar estas estructuras de secuencias y elementos de datos en sus aplicaciones según lo elijan. 
  
- [Estructura de secuencia PropertyDefinition](propertydefinition-stream-structure.md)
    
- [Estructura de secuencia FieldDefinition](fielddefinition-stream-structure.md)
    
- [Estructura de flujo SkipBlock](skipblock-stream-structure.md)
    
- [Estructura de secuencia FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
    
- [Estructura de secuencias PackedAnsiString](packedansistring-stream-structure.md)
    
- [Estructura de secuencias PackedUnicodeString](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Consulte también



[Elementos y campos de Outlook](outlook-items-and-fields.md)
  
[Agregar una definición para un campo User-Defined nuevo](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Ejemplo de secuencia PropertyDefinition](propertydefinition-stream-sample.md)

