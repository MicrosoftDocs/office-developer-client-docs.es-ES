---
title: Perfiles y servicios de mensajería
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df0db1e4-69c8-44ec-bb2a-d31fc8a564b9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 78a13bacf13b019bbf9436830ad66db7fdfaf425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415470"
---
# <a name="message-services-and-profiles"></a>Perfiles y servicios de mensajería
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Algunos usuarios requieren los servicios de varios sistemas de mensajería, cada uno con uno o más proveedores de servicios. Dado que es engorroso instalar y configurar cada uno de estos proveedores de servicios individualmente, y dado que un servidor de mensajería normalmente requiere que un grupo de proveedores relacionados exponga todas sus funciones, MAPI incluye el concepto de servicio de mensajes. Los servicios de mensajes ayudan a los usuarios a instalar y configurar sus proveedores de servicios.
  
Para crear un servicio de mensajes, un desarrollador escribe un programa de punto de entrada de servicio de mensajes para controlar la configuración de cada proveedor en el servicio y un programa de instalación para hacer lo siguiente:
  
- Instale cada proveedor en el servicio.
    
- Cree entradas del registro y del archivo de inicialización.
    
- Cree entradas en el archivo de configuración MAPI, Mapisvc.inf.
    
El archivo Mapisvc.inf contiene información relacionada con la configuración de todos los servicios de mensajes y proveedores de servicios instalados en el equipo. Se organiza en secciones jerárquicas, con cada nivel vinculado al siguiente. En la parte superior hay tres secciones que contienen lo siguiente: 
  
- Una lista de archivos de ayuda del servicio de mensajes.
    
- Una lista de los servicios de mensajes más importantes o predeterminados.
    
- Una lista de todos los servicios del equipo.
    
El siguiente nivel contiene secciones para cada servicio de mensajes y el último nivel contiene secciones para cada proveedor de servicios de un servicio. MAPI requiere que los programadores de proveedores de servicios y servicios de mensajes agreguen ciertas entradas a Mapisvc.inf; los desarrolladores pueden agregar otras entradas a su propia discreción. La mayor parte de la información de Mapisvc.inf termina en uno o más perfiles, una colección de información de configuración para el conjunto preferido de servicios de mensajes de un usuario. Dado que un equipo puede tener varios usuarios y un solo usuario puede tener varios conjuntos de preferencias, pueden existir muchos perfiles en un equipo. Cada perfil describe un conjunto diferente de servicios de mensajes. Tener varios perfiles permite a un usuario trabajar, por ejemplo, en casa con un conjunto de servicios de mensajes y en la oficina con un conjunto diferente.
  
Los perfiles se crean en la instalación del servicio de mensajes o en la hora de inicio de sesión por parte de una aplicación cliente que proporciona compatibilidad con la configuración. MAPI proporciona dos aplicaciones cliente de este tipo: un elemento del Panel de control y el Asistente para perfiles. El elemento panel de control es una aplicación de configuración de servicio completo con la que los usuarios pueden crear, eliminar, editar y copiar perfiles, así como realizar modificaciones en las entradas de un perfil. El Asistente para perfiles es una aplicación sencilla diseñada para que agregar un servicio de mensajes a un perfil sea lo más fácil posible. El Asistente para perfiles consta de una serie de cuadros de diálogo, denominados páginas de propiedades, que preguntan al usuario durante el proceso de instalación y configuración de un servicio. Al usuario solo se le piden valores para la configuración más crítica; todas las demás opciones heredan los valores predeterminados. Una vez creado el perfil, los usuarios no pueden realizar cambios. 
  
Mientras que el elemento panel de control siempre se invoca a través del Panel de control, hay una variedad de escenarios que pueden hacer que se llame al Asistente para perfiles. Las aplicaciones cliente pueden llamar al Asistente para perfiles para crear un perfil predeterminado en el momento del inicio de sesión cuando aún no se haya creado uno. En lugar de volver a implementar código para agregar un perfil, el elemento del Panel de control u otra aplicación cliente puede confiar en la funcionalidad que ya se encuentra en el Asistente para perfiles. Un servicio de mensajes, en su función de punto de entrada, puede llamar al Asistente para perfiles cuando el servicio necesita agregarse al perfil predeterminado. Los servicios de mensajes que usan el Asistente para perfiles deben escribir una función de punto de entrada adicional y un procedimiento Windows cuadro de diálogo estándar. El Asistente para perfiles llama a la función de punto de entrada para recuperar el cuadro de diálogo de configuración del servicio mientras el procedimiento del cuadro de diálogo controla los mensajes que se generan cuando se usa este cuadro de diálogo. 
  
Los perfiles se organizan de forma similar al archivo Mapisvc.inf. Los perfiles tienen secciones jerárquicas vinculadas; Los proveedores de servicios poseen secciones en el nivel más bajo, los servicios de mensajes poseen secciones en el nivel medio y MAPI posee secciones en el nivel más alto. Cada sección se identifica con un identificador único conocido como [MAPIUID](mapiuid.md). Las secciones MAPI contienen información interna de MAPI, como los identificadores de todas las secciones de perfil de servicio de mensajes y vínculos a cada una de las otras secciones. Cada sección de servicio de mensajes almacena vínculos a sus secciones de proveedor y cada sección de proveedor almacena un vínculo a su sección de servicio. 
  
En la siguiente ilustración se muestra el contenido de dos perfiles típicos. Sam tiene dos perfiles en su equipo, uno para uso en casa y otro para uso de office. El perfil principal contiene tres servicios de mensajes. Message Service X es un servicio de proveedor único para la administración de libreta de direcciones. Message Services Y y Z tienen tres proveedores: un proveedor de libreta de direcciones, un proveedor de almacén de mensajes y un proveedor de transporte. El perfil de trabajo de Sam contiene dos servicios de mensajes diferentes, cada uno de los cuales tiene un proveedor de libreta de direcciones, un proveedor de almacén de mensajes y un proveedor de transporte. 
  
**Ejemplo de perfil**
  
![Ejemplo de perfil](media/amapi_56.gif "Ejemplo de perfil Ejemplo de perfil")
  
En la siguiente ilustración se muestra un perfil que incluye dos servicios de mensajes. El código para instalar y configurar los proveedores de servicios que pertenecen al servicio de mensajes reside en la misma DLL que el código de los proveedores. Este código lee información del perfil en el momento del inicio de sesión para configurar los proveedores de servicios y solicita al usuario, si es posible y necesario, que falte información. Este código común también controla las solicitudes de un cliente para ver o cambiar las opciones de configuración de cualquiera de los proveedores.
  
**Instalación y configuración de proveedores de servicio**
  
![Instalación y configuración de proveedores de servicios]Instalación y configuración de proveedores de(media/amapi_55.gif "servicios")
  
## <a name="see-also"></a>Vea también

- [MAPIUID](mapiuid.md)
- [Información general sobre programación de MAPI](mapi-programming-overview.md)

