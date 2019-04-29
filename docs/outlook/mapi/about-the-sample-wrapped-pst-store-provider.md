---
title: Información sobre el proveedor de almacén de archivos PST ajustado de ejemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: 'Última modificación: 3 de julio de 2012'
ms.openlocfilehash: 779dd96c4f07c0c5eee60ae046cd17db98eebfd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432726"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a>Información sobre el proveedor de almacén de archivos PST ajustado de ejemplo

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
## <a name="overview-of-message-store-providers"></a>Información general sobre los proveedores de almacenamiento de mensajes

Los proveedores de almacén de mensajes administran el almacenamiento y la recuperación de mensajes y otra información para los usuarios de las aplicaciones cliente. La información del mensaje se organiza mediante un sistema jerárquico conocido como almacén de mensajes. El almacén de mensajes se implementa en varios niveles, con contenedores denominados carpetas que contienen mensajes de distintos tipos. No hay ningún límite en el número de niveles de un almacén de mensajes; las carpetas pueden contener varias subcarpetas.
  
Los datos del almacén de mensajes se pueden usar de varias formas. Además del uso típico del correo electrónico, las carpetas se pueden usar como foro de discusión pública, como repositorio para los documentos de referencia o como contenedor para la información del tablón de anuncios. Un solo almacén de mensajes puede contener muchos tipos de información, algunas modificables y otras no. Varios clientes pueden instalar el mismo almacén de mensajes, lo que facilita y agiliza el uso compartido de datos.
  
Las carpetas del almacén de mensajes le permiten ordenar y filtrar los mensajes y personalizar la vista en una pantalla de interfaz de usuario (UI). Los vínculos a mensajes filtrados se conservan en carpetas especiales llamadas carpetas de resultados de búsqueda. El usuario de una aplicación cliente introduce criterios de filtrado, a los que MAPI hace referencia como una restricción, y los criterios se aplican a los mensajes almacenados en una o más carpetas. Por ejemplo, es posible que un usuario desee ver sólo los mensajes relacionados con un asunto concreto con fechas de llegada que son más recientes que la semana pasada. Las referencias a los mensajes que coinciden con los criterios se enumeran en la carpeta de resultados de búsqueda y los mensajes reales permanecen en sus carpetas normales.
  
Los mensajes son las unidades de datos que se transfieren de un usuario o aplicación a otro usuario o aplicación. Cada mensaje contiene el texto del mensaje y la información sobre el mensaje que se usa para la transmisión. Algunos mensajes incluyen uno o más datos adjuntos, o datos adicionales relacionados con un mensaje en forma de archivo, otro mensaje o un objeto OLE, o se transportan con un mensaje.
  
## <a name="the-sample-wrapped-pst-store-provider"></a>El proveedor de almacén de archivos PST ajustado de muestra

La API de replicación permite replicar elementos de un repositorio de datos back-end en un almacén de archivos PST de Outlook. La API de replicación se usa para replicar los datos en un almacén de archivos PST dedicado y realizar un seguimiento del estado de sincronización. Este método no requiere que introduzca un proveedor de almacén MAPI personalizado, que es complejo de escribir y mantener. Sin embargo, el proveedor de almacén PST tiene que ajustarse para que funcione con la API de replicación.
  
El proveedor de almacén de archivos PST ajustado de ejemplo usa el proveedor de archivos de carpetas personales (PST) como back-end para almacenar datos. El proveedor de almacén de archivos PST ajustado debe usarse junto con la API de replicación. Para obtener más información, vea [acerca de la API de replicación](about-the-replication-api.md). La mayoría de las funciones del proveedor de almacén de archivos PST ajustado de ejemplo pasan sus argumentos directamente al proveedor de PST subyacente. Algunas funciones requieren una implementación especial y se describen en los siguientes temas.
  
## <a name="in-this-section"></a>En esta sección

- [Instalación del proveedor de almacén de archivos PST ajustado de ejemplo](installing-the-sample-wrapped-pst-store-provider.md)
    
- Explica cómo descargar e instalar el proveedor de almacén de archivos PST ajustado de ejemplo.
    
- [Inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md)
    
- El primer paso para implementar un proveedor de almacén de archivos PST ajustado es inicializar y configurar el proveedor de almacén de archivos PST ajustado.
    
- [Inicio de sesión en un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md)
    
- Después de inicializar un proveedor de almacén de archivos PST ajustado, debe implementar funciones para que MAPI y la cola MAPI puedan iniciar sesión en el proveedor de almacén de archivos PST ajustado.
    
- [Usar un proveedor de almacén de archivos PST ajustado](using-a-wrapped-pst-store-provider.md)
    
- Para usar un proveedor de almacén de archivos PST ajustado, debe ajustar la interfaz **[IMAPISupport:: IUnknown](imapisupportiunknown.md)** para implementar las tareas comunes del proveedor de almacenamiento de PST ajustado. 
    
- [Apagar un proveedor de almacén de archivos PST ajustado](shutting-down-a-wrapped-pst-store-provider.md)
    
- Una vez que haya terminado de usar un proveedor de almacén de archivos PST ajustado, debe apagar correctamente el proveedor de almacén de archivos PST ajustado.
    
## <a name="see-also"></a>Ver también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Desarrollar un proveedor de almac�n de mensajes de MAPI](developing-a-mapi-message-store-provider.md)

