---
title: Acerca del proveedor de almacén PST ajustado de ejemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: 779dd96c4f07c0c5eee60ae046cd17db98eebfd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432726"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a>Acerca del proveedor de almacén PST ajustado de ejemplo

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
## <a name="overview-of-message-store-providers"></a>Información general sobre los proveedores de almacén de mensajes

Los proveedores de almacén de mensajes administran el almacenamiento y la recuperación de mensajes y otra información para los usuarios de las aplicaciones cliente. La información del mensaje se organiza mediante un sistema jerárquico conocido como almacén de mensajes. El almacén de mensajes se implementa en varios niveles, con contenedores denominados carpetas que almacenan mensajes de diferentes tipos. No hay ningún límite en el número de niveles de un almacén de mensajes; carpetas pueden contener muchas subcarpetas.
  
Los datos del almacén de mensajes se pueden usar de varias maneras. Además del uso típico del correo electrónico, las carpetas se pueden usar como un foro de discusión pública, como repositorio para documentos de referencia o como contenedor para la información del tablón de anuncios. Un único almacén de mensajes puede contener muchos tipos de información, algunos modificables y otros no. Varios clientes pueden instalar el mismo almacén de mensajes, lo que facilita y facilita el uso compartido de datos.
  
Las carpetas del almacén de mensajes permiten ordenar y filtrar mensajes y personalizar la vista en una pantalla de interfaz de usuario (UI). Los vínculos a mensajes filtrados se mantienen en carpetas especiales denominadas carpetas de resultados de búsqueda. El usuario de una aplicación cliente escribe criterios de filtrado, a los que MAPI hace referencia como restricción, y los criterios se aplican a los mensajes almacenados en una o más carpetas. Por ejemplo, es posible que un usuario quiera ver solo los mensajes que tratan con un asunto determinado con fechas de llegada más recientes que la semana pasada. Las referencias a los mensajes que coinciden con los criterios se enumeran en la carpeta de resultados de búsqueda y los mensajes reales permanecen en sus carpetas regulares.
  
Los mensajes son las unidades de datos transferidas de un usuario o aplicación a otro usuario o aplicación. Cada mensaje contiene algún texto de mensaje e información sobre de mensaje que se usa para la transmisión. Algunos mensajes incluyen uno o varios datos adjuntos, o datos adicionales relacionados con y se transportan con un mensaje en forma de archivo, otro mensaje o un objeto OLE.
  
## <a name="the-sample-wrapped-pst-store-provider"></a>Proveedor de almacén PST ajustado de ejemplo

La API de replicación permite replicar elementos de un repositorio de datos back-end en un Outlook PST. Use la API de replicación para replicar los datos en un almacén DE PST dedicado y realizar un seguimiento del estado de sincronización. Este enfoque no requiere que se presente un proveedor de almacén MAPI personalizado, que es complejo de escribir y mantener. Sin embargo, el proveedor del almacén PST necesita ajustarse para funcionar con la API de replicación.
  
El proveedor de almacén PST ajustado de ejemplo usa el proveedor de archivos de carpetas personales (PST) como back-end para almacenar datos. El proveedor del almacén PST ajustado debe usarse junto con la API de replicación. Para obtener más información, vea [Acerca de la API de replicación](about-the-replication-api.md). La mayoría de las funciones del proveedor de almacén PST ajustado de muestra pasan sus argumentos directamente al proveedor de PST subyacente. Algunas funciones requieren una implementación especial y se describen en los temas siguientes.
  
## <a name="in-this-section"></a>En esta sección

- [Instalación del proveedor de almacén PST ajustado de muestra](installing-the-sample-wrapped-pst-store-provider.md)
    
- Explica cómo descargar e instalar el proveedor de la tienda PST encapsulada de muestra.
    
- [Inicializar un proveedor de almacenamiento PST ajustado](initializing-a-wrapped-pst-store-provider.md)
    
- El primer paso para implementar un proveedor de almacenamiento PST ajustado es inicializar y configurar el proveedor de almacenamiento PST ajustado.
    
- [Iniciar sesión en un proveedor de almacenamiento PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md)
    
- Después de inicializar un proveedor de almacenamiento PST ajustado, debe implementar funciones para que MAPI y la cola MAPI puedan iniciar sesión en el proveedor de almacenamiento PST ajustado.
    
- [Uso de un proveedor de almacenamiento PST ajustado](using-a-wrapped-pst-store-provider.md)
    
- Para usar un proveedor de almacenamiento PST ajustado, debe ajustar la interfaz **[IMAPISupport::IUnknown](imapisupportiunknown.md)** para implementar tareas comunes del proveedor del almacén PST ajustado. 
    
- [Apagar un proveedor de almacenamiento PST ajustado](shutting-down-a-wrapped-pst-store-provider.md)
    
- Una vez que termine de usar un proveedor de almacenamiento PST ajustado, debe cerrar correctamente el proveedor de almacenamiento PST ajustado.
    
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Desarrollar un proveedor de almac�n de mensajes de MAPI](developing-a-mapi-message-store-provider.md)

