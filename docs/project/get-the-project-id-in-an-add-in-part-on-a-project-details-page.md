---
title: Obtener el identificador del proyecto en una parte del complemento en una página de detalles de Project
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Los elementos de complemento se hospedan en elementos iframe que están completamente aislados de la página de hospedaje. Para obtener información sobre el proyecto actual desde un elemento de complemento en la página detalles del proyecto (PDP), puede usar el método window.postMessage, un agente de escucha de eventos y un controlador de eventos que analiza el identificador de proyecto del mensaje.
ms.openlocfilehash: ffaf9cb7dac783a754b2d56b5ece4d5a7a0319be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322599"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>Obtener el identificador del proyecto en una parte del complemento en una página de detalles de Project

Los elementos de complemento se hospedan en elementos **iframe** que están completamente aislados de la página de hospedaje. Para obtener información sobre el proyecto actual desde un elemento de complemento en la página detalles del proyecto (PDP), puede usar el método **window.postMessage,** un agente de escucha de eventos y un controlador de eventos que analiza el identificador de proyecto del mensaje. 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>Requisitos previos para crear un elemento de complemento hospedado en SharePoint que obtiene el identificador del proyecto
<a name="Prereqs"> </a>

Para usar el ejemplo de código de este artículo, necesitará una de las siguientes opciones:
  
- SharePoint 2013 y Project Server 2013, configurados para el aislamiento de complementos. Si está desarrollando de forma remota, el servidor debe admitir la instalación local de complementos o debe instalar el complemento en un sitio para desarrolladores.
  
- SharePoint Online y Project Online
    
    - Visual Studio 2013, Visual Studio 2012 con Office Developer Tools para Visual Studio 2013 o Napa
        
    - Permisos suficientes para el usuario que ha iniciado la sesión:
        
        - Permisos de administrador local en el equipo de desarrollo.
            
        - Acceso de lectura a al menos un proyecto.
            
        - Permiso para editar páginas en el sitio de Project Web App.
            
        - Debe iniciar sesión como un usuario distinto de la cuenta del sistema. La cuenta del sistema no tiene permiso para instalar un complemento.
    
Vea los requisitos previos para crear un complemento para [Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) para obtener más información acerca de los complementos para Project. Vea Configurar un entorno de desarrollo local para complementos de [SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) para obtener instrucciones sobre la configuración local (incluido cómo deshabilitar la comprobación de bucle recuperación, si es necesario). Si está desarrollando de forma remota, vea Desarrollar aplicaciones [para SharePoint en un sistema remoto.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins)
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>Crear el complemento hospedado en SharePoint y el elemento web cliente
<a name="CreateApp"> </a>

1. Abra Visual Studio y elija **Archivo**  >  **nuevo**  >  **proyecto.**
    
2. En el cuadro de diálogo **Nuevo proyecto**, elija **.NET Framework 4.5** en la lista desplegable situada en la parte superior del cuadro de diálogo. 
    
3. En la **lista plantillas,** elija **Visual C#**  >  **Office/SharePoint**  >  **Add-ins**  >  **Add-ins for SharePoint 2013**.
    
4. Asigne al complemento el nombre GetProjectIdAddinPart y, a continuación, elija el **botón** Aceptar. 
    
