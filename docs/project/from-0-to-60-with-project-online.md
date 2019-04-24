---
title: De 0 a 60 con Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Un desarrollador de aplicaciones puede personalizar un sitio de Project online (SharePoint hospedado) mediante el uso de aplicaciones independientes o de complementos de Project. Una gran cantidad de aplicaciones es posible que van desde necesidades de direccionamiento de las personas involucradas en un proyecto a funciones de soporte de PMO, como una de las siguientes:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344411"
---
# <a name="from-0-to-60-with-project-online"></a>De 0 a 60 con Project Online

Un desarrollador de aplicaciones puede personalizar un sitio de Project online (SharePoint hospedado) mediante el uso de aplicaciones independientes o de complementos de Project. Una gran cantidad de aplicaciones es posible que van desde necesidades de direccionamiento de las personas involucradas en un proyecto a funciones de soporte de PMO, como una de las siguientes:
  
- Entrada de datos de tarjetas de registro simplificadas para trabajadores
- Aprobación eficaz de la tarjeta de horas para supervisores
- Supervisión de los permisos (adquisición y estado) necesarios para un proyecto
- Estado/comprobación de estado de los proyectos activos
- Informe de problemas
- Informe de estado de administración de cambios
    
Project online incluye compatibilidad con la API para acomodar los siguientes escenarios:
  
- Para un complemento hospedado de Project (SharePoint):
    
  - Código (JavaScript, HTML, CSS) que se hospeda en SharePoint Online
  - Activos que se descargan en el explorador y se ejecutan con SharePoint Online.  
  - Lógica empresarial en JavaScript   
  - Obtener acceso a los datos que se encuentran en Project online o en SharePoint (pero no se limita a ellos):  
  - Custom fields  
  - Listas
    
- Para un complemento hospedado por el proveedor de Project (SharePoint):
    
  - Código que existe en un sitio externo al sitio de Project online 
  - Un sitio externo, que puede estar (sin limitarse a):  
  - Otro sitio de SharePoint  
  - Aplicación o servicio web creado en cualquier plataforma  
  - El sitio externo contiene lógica empresarial  
  - El explorador se redirige desde Project online al sitio externo con tokens de acceso a Project online.  
  - El sitio externo puede realizar llamadas a SharePoint y Project online
    
- Para un complemento externo/independiente:
    
  - El usuario ejecuta una aplicación en su dispositivo
  - La aplicación autentica y llama a las API de Project online directamente
    

|Tipo de aplicación|Implementación de la API|Entorno de destino|Ejemplos de aplicaciones|
|:-----|:-----|:-----|:-----|
|Proyecto hospedado  <br/> |JSOM (modelo de objetos de Java Script)  <br/> REST  <br/> |Explorador  <br/> |Entrada de tarjeta de registro  <br/> Aprobación de la tarjeta de horas  <br/> Estado de proyecto  <br/> Informe de problemas  <br/> |
|Proveedor de proyecto hospedado  <br/> |Biblioteca cliente de CSOM  <br/> |Sitio web/aplicación de Azure  <br/> Entorno que no es de Windows (lámpara, etc.)  <br/> |Validador de parte de horas externo  <br/> Importador de Project  <br/> |
|Externa/independiente  <br/> |REST  <br/> CSOM  <br/> |REST: cualquier plataforma  <br/> CSOM: cualquier plataforma compatible con .NET  <br/> |Entrada de tarjeta de registro  <br/> Migración de proyectos a un sitio nuevo  <br/> Cambiar el estado de administración.  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>¿Qué se debe hacer para empezar a desarrollar aplicaciones para Project online?

Los elementos comunes necesarios para desarrollar aplicaciones de Project online son una cuenta de Project online y datos de prueba, así como proyectos e información relacionada con el proyecto, que incluyen asignaciones, tareas, recursos y campos personalizados. También se necesita un entorno de desarrollo, pero las características específicas del entorno de desarrollo dependen del tipo de aplicación y de la interfaz de la API necesaria para la aplicación. En las siguientes secciones se describen las necesidades de desarrollo de las tres interfaces API.
  
En la documentación de referencia se describe el modelo de objetos que es común para las tres interfaces, así como una asignación de entidad que muestra las relaciones entre los componentes del modelo de objetos.
  
## <a name="project-hosted-add-in-development-environment"></a>Entorno de desarrollo de complementos hospedados en Project

Un complemento hospedado es un complemento que reside en el servidor y se descarga en un explorador para la ejecución en tiempo de ejecución. Los complementos hospedados pueden usar las interfaces de JSOM o REST y están escritos en JavaScript. Project online proporciona referencias a la biblioteca JSOM para la ejecución en tiempo de ejecución. SuPoniendo que el desarrollo se encuentra en una plataforma Windows, los recursos necesarios siguen estos pasos:
  
- Visual Studio 2015 (preferido) o Visual Studio 2013
    
