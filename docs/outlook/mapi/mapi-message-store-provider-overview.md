---
title: Introducción al proveedor de almacenamiento de mensajes MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eae44469-b217-4d05-b47f-5a0b1fab7056
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5d4ef074523cd654c3db2d686494d9a4f864e7cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345881"
---
# <a name="mapi-message-store-provider-overview"></a>Introducción al proveedor de almacenamiento de mensajes MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de almacén de mensajes administran el almacenamiento y la recuperación de mensajes y otra información para los usuarios de las aplicaciones cliente. La información del mensaje se organiza mediante un sistema jerárquico conocido como almacén de mensajes. El almacén de mensajes se implementa en varios niveles, con contenedores denominados carpetas que contienen mensajes de distintos tipos. No hay ningún límite en el número de niveles de un almacén de mensajes; las carpetas pueden contener varias subcarpetas. 
  
En la siguiente ilustración se muestra la arquitectura del almacén de mensajes jerárquico.
  
**Arquitectura del almacén de mensajes**
  
![Arquitectura del almacén de mensajes] (media/amapi_03.gif "Arquitectura del almacén de mensajes")
  
La figura muestra dos carpetas, una con una subcarpeta. Los usuarios de la aplicación cliente pueden tener acceso a una vista de Resumen de los mensajes contenidos en cada carpeta o visualizarlos individualmente con un formulario. Si el cliente muestra un formulario estándar que proporciona MAPI o un formulario personalizado que proporciona un desarrollador de formularios depende del tipo, o clase, del mensaje. La primera carpeta contiene mensajes de notas y utiliza el formulario de notas estándar de MAPI. La segunda carpeta contiene mensajes de solicitud de inventario y usa un formulario de inventario personalizado. La información de ambos formularios representa las propiedades del mensaje.
  
Puede usar los datos del almacén de mensajes de varias formas. Además de usar datos para el correo electrónico tradicional, puede usar carpetas como foro para discusión pública, como repositorio para los documentos de referencia o como contenedor de correo de voz, calendario, contactos o tareas, por ejemplo. Un solo almacén de mensajes puede contener muchos tipos de información. Varios clientes pueden instalar el mismo almacén de mensajes. Esto hace que el uso compartido de los datos sea fácil y rápido. 
  
Las carpetas del almacén de mensajes permiten ordenar y filtrar los mensajes y personalizar la presentación del mensaje en una interfaz de usuario. Los vínculos a mensajes filtrados se conservan en carpetas especiales llamadas carpetas de resultados de búsqueda. El usuario de una aplicación cliente introduce criterios de filtrado, a los que MAPI hace referencia como una restricción, y los criterios se aplican a los mensajes almacenados en una o más carpetas. Por ejemplo, es posible que un usuario desee ver sólo los mensajes que tratan un tema concreto y que tienen fechas de llegada más recientes que la semana pasada. Las referencias a los mensajes que coinciden con los criterios se enumeran en la carpeta de búsqueda y los mensajes reales permanecen en sus carpetas normales.
  
Los mensajes son las unidades de datos que se transfieren de un usuario o aplicación a otro usuario o aplicación. Todos los mensajes contienen texto de mensaje, con formato sencillo o complejo, e información de sobre del mensaje que se usa para la transmisión. Algunos mensajes incluyen uno o más datos adjuntos, o datos adicionales relacionados con un mensaje en forma de archivo, otro mensaje o un objeto OLE, o se transportan con un mensaje. 
  
Según el proveedor de almacenamiento de mensajes, un usuario puede guardar un nuevo mensaje que se está escribiendo actualmente además de los mensajes que se han enviado o recibido. Los mensajes se pueden copiar o mover de una carpeta a otra con cada copia convirtiéndose en un mensaje independiente que se puede copiar, eliminar o modificar de forma individual. Otra característica que habilitan algunos proveedores de almacenamiento de mensajes es la capacidad de cambiar un mensaje tras su recepción y volver a almacenarlo en su carpeta. Un usuario puede aprovechar esta característica para girar un mensaje de fax que llegó al revés. El usuario puede almacenar la vista correcta en la carpeta para verla posteriormente. 
  
## <a name="see-also"></a>Vea también

- [Arquitectura y características de MAPI](mapi-features-and-architecture.md)

