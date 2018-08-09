---
title: Establecer una posición de tabla con un valor decimal
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 104de38a41408091a6fbb69995de4f41f6fea6a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820648"
---
# <a name="setting-table-position-with-a-fractional-value"></a>Establecer una posición de tabla con un valor decimal

  
  
**Hace referencia a**: Outlook 
  
Los usuarios de la tabla pueden mover a una posición que representa un porcentaje aproximado de filas en relación con el total. En lugar de mover a una fila exacto, este método de colocación divide la tabla en partes según las fracciones. Pueden mover los usuarios de la tabla, por ejemplo, en punto de intermedio de una tabla o en la fila que es 7 y 8 de la forma a través de la tabla. 
  
 **Para mover el cursor un número aproximado de filas**
  
- Llamar a [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md). **SeekRowApprox** se mueve a la fila que representa un porcentaje determinado de filas en relación con el principio de la tabla. Este porcentaje se especifica en los parámetros _ulNumerator_ y _ulDenominator_ . **SeekRowApprox** se usa con frecuencia para implementar las barras de desplazamiento. 
    
 **Para determinar la posición aproximada de una tabla**
  
- Llame a [IMAPITable::QueryPosition](imapitable-queryposition.md). **QueryPosition** puede utilizarse para informar al usuario de la posición actual. Establece un valor fraccionario según el número de filas en la tabla y el número de la fila actual. Esperar que este valor representa una aproximación. Se recomienda no para calcular la posición exacta debido a que las implementaciones precisas pueden ser costosas invocar, especialmente en las tablas ordenadas por categorías los implementadores de tabla. 
    
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

