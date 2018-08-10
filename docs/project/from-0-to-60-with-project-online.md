---
title: De 0 a 60 con Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Un desarrollador de aplicaciones puede personalizar un sitio de Project Online (SharePoint hospedado), uso de aplicaciones independientes o complementos en el proyecto. Una gran cantidad de aplicaciones es posible que van desde hacer frente a las necesidades de los implicados en un proyecto a las funciones de soporte PMO, por ejemplo, cualquiera de las siguientes opciones:'
ms.openlocfilehash: c50ed12e9f1127f6313a02db4d84a151778e17b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821302"
---
# <a name="from-0-to-60-with-project-online"></a>De 0 a 60 con Project Online

Un desarrollador de aplicaciones puede personalizar un sitio de Project Online (SharePoint hospedado), uso de aplicaciones independientes o complementos en el proyecto. Una gran cantidad de aplicaciones es posible que van desde hacer frente a las necesidades de los implicados en un proyecto a las funciones de soporte PMO, por ejemplo, cualquiera de las siguientes opciones:
  
- Entrada de datos de tarjetas de horas trabajadas simplificadas para los trabajadores
- Aprobación de tarjetas de horas trabajadas eficaz para supervisores
- Supervisión de los permisos necesarios para un proyecto (compras y estado)
- Comprobación de estado y mantenimiento de los proyectos activos
- Informe de problemas
- Cambiar el informe de estado de administración
    
Project Online incluye compatibilidad con la API para dar cabida a los siguientes escenarios:
  
- Para un complemento de Project (SharePoint) hospedado:
    
  - Código (JavaScript, HTML, CSS) que se hospeda en SharePoint Online
  - Activos que se descarga en el explorador y se ejecutan en SharePoint Online.  
  - Lógica de negocios que se encuentra en JavaScript   
  - Obtenga acceso a datos es en/almacena en Project Online o SharePoint como (pero no está limitado a):  
  - Campos personalizados  
  - Listas
    
- Para un proyecto (SharePoint) hospedada en proveedor complemento:
    
  - Código que se encuentra en un sitio externo para el sitio de Project Online 
  - Un sitio externo, que puede ser (pero no está limitado a):  
  - Otro sitio de SharePoint  
  - Servicio de la aplicaciones Web creadas en cualquier plataforma  
  - El sitio externo contiene lógica empresarial  
  - El explorador se redirige desde Project Online a sitios externos con tokens de acceso a Project Online  
  - El sitio externo puede realizar llamadas a SharePoint y Project Online
    
- Para un complemento en independiente o externo:
    
  - Usuario ejecuta una aplicación en su dispositivo
  - Aplicación autentica y llama directamente a las API de proyecto en línea
    

|Tipo de aplicación|Implementación de la API|Entorno de destino|Ejemplos de aplicaciones|
|:-----|:-----|:-----|:-----|
|Proyecto hospedado  <br/> |JSOM (modelo de objetos de secuencia de comandos de Java)  <br/> REST  <br/> |Explorador  <br/> |Entrada de tarjetas de horas trabajadas  <br/> Aprobación de tarjetas de horas trabajadas  <br/> Estado de proyecto  <br/> Informe de problemas  <br/> |
|Hospedada de proveedor de proyecto  <br/> |Biblioteca de cliente de CSOM  <br/> |Sitio Web de Azure/aplicación  <br/> Entorno de que no son de Windows (LAMP, etcetera).  <br/> |Validador de partes de horas externos  <br/> Importador de Project  <br/> |
|Independiente o externo  <br/> |REST  <br/> CSOM  <br/> |REST - cualquier plataforma  <br/> CSOM - cualquier plataforma .NET compatibles  <br/> |Entrada de tarjetas de horas trabajadas  <br/> Migración de proyectos a un sitio nuevo  <br/> Cambiar el estado de la administración.  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>¿Qué necesita para comenzar a desarrollar aplicaciones para Project Online?

Los elementos comunes necesarios para el desarrollo de aplicaciones de Project Online son una cuenta de Project Online y probar datos--proyectos e información relacionados con los proyectos que incluyen las asignaciones, tareas, recursos y campos personalizados. Un entorno de desarrollo se necesita también, pero elementos específicos del entorno de desarrollo dependen del tipo de aplicación y la interfaz de API necesarios para la aplicación. En las secciones siguientes se describen las necesidades de desarrollo de las tres interfaces API.
  
La documentación de referencia describe el modelo de objetos que es común para las tres interfaces, así como una asignación de entidad que se muestra las relaciones entre los componentes del modelo de objeto.
  
## <a name="project-hosted-add-in-development-environment"></a>Entorno de desarrollo de complementos de proyecto hospedado

Un complemento hospedado es un complemento que reside en el servidor y se descarga en un explorador para el tiempo de ejecución. Complementos hospedados pueden usar las interfaces JSOM o REST y se escriben en JavaScript. Project Online proporciona referencias a la biblioteca JSOM de tiempo de ejecución. Desarrollo se supone que está en una plataforma de Windows, el seguimiento de los recursos necesarios:
  
- Visual Studio de 2015 (preferido) o Visual Studio 2013
    
- Herramientas de desarrollo de Office para Visual Studio
    
