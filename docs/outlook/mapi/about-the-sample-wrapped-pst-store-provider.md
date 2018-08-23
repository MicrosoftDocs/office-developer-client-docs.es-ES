---
title: Información sobre el proveedor de almacén de archivos PST ajustado de muestra
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: 'Última modificación: 03 de julio de 2012'
ms.openlocfilehash: 399c86d189cfc4160d151f417a6dd20364e60ce3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563831"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a>Información sobre el proveedor de almacén de archivos PST ajustado de muestra

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
## <a name="overview-of-message-store-providers"></a>Información general de los proveedores de almacén de mensajes

Los proveedores de almacén de mensajes controlan el almacenamiento y la recuperación de mensajes y otra información para los usuarios de aplicaciones de cliente. La información del mensaje se organiza mediante el uso de un sistema jerárquico conocido como un almacén de mensajes. El almacén de mensajes se implementa en varios niveles, con contenedores denominados carpetas que contienen mensajes de distintos tipos. No hay ningún límite para el número de niveles en un almacén de mensajes; las carpetas pueden contener varias subcarpetas.
  
Datos de almacén de mensajes se pueden usar en una variedad de formas. Además del uso típico de correo electrónico, las carpetas se pueden utilizar como un foro de discusión público, como un repositorio para documentos de referencia o como un contenedor para la información del boletín electrónico. Un almacén de mensajes solo puede contener muchos tipos de información, puede modificar algunas y otras no. Varios clientes pueden instalar el mismo almacén de mensajes, haciendo que sea fácil y rápida para compartir datos.
  
Carpetas de almacén de mensajes le permiten ordenar y filtrar los mensajes y para personalizar la vista en una presentación (UI) de la interfaz de usuario. Vínculos a mensajes filtrados se conservan en carpetas especiales denominadas carpetas de resultados de búsqueda. El usuario de una aplicación cliente entra en criterios de filtrado, que MAPI hace referencia a como una restricción y los criterios se aplica a los mensajes almacenados en una o varias carpetas. Por ejemplo, es posible que un usuario desee ver sólo los mensajes que se trabaja con un tema concreto con las fechas de llegada que son más recientes que la última semana. Las referencias a los mensajes que coinciden con los criterios aparecen en la carpeta de resultados de búsqueda y los mensajes reales permanecen en sus carpetas regulares.
  
Los mensajes son las unidades de datos que se transfiere desde una aplicación a otro usuario o aplicación o usuario. Cada mensaje contiene algunos texto del mensaje y la información de sobre del mensaje que se usa para la transmisión. Algunos mensajes incluyen uno o más datos adjuntos o datos adicionales relacionados con y transportar con un mensaje en el formulario de un archivo, otro mensaje o un objeto OLE.
  
## <a name="the-sample-wrapped-pst-store-provider"></a>El ejemplo de proveedor de almacén de archivos PST de ajustado

La API de replicación permite replicar los elementos de un repositorio de datos de back-end en un almacén de archivos PST de Outlook. Usar la API de replicación para replicar los datos en un almacén de archivos PST dedicado y realizar un seguimiento de estado de sincronización. Este enfoque no requiere introducir un proveedor de almacén MAPI personalizado, que es el tipo complejo para escribir y mantener. Sin embargo, el proveedor de almacén de archivos PST deba ajustarse para trabajar con la API de replicación.
  
El proveedor de almacén de archivos PST ajustado de ejemplo usa el proveedor de carpetas personales (PST) como back-end para almacenar los datos. El proveedor de almacén de archivos PST ajustado debe usarse junto con la API de replicación. Para obtener más información, vea [Acerca de la API de replicación](about-the-replication-api.md). La mayoría de las funciones en el proveedor de almacén de archivos PST ajustado de ejemplo pasa sus argumentos directamente al proveedor de PST subyacente. Ciertas funciones requieren implementación especial y se describen en los temas siguientes.
  
## <a name="in-this-section"></a>En esta sección

- [Instalar la muestra de proveedor de almacén de archivos PST ajustado](installing-the-sample-wrapped-pst-store-provider.md)
    
- Se explica cómo descargar e instalar al proveedor de almacén de archivos PST ajustado de ejemplo.
    
- [Inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md)
    
- Es el primer paso en la implementación de un proveedor de almacén de archivos PST ajustado inicializar y configurar el proveedor de almacén de archivos PST ajustado.
    
- [Iniciar sesión en un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md)
    
- Después de Inicializa un proveedor de almacén de archivos PST ajustado, debe implementar las funciones para que MAPI y la cola MAPI pueden iniciar sesión en el proveedor de almacén de archivos PST ajustado.
    
- [Usar un proveedor de almacén de archivos PST ajustado](using-a-wrapped-pst-store-provider.md)
    
- Para usar un almacén de archivos PST ajustado proveedor debe ajustar la interfaz **[IMAPISupport::IUnknown](imapisupportiunknown.md)** para implementar comunes ajustado tareas de proveedor de almacén de archivos PST. 
    
- [Apagar un proveedor de almacén de archivos PST ajustado](shutting-down-a-wrapped-pst-store-provider.md)
    
- Cuando termine de usar un proveedor de almacén de archivos PST ajustado, debe cerrar correctamente el proveedor de almacén de archivos PST ajustado.
    
## <a name="see-also"></a>Recursos adicionales



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Desarrollar un proveedor de almac�n de mensajes de MAPI](developing-a-mapi-message-store-provider.md)

