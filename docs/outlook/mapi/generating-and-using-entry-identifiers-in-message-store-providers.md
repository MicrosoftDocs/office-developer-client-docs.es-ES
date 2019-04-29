---
title: Generar y usar identificadores de entrada en proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 005742eaaba81600be249d52e5d8098e9f286f17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437682"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a>Generar y usar identificadores de entrada en proveedores de almacenamiento de mensajes

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando se crea una nueva carpeta o mensaje en un almacén de mensajes, el proveedor de almacén de mensajes tiene que asignar a ese objeto un identificador de entrada para que las aplicaciones cliente puedan hacer referencia a él. Los proveedores de almacenamiento de mensajes pueden reutilizar los identificadores de entrada a largo plazo de los objetos eliminados o crear identificadores nuevos. No hay ningún requisito para los proveedores de almacenamiento de mensajes de una forma o de otra; sin embargo, si es viable, un proveedor de almacenamiento de mensajes siempre debe generar nuevos identificadores de entrada a largo plazo para los nuevos objetos, en lugar de volver a usar los antiguos. Es preciso volver a usar los identificadores de entrada a corto plazo cuando se eliminan los objetos a los que hacen referencia.
  
El motivo de esta eliminación es que los clientes pueden almacenar en la memoria caché los identificadores de entrada, a veces durante largos períodos de tiempo. Si esto sucede y el proveedor de almacén de mensajes sí que reutiliza los identificadores de entrada, es posible que el identificador de entrada haga referencia a un objeto diferente cuando el cliente Abra el identificador de entrada que cuando obtuvo el identificador de entrada por primera vez. Si el proveedor de almacenamiento de mensajes no reutiliza los identificadores de entrada, o si al menos usa una combinación de generación de identificadores de entrada que no se repite durante mucho tiempo, no se puede producir este problema.
  
De forma similar, los proveedores de almacenamiento de mensajes deberían intentar conservar los identificadores de entrada para carpetas y mensajes cuando se mueven en el almacén de mensajes. Si el proveedor de almacén de mensajes puede hacerlo, las referencias a objetos en el almacén no dejarán de ser válidas cuando el objeto se mueva a otra ubicación del almacén.
  
## <a name="see-also"></a>Ver también

- [Caracter�sticas de almac�n de mensajes](message-store-features.md)

