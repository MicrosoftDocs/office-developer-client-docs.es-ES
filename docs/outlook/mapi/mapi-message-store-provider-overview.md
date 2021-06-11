---
title: Introducción al proveedor de almacén de mensajes MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eae44469-b217-4d05-b47f-5a0b1fab7056
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5d4ef074523cd654c3db2d686494d9a4f864e7cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429316"
---
# <a name="mapi-message-store-provider-overview"></a>Introducción al proveedor de almacén de mensajes MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de almacén de mensajes administran el almacenamiento y la recuperación de mensajes y otra información para los usuarios de las aplicaciones cliente. La información del mensaje se organiza mediante un sistema jerárquico conocido como almacén de mensajes. El almacén de mensajes se implementa en varios niveles, con contenedores denominados carpetas que retienen mensajes de diferentes tipos. No hay ningún límite en el número de niveles de un almacén de mensajes; carpetas pueden contener muchas subcarpetas. 
  
En la siguiente ilustración se muestra la arquitectura jerárquica del almacén de mensajes.
  
**Arquitectura del almacén de mensajes**
  
![Arquitectura del almacén de mensajes]Arquitectura del almacén de(media/amapi_03.gif "mensajes")
  
La figura muestra dos carpetas, una con una subcarpeta. Los usuarios de la aplicación cliente pueden obtener acceso a una vista de resumen de los mensajes contenidos en cada carpeta o verlos individualmente con un formulario. Si el cliente muestra un formulario estándar que MAPI proporciona o un formulario personalizado que proporciona un desarrollador de formularios depende del tipo o clase del mensaje. La primera carpeta contiene mensajes de nota y usa el formulario de nota estándar MAPI. La segunda carpeta contiene mensajes de solicitud de inventario y usa un formulario de inventario personalizado. La información de ambos formularios representa las propiedades del mensaje.
  
Puede usar los datos del almacén de mensajes de varias maneras. Además de usar datos para el correo electrónico tradicional, puede usar carpetas como un foro de discusión pública, como repositorio para documentos de referencia o como contenedor para correo de voz, calendario, contactos o tareas, por ejemplo. Un único almacén de mensajes puede contener muchos tipos de información. Varios clientes pueden instalar el mismo almacén de mensajes. Esto hace que el uso compartido de datos sea fácil y rápido. 
  
Las carpetas del almacén de mensajes permiten ordenar y filtrar mensajes y personalizar la presentación de mensajes en una interfaz de usuario. Los vínculos a mensajes filtrados se mantienen en carpetas especiales denominadas carpetas de resultados de búsqueda. El usuario de una aplicación cliente escribe criterios de filtrado, a los que MAPI hace referencia como restricción, y los criterios se aplican a los mensajes almacenados en una o más carpetas. Por ejemplo, es posible que un usuario quiera ver solo los mensajes que tratan con un asunto determinado y tienen fechas de llegada más recientes que la semana pasada. Las referencias a los mensajes que coinciden con los criterios se enumeran en la carpeta de búsqueda y los mensajes reales permanecen en sus carpetas regulares.
  
Los mensajes son las unidades de datos que se transfieren de un usuario o aplicación a otro usuario o aplicación. Cada mensaje contiene texto de mensaje, con formato simple o complejo, e información de sobre de mensaje que se usa para la transmisión. Algunos mensajes incluyen uno o varios datos adjuntos, o datos adicionales relacionados con y se transportan con un mensaje en forma de archivo, otro mensaje o un objeto OLE. 
  
Según el proveedor del almacén de mensajes, un usuario puede guardar un nuevo mensaje que se está redactando actualmente además de los mensajes que se han enviado o recibido. Los mensajes se pueden copiar o mover de una carpeta a otra y cada copia se convierte en un mensaje independiente que se puede copiar, eliminar o modificar individualmente. Otra característica que habilitan algunos proveedores de almacén de mensajes es la capacidad de cambiar un mensaje después de que se haya recibido y volver a almacenarlo en su carpeta. Un usuario puede aprovechar esta característica para girar un mensaje de fax que llegó al revés. El usuario puede almacenar la vista correcta en la carpeta para su posterior visualización. 
  
## <a name="see-also"></a>Vea también

- [Características y arquitectura MAPI](mapi-features-and-architecture.md)