- Idioma de JavaScript
    
Visite https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages para una aplicación de ejemplo. 
  
Puede descargar y ejecutar el ejemplo en unos cuantos pasos sencillos:
  
1. Descargue y abra la aplicación de ejemplo
    
2. Actualice SiteURL en la ventana Propiedades
    
   Project Online examina del ámbito de aplicación del complemento y los permisos de usuario para controlar el acceso a la información en el host de Project Online. Si el acceso se deniega explícitamente en la configuración de uno o ambos, Project Online deniega el acceso a la información. De lo contrario, se concede el acceso.
    
3. Habilitar sideloading en su sitio. Vea el artículo [Configurar Project Online para el desarrollo de la aplicación ](http://nearbaseline.com/2013/12/configuring-project-online-for-app-development/.aspx)para obtener más información. 
    
4. Genere el proyecto.
    
5. Ejecutar el proyecto.
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Entorno hospedado por el proveedor de desarrollo de complementos del proyecto

Complementos de proveedor hospedado son aplicaciones escritas y que residen en cualquier plataforma web. Puede conectarse y realizar operaciones de datos con el resto (o CSOM para plataformas de Microsoft) API. Para el desarrollo se pueden usar cualquier lenguaje y el entorno que admite la interfaz REST. 
  
Un ejemplo del entorno de desarrollo de Windows para este tipo de aplicación incluye los siguientes elementos:
  
-  Visual Studio de 2015 (preferido) o Visual Studio 2013 
    
- Herramientas de desarrollo de Microsoft Office para Visual Studio (suministrado con las ediciones de Visual Studio 2015 Professional y Enterprise)
    
- .NET framework 4.0 o posterior
    
- [Paquete de CSOM de SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM/.aspx) (para las llamadas CSOM) 
    
- Un lenguaje de programación, como C# 
    
Visite https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations para trabajar scripts de ejemplo. 
  
Puede ejecutar el ejemplo en unos cuantos pasos:
  
1. Descargue y abra la aplicación de ejemplo
    
2. Actualice SiteURL en la ventana Propiedades
    
   Project Online examina del ámbito de aplicación del complemento y los permisos de usuario para controlar el acceso a la información en el host de Project Online. Si el acceso se deniega explícitamente en la configuración de uno o ambos, Project Online deniega el acceso a la información. De lo contrario, se concede el acceso.
    
3. Habilitar sideloading en su sitio. Vea el artículo [Configurar Project Online para el desarrollo de la aplicación ](http://nearbaseline.com/2013/12/configuring-project-online-for-app-development/.aspx)para obtener más información. 
    
4. Genere el proyecto.
    
5. Ejecutar el proyecto.
    
## <a name="externalstandalone-application-development-environment"></a>Entorno de desarrollo de la aplicación externa o independiente

Una aplicación independiente puede llamar a Project Online mediante el modelo de objetos de lado cliente (COM) o REST para comunicarse con Project Online para crear, recuperar, actualizar y eliminar la información que reside en el servidor. Esto es una aplicación de cliente independiente que depende del nivel de acceso de usuario para que se ejecute. 
  
Un ejemplo del entorno de desarrollo de Windows para este tipo de aplicación incluye los siguientes elementos:
  
- Visual Studio de 2015 (preferido) o Visual Studio 2013 
    
- Herramientas de desarrollo de Microsoft Office para Visual Studio (suministrado con las ediciones de Visual Studio 2015 Professional y Enterprise)
    
- .NET framework 4.0 o posterior
    
- [Paquete de CSOM de SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM/.aspx) (para las llamadas CSOM) 
    
- Un lenguaje de programación, como C# 
    
Visite https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields para una aplicación de ejemplo. 
  
Puede ejecutar el ejemplo en unos cuantos pasos:
  
1. Descargar la aplicación de ejemplo
    
2. Hacer un par de cambios para tener acceso a su sitio Project Online: el nombre del sitio, la cuenta de usuario y la contraseña.
    
   Asegúrese de que el usuario tiene acceso a todos los proyectos. Project Online usa los permisos de usuario para controlar el acceso a la información en el almacén de datos.
    
3. Agregue el ensamblado de SharePoint a las referencias del uso de la consola de administrador de paquetes de Nuget, disponible en el menú Herramientas escribiendo lo siguiente en la consola de Nuget: 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. Genere el proyecto.
    
5. Ejecutar el proyecto.
    
## <a name="next-steps"></a>Pasos siguientes

Cada aplicación de ejemplo tiene un artículo para explicar los aspectos de trabajar con la API de proyecto individuales. Los artículos aparecen en la lista siguiente, junto con algunos artículos que describen las relaciones entre entidades, información sobre el sistema de consulta y obtener acceso a campos personalizados. 
  
- [Desarrollar una aplicación de Project Online con el modelo de objetos de cliente](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [Desarrollo de un complemento Project Online mediante el modelo de objetos de JavaScript (JSOM)](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Obtener acceso a campos personalizados de empresa de Project Online](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>Vea también

Para obtener documentación y ejemplos relacionados con Project Online y el desarrollo de aplicaciones con CSOM, vea el [Portal del proyecto de desarrollo](http://dev.office.com/project.aspx).
    

