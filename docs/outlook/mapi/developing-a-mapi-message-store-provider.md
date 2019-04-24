---
title: Desarrollar un proveedor de almacén de mensajes de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83692674-0b5a-468d-9cd7-a2ac3d140bda
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 76332b57b2957b5682efb415121ea6db42409c30
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316766"
---
# <a name="developing-a-mapi-message-store-provider"></a>Desarrollar un proveedor de almacén de mensajes de MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Al igual que otros proveedores de servicios MAPI, los almacenes de mensajes son bibliotecas de vínculos dinámicos (dll) que presentan los servicios de un mecanismo de almacenamiento subyacente a las aplicaciones cliente de MAPI y a la cola MAPI. El proveedor de almacén de mensajes presenta el mecanismo de almacenamiento subyacente como un conjunto jerárquico de carpetas y mensajes que los clientes MAPI y la cola MAPI pueden usar.
  
La siguiente ilustración muestra la arquitectura básica del almacén de mensajes de MAPI.
  
**Arquitectura del almacén de mensajes**
  
![Arquitectura del almacén de mensajes] (media/storearc.gif "Arquitectura del almacén de mensajes")
  
Puede implementar un proveedor de almacenamiento de mensajes con cualquier tipo de mecanismo de almacenamiento subyacente que desee. Sin embargo, debe tener en cuenta las preocupaciones de rendimiento. Además, el mecanismo de almacenamiento subyacente debe presentarse como una colección jerárquica de objetos MAPI. Estos requisitos significan que los almacenes de mensajes se implementan normalmente mediante un producto de base de datos existente que admite el almacenamiento jerárquico de objetos en la base de datos y que tiene una interfaz de programación o una estructura de archivos bien definida. Por ejemplo, las bases de datos de Microsoft Office Access, SQL y Oracle pueden usarse como mecanismo de almacenamiento subyacente. Algunos productos de base de datos tienen conjuntos de características que facilitan la implementación de características MAPI, de modo que la elección del producto de base de datos puede verse afectada por las características que su proveedor de almacenamiento de mensajes necesita admitir.
  
El uso de una base de datos existente como mecanismo de almacenamiento subyacente le ahorra trabajo, ya que suele ser más fácil presentar objetos de base de datos a clientes MAPI como objetos MAPI que implementar su propio mecanismo de almacenamiento jerárquico. Esto le permite tratar las operaciones MAPI en un nivel superior que si implementa su propio mecanismo de almacenamiento jerárquico. Por ejemplo, la búsqueda de un mensaje con una línea de asunto en particular se convierte en un asunto bastante sencillo de construir y enviar una consulta de base de datos adecuada, en lugar de implementar rutinas complejas para buscar en el mecanismo de almacenamiento jerárquico.
  
Los proveedores de almacenamiento de mensajes se comunican con los clientes MAPI y la cola MAPI para realizar operaciones en carpetas y objetos. El proveedor de almacén de mensajes convierte esas operaciones en operaciones de nivel inferior en el mecanismo de almacenamiento subyacente. La cola MAPI suele comunicarse con el proveedor de almacenamiento de mensajes al enviar y recibir mensajes. Los clientes MAPI suelen comunicarse con los proveedores de almacenamiento de mensajes para manipular la jerarquía de carpetas y para leer, editar, eliminar y enviar mensajes.
  
El administrador de trabajos en cola MAPI y los clientes MAPI se comunican con el proveedor de almacenamiento de mensajes para crear nuevos mensajes. Las aplicaciones cliente realizan esta tarea cuando los usuarios redactan un mensaje. La cola MAPI hace esto cuando recibe un mensaje entrante. En cualquier caso, el nuevo mensaje se crea normalmente en la carpeta Bandeja de entrada del almacén de mensajes, si hay alguno.
  
Los proveedores de almacenamiento de mensajes usan las tablas, carpetas, mensajes y propiedades MAPI de forma intensiva. Los detalles de implementación de esos objetos se documentan en [las tablas MAPI](mapi-tables.md), [las carpetas MAPI](mapi-folders.md), [los mensajes MAPI](mapi-messages.md)y la [información general de las propiedades MAPI](mapi-property-overview.md). Debe familiarizarse con el material antes de intentar implementar un proveedor de almacenamiento de mensajes.
  
Hay dos tipos importantes de proveedores de almacenamiento de mensajes: los que pueden actuar como almacén de mensajes predeterminado del usuario y los que no. Un almacén de mensajes predeterminado es aquél en el que las aplicaciones cliente y la cola MAPI pueden realizar cualquier tarea de mensajería, como la recepción de mensajes o la creación de carpetas. Un proveedor de almacenamiento de mensajes predeterminado debe admitir varias características más que el número mínimo requerido para todos los proveedores de almacenamiento de mensajes.
  
## <a name="see-also"></a>Vea también

- [Conceptos de MAPI](mapi-concepts.md)

