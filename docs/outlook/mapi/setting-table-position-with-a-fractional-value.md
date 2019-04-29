---
title: Establecer la posición de la tabla con un valor fraccionario
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
# <a name="setting-table-position-with-a-fractional-value"></a>Establecer la posición de la tabla con un valor fraccionario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Table los usuarios pueden desplazarse a una posición que representa un porcentaje aproximado de filas en relación con el total. En lugar de desplazarse a una fila exacta, este método de colocación divide la tabla en partes basadas en fracciones. Tabla los usuarios pueden mover, por ejemplo, al punto de medio camino de una tabla o a la fila que se encuentra en el 7/8 del recorrido de la tabla. 
  
 **Para mover el cursor un número aproximado de filas**
  
- Llame al [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md). **SeekRowApprox** se desplaza a la fila que representa un porcentaje en particular de las filas en relación con el principio de la tabla. Este porcentaje se especifica en los parámetros _ulNumerator_ y _ulDenominator_ . **SeekRowApprox** se usa con frecuencia para implementar barras de desplazamiento. 
    
 **Para determinar la posición aproximada de una tabla**
  
- Llame al [IMAPITable:: QueryPosition](imapitable-queryposition.md). **QueryPosition** puede usarse para informar al usuario de la posición actual. Establece un valor fraccionario basado en el número de filas de la tabla y en el número de la fila actual. Se espera que este valor represente una aproximación. Se recomienda a los implementadores de tablas no calcular la posición exacta porque las implementaciones precisas pueden ser costosas de invocar, especialmente en tablas clasificadas. 
    
## <a name="see-also"></a>Ver también



[Tablas MAPI](mapi-tables.md)

