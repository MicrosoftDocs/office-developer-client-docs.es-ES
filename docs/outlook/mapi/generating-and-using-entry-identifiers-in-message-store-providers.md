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
  
Cuando se crea una nueva carpeta o mensaje en un almacén de mensajes, el proveedor de almacenamiento de mensajes tiene que asignar a ese objeto un identificador de entrada para que las aplicaciones cliente puedan hacer referencia a él. Los proveedores de almacenamiento de mensajes pueden volver a usar los identificadores de entrada a largo plazo de los objetos eliminados o crear nuevos identificadores. No hay ningún requisito de una forma u otra para los proveedores de al almacenamiento de mensajes; sin embargo, si es factible, un proveedor de almacén de mensajes siempre debe generar nuevos identificadores de entrada a largo plazo para objetos nuevos en lugar de volver a usar los antiguos. Es bueno volver a usar los identificadores de entrada a corto plazo cuando se eliminan los objetos a los que hacen referencia.
  
El motivo de esta eliminación es que los clientes pueden almacenar en caché los identificadores de entrada, a veces durante largos períodos de tiempo. Si esto sucede y el proveedor del almacén de mensajes reutiliza los identificadores de entrada, es posible que el identificador de entrada haga referencia a un objeto diferente cuando el cliente abre el identificador de entrada que cuando obtuvo el identificador de entrada por primera vez. Si el proveedor del almacén de mensajes no reutiliza los identificadores de entrada o, al menos, usa un esquema de generación de identificadores de entrada que no se repite durante mucho tiempo, este problema no se puede producir.
  
Del mismo modo, los proveedores de al almacenamiento de mensajes deben intentar conservar los identificadores de entrada de las carpetas y los mensajes cuando se mueven en el almacén de mensajes. Si el proveedor del almacén de mensajes puede hacerlo, las referencias a objetos del almacén no serán válidas cuando el objeto se mueve a una ubicación diferente del almacén.
  
## <a name="see-also"></a>Consulte también

- [Caracter�sticas de almac�n de mensajes](message-store-features.md)

