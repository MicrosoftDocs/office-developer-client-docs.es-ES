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
ms.openlocfilehash: 1c225712e354d72b79313ee4c3f36da55f11b0a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587519"
---
# <a name="transmitting-and-copying-named-properties"></a>Transmitir y copiar propiedades con nombre

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Siempre que se envía una propiedad con nombre, mover o copian, el nombre permanece constante, pero debe cambiar el identificador para adherirse a la asignación del objeto de destino. La única excepción a esta regla es cuando el origen y destino tienen la misma firma de asignación, realizar reasignación innecesarios.
  
Es responsabilidad del proveedor de transporte para volver a asignar los nombres de propiedades con nombre transmitidos a identificadores adecuados que funcionan en el destino. El proveedor de transporte envío no sabe cuál es la asignación correcta en el destino; se debe transmitir los nombres y se basan en el proveedor de transporte receptora para asignarlos a identificadores que funcionan. La implementación de MAPI de TNEF controla la reasignación de propiedades con nombre para los proveedores de transporte. Los proveedores de transporte pueden controlar la reasignación manualmente o usar la implementación de TNEF. 
  
Una reasignación similar de propiedades con nombre debe producirse cuando estas propiedades se copian entre almacenes de mensajes. Sin embargo, debido a que los proveedores de almacén de mensaje pueden recuperar el nombre de la asignación del identificador de destino, pueden volver a asignar las propiedades inmediatamente y no tiene que se basan en el almacén de mensajes de destino. 
  
## <a name="see-also"></a>Recursos adicionales



[Con el nombre de las propiedades de MAPI](mapi-named-properties.md)

