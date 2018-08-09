---
title: Generación y uso de identificadores de entrada en el mensaje de los proveedores de almacén
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3bfda4a1dbe464c744917c2e9b3ca66eaf88fd20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816923"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a>Generación y uso de identificadores de entrada en el mensaje de los proveedores de almacén

**Hace referencia a**: Outlook 
  
Cuando se crea una nueva carpeta o mensaje en un almacén de mensajes, el proveedor de almacén de mensajes tiene que asignar un identificador de entrada de ese objeto para que las aplicaciones cliente pueden hacer referencia a él. Los proveedores de almacén de mensajes pueden volver a usar los identificadores de entrada a largo plazo inactivo de objetos eliminados o crear nuevos identificadores. No hay ningún requisito de una forma o el otro para los proveedores de almacén de mensajes; Sin embargo, si es factible, un proveedor de almacén de mensajes siempre debe generar nuevos identificadores de entrada a largo plazo para los nuevos objetos en lugar de reutilización de las antiguas. Es preciso volver a usar los identificadores de entrada a corto plazo cuando se eliminan los objetos que hacen referencia a.
  
La razón de esta eliminación es que los clientes pueden almacenar en caché los identificadores de entrada, en ocasiones, durante largos períodos de tiempo. Si esto sucede y el proveedor de almacenamiento de mensaje volver a usar los identificadores de entrada, es posible que el identificador de entrada hacer referencia a un objeto diferente cuando el cliente abre el identificador de entrada de cuándo obtuvo el identificador de entrada. Si el proveedor de almacén de mensajes no volver a usar los identificadores de entrada, o al menos utiliza un esquema de generación de identificador de entrada que no se repiten durante un tiempo prolongado muy: no se puede producir este problema.
  
De forma similar, los proveedores de almacén de mensajes deben intentar conservar los identificadores de entrada para las carpetas y los mensajes cuando se mueven en el almacén de mensajes. Si el proveedor de almacenamiento de mensajes puede hacer, las referencias a objetos en el almacén no será válidas cuando el objeto se mueve a una ubicación diferente en el almacén.
  
## <a name="see-also"></a>Vea también

- [Caracter�sticas de almac�n de mensajes](message-store-features.md)

