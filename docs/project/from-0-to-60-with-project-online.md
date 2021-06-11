---
title: De 0 a 60 con Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Un desarrollador de aplicaciones puede personalizar un Project Online web (SharePoint hospedado) mediante aplicaciones independientes o Project complementos. Es posible una gran cantidad de aplicaciones que van desde satisfacer las necesidades de los participantes en un proyecto hasta las funciones de soporte técnico de PMO, como cualquiera de las siguientes:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344411"
---
# <a name="from-0-to-60-with-project-online"></a>De 0 a 60 con Project Online

Un desarrollador de aplicaciones puede personalizar un Project Online web (SharePoint hospedado) mediante aplicaciones independientes o Project complementos. Es posible una gran cantidad de aplicaciones que van desde satisfacer las necesidades de los participantes en un proyecto hasta las funciones de soporte técnico de PMO, como cualquiera de las siguientes:
  
- Entrada de datos de tarjeta de tiempo optimizada para los trabajadores
- Aprobación eficiente de tarjetas de tiempo para supervisores
- Supervisión de permisos (adquisición y estado) necesarios para un proyecto
- Comprobación de estado/estado de los proyectos activos
- Informe de problemas
- Informe de estado de administración de cambios
    
Project Online incluye compatibilidad con api para dar cabida a los siguientes escenarios:
  
- Para un complemento Project (SharePoint) hospedado:
    
  - Código (JavaScript, HTML, CSS) hospedado en SharePoint Online
  - Activos que se descargan en el explorador y se ejecutan en SharePoint Online.  
  - Lógica empresarial que está en JavaScript   
  - Acceder a los datos que se almacenan en Project Online o SharePoint como (pero no se limita a):  
  - Campos personalizados  
  - Listas
    
- Para un complemento Project (SharePoint) hospedado por el proveedor:
    
  - Código que existe en un sitio externo al sitio Project Online sitio 
  - Un sitio externo, que puede ser (pero no está limitado a):  
  - Otro SharePoint web  
  - Aplicación web/servicio integrado en cualquier plataforma  
  - El sitio externo contiene lógica empresarial  
  - El explorador se redirige desde Project Online al sitio externo con tokens de acceso a Project Online  
  - El sitio externo puede realizar llamadas a SharePoint y Project Online
    
- Para un complemento externo/independiente:
    
  - El usuario ejecuta una aplicación en su dispositivo
  - La aplicación autentica y llama a Project Online API directamente
    

|Tipo de aplicación|Implementación de API|Entorno de destino|Ejemplos de aplicación|
|:-----|:-----|:-----|:-----|
|Project hospedado  <br/> |JSOM (Java de objetos script)  <br/> REST  <br/> |Explorador  <br/> |Entrada de tarjeta de tiempo  <br/> Aprobación de tarjetas de tiempo  <br/> Estado de proyecto  <br/> Informe de problemas  <br/> |
|Project Proveedor hospedado  <br/> |Biblioteca de cliente CSOM  <br/> |Sitio web/aplicación de Azure  <br/> Entorno no Windows (LAMP, etc.)  <br/> |Validador de partes de horas externo  <br/> Project Importador  <br/> |
|Externo/Independiente  <br/> |REST  <br/> CSOM  <br/> |REST: cualquier plataforma  <br/> CSOM: cualquier plataforma compatible con .NET  <br/> |Entrada de tarjeta de tiempo  <br/> Migración de proyectos a un nuevo sitio  <br/> Cambiar estado de administración.  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>¿Qué se necesita para empezar a desarrollar aplicaciones para Project Online?

Los elementos comunes necesarios para desarrollar aplicaciones Project Online son una cuenta de Project Online y datos de prueba, proyectos e información relacionada con proyectos que incluyen asignaciones, tareas, recursos y campos personalizados. También se necesita un entorno de desarrollo, pero los detalles del entorno de desarrollo dependen del tipo de aplicación y de la interfaz api necesaria para la aplicación. En las siguientes secciones se describen las necesidades de desarrollo de las tres interfaces de API.
  
La documentación de referencia describe el modelo de objetos que es común para las tres interfaces, así como un mapa de entidades que muestra las relaciones entre los componentes del modelo de objetos.
  
## <a name="project-hosted-add-in-development-environment"></a>Project de desarrollo de complementos hospedados

Un complemento hospedado es un complemento que reside en el servidor y se descarga en un explorador para la ejecución en tiempo de ejecución. Los complementos hospedados pueden usar las interfaces JSOM o REST y se escriben en JavaScript. Project Online proporciona referencias a la biblioteca JSOM para la ejecución en tiempo de ejecución. Suponiendo que el desarrollo se encuentra en Windows plataforma, los recursos necesarios son los siguientes:
  
- Visual Studio 2015 (preferido) o Visual Studio 2013
    
