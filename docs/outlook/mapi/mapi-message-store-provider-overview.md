---
title: Información general sobre el proveedor de almacén de mensajes MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eae44469-b217-4d05-b47f-5a0b1fab7056
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5cc8261dfee6803492ffcf62c182930e2ac6d425
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818160"
---
# <a name="mapi-message-store-provider-overview"></a>Información general sobre el proveedor de almacén de mensajes MAPI
  
**Hace referencia a**: Outlook 
  
Los proveedores de almacén de mensajes controlan el almacenamiento y la recuperación de mensajes y otra información para los usuarios de aplicaciones de cliente. La información del mensaje se organiza mediante el uso de un sistema jerárquico conocido como un almacén de mensajes. El almacén de mensajes se implementa en varios niveles, con contenedores denominados contiene mensajes de distintos tipos de carpetas. No hay ningún límite para el número de niveles en un almacén de mensajes; las carpetas pueden contener varias subcarpetas. 
  
En la siguiente ilustración muestra la arquitectura de almacenamiento de mensaje jerárquica.
  
**Arquitectura del almacén de mensajes**
  
![Arquitectura del almacén de mensajes] (media/amapi_03.gif "Arquitectura del almacén de mensajes")
  
La ilustración muestra dos carpetas, uno con una subcarpeta. Los usuarios de la aplicación de cliente pueden tener acceso a una vista de resumen de los mensajes contenidos en cada carpeta o verlas individualmente con un formulario. Si el cliente muestra un formulario estándar que suministran los MAPI o un formulario personalizado que proporciona un programador de formulario depende el tipo o clase del mensaje. La primera carpeta contiene los mensajes de nota y usa el formulario de nota estándar de MAPI. La segunda carpeta contiene los mensajes de solicitud de inventario y usa un formulario personalizado de inventario. La información en ambos formularios representa las propiedades del mensaje.
  
Puede usar datos de almacén de mensajes en una variedad de formas. Además de usar los datos para el correo electrónico tradicional, puede utilizar las carpetas como un foro de discusión público, como un repositorio para documentos de referencia, o bien como un contenedor para el correo de voz, calendario, contactos o tareas, por ejemplo. Un almacén de mensajes solo puede contener muchos tipos de información. Varios clientes pueden instalar el mismo almacén de mensajes. Esto hace que el uso compartido de datos fácil y rápida. 
  
Carpetas de almacén de mensajes permiten ordenar y filtrar los mensajes y para personalizar la presentación del mensaje en una interfaz de usuario. Vínculos a mensajes filtrados se conservan en carpetas especiales denominadas carpetas de resultados de búsqueda. El usuario de una aplicación cliente entra en criterios de filtrado, que MAPI hace referencia a como una restricción y los criterios se aplica a los mensajes almacenados en una o varias carpetas. Por ejemplo, es posible que un usuario desee ver sólo los mensajes que abordar los problemas con un tema concreto y tienen las fechas de llegada que son más recientes que la última semana. Las referencias a los mensajes que coinciden con los criterios aparecen en la carpeta de búsqueda, y los mensajes reales permanecen en sus carpetas regulares.
  
Los mensajes son las unidades de datos que se transfieren desde una aplicación a otro usuario o aplicación o usuario. Cada mensaje contiene algunos texto del mensaje, con el formato simples o complejos y la información de sobre del mensaje que se usa para la transmisión. Algunos mensajes incluyen uno o más datos adjuntos o datos adicionales relacionados con y transportar con un mensaje en el formulario de un archivo, otro mensaje o un objeto OLE. 
  
Según el mensaje de proveedor de almacén, un usuario puede guardar un nuevo mensaje actualmente que se está escribiendo además a los mensajes que se han enviado o recibido. Los mensajes se pueden copiar o mover de una carpeta a otra con cada copia se convierta en un mensaje independiente que se puede copiar, eliminar o modificar individualmente. Otra característica que habilitar los proveedores de almacén de algunos mensajes es la capacidad para cambiar un mensaje después de que se ha recibido y almacenar en su carpeta. Un usuario puede aprovechar esta característica para girar un mensaje de fax que llega a boca abajo. El usuario puede almacenar la vista correcta en la carpeta para su posterior consulta. 
  
## <a name="see-also"></a>Vea también

- [Arquitectura y las características MAPI](mapi-features-and-architecture.md)

