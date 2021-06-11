---
title: Transmisión y copia de propiedades con nombre
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
# <a name="transmitting-and-copying-named-properties"></a>Transmisión y copia de propiedades con nombre

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Siempre que se envía, mueve o copia una propiedad con nombre, el nombre permanece constante, pero el identificador debe cambiar para cumplir con la asignación del objeto de destino. La única excepción a esta regla es cuando el origen y el destino tienen la misma firma de asignación, lo que hace innecesaria la nueva asignación.
  
Es responsabilidad del proveedor de transporte volver a asignar los nombres de las propiedades con nombre transmitidas a los identificadores adecuados que funcionan en el destino. El proveedor de transporte de envío no puede saber cuál es la asignación correcta en el destino; debe transmitir los nombres y confiar en el proveedor de transporte de recepción para asignarlos a los identificadores que funcionan. La implementación MAPI de TNEF controla la remapping de propiedades con nombre para proveedores de transporte. Los proveedores de transporte pueden controlar la remapping manualmente o usar la implementación de TNEF. 
  
Cuando estas propiedades se copian entre almacenes de mensajes, debe producirse una nueva remapping similar de propiedades con nombre. Sin embargo, como los proveedores de almacén de mensajes pueden recuperar el nombre a la asignación de identificadores del destino, pueden volver a asignar las propiedades de inmediato y no tienen que depender del almacén de mensajes de destino. 
  
## <a name="see-also"></a>Vea también



[Propiedades con nombre MAPI](mapi-named-properties.md)

