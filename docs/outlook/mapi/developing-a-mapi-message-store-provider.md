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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412614"
---
# <a name="developing-a-mapi-message-store-provider"></a>Desarrollar un proveedor de almacén de mensajes de MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Al igual que otros proveedores de servicios MAPI, los almacenes de mensajes son bibliotecas de vínculos dinámicos (DLL) que presentan los servicios de un mecanismo de almacenamiento subyacente para las aplicaciones cliente MAPI y la cola MAPI. El proveedor del almacén de mensajes presenta el mecanismo de almacenamiento subyacente como un conjunto jerárquico de carpetas y mensajes que los clientes MAPI y la cola MAPI pueden usar.
  
En la siguiente ilustración se muestra la arquitectura básica del almacén de mensajes MAPI.
  
**Arquitectura del almacén de mensajes**
  
![Arquitectura del almacén de mensajes]Arquitectura del almacén de(media/storearc.gif "mensajes")
  
Puedes implementar un proveedor de almacén de mensajes mediante cualquier tipo de mecanismo de almacenamiento subyacente que quieras. Sin embargo, debe ser consciente de los problemas de rendimiento. Además, el mecanismo de almacenamiento subyacente debe presentarse como una colección jerárquica de objetos MAPI. Estos requisitos significan que los almacenes de mensajes normalmente se implementan mediante un producto de base de datos existente que admite el almacenamiento jerárquico de objetos en la base de datos y que tiene una interfaz de programación o una estructura de archivos bien definida. Por ejemplo, Microsoft Office bases de datos de Access, SQL y Oracle se pueden usar como mecanismo de almacenamiento subyacente. Algunos productos de base de datos tienen conjuntos de características que facilitan la implementación de características MAPI, por lo que la elección del producto de base de datos puede verse afectada por las características que el proveedor del almacén de mensajes necesita admitir.
  
El uso de una base de datos existente como mecanismo de almacenamiento subyacente ahorra trabajo porque suele ser más fácil presentar objetos de base de datos a los clientes MAPI como objetos MAPI que implementar su propio mecanismo de almacenamiento jerárquico. Esto le permite tratar las operaciones MAPI en un nivel superior que si implementa su propio mecanismo de almacenamiento jerárquico. Por ejemplo, la búsqueda de un mensaje con una línea de asunto determinada se convierte en una cuestión bastante sencilla de crear y enviar una consulta de base de datos adecuada, en lugar de implementar rutinas complejas para buscar en el mecanismo de almacenamiento jerárquico.
  
Los proveedores de almacén de mensajes se comunican con clientes MAPI y la cola MAPI para realizar operaciones en carpetas y objetos. El proveedor del almacén de mensajes convierte esas operaciones en operaciones de nivel inferior en el mecanismo de almacenamiento subyacente. La cola MAPI normalmente se comunica con el proveedor del almacén de mensajes al enviar y recibir mensajes. Normalmente, los clientes MAPI se comunican con proveedores de almacén de mensajes para manipular la jerarquía de carpetas y para leer, editar, eliminar y enviar mensajes.
  
Tanto la cola MAPI como los clientes MAPI se comunican con el proveedor del almacén de mensajes para crear nuevos mensajes. Las aplicaciones cliente hacen esto cuando los usuarios redacten un mensaje. La cola MAPI hace esto cuando recibe un mensaje entrante. En cualquier caso, el nuevo mensaje normalmente se crea en la carpeta Bandeja de entrada del almacén de mensajes, si hay uno.
  
Los proveedores de almacén de mensajes usan mucho las tablas, carpetas, mensajes y propiedades MAPI. Los detalles de implementación de esos objetos se documentan en [Tablas MAPI,](mapi-tables.md) [Carpetas MAPI,](mapi-folders.md)Mensajes [MAPI](mapi-messages.md)y Información general [sobre la propiedad MAPI](mapi-property-overview.md). Debes familiarizarte con ese material antes de intentar implementar un proveedor de almacén de mensajes.
  
Hay dos tipos importantes de proveedores de almacén de mensajes: los que pueden actuar como almacén de mensajes predeterminado de un usuario y los que no pueden. Un almacén de mensajes predeterminado es uno en el que las aplicaciones cliente y la cola MAPI pueden realizar cualquier tarea de mensajería, como recibir mensajes o crear carpetas. Un proveedor de almacén de mensajes predeterminado debe admitir varias características más que el número mínimo necesario para todos los proveedores de almacén de mensajes.
  
## <a name="see-also"></a>Vea también

- [Conceptos MAPI](mapi-concepts.md)

