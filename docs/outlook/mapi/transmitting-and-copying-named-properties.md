---
title: Transmitir y copiar propiedades con nombre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6534e7344a62717e406c112249d26407b0852d93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437780"
---
# <a name="transmitting-and-copying-named-properties"></a>Transmitir y copiar propiedades con nombre

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando se envía, se mueve o se copia una propiedad con nombre, el nombre permanece constante pero el identificador debe cambiar para cumplir con la asignación del objeto de destino. La única excepción a esta regla es cuando el origen y el destino tienen la misma firma de asignación, lo que hace que la reasignación sea innecesaria.
  
Es responsabilidad del proveedor de transporte reasignar los nombres de las propiedades transmitidas con nombre a identificadores adecuados que funcionan en el destino. El proveedor de transporte de envío no puede saber cuál es la asignación correcta en el destino; debe transmitir los nombres y confiar en el proveedor de transporte receptor para asignarlos a identificadores que funcionen. La implementación MAPI de TNEF controla la reasignación de las propiedades con nombre para los proveedores de transporte. Los proveedores de transporte pueden controlar la reasignación manualmente o usar la implementación TNEF. 
  
La reasignación similar de las propiedades con nombre debe producirse cuando se copian estas propiedades entre almacenes de mensajes. Sin embargo, como los proveedores de almacenamiento de mensajes pueden recuperar el nombre de la asignación del identificador del destino, pueden reasignar las propiedades inmediatamente y no tienen que depender del almacén de mensajes de destino. 
  
## <a name="see-also"></a>Ver también



[Propiedades con nombre MAPI](mapi-named-properties.md)

