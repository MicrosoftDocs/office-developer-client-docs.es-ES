---
title: Desarrollar un proveedor de almacén de mensajes MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83692674-0b5a-468d-9cd7-a2ac3d140bda
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 040c851d64f60c319250fd0e08620285b6f2f0db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816676"
---
# <a name="developing-a-mapi-message-store-provider"></a>Desarrollar un proveedor de almacén de mensajes MAPI
  
**Hace referencia a**: Outlook 
  
Al igual que otros proveedores de servicios MAPI, los almacenes de mensajes son bibliotecas de vínculos dinámicos (DLL) que presentan los servicios de un mecanismo de almacenamiento subyacente para las aplicaciones cliente MAPI y la cola de MAPI. El proveedor de almacenamiento de mensaje presenta el mecanismo de almacenamiento subyacente como un conjunto jerárquico de carpetas y los mensajes que pueden usar los clientes MAPI y la cola de MAPI.
  
En la siguiente ilustración muestra la arquitectura básica de almacén de mensajes MAPI.
  
**Arquitectura del almacén de mensajes**
  
![Arquitectura del almacén de mensajes] (media/storearc.gif "Arquitectura del almacén de mensajes")
  
Puede implementar un proveedor de almacén de mensajes mediante el uso de cualquier tipo de le apetece un mecanismo de almacenamiento subyacente. Sin embargo, debe tener en cuenta cuestiones de rendimiento. Además, el mecanismo de almacenamiento subyacente debe presentarse como una colección jerárquica de objetos MAPI. Estos requerimientos significan que los almacenes de mensajes normalmente se implementan mediante el uso de un producto de base de datos existente que admite el almacenamiento jerárquico de objetos en la base de datos y que tiene una interfaz de programación o la estructura de archivos bien definido. Por ejemplo, las bases de datos de Microsoft Office Access, SQL y Oracle pueden usarse como el mecanismo de almacenamiento subyacente. Algunos productos de la base de datos tienen conjuntos de características que hacen que sea más fácil implementar características MAPI, por lo que su elección de producto de la base de datos puede verse afectada por las características que debe admitir su proveedor de almacén de mensajes.
  
Uso de una base de datos existente como el guarda de mecanismo de almacenamiento subyacente que funcionan porque es suele ser más fácil a los objetos de base de datos está presente a los clientes MAPI como objetos MAPI que implementar su propio mecanismo de almacenamiento de información jerárquico. Esto permite tratar las operaciones de MAPI en un nivel superior si implementar su propio mecanismo de almacenamiento de información jerárquico. Por ejemplo, busca un mensaje con una línea de asunto concreto se convierte en una cuestión bastante sencilla de construcción y envío de una consulta de base de datos adecuada, en lugar de implementar complejas rutinas para buscar el mecanismo de almacenamiento de información jerárquico.
  
Los proveedores de almacén de mensajes comunican con los clientes MAPI y la cola de MAPI para realizar operaciones en carpetas y los objetos. El proveedor de almacén de mensajes traduce estas operaciones en las operaciones de nivel inferiores en el mecanismo de almacenamiento subyacente. La cola MAPI normalmente se comunica con el proveedor de almacén de mensajes al enviar y recibir mensajes. Normalmente, los clientes MAPI se comunican con los proveedores de almacén de mensajes para manipular la jerarquía de carpetas y para leer, editar, eliminar y enviar mensajes.
  
Tanto la cola MAPI y los clientes MAPI comunican con el proveedor de almacenamiento de mensaje para crear mensajes nuevos. Las aplicaciones cliente de hacerlo cuando los usuarios redacción un mensaje. La cola MAPI hace cuando recibe un mensaje entrante. En cualquier caso, normalmente se crea el nuevo mensaje en la carpeta Bandeja de entrada del almacén de mensajes, si hay alguno.
  
Los proveedores de almacén de mensajes realizar un uso intensivo de tablas, las carpetas, los mensajes y las propiedades MAPI. Los detalles de implementación para aquellos objetos que se documentan en [Tablas de MAPI](mapi-tables.md), [Las carpetas de MAPI](mapi-folders.md), [Los mensajes de MAPI](mapi-messages.md)e [Información general sobre la propiedad de MAPI](mapi-property-overview.md). Debe familiarizarse con la que el material antes de intentar implementar un proveedor de almacén de mensajes.
  
Hay dos tipos importantes de los proveedores de almacén de mensajes: aquellos que pueden actuar como valor predeterminado de un usuario de mensajes almacén y aquellos que no se puede. Un almacén de mensajes predeterminado es uno en cliente que las aplicaciones y la cola MAPI pueden realizar cualquier tarea de mensajería, como recibir mensajes o la creación de carpetas. Un proveedor de almacén de mensajes predeterminado debe admitir varias características que el número mínimo necesario para todos los proveedores de almacén de mensajes.
  
## <a name="see-also"></a>Vea también

- [Conceptos MAPI](mapi-concepts.md)