- Office de desarrollo para Visual Studio
    
- Lenguaje JavaScript
    
Visite https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages una aplicación de ejemplo. 
  
Puede descargar y ejecutar el ejemplo en unos sencillos pasos:
  
1. Descargar y abrir la aplicación de ejemplo
    
2. Actualizar SiteURL en la ventana Propiedades
    
   Project Online examina el ámbito de aplicación del complemento y los permisos de usuario para administrar el acceso a la información en el host Project Online usuario. Si el acceso se deniega explícitamente en cualquiera de las dos opciones de configuración, Project Online deniega el acceso a la información. De lo contrario, se concede acceso.
    
3. Habilitar [la instalación local](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) en el sitio.  
    
4. Cree el proyecto.
    
5. Ejecute el proyecto.
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Project de desarrollo de complementos hospedados por el proveedor

Los complementos hospedados por el proveedor son aplicaciones escritas y que residen en cualquier plataforma web. Pueden conectarse y realizar operaciones de datos mediante la API de REST (o CSOM para plataformas Microsoft). Cualquier idioma y entorno que admita la interfaz REST se puede usar para el desarrollo. 
  
Un ejemplo del entorno Windows desarrollo de este tipo de aplicación incluye los siguientes elementos:
  
-  Visual Studio 2015 (preferido) o Visual Studio 2013 
    
- Microsoft Office Herramientas de desarrollo para Visual Studio (suministradas con Visual Studio ediciones Professional y Enterprise 2015)
    
- .NET Framework 4.0 o posterior
    
- [Paquete CSOM de SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para llamadas CSOM) 
    
- Un lenguaje de programación, como C # 
    
Visita https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations para ver scripts de ejemplo de trabajo. 
  
Puede ejecutar el ejemplo en unos pocos pasos:
  
1. Descargar y abrir la aplicación de ejemplo
    
2. Actualizar SiteURL en la ventana Propiedades
    
   Project Online examina el ámbito de aplicación del complemento y los permisos de usuario para administrar el acceso a la información en el host Project Online usuario. Si el acceso se deniega explícitamente en cualquiera de las dos opciones de configuración, Project Online deniega el acceso a la información. De lo contrario, se concede acceso.
    
3. Habilitar [la instalación local](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) en el sitio. 
    
4. Cree el proyecto.
    
5. Ejecute el proyecto.
    
## <a name="externalstandalone-application-development-environment"></a>Entorno de desarrollo de aplicaciones externo/independiente

Una aplicación independiente puede llamar a Project Online mediante el Modelo de objetos del lado cliente (CSOM) o REST para comunicarse con Project Online para crear, recuperar, actualizar y eliminar información que reside en el servidor. Se trata de una aplicación cliente independiente que depende del nivel de acceso de usuario que se va a ejecutar. 
  
Un ejemplo del entorno Windows desarrollo de este tipo de aplicación incluye los siguientes elementos:
  
- Visual Studio 2015 (preferido) o Visual Studio 2013 
    
- Microsoft Office Herramientas de desarrollo para Visual Studio (suministradas con Visual Studio ediciones Professional y Enterprise 2015)
    
- .NET Framework 4.0 o posterior
    
- [Paquete CSOM de SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para llamadas CSOM) 
    
- Un lenguaje de programación, como C # 
    
Visite https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields una aplicación de ejemplo. 
  
Puede ejecutar el ejemplo en unos pocos pasos:
  
1. Descargar la aplicación de ejemplo
    
2. Realice un par de cambios para obtener acceso a Project Online sitio: el nombre del sitio, la cuenta de usuario y la contraseña.
    
   Asegúrese de que el usuario tiene acceso a todos los proyectos. Project Online los permisos de usuario para administrar el acceso a la información en el almacén de datos.
    
3. Agregue el ensamblado SharePoint a las referencias mediante la Consola de nuget Administrador de paquetes, disponible en el menú Herramientas escribiendo lo siguiente en la consola de Nuget: 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. Cree el proyecto.
    
5. Ejecute el proyecto.
    
## <a name="next-steps"></a>Pasos siguientes

Cada aplicación de ejemplo tiene un artículo para explicar los aspectos más destacados de trabajar con la API Project individual. Los artículos aparecen en la siguiente lista, junto con algunos artículos que describen las relaciones de entidad, la información sobre el sistema de consultas y el acceso a campos personalizados. 
  
- [Desarrollo de una aplicación Project Online con el modelo de objetos del lado cliente](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [Desarrollar un complemento Project Online con el modelo de objetos de JavaScript (JSOM)](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Obtener acceso a campos personalizados de empresa de Project Online](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>Vea también

Para conocer la documentación y los ejemplos relacionados con Project Online y el desarrollo de aplicaciones con CSOM, consulte el [Portal de desarrollo del proyecto](https://developer.microsoft.com/en-us/project).
    

