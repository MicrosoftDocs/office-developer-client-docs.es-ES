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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356969"
---
# <a name="message-services-and-profiles"></a>Perfiles y servicios de mensajería
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Algunos usuarios necesitan los servicios de varios sistemas de mensajería, cada uno con uno o varios proveedores de servicios. Debido a que es engorroso instalar y configurar cada uno de estos proveedores de servicios de forma individual y que, por lo general, un servidor de mensajería requiere un grupo de proveedores relacionados para exponer todas sus funciones, MAPI incluye el concepto de servicio de mensajes. Los servicios de mensajes ayudan a los usuarios a instalar y configurar sus proveedores de servicios.
  
Para crear un servicio de mensajes, un desarrollador escribe un programa de punto de entrada de servicio de mensajes para controlar la configuración de cada proveedor en el servicio y un programa de instalación para hacer lo siguiente:
  
- Instale cada proveedor en el servicio.
    
- Crear entradas del registro y del archivo de inicialización.
    
- Cree entradas en el archivo de configuración de MAPI, MAPISVC. inf.
    
El archivo MAPISVC. inf contiene información relacionada con la configuración de todos los servicios de mensajes y los proveedores de servicios instalados en el equipo. Está organizada en secciones jerárquicas, cada uno de los cuales está vinculado con el siguiente. En la parte superior hay tres secciones que contienen lo siguiente: 
  
- Una lista de los archivos de ayuda del servicio de mensajes.
    
- Una lista de los servicios de mensajes más importantes o predeterminados.
    
- Una lista de todos los servicios del equipo.
    
El siguiente nivel contiene secciones para cada servicio de mensajes y el último nivel contiene secciones para cada proveedor de servicios de un servicio. MAPI requiere que los desarrolladores de proveedores de servicios y servicios de mensajes agreguen determinadas entradas a MAPISVC. inf; los desarrolladores pueden agregar otras entradas según su propio criterio. La mayor parte de la información en MAPISVC. inf termina en uno o más perfiles, una colección de información de configuración para un conjunto de servicios de mensajes preferido por un usuario. Como un equipo puede tener varios usuarios y un único usuario puede tener varios conjuntos de preferencias, pueden existir muchos perfiles en un equipo. Cada perfil describe un conjunto diferente de servicios de mensajes. Tener varios perfiles permite al usuario trabajar, por ejemplo, en casa con un conjunto de servicios de mensajes y en la oficina con un conjunto diferente.
  
Una aplicación cliente que proporciona compatibilidad con la configuración crea perfiles en el momento de la instalación o el inicio de sesión del servicio de mensajes. MAPI proporciona dos aplicaciones cliente de este tipo: un elemento del panel de control y el Asistente para perfiles. El elemento del panel de control es una aplicación de configuración de servicio completo con la que los usuarios pueden crear, eliminar, editar y copiar perfiles, así como realizar modificaciones en las entradas de un perfil. El Asistente para perfiles es una aplicación sencilla diseñada para que la adición de un servicio de mensajes a un perfil sea lo más sencilla posible. El Asistente para perfiles consta de una serie de cuadros de diálogo, denominados páginas de propiedades, que solicitan al usuario el proceso de instalación y configuración de un servicio. Al usuario solo se le solicitan los valores de la configuración más crítica; todas las demás opciones heredan los valores predeterminados. Una vez creado el perfil, los usuarios no pueden realizar cambios. 
  
Mientras que el elemento del panel de control siempre se invoca mediante el panel de control, hay varios escenarios que pueden hacer que se llame al Asistente para perfiles. Las aplicaciones cliente pueden llamar al Asistente para perfiles para crear un perfil predeterminado en el momento del inicio de sesión cuando no se ha creado todavía uno. En lugar de reimplementar el código para agregar un perfil, el elemento del panel de control u otra aplicación cliente puede confiar en la funcionalidad que ya se encuentra en el Asistente para perfiles. Un servicio de mensajes, en su función de punto de entrada, puede llamar al asistente de perfil cuando es necesario agregar el servicio al perfil predeterminado. Los servicios de mensajes que usan el Asistente para perfiles deben escribir una función de punto de entrada adicional y un procedimiento de cuadro de diálogo estándar de Windows. El Asistente para perfiles llama a la función de punto de entrada para recuperar el cuadro de diálogo de configuración del servicio mientras el procedimiento de cuadro de diálogo controla los mensajes que se generan cuando se utiliza este cuadro de diálogo. 
  
Los perfiles se organizan de forma similar al archivo MAPISVC. inf. Los perfiles tienen secciones jerárquicas vinculadas; los proveedores de servicios poseen secciones en el nivel más bajo, servicios de mensajes propios en secciones en el nivel medio y MAPI posee secciones en el nivel superior. Cada sección se identifica con un identificador único conocido como [MAPIUID](mapiuid.md). Las secciones de MAPI contienen información interna de MAPI, como los identificadores de todas las secciones de Perfil de servicio de mensajes y vínculos a cada una de las demás secciones. Cada sección de servicio de mensajes almacena vínculos a sus secciones de proveedor y cada sección de proveedor almacena un vínculo a su sección de servicio. 
  
En la siguiente ilustración se muestra el contenido de dos perfiles típicos. Sam tiene dos perfiles en su equipo, uno para uso doméstico y otro para el uso de Office. El perfil de inicio contiene tres servicios de mensajes. El servicio de mensajes X es un servicio de proveedor único para la administración de la libreta de direcciones. Los servicios de mensajes y y Z tienen tres proveedores: un proveedor de la libreta de direcciones, un proveedor de almacenamiento de mensajes y un proveedor de transporte. El perfil de trabajo de Sam contiene dos servicios de mensajes diferentes, cada uno de los cuales tiene un proveedor de la libreta de direcciones, un proveedor de almacenamiento de mensajes y un proveedor de transporte. 
  
**Ejemplo de perfil**
  
![Ejemplo de perfil] (media/amapi_56.gif "Ejemplo de perfil")
  
En la siguiente ilustración se muestra un perfil que incluye dos servicios de mensajes. El código para instalar y configurar los proveedores de servicios que pertenecen al servicio de mensajes reside en la misma DLL que el código de los proveedores. Este código lee la información del perfil en el momento del inicio de sesión para configurar los proveedores de servicios, y solicita al usuario, si es posible y necesario, que le falte información. Las solicitudes de un cliente para ver o cambiar las opciones de configuración de cualquiera de los proveedores también se controlan mediante este código común.
  
**Instalación y configuración de proveedores de servicio**
  
![Instalación y configuración de proveedores de servicios] (media/amapi_55.gif "Instalación y configuración de proveedores de servicios")
  
## <a name="see-also"></a>Vea también

- [MAPIUID](mapiuid.md)
- [Información general sobre programación de MAPI](mapi-programming-overview.md)

