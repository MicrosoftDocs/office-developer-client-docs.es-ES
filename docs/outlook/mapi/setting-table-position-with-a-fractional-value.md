---
title: Establecer la posición de la tabla con un valor fraccional
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7800a58cad7b4e2b0b1696706c8e1d401ed424d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437339"
---
# <a name="setting-table-position-with-a-fractional-value"></a>Establecer la posición de la tabla con un valor fraccional

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los usuarios de la tabla pueden moverse a una posición que representa un porcentaje aproximado de filas en relación con el total. En lugar de pasar a una fila exacta, este método de posicionamiento divide la tabla en partes basadas en fracciones. Los usuarios de la tabla pueden moverse, por ejemplo, al punto medio de una tabla o a la fila 7/8 del camino a través de la tabla. 
  
 **Para mover el cursor un número aproximado de filas**
  
- Llame [a IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md). **SeekRowApprox** se mueve a la fila que representa un porcentaje determinado de filas en relación con el principio de la tabla. Este porcentaje se especifica en los parámetros _ulNumerator_ y _ulDenominator._ **SeekRowApprox** se usa con frecuencia para implementar barras de desplazamiento. 
    
 **Para determinar la posición aproximada de una tabla**
  
- Llame [a IMAPITable::QueryPosition](imapitable-queryposition.md). **QueryPosition** puede usarse para informar al usuario de la posición actual. Establece un valor fraccionrio en función del número de filas de la tabla y del número de la fila actual. Se espera que este valor represente una aproximación. Se recomienda que los implementadores de tablas no calculen la posición exacta porque las implementaciones precisas pueden resultar costosas de invocar, especialmente en tablas categorizadas. 
    
## <a name="see-also"></a>Consulte también



[Tablas MAPI](mapi-tables.md)

