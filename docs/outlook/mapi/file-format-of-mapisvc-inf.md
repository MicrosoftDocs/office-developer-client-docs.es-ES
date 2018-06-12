---
title: Formato de archivo de MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b48eda17-83a8-4dc4-85c8-4ca827d13d25
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 47b698eb12577442e5b2d9ea9ecae3e8a13e402b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816807"
---
# <a name="file-format-of-mapisvcinf"></a>Formato de archivo de MapiSvc.inf

**Se aplica a**: Outlook 
  
El archivo MapiSvc.inf actúa como la base de datos central para la información de configuración de servicio de mensajes MAPI. MapiSvc.inf contiene información acerca de cada uno de los servicios de mensaje instalados en la estación de trabajo, la información acerca de los proveedores de servicios que pertenecen a cada servicio de mensajes y la información sobre el subsistema MAPI. MapiSvc.inf es el origen principal de información de perfiles. Es decir, cuando se está generando un perfil nuevo o uno existente modificado, información relevante para cada servicio de mensajes o proveedor de servicios se copió desde MapiSvc.inf. 
  
MapiSvc.inf se divide en las secciones jerárquicas vinculadas:
  
1. Sección que contiene información que se aplica a todos los perfiles. Esta sección consta de tres partes:
    
   - Sección **[services]** , que proporciona vínculos a cada uno de los mensajes subsiguientes secciones de servicio. 
    
   - Sección **[Help File Mappings]** , que contiene información acerca de. Proporcionado por los servicios de mensajes de los archivos HLP. 
    
   - Sección **[Services predeterminado]** , servicios de mensajes que componen una instalación predeterminada de la lista. 
    
2. Sección que contiene información que se aplica a los servicios de mensajes individuales. Las entradas de estas secciones proporcionan vínculos a las secciones de proveedor de servicios posteriores.
    
3. Sección que contiene información que se aplica a los proveedores de servicio individuales en un servicio de mensajes.
    
En la siguiente ilustración se muestra la organización de un archivo MapiSvc.inf típica. Hay tres servicios de mensaje: AB, MsgService y MS. El nombre en el lado derecho del signo igual para cada servicio de mensajes es el nombre para mostrar del servicio. Cada servicio de mensajes tiene su propia sección en otro lugar en el archivo que está vinculado a una o varias secciones de proveedor de servicio. Hay una sección de proveedor de servicio para cada proveedor de servicios que pertenece al servicio de mensajes. Los servicios de mensaje AB y MS son servicios de proveedor único mientras que pertenecen tres proveedores de servicios para el servicio MsgService.
  
**Organización del archivo MapiSvc.inf**
  
![Organización del archivo MapiSvc.inf] (media/amapi_30.gif "Organización del archivo MapiSvc.inf")
  
MAPI proporciona una versión de la estructura del archivo MapiSvc.inf que contiene las entradas para el subsistema MAPI. Cada implementador del servicio mensaje agrega las entradas que son adecuadas para su servicio y los proveedores de servicios que pertenecen a su servicio. Algunas de las entradas son necesarios, mientras que otros son opcionales. Por ejemplo, MAPI requiere que se especifican el nombre y la ruta de acceso de cada uno de los proveedores de servicios en el servicio de mensajes. Sin esta información, no se puede cargados.
  
Puede agregar información requerida y opcional en la sección para su servicio de mensajes o a las secciones de proveedor de servicio. Donde colocar la información que describe el servicio de mensajes depende el número de proveedores de servicios en el servicio. Debido a que esta información se aplica a cada proveedor de servicios en el servicio, se debe hacer accesible para todos los proveedores. Almacenarlo en la sección servicio de mensaje, la opción preferida, o en todas las secciones de proveedor de servicio. Almacenar información una vez evitar la replicación innecesaria y la necesidad de mantener varias copias sincronizadas.
  
Si el mensaje es un servicio de proveedor único, almacenar toda la información del servicio de mensajes en la sección del proveedor de servicios en lugar de en la sección para el servicio. Obtener acceso a la sección del proveedor de servicio es más rápido y más directa que obtener acceso a la sección servicio de mensaje. 
  
Almacenar datos de configuración de pública sólo en el archivo MapiSvc.inf. La información privada o requiere protección adicional, como las contraseñas u otras credenciales, no debe incluirse en este archivo. Participar en su lugar, ya sea no para almacenar la información de este tipo en absoluto o mantener en el perfil como propiedades seguras. Propiedades seguras tienen las características de protección integrada, como el cifrado.
  

