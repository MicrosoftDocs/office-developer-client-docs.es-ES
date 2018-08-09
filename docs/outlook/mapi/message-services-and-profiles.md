---
title: Los perfiles y servicios de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df0db1e4-69c8-44ec-bb2a-d31fc8a564b9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0f55d4cda013810884177a0f47e861e3693defd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818404"
---
# <a name="message-services-and-profiles"></a>Los perfiles y servicios de mensajes
  
**Hace referencia a**: Outlook 
  
Algunos usuarios requieren los servicios de varios sistemas de mensajería, cada uno con uno o más proveedores de servicio. Porque se multisistema para instalar y configurar cada uno de estos proveedores de servicios de forma individual, y debido a que un servidor de mensajería normalmente requiere un grupo de proveedores relacionados para exponer toda su funcionalidad, MAPI incluye el concepto de un servicio de mensajes. Servicios de mensajes para los usuarios de instalar y configurar los proveedores de servicios.
  
Para crear un servicio de mensajes, un desarrollador escribe un programa de punto de entrada del servicio de mensajes para administrar la configuración de cada proveedor en el servicio y un programa de instalación para hacer lo siguiente:
  
- Instalación de cada proveedor en el servicio.
    
- Crear las entradas del archivo de registro e inicialización.
    
- Crear entradas en el archivo de configuración de MAPI, Mapisvc.inf.
    
El archivo Mapisvc.inf contiene información relacionada con la configuración de todos los servicios de mensajes y los proveedores de servicios instalados en el equipo. Se organiza en secciones jerárquicas, con cada nivel vinculada a la siguiente. En la parte superior son tres secciones que contienen lo siguiente: 
  
- Una lista de archivos de Ayuda de servicio de mensajes.
    
- Una lista de los servicios de mensaje más importantes, o de forma predeterminada.
    
- Una lista de todos los servicios en el equipo.
    
El siguiente nivel contiene las secciones para cada servicio de mensajes y el último nivel contiene las secciones para cada proveedor de servicios en un servicio. MAPI requiere que los programadores de proveedores de servicios y los servicios de message agregar determinadas entradas a Mapisvc.inf; los programadores pueden agregar otras entradas a su propia discreción. La mayoría de la información de Mapisvc.inf termina en uno o más perfiles, una colección de información de configuración para un usuario preferido conjunto de servicios de mensaje. Debido a que un equipo puede tener varios usuarios y un único usuario puede tener varios conjuntos de preferencias, muchos perfiles pueden existir en un equipo. Cada perfil describe un conjunto diferente de servicios de mensajes. Tener varios perfiles permite a un usuario trabajar, por ejemplo, en casa con un conjunto de servicios de mensajes y en la oficina con un conjunto diferente.
  
Los perfiles se crean en el tiempo de inicio de sesión o la instalación del servicio de mensajes por una aplicación cliente que proporciona compatibilidad de configuración. MAPI proporciona dos de esos clientes aplicaciones: un elemento del Panel de Control y el Asistente para perfiles. El elemento del Panel de Control es una aplicación de servicio completo de configuración con la que los usuarios pueden crear, eliminar, editar y copiar los perfiles de, así como realizar modificaciones en las entradas en un perfil de. El Asistente para perfiles es una sencilla aplicación diseñada para facilitar la adición de un servicio de mensajes a un perfil tan fácil como sea posible. El Asistente para perfiles consta de una serie de cuadros de diálogo, denominado páginas de propiedades, que pregunta al usuario a través del proceso de instalación y configuración de un servicio. Se solicita al usuario sólo para los valores de la configuración más importante; todas las demás opciones heredan los valores predeterminados. Una vez que se ha creado el perfil, los usuarios no pueden realizar cambios. 
  
Mientras que el elemento del Panel de Control siempre se invoca a través del Panel de Control, hay una variedad de escenarios que pueden hacer que el Asistente para perfiles para llamarla. Las aplicaciones cliente pueden llamar el Asistente para perfiles para crear un perfil predeterminado en tiempo de inicio de sesión cuando uno aún no se ha creado. En lugar de volver a implementarlo código para agregar un perfil, el elemento del Panel de Control u otra aplicación de cliente puede basarse en la funcionalidad ya está en el Asistente para perfiles. En su función de punto de entrada, un servicio de mensajes, puede llamar al Asistente para perfiles cuando el servicio debe agregarse al perfil predeterminado. Servicios de mensaje que utilice al Asistente para perfiles deben escribir una función de punto de entrada adicional y un procedimiento de cuadro de diálogo estándar de Windows. El Asistente para perfiles llama a la función de punto de entrada para recuperar el cuadro de diálogo de configuración del servicio mientras el procedimiento de cuadro de diálogo controla los mensajes que se generan cuando este cuadro de diálogo está en uso. 
  
Los perfiles se organizan de forma similar al archivo Mapisvc.inf. Los perfiles de han vinculado secciones jerárquicas; secciones propios de los proveedores de servicio en el nivel más bajo, servicios de mensajes propietario secciones en el nivel intermedio, y MAPI propietario de secciones en el nivel más alto. Cada sección se identifica con un identificador único conocido como un [MAPIUID](mapiuid.md). Las secciones MAPI contienen información interna MAPI, como los identificadores de todas las secciones de perfil de servicio de mensajes y vínculos a cada una de las demás secciones. Cada sección del servicio de mensajes almacena vínculos a secciones de su proveedor, y cada sección del proveedor almacena un vínculo a la sección servicio. 
  
En la siguiente ilustración se muestra el contenido de dos perfiles típicos. SAM tiene dos perfiles en su equipo, uno para uso doméstico y otro para uso en la oficina. El perfil de la página principal contiene tres servicios de mensaje. X de servicio del mensaje es un servicio de proveedor único para la administración de la libreta de direcciones. Mensaje de servicios Y y Z tienen tres proveedores: un proveedor de la libreta de direcciones, un proveedor de almacén de mensajes y un proveedor de transporte. Perfil de trabajo de SAM contiene dos servicios de mensaje diferentes, cada uno de los cuales tiene un proveedor de la libreta de direcciones, un proveedor de almacén de mensajes y un proveedor de transporte. 
  
**Ejemplo de perfil**
  
![Ejemplo de perfil] (media/amapi_56.gif "Ejemplo de perfil")
  
En la siguiente ilustración muestra un perfil que incluye dos servicios de mensaje. El código para instalar y configurar los proveedores de servicios que pertenecen al servicio de mensajes reside en la misma DLL que el código para los proveedores. Este código lee la información del perfil de tiempo de inicio de sesión para configurar los proveedores de servicios y lo solicita el usuario, si es posible y es necesario, para obtener información que faltan. También se controlan las solicitudes de un cliente para ver o cambiar la configuración para cualquiera de los proveedores por este código común.
  
**Instalación y configuración de proveedores de servicio**
  
![Instalar y configurar los proveedores de servicios] (media/amapi_55.gif "Instalar y configurar los proveedores de servicios")
  
## <a name="see-also"></a>Vea también

- [MAPIUID](mapiuid.md)
- [Informaci�n general sobre programaci�n de MAPI](mapi-programming-overview.md)

