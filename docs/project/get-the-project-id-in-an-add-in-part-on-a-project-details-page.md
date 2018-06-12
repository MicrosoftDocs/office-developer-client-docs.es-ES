---
title: Obtener el identificador del proyecto en un elemento en en una página de detalles del proyecto
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Complemento de elementos se hospedan en elementos iframe que están completamente aislados de la página de hospedaje. Para obtener información acerca del proyecto actual de un elemento en en página de detalles de proyecto (PDP), puede usar el método window.postMessage, un agente de escucha de evento y un controlador de eventos que analiza el identificador de proyecto desde el mensaje.
ms.openlocfilehash: 6704dae7ded385f86d2da47a1334ae4c81622a74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821296"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>Obtener el identificador del proyecto en un elemento en en una página de detalles del proyecto

Complemento de elementos se hospedan en elementos **iframe** que están completamente aislados de la página de hospedaje. Para obtener información acerca del proyecto actual de un elemento en en página de detalles de proyecto (PDP), puede usar el método **window.postMessage** , un agente de escucha de evento y un controlador de eventos que analiza el identificador de proyecto desde el mensaje. 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>Requisitos previos para la creación de un hospedada en SharePoint complemento de elemento que se obtiene el identificador del proyecto
<a name="Prereqs"> </a>

Para usar el ejemplo de código de este artículo, necesitará los siguientes elementos:
  
- SharePoint 2013 y Project Server 2013, configurado para el aislamiento de complemento. Si está desarrollando de forma remota, el servidor debe admitir sideloading de complementos o debe instalar el complemento en un sitio para desarrolladores.
  
- SharePoint Online y Project Online
    
    - Visual Studio 2013, Visual Studio 2012 con Office Developer Tools para Visual Studio 2013 o Napa
        
    - Permisos suficientes para el usuario que ha iniciado la sesión:
        
        - Permisos de administrador local en el equipo de desarrollo.
            
        - Acceso de lectura para al menos un proyecto.
            
        - Permiso para editar las páginas en el sitio de Project Web App.
            
        - Debe iniciar sesión como un usuario que no sea la cuenta del sistema. La cuenta del sistema no tiene permiso para instalar un complemento.
    
Para obtener más información acerca de los complementos para Project, vea [requisitos previos para crear un complemento para Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) . Para obtener instrucciones acerca de la instalación local (incluidos los procedimientos para deshabilitar la comprobación de bucle invertido, si es necesario), vea [configurar un entorno de desarrollo local para SharePoint Add-ins](http://msdn.microsoft.com/library/b0878c12-27c9-4eea-ae3b-7e79e5a8838d%28Office.15%29.aspx) . Si está desarrollando de forma remota, vea [Developing aplicaciones para SharePoint en un sistema remoto](http://msdn.microsoft.com/library/bf35d59c-9b84-42e5-877e-fa6881a7b6fc%28Office.15%29.aspx).
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>Crear el elemento de web hospedada en SharePoint, en Agregar y cliente
<a name="CreateApp"> </a>

1. Abra Visual Studio y elija **archivo** > **New** > **Project**.
    
2. En el cuadro de diálogo **Nuevo proyecto**, seleccione **.NET Framework 4.5** en la lista desplegable situada en la parte superior del cuadro de diálogo. 
    
3. En la lista de **plantillas** , elija **Visual C#** > **Office/SharePoint** > **Add-ins** > **Add-in for SharePoint 2013**.
    
4. Nombre GetProjectIdAddinPart en Agregar y, a continuación, elija el botón **Aceptar** . 
    
5. En el cuadro de diálogo **nuevo complemento para SharePoint** , escriba la dirección URL del sitio de PWA que desea usar para la depuración (por ejemplo: _https://contoso.com/sites/pwasite/_).
    
6. Elija la opción **hospedada en SharePoint** para hospedar el complemento y, a continuación, elija el botón **Finalizar** . 
    
7. En el **Explorador de soluciones**, abra el menú contextual para el proyecto GetProjectIdAddinPart y, a continuación, elija **Agregar** > **Nuevo elemento**.
    
8. En el cuadro de diálogo **Agregar nuevo elemento** , elija el **elemento web de cliente (Host Web)**, el elemento web GetProjectId el nombre y, a continuación, elija el botón **Agregar** . 
    
9. En el cuadro de diálogo **elemento web cliente crear** , elija la opción **crear una nueva página de elementos web de cliente** y, a continuación, elija el botón **Finalizar** . 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>Obtener el identificador del proyecto en la parte del complemento
<a name="GetProjectId"> </a>

El elemento GetProjectId complemento define su código personalizado en la página GetProjectId.aspx del elemento web de cliente. La lógica que recibe y controla el mensaje se define en el elemento **head** de la página y los controles de página están definidos en el elemento **body** de la página. 
  
1. Abra la página de elementos web de GetProjectId.aspx (en la carpeta **páginas** ). 
    
2. En el elemento **head** de la página, reemplace el código entre las etiquetas de **script** con el siguiente código. 
    
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

3. Agregue el código siguiente en el elemento **body** de la página. El código define un control span que muestra el identificador de proyecto. 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. En el archivo Elements.xml, opcionalmente, cambie el nombre, el título, la descripción y el tamaño predeterminado de la parte del complemento. En este ejemplo se utiliza los valores predeterminados.
    
5. Para probar el elemento en Agregar, en la barra de menús, elija **Depurar**, **Iniciar depuración**. Si se le pedirá que modifique el archivo web.config, elija el botón **Aceptar** . 
    
   Para depurar el elemento complemento, establezca puntos de interrupción apropiados en la secuencia de comandos que ha agregado.
    
6. Vaya a una página PDP y elija **Editar página** en el menú Herramientas (icono de engranaje). 
    
7. Agregar el elemento de **Título GetProjectId** a un elemento web en la página. Muestra el identificador del proyecto en el control **span** en la página de elementos web. 
    
## <a name="next-steps"></a>Siguientes pasos
<a name="NextSteps"> </a>

El elemento en en este ejemplo no tener acceso a datos de Project Server o datos de SharePoint. Puede usar el identificador de producto para obtener información acerca del proyecto actual mediante el uso de un cliente de la API, como el modelo de objetos de JavaScript o el servicio REST.
  
En el archivo AppManifest.xml, especifique los permisos que el complemento necesita obtener acceso a datos de Project Server o datos de SharePoint. 
  
Consulte [Crear complemento elementos para instalar con el complemento de SharePoint](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) para aprender a establecer propiedades personalizadas para una parte del complemento. 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>Ejemplo: Obtener el identificador del proyecto en un elemento en en una página PDP
<a name="CodeExample"> </a>

El ejemplo siguiente es el código completo en la página de GetProjectID.aspx del elemento web de cliente. El código registra un agente de escucha de evento y un controlador de eventos que recibe y analiza un mensaje que contiene el identificador de proyecto.
  
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

## <a name="see-also"></a>Ver también

- [Tareas de programación de Project](project-programming-tasks.md)
- [Crear un complemento de hospedada en SharePoint Project Server](create-a-sharepoint-hosted-project-server-add-in.md)
- [Crear elementos de complemento para instalarlos con el complemento de SharePoint](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