5. En el cuadro de diálogo Nuevo complemento para **SharePoint,** escriba la dirección URL del sitio de PWA que desea usar para la depuración (por ejemplo:  _https://contoso.com/sites/pwasite/_ ).
    
6. Elija la **opción hospedada en SharePoint** para hospedar el complemento y, a continuación, elija el **botón** Finalizar. 
    
7. En **el Explorador de** soluciones, abra el menú contextual del proyecto GetProjectIdAddinPart y, a continuación, elija **Agregar**  >  **nuevo elemento**.
    
8. En el **cuadro de diálogo Agregar** nuevo elemento, elija Elemento web cliente (Web de **host),** asigne al elemento web el nombre GetProjectId y, a continuación, elija el **botón** Agregar. 
    
9. En el **cuadro de diálogo Crear** elemento web cliente, elija la opción Crear una nueva página de elementos web cliente y, **a** continuación, elija el **botón** Finalizar. 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>Obtener el identificador de proyecto en el elemento de complemento
<a name="GetProjectId"> </a>

El elemento de complemento GetProjectId define su código personalizado en la página GetProjectId.aspx del elemento web cliente. La lógica que recibe y controla el  mensaje se define en el elemento head  de la página y los controles de página se definen en el elemento de cuerpo de la página. 
  
1. Abra la página del elemento web GetProjectId.aspx (en la **carpeta** Pages). 
    
2. En el **elemento head** de la página, reemplace el código entre las etiquetas **de script** por el código siguiente. 
    
   ```js
        'use strict';
        // Define global variables.
        var hostUrl = '';
        var projectUid;
        // Set the style of the client web part page to be consistent with the host web.
                (function () {
                    var hostUrl = '';
                    var link = document.createElement('link');
                    link.setAttribute('rel', 'stylesheet');
                    if (document.URL.indexOf('?') != -1) {
                        var params = document.URL.split('?')[1].split('&');
                        for (var i = 0; i < params.length; i++) {
                            var p = decodeURIComponent(params[i]);
                            if (/^SPHostUrl=/i.test(p)) {
                                hostUrl = p.split('=')[1];
                                link.setAttribute('href', hostUrl + '/_layouts/15/defaultcss.ashx');
                                break;
                            }
                        }
                    }
                    if (hostUrl == '') {
                        link.setAttribute('href', '/_layouts/15/1033/styles/themable/corev15.css');
                    }
                    document.head.appendChild(link);
                })();
        // Get the message.
        function getProjectUid() {
            window.parent.postMessage('getprojectuid', hostUrl);
        }
        getProjectUid();
        // Add an event listener and register the event handler.
        // If the IE browser version is earlier than 9, use the attachEvent method.
        if (window.addEventListener) {
            window.addEventListener("message", onMessage, false);
        }
        else {
            if (window.attachEvent) {
                window.attachEvent("onmessage", onMessage);
            }
        }
        // Get the project ID from the message.
        function onMessage(event) {
            // Verify the message origin.
            if (hostUrl.indexOf(event.origin) != 0) return;
            // The expected message format is "<PDPProjectUid>00000000-0000-0000-0000-000000000000</PDPProjectUid>,"
            // so validate by using the length and the start and end tags.
            var length = event.data.length;
            if (length = 67) {
                var expectedStart = "<PDPProjectUid>";
                var expectedEnd = "</PDPProjectUid>";
                var endTagPosition = length - expectedEnd.length;
                var start = event.data.substr(0, expectedStart.length);
                var end = event.data.substr(endTagPosition, expectedEnd.length);
                // Parse out the project ID.
                if (start == expectedStart && end == expectedEnd) {
                    projectUid = event.data.substr(expectedStart.length, 36);
                    $get('projectUid').innerText = projectUid;
                }
            }
        }
   ```

3. Agregue el siguiente código en el **elemento de** cuerpo de la página. El código define un control span que muestra el identificador del proyecto. 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. En el Elements.xml, si lo desea, cambie el nombre, el título, la descripción y el tamaño predeterminado del elemento de complemento. En este ejemplo se usan los valores predeterminados.
    
5. Para probar el elemento de complemento, en la barra de menús, elija **Depurar**, **Iniciar depuración.** Si se le pide que modifique el archivo web.config, elija el botón **Aceptar**. 
    
   Para depurar el elemento de complemento, establezca los puntos de interrupción adecuados en el script que agregó.
    
6. Vaya a una página de PDP y elija **Editar página** en el menú Herramientas (icono de engranaje). 
    
7. Agregue el **elemento de título GetProjectId** a un elemento web de la página. El identificador del proyecto se muestra en el control **span** de la página del elemento web. 
    
## <a name="next-steps"></a>Pasos siguientes
<a name="NextSteps"> </a>

El elemento de complemento de este ejemplo no tiene acceso a los datos de Project Server ni a los datos de SharePoint. Puede usar el identificador del producto para obtener información sobre el proyecto actual mediante una API de cliente, como el modelo de objetos de JavaScript o el servicio REST.
  
En el AppManifest.xml, especifique los permisos que el complemento necesita para tener acceso a datos de Project Server o datos de SharePoint. 
  
Vea Crear elementos de complemento para instalarlos con el complemento de [SharePoint](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) para obtener información sobre cómo establecer propiedades personalizadas para un elemento de complemento. 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>Ejemplo: Obtener el identificador de proyecto en un elemento de complemento en una página de PDP
<a name="CodeExample"> </a>

El siguiente ejemplo es el código completo de la página GetProjectID.aspx del elemento web cliente. El código registra un agente de escucha de eventos y un controlador de eventos que recibe y analiza un mensaje que contiene el identificador del proyecto.
  
```HTML
<%@ Page language="C#" Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<WebPartPages:AllowFraming ID="AllowFraming" runat="server" />
<html>
<head>
    <title></title>
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/MicrosoftAjax.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.js"></script>
    <script type="text/javascript">
        'use strict';
        // Define global variables.
        var hostUrl = '';
        var projectUid;
        // Set the style of the client web part page to be consistent with the host web.
        (function () {
            var hostUrl = '';
            var link = document.createElement('link');
            link.setAttribute('rel', 'stylesheet');
            if (document.URL.indexOf('?') != -1) {
                var params = document.URL.split('?')[1].split('&');
                for (var i = 0; i < params.length; i++) {
                    var p = decodeURIComponent(params[i]);
                    if (/^SPHostUrl=/i.test(p)) {
                        hostUrl = p.split('=')[1];
                        link.setAttribute('href', hostUrl + '/_layouts/15/defaultcss.ashx');
                        break;
                    }
                }
            }
            if (hostUrl == '') {
                link.setAttribute('href', '/_layouts/15/1033/styles/themable/corev15.css');
            }
            document.head.appendChild(link);
        })();
        // Get the message.
        function getProjectUid() {
            window.parent.postMessage('getprojectuid', hostUrl);
        }
        getProjectUid();
        // Add an event listener and register the event handler.
        // If the IE browser version is earlier than 9, use the attachEvent method.
        if (window.addEventListener) {
            window.addEventListener("message", onMessage, false);
        }
        else {
            if (window.attachEvent) {
                window.attachEvent("onmessage", onMessage);
            }
        }
        // Get the project ID from the message.
        function onMessage(event) {
            // Verify the message origin.
            if (hostUrl.indexOf(event.origin) != 0) return;
            // The expected message format is "<PDPProjectUid>00000000-0000-0000-0000-000000000000</PDPProjectUid>,"
            // so validate by using the length and the start and end tags.
            var length = event.data.length;
            if (length = 67) {
                var expectedStart = "<PDPProjectUid>";
                var expectedEnd = "</PDPProjectUid>";
                var endTagPosition = length - expectedEnd.length;
                var start = event.data.substr(0, expectedStart.length);
                var end = event.data.substr(endTagPosition, expectedEnd.length);
                // Parse out the project ID.
                if (start == expectedStart && end == expectedEnd) {
                    projectUid = event.data.substr(expectedStart.length, 36);
                    $get('projectUid').innerText = projectUid;
                }
            }
        }
    </script>
</head>
<body>
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
</body>
</html>

```

## <a name="see-also"></a>Consulte también

- [Tareas de programación de Project](project-programming-tasks.md)
- [Crear un complemento de Project Server hospedado por SharePoint](create-a-sharepoint-hosted-project-server-add-in.md)
- [Crear elementos de complemento para instalarlos con el complemento de SharePoint](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

