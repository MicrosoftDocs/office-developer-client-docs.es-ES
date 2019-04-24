---
title: Introducción al perfil MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e196800b717ce2528da4b9871bad7425f3a2c326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328171"
---
# <a name="mapi-profile-overview"></a>Introducción al perfil MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un perfil es una colección de información sobre los servicios de mensajes y los proveedores de servicios que un usuario de una aplicación cliente desea que esté disponible durante una sesión MAPI en particular. Cada usuario tiene al menos un perfil; muchos usuarios conservan varios. Por ejemplo, un usuario puede tener un perfil para trabajar con un servicio de almacén de mensajes basado en servidor y otro perfil para trabajar con un servicio de almacén de mensajes en el equipo local. Es posible que un usuario desee tener acceso a un conjunto de sistemas de mensajería con los servicios de transporte adecuados para una parte del día y otro para el resto del día. Los perfiles proporcionan una forma flexible de seleccionar combinaciones de los servicios del sistema de mensajería. 
  
Los perfiles pueden tener nombres de hasta 64 caracteres alfanuméricos en longitud. Los nombres pueden incluir caracteres de énfasis, el subrayado y los espacios incrustados, y no pueden incluir espacios iniciales o finales. 
  
Los perfiles se organizan jerárquicamente y se dividen en secciones, con una sección para cada servicio de mensajes y una sección para cada proveedor de servicios en un servicio. Las secciones relacionadas están vinculadas, lo que facilita el desplazamiento por la información. Cada sección contiene una serie de entradas que MAPI o una aplicación cliente usan para la configuración.
  
Las entradas incluidas en un perfil varían del servicio de mensajes al servicio de mensajes. Entre las entradas comunes se incluyen las siguientes:
  
- El nombre de cada servicio de mensajes o proveedor de servicios.
    
- El nombre de los archivos DLL que contienen proveedores de servicios y servicios de mensajes.
    
- El nombre de la función de punto de entrada de cada servicio de mensajería.
    
- Una lista de los proveedores de servicios que componen cada servicio de mensajes.
    
Los perfiles se pueden crear en el momento de la instalación, cuando MAPI o un servicio de mensajes se carga en un equipo o en un momento posterior. MAPI proporciona el Asistente para perfiles para la administración de perfiles. 
  
El Asistente para perfiles es una aplicación que crea nuevos perfiles con una cantidad mínima de trabajo. El asistente usa los valores predeterminados para la configuración siempre que sea posible, lo que ahorra tiempo y esfuerzo a los usuarios. Los usuarios escriben valores solo cuando son absolutamente necesarios. Para obtener más información, consulte [creación de un perfil con el Asistente para perfiles](creating-a-profile-by-using-the-profile-wizard.md). También puede usar la herramienta de personalización de Office para crear un nuevo perfil. Para obtener más información, vea la [Herramienta de personalización de Office](https://go.microsoft.com/fwlink/?LinkId=123000).
  
## <a name="see-also"></a>Vea también



[Arquitectura y características de MAPI](mapi-features-and-architecture.md)