- Herramientas de desarrollo de Office para Visual Studio
    
- Lenguaje JavaScript
    
Visite https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages para obtener una aplicación de ejemplo. 
  
Puede descargar y ejecutar el ejemplo en unos sencillos pasos:
  
1. Descarga y apertura de la aplicación de ejemplo
    
2. Actualizar SiteURL en la ventana Propiedades
    
   Project online examina tanto el ámbito de aplicación del complemento como los permisos de usuario para controlar el acceso a la información en el host de Project online. Si se deniega explícitamente el acceso en una o ambas configuraciones, Project online deniega el acceso a la información. De lo contrario, se concede el acceso.
    
3. Habilite la [transferencia local](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) en su sitio.  
    
4. Cree el proyecto.
    
5. Ejecute el proyecto.
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Entorno de desarrollo de complementos hospedados por el proveedor de Project

Los complementos hospedados por el proveedor son aplicaciones escritas y que residen en cualquier plataforma Web. Pueden conectar y realizar operaciones de datos con la API de REST (u CSOM para plataformas de Microsoft). Cualquier lenguaje y entorno que admita la interfaz de REST puede usarse para el desarrollo. 
  
Un ejemplo del entorno de desarrollo de Windows para este tipo de aplicación incluye los siguientes elementos:
  
-  Visual Studio 2015 (preferido) o Visual Studio 2013 
    
- Herramientas de desarrollo de Microsoft Office para Visual Studio (incluidas con Visual Studio 2015 Professional y Enterprise Editions)
    
- .NET Framework 4,0 o posterior
    
- [Paquete CSOM de SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para llamadas CSOM) 
    
- Un lenguaje de programación, como C# 
    
Visite https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations para trabajar con scripts de ejemplo. 
  
Puede ejecutar el ejemplo en unos pocos pasos:
  
1. Descarga y apertura de la aplicación de ejemplo
    
2. Actualizar SiteURL en la ventana Propiedades
    
   Project online examina tanto el ámbito de aplicación del complemento como los permisos de usuario para controlar el acceso a la información en el host de Project online. Si se deniega explícitamente el acceso en una o ambas configuraciones, Project online deniega el acceso a la información. De lo contrario, se concede el acceso.
    
3. Habilite la [transferencia local](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) en su sitio. 
    
4. Cree el proyecto.
    
5. Ejecute el proyecto.
    
## <a name="externalstandalone-application-development-environment"></a>Entorno de desarrollo de aplicaciones externas/independientes

Una aplicación independiente puede llamar a Project online mediante el modelo de objetos del lado cliente (CSOM) o REST para comunicarse con Project online para crear, recuperar, actualizar y eliminar información residente en el servidor. Se trata de una aplicación cliente independiente que depende del nivel de acceso de usuario que se va a ejecutar. 
  
Un ejemplo del entorno de desarrollo de Windows para este tipo de aplicación incluye los siguientes elementos:
  
- Visual Studio 2015 (preferido) o Visual Studio 2013 
    
- Herramientas de desarrollo de Microsoft Office para Visual Studio (incluidas con Visual Studio 2015 Professional y Enterprise Editions)
    
- .NET Framework 4,0 o posterior
    
- [Paquete CSOM de SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para llamadas CSOM) 
    
- Un lenguaje de programación, como C# 
    
Visite https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields para obtener una aplicación de ejemplo. 
  
Puede ejecutar el ejemplo en unos pocos pasos:
  
1. Descargar la aplicación de ejemplo
    
2. Realice un par de cambios para obtener acceso al sitio de Project online: el nombre del sitio, la cuenta de usuario y la contraseña.
    
   Asegúrese de que el usuario tiene acceso a todos los proyectos. Project online usa permisos de usuario para regir el acceso a la información en el almacén de datos.
    
3. Agregue el ensamblado de SharePoint a las referencias mediante la consola del administrador de paquetes de Nuget, disponible en el menú herramientas; para ello, escriba lo siguiente en la consola de Nuget: 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. Cree el proyecto.
    
5. Ejecute el proyecto.
    
## <a name="next-steps"></a>Pasos siguientes

Cada aplicación de ejemplo tiene un artículo para explicar los aspectos destacados del trabajo con la API de proyecto individual. Los artículos aparecen en la lista siguiente, junto con algunos artículos que describen las relaciones entre las entidades, la información sobre el sistema de consultas y el acceso a los campos personalizados. 
  
- [Desarrollo de una aplicación de Project online con el modelo de objetos del lado cliente](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [Desarrollar un complemento de Project online con el modelo de objetos de JavaScript (JSOM)](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Obtener acceso a campos personalizados de empresa de Project Online](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>Vea también

Para conocer la documentación y los ejemplos relacionados con Project Online y el desarrollo de aplicaciones con CSOM, consulte el [Portal de desarrollo del proyecto](https://developer.microsoft.com/en-us/project).
    

