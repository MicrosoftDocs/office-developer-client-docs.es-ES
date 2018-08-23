---
title: Agregue una definición para un nuevo campo definido por el usuario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a2f9d1623c3733292ebf5c65452ac0d65f577c4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592720"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Agregue una definición para un nuevo campo definido por el usuario
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando se agrega un campo definido por el usuario a un elemento de Microsoft Outlook, agregue una definición de campo en la estructura de secuencia [PropertyDefinition](propertydefinition-stream-structure.md) correspondiente. Use el procedimiento siguiente para agregar una nueva definición de campo a una estructura de secuencia PropertyDefinition. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>Para agregar una definición para un nuevo campo definido por el usuario

1. Copie las definiciones de campo existente de la estructura de la secuencia de PropertyDefinition en una matriz de definiciones de campo nuevo. 
    
2. Si las definiciones de campo existente que se encuentran en el formato PropDefV1, convertirlos al formato de PropDefV2. Para obtener más información acerca de los formatos de definición de campo, vea [PropertyDefinition secuencia estructura](propertydefinition-stream-structure.md) y la [Estructura de la secuencia de FieldDefinition](fielddefinition-stream-structure.md).
    
3. Crear una definición del nuevo campo definido por el usuario en el formato PropDefV2 y agregarlo a la matriz.
    
4. Establezca el elemento de versión de la estructura de la secuencia de PropertyDefinition como 0 x 0103, si el elemento Version no se ha establecido para ese valor.
    
5. Incrementar el elemento FieldDefinitionCount en 1.
    
6. Almacenar la matriz como el valor del elemento FieldDefinitions.
    
## <a name="see-also"></a>Recursos adicionales

- [Muestra de la secuencia PropertyDefinition](propertydefinition-stream-structure.md)

