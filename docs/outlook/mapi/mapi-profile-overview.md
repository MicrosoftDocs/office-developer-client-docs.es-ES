---
title: Introducción a perfiles MAPI
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
# <a name="mapi-profile-overview"></a>Introducción a perfiles MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un perfil es una colección de información sobre los servicios de mensajes y los proveedores de servicios que un usuario de una aplicación cliente desea que esté disponible durante una sesión MAPI determinada. Cada usuario tiene al menos un perfil; muchos usuarios mantienen varios. Por ejemplo, un usuario puede tener un perfil para trabajar con un servicio de almacén de mensajes basado en servidor y otro perfil para trabajar con un servicio de almacén de mensajes en el equipo local. Es posible que un usuario quiera tener acceso a un conjunto de sistemas de mensajería mediante los servicios de transporte adecuados durante parte del día y otro conjunto para el resto del día. Los perfiles proporcionan una forma flexible de seleccionar combinaciones de servicios del sistema de mensajería. 
  
Los perfiles pueden tener nombres de hasta 64 caracteres alfanuméricos de longitud. Los nombres pueden incluir caracteres de énfal, el carácter de subrayado y espacios incrustados, y no pueden incluir espacios iniciales o finales. 
  
Los perfiles se organizan jerárquicamente y se dividen en secciones, con una sección para cada servicio de mensajes y una sección para cada proveedor de servicios de un servicio. Las secciones relacionadas están vinculadas, lo que facilita la navegación por la información. Cada sección contiene una serie de entradas que MAPI o una aplicación cliente usa para la configuración.
  
Las entradas incluidas en un perfil varían del servicio de mensajes al servicio de mensajes. Algunas de las entradas comunes incluyen lo siguiente:
  
- Nombre de cada servicio de mensajes o proveedor de servicios.
    
- Nombre de las DLL que contienen proveedores de servicios y servicios de mensajes.
    
- Nombre de la función de punto de entrada de cada servicio de mensajes.
    
- Una lista de los proveedores de servicios que forma cada servicio de mensajes.
    
Los perfiles se pueden crear en el momento de la instalación, cuando MAPI o un servicio de mensajes se cargan en un equipo o en cualquier momento posterior. MAPI proporciona el Asistente para perfiles para la administración de perfiles. 
  
El Asistente para perfiles es una aplicación que crea nuevos perfiles con una cantidad mínima de trabajo. El asistente usa valores predeterminados para la configuración siempre que sea posible, lo que ahorra tiempo y esfuerzo a los usuarios. Los usuarios escriben valores solo cuando es absolutamente necesario. Para obtener más información, vea [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md). También puede usar la herramienta de personalización Office para crear un perfil nuevo. Para obtener más información, vea la [Herramienta de personalización de Office](https://go.microsoft.com/fwlink/?LinkId=123000).
  
## <a name="see-also"></a>Vea también



[Características y arquitectura MAPI](mapi-features-and-architecture.md)

