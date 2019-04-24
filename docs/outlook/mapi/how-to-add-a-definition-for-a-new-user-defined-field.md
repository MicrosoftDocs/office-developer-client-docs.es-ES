---
title: Agregar una definición para un nuevo campo definido por el usuario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299072"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Agregar una definición para un nuevo campo definido por el usuario
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando se agrega un campo definido por el usuario a un elemento de Microsoft Outlook, se agrega una definición de campo a la estructura de secuencia [PropertyDefinition](propertydefinition-stream-structure.md) correspondiente. Use el siguiente procedimiento para agregar una nueva definición de campo a una estructura de secuencia PropertyDefinition. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>Para agregar una definición para un nuevo campo definido por el usuario

1. Copie las definiciones de campo existentes de la estructura de secuencia PropertyDefinition a una nueva matriz de definiciones de campo. 
    
2. Si alguna de las definiciones de campo existentes tiene el formato PropDefV1, conviértalos al formato PropDefV2. Para obtener más información acerca de los formatos de definición de campo, vea [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) y [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).
    
3. Cree una definición del nuevo campo definido por el usuario en el formato PropDefV2 y agréguelo a la matriz.
    
4. Establezca el elemento version de la estructura de secuencia PropertyDefinition como 0x0103, si no se ha establecido el elemento version en ese valor.
    
5. Incremente el elemento FieldDefinitionCount en 1.
    
6. Almacene la matriz como el valor del elemento FieldDefinitions.
    
## <a name="see-also"></a>Vea también

- [Estructura de la secuencia PropertyDefinition](propertydefinition-stream-structure.md)

