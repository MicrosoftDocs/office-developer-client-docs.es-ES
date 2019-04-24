---
title: Formato de archivo de MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: b48eda17-83a8-4dc4-85c8-4ca827d13d25
description: 'Última modificación: 23 de julio de 2011'
localization_priority: Priority
ms.openlocfilehash: 934bb491c0521b1d76d5400aac4728fbd34ba625
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334877"
---
# <a name="file-format-of-mapisvcinf"></a>Formato de archivo de MapiSvc.inf

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El archivo MapiSvc.inf actúa como la base de datos central para la información de configuración del servicio de mensajes MAPI. MapiSvc.inf contiene información sobre cada uno de los servicios de mensajes instalados en la estación de trabajo, información sobre los proveedores de servicios que pertenecen a cada servicio de mensajes e información sobre el subsistema MAPI. MapiSvc.inf es la fuente principal de información de los perfiles. Es decir, cuando se está creando un perfil nuevo o se está modificando un perfil existente, la información relevante para cada servicio de mensajes o proveedor de servicios se copia de MapiSvc.inf. 
  
MapiSvc.inf está dividido en secciones jerárquicas vinculadas:
  
1. Sección que contiene información que se aplica a todos los perfiles. Esta sección cuenta con tres partes:
    
   - La sección **[Servicios]** proporciona vínculos a cada una de las secciones de servicio de mensajes siguiente. 
    
   - La sección **[Asignaciones de archivos de ayuda]** contiene información sobre los archivos .HLP proporcionados por los servicios del mensajes. 
    
   - La sección **[Servicios predeterminados]** lista los servicios de mensajes que forman una instalación predeterminada. 
    
2. Sección que contiene información que se aplica a servicios de mensajes individuales. Las entradas de estas secciones proporcionan vínculos a secciones del proveedor de servicios siguientes.
    
3. Sección que contiene información que se aplica a los proveedores de servicios individuales en un servicio de mensajes.
    
La ilustración siguiente muestra la organización de un archivo MapiSvc.inf típico. Hay tres servicios de mensajes: AB, MsgService y MS. El nombre en el lado derecho del signo igual de cada servicio de mensajes es el nombre para mostrar del servicio. Cada servicio de mensajes tiene su propia sección en otra ubicación del archivo que se vincula a una o varias secciones del proveedor de servicios. Hay una sección del proveedor de servicios para cada proveedor que pertenece al servicio de mensajes. Los servicios de mensaje AB y MS son servicios de proveedor único mientras que tres proveedores de servicios pertenecen al servicio MsgService.
  
**Organización de archivos MapiSvc.inf**
  
![Organización de archivos MapiSvc.inf](media/amapi_30.gif "Organización de archivos MapiSvc.inf")
  
MAPI proporciona una versión de la estructura del archivo MapiSvc.inf que contiene las entradas de subsistema MAPI. El implementador de servicios de cada mensaje agrega entradas adecuadas para el servicio y para los proveedores de servicios que pertenecen al mismo. Algunas entradas son necesarias, otras son opcionales. Por ejemplo, MAPI requiere que especifique el nombre y la ruta de cada uno de los proveedores de servicios en el servicio de mensajes. Sin esta información, no se puede cargarlos.
  
Puede agregar información necesaria y opcional en la sección del servicio de mensajes o en las secciones del proveedor de servicios. El lugar donde coloque la información que describe su servicio de mensajes depende de la cantidad de proveedores de servicios en el servicio. Como esta información se aplica a cada proveedor del servicio, es necesario que sea accesible para todos los proveedores. Almacénela en la sección de servicio de mensajes, la opción recomendada, o en todas las secciones del proveedor de servicios. Almacene la información una vez para evitar la replicación innecesaria ni necesidad de mantener varias copias sincronizadas.
  
Si el servicio de mensajes es un servicio de proveedor único, almacene toda la información del servicio de mensajes en la sección del proveedor de servicios en lugar de la sección del servicio. Acceder a la sección del proveedor de servicios es más rápido y directo que acceder a la sección de servicio de mensajes. 
  
Almacene únicamente los datos de configuración públicos en el archivo MapiSvc.inf. Información privada o que requiere protección adicional, como contraseñas u otras credenciales, no debe incluirse en el archivo. En su lugar, opte por no almacenar del todo información de este tipo o guárdela en el perfil como propiedades seguras. Propiedades seguras tienen características de protección integradas como cifrado.
  

