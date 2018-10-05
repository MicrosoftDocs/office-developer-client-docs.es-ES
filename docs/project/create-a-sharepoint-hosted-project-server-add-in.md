---
title: Crear un complemento de Project Server hospedado por SharePoint
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: De los tres tipos de aplicaciones que se pueden crear para Project Online (autohospedada, hospedada en proveedor y hospedadas en SharePoint), es la más sencilla de crear e implementar la aplicación hospedada en SharePoint.
ms.openlocfilehash: 7a74f5b3b848f3fa238051f5b9f9f563c38417b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399588"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a>Crear un complemento de Project Server hospedado por SharePoint

De los tres tipos de aplicaciones que se pueden crear para Project Online (autohospedada, hospedada en proveedor y hospedadas en SharePoint), es la más sencilla de crear e implementar la aplicación hospedada en SharePoint. Una aplicación hospedada en SharePoint no requieren autenticación de OAuth y no se use Azure o no requieren mantenimiento de un sitio local de los recursos hospedada por el proveedor. La plantilla de **aplicación para SharePoint 2013** en Visual Studio es un marco de trabajo conveniente para el desarrollo de aplicaciones que pueden publicarse y se venden en la tienda Office o implementadas en un catálogo de aplicaciones privada en SharePoint. 
  
En Project, estado es un proceso donde un integrante del grupo puede usar la página de tareas en Project Web App para enviar el estado de una tarea asignada, como el número de horas trabajadas cada día de una semana empleado en trabajar en la tarea. El propietario de asignación (normalmente, el jefe de proyecto) puede aprobar o rechazar el estado. Cuando se aprueba el estado, Project recalcula la programación. La aplicación **QuickStatus** muestra las tareas asignadas, donde el usuario puede actualizar rápidamente porcentaje completado y enviar el estado de las asignaciones seleccionadas para su aprobación. Aunque la página de tareas en Project Web App tiene mucho más funcionalidad, la aplicación **QuickStatus** es un ejemplo que proporciona una interfaz simplificada. 
  
La aplicación **QuickStatus** es un ejemplo para desarrolladores; no está pensada para su uso en un entorno de producción. El propósito principal es mostrar un ejemplo de desarrollo de aplicaciones para Project Online, no para crear una aplicación de estado totalmente funcional. Para un mejor enfoque para la administración de Estados, vea la recomendación de los [pasos siguientes](#pj15_StatusingApp_NextSteps).
  
Para obtener información general sobre el estado, vea el [progreso de la tarea](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress). Para obtener más información acerca de cómo desarrollar complementos para SharePoint y Project Server, vea [SharePoint Add-ins](https://msdn.microsoft.com/library/jj163230.aspx).

<a name="pj15_StatusingApp_Prerequisites"> </a>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a>Requisitos previos para crear una aplicación para Project Server 2013

Para desarrollar aplicaciones relativamente sencillas que se pueden implementar para Project Online o a una instalación local de Project Server 2013, puede usar el Napa, que proporcionan un entorno de desarrollo en línea. Para las aplicaciones más complejas, modificación de la cinta de opciones de Project Web App y facilitar la depuración durante el desarrollo, se puede usar Visual Studio 2012 o Visual Studio 2013. Por ejemplo, con una instalación local, puede comprobar manualmente las tablas de datos de borrador para que los cambios en la base de datos de Project Server. En este artículo se muestra cómo llevar a cabo el desarrollo de aplicaciones con Visual Studio.
  
El desarrollo de aplicaciones de Project Server con Visual Studio exige lo siguiente:
  
- Asegúrese de haber instalado los Service Pack y las actualizaciones de Windows más recientes en el equipo de desarrollo local. El sistema operativo puede ser Windows 7, Windows 8, Windows Server 2008 o Windows Server 2012.
    
- Debe tener un equipo que tenga instalado, donde el equipo está configurado para el aislamiento de aplicaciones y sideloading de aplicaciones de Project Server 2013 y de SharePoint Server 2013. Sideloading permite a Visual Studio instalar temporalmente la aplicación para la depuración. Puede usar una instalación local de SharePoint y Project Server. Para obtener más información, vea [configurar un entorno de desarrollo local para aplicaciones para SharePoint](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx).
    
   > [!NOTE]
   > Para una instalación local, configure una aplicación aislado dominio *antes de* crear un catálogo de aplicaciones corporativo. 
  
- El equipo de desarrollo puede ser un equipo remoto que tiene Office Developer Tools para Visual Studio 2012 instalado. Asegúrese de que ha instalado la versión más reciente; vea la sección *Herramientas* de las [descargas de aplicaciones para Office y SharePoint](https://msdn.microsoft.com/office/apps/fp123627.aspx).
    
- Compruebe que la instancia de Project Web App va a usar para el desarrollo y la prueba es accesible en el explorador.
    
Para obtener información acerca del uso de las herramientas en línea, vea [configurar un entorno de desarrollo de aplicaciones para SharePoint en Office 365](https://msdn.microsoft.com/library/fp161179.aspx). Para obtener un tutorial de creación de una aplicación simple de Project Server que usa las herramientas en línea, vea la serie de blog EPMSource, [creación de su primera aplicación de Project Server](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).

<a name="pj15_StatusingApp_UsingVisualStudio"> </a>

## <a name="using-visual-studio-to-create-a-project-server-app"></a>Empleo de Visual Studio para crear una aplicación de Project Server

Office Developer Tools para Visual Studio 2012 incluye una plantilla para las aplicaciones de SharePoint que se pueden usar con Project Server 2013. Cuando se crea una solución de aplicación, la solución incluye los siguientes archivos para que el código personalizado:
  
- **AppManifest.xml** incluye la configuración del título de la aplicación, el ámbito de solicitud de permisos y otras propiedades. El procedimiento 1 incluye los pasos para establecer las propiedades mediante el diseñador de manifiestos. 
    
- **Default.aspx** en la carpeta Páginas de la página principal de la aplicación. El procedimiento 2 muestra cómo agregar contenido HTML5 para la aplicación **QuickStatus**. 
    
- **App.js** en la carpeta de secuencias de comandos es el archivo principal para el código JavaScript personalizado. Procedimiento 3 explica el código JavaScript para la aplicación **QuickStatus** . 
    
   Si se agregan controles comerciales como una cuadrícula basada en jQuery o un selector de fecha, puede agregar referencias a archivos JavaScript adicionales en el archivo Default.aspx.
    
- **App.css** en la carpeta Contenido es el archivo principal de los estilos CSS3 personalizados. Los procedimientos 2 y 3 incluyen información sobre los estilos de las hojas de estilos en cascada (CSS) de la aplicación **QuickStatus**. Puede agregar referencias a archivos CSS adicionales en el archivo Default.aspx. 
    
- **AppIcon.png** en la carpeta de imágenes es el icono de 96 x 96 que la aplicación se muestra en la tienda de Office o el catálogo de aplicaciones. 
    
Para modificar la cinta de opciones de Project Web App, puede agregar una acción personalizada de la cinta de opciones. La sección [código de ejemplo para la aplicación QuickStatus](#pj15_StatusingApp_Example) incluye el código completo para los archivos Default.aspx, App.js, App.css, Elements.xml y AppManifest.xml modificados. 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a>Procedimiento 1. Crear un proyecto de aplicación en Visual Studio

1. Ejecute Visual Studio 2012 como administrador y, a continuación, seleccione **Nuevo proyecto** en la página de inicio. 
    
2. En el cuadro de diálogo **Nuevo proyecto**, expanda los nodos **Plantillas**, **Visual C#** y **Office o SharePoint** y seleccione **Aplicaciones**. Use **.NET Framework 4.5** predeterminado en la lista desplegable del marco de destino en la parte superior del panel central y, a continuación, seleccione **Aplicación de SharePoint 2013** (ilustración 1). 
    
3. En el campo **nombre** , escriba QuickStatus, vaya a la ubicación donde desea guardar la aplicación y, a continuación, elija **Aceptar**.
    
   **Ilustración 1. Creación de una aplicación de Project Server en Visual Studio**

   ![Crear un proyecto de aplicación de servidor en Visual Studio] (media/pj15_CreateStatusingApp_NewProject.gif "Crear un proyecto de aplicación de servidor en Visual Studio")
  
4. En el cuadro de diálogo **Nueva aplicación para SharePoint**, rellene los tres campos siguientes: 
    
   - En el cuadro de texto superior, escriba el nombre que desea que la aplicación para mostrar en Project Web App. Por ejemplo, escriba rápido de estado de actualización.
    
   - De sitio que se va a usar para la depuración, escriba la dirección URL de la instancia de Project Web App. Por ejemplo, escriba `https://ServerName/ProjectServerName` (reemplazando _ServerName_ y _ProjectServerName_ con sus propios valores) y, a continuación, seleccione **Validar**. Si todo va bien, Visual Studio muestra la **conexión correcta**. Si recibe un mensaje de error, asegúrese de que la dirección URL de Project Web App es correcta y que el equipo de Project Server está configurado para el aislamiento de aplicaciones y sideloading de aplicaciones. Para obtener más información, vea la sección [requisitos previos para crear una aplicación para Project Server 2013](#pj15_StatusingApp_Prerequisites) . 
    
   - En la lista desplegable **¿Cómo desea hospedar la aplicación para SharePoint?**, seleccione **Hospedada por SharePoint**.
    
   > [!CAUTION]
   > Si por error selecciona el tipo de proyecto predeterminado **Hospedada por el proveedor**, Visual Studio crea dos proyectos en la solución: un proyecto **QuickStatus** y un proyecto **QuickStatusWeb**. Si ve dos proyectos, elimine esa solución y vuelva a empezar. 
  
5. Seleccione **Aceptar** para crear la solución **QuickStatus**, el proyecto **QuickStatus** y los archivos predeterminados. 
    
6. Abra la vista del diseñador de manifiestos (por ejemplo, haga doble clic en el archivo AppManifest.xml). En la pestaña **General**, el cuadro de texto **Título** debería mostrar el nombre de la aplicación que escribió en el paso 4. Seleccione la pestaña **Permisos** para agregar las siguientes solicitudes de permisos para la aplicación (ilustración 2): 
    
   - En la primera fila de la lista **Solicitudes de permiso**, en la columna **Ámbito**, seleccione **Estado** en la lista desplegable. En la columna **Permiso**, seleccione **SubmitStatus**.
    
   - Agregue una fila si **Ámbito** es **Varios proyectos** y **Permiso** es **Read**.
    
   **Ilustración 2. Establecimiento del ámbito de permisos de una aplicación de estado**

   ![Definir el ámbito de permiso de una aplicación de estado] (media/pj15_CreateStatusingApp_PermissionScope.gif "Definir el ámbito de permiso de una aplicación de estado")
  
La aplicación **QuickStatus** permite a un usuario de Project Web App leer las asignaciones para ese usuario de varios proyectos, cambiar el porcentaje de trabajo completado y enviar la actualización. Los otros ámbitos de solicitud de permisos que se muestra en la lista desplegable en la figura 2 no son necesarios para esta aplicación. Los ámbitos de solicitud de permiso son los permisos que la aplicación solicita en nombre del usuario. Si el usuario no tiene los permisos de dichos en Project Web App, no se ejecuta la aplicación. Una aplicación puede tener varios ámbitos de solicitud de permiso, las de otros permisos de SharePoint, incluidas pero debe tener el mínimo necesario para la funcionalidad de la aplicación. A continuación está los ámbitos de solicitud de permiso que están relacionadas con Project Server: 

- **Recursos de empresa**: permisos de administrador de recursos, para leer o escribir información acerca de otros usuarios de Project Web App.
    
- **Varios proyectos**: leer o escribir en más de un proyecto donde el usuario tiene los permisos solicitados.
    
- **Project Server**: requiere que el usuario de la aplicación tener permisos de administrador de Project Web App.
    
- **Informes**: leer el servicio **ProjectData** OData de Project Web App (requiere sólo de inicio de sesión permisos de Project Web App). 
    
- **Proyecto único**: leer o escribir en un proyecto donde el usuario tiene los permisos solicitados.
    
- **Estado**: enviar actualizaciones de los estados de las asignaciones, como horas trabajadas, porcentaje completado y nuevas asignaciones.
    
- **Flujo de trabajo**: si el usuario tiene permiso para ejecutar flujos de trabajo de Project Server, la aplicación se ejecuta con permisos elevados para el flujo de trabajo.
    
Para obtener más información acerca de los ámbitos de solicitud de permiso para Project Server 2013, vea la sección *aplicaciones de Project* en [actualizaciones para desarrolladores en Project 2013](updates-for-developers-in-project-2013.md) y [los permisos de aplicación en SharePoint 2013](https://msdn.microsoft.com/library/fp142383.aspx).


<a name="pj15_StatusingApp_HTML"> </a>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a>Creación de contenido HTML para la aplicación QuickStatus

Antes de comenzar a codificar el contenido HTML, diseño de la interfaz de usuario y la experiencia del usuario para la aplicación QuickStatus (en la figura 3 muestra un ejemplo de la página completado). Un diseño también puede incluir un esquema de las funciones de JavaScript que interactúan con el código HTML. Para obtener información general, vea [Diseño de la experiencia de usuario de aplicaciones en SharePoint 2013](https://msdn.microsoft.com/library/fp179934.aspx).
  
**Ilustración 3. Diseño de la página de la aplicación QuickStatus**

![Diseño de la página de la aplicación QuickStatus] (media/pj15_CreateStatusingApp_AfterRefresh.gif "Diseño de la página de la aplicación QuickStatus")
  
La aplicación muestra el nombre para mostrar en la parte superior, que es el valor del elemento **Title** de AppManifest.xml. 
  
De forma predeterminada, la página emplea HTML5. A continuación se enumeran los elementos HTML estándar de los objetos principales de la IU que la aplicación **QuickStatus** contiene en el cuerpo de la página: 
  
- Un elemento **form** contiene todos los demás elementos de interfaz de usuario. 
    
- Un elemento **fieldset** crea un contenedor y un borde para la tabla de asignaciones; el elemento secundario **legend** proporciona una etiqueta para el contenedor. 
    
- Un elemento de **tabla** incluye un título y un encabezado de la tabla. Las funciones de JavaScript cambiar el título de tabla y agregar filas para las asignaciones. 
    
   > [!NOTE]
   > Para paginar y ordenar fácilmente, una aplicación de producción probablemente emplearía un control de cuadrícula comercial basado en jQuery en lugar de una tabla. 
  
   La tabla incluye columnas para el nombre del proyecto, el nombre de tarea con una casilla de verificación, el trabajo real, el porcentaje de trabajo completado, restante y fecha de finalización de la asignación. Las funciones de JavaScript creación la casilla de verificación y el campo de entrada de texto para el porcentaje completado de cada tarea.
    
- Un elemento **input** para que un cuadro de texto establezca el porcentaje completado de todas las asignaciones seleccionadas. 
    
- Un elemento **button** envía los cambios de estado. 
    
- Un elemento **button** actualiza la página. 
    
- Un elemento de **botón** sale de la aplicación y se devuelve a la página de tareas en Project Web App. 
    
Los elementos de botón y el cuadro de texto inferior están dentro de los elementos **div** , para que CSS puede administrar fácilmente la posición y la apariencia de los objetos de la interfaz de usuario. Una función de JavaScript, agrega un párrafo en la parte inferior de la página que contiene los resultados para el éxito o el fracaso de la actualización de estado. 
  
### <a name="procedure-2-to-create-the-html-content"></a>Procedimiento 2. Crear el contenido HTML

1. En Visual Studio, abra el archivo Default.aspx.
    
   El archivo incluye dos elementos de **asp: Content** : el elemento con el `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` atributo se agrega en el encabezado de página y el elemento con el `ContentPlaceHolderID="PlaceHolderMain"` atributo se coloca dentro del elemento de **cuerpo de la** página. 
    
2. En la `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` de control para el encabezado de página, agregue una referencia al archivo PS.js en el equipo de Project Server. Para realizar pruebas y depuración, puede usar PS.debug.js. 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   La infraestructura de la aplicación utiliza el `/_layouts/15/` directorio virtual para el sitio de SharePoint en IIS. El archivo físico es `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`.
    
   > [!NOTE]
   > Antes de implementar la aplicación para usar en producción, quitar `.debug` de las referencias de script para mejorar el rendimiento. 
  
3. En el `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` controlar para el cuerpo de la página, elimine el elemento generado **div** y, a continuación, agregue el código HTML para los objetos de la interfaz de usuario. El elemento de **tabla** contiene sólo una fila de encabezado. La columna **nombre de la tarea** incluye un control de entrada de la casilla de verificación. Texto para el elemento de **título** se sustituye por la devolución de llamada **onGetUserNameSuccess** para la función **getUserInfo** en el archivo App.js. 
    
    ```HTML
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
        <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
        </div>
    </form>
    ```

4. En el archivo App.css, agregue el código CSS para la posición y el aspecto de los elementos de la IU. Para ver el código CSS completo de la aplicación **QuickStatus**, consulte la sección [Código de ejemplo de la aplicación QuickStatus](#pj15_StatusingApp_Example). 
    
Procedimiento 3 agrega las funciones de JavaScript para leer las asignaciones y crear las filas de tabla y para cambiar y actualizar el porcentaje completado de la asignación. Los pasos reales son más iterativos en el desarrollo de una aplicación, donde es crear parte del código HTML, agregar y probar los estilos relacionados y las funciones de JavaScript, modificar o agregar más código HTML y, a continuación, repita el proceso.

<a name="pj15_StatusingApp_JavaScript"> </a>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a>Creación de las funciones JavaScript para la aplicación QuickStatus

La plantilla de Visual Studio para una aplicación de SharePoint incluye la App.js archivo, que contiene código de inicialización predeterminada que obtiene el contexto de cliente de SharePoint y muestra básica obtener y configurar las acciones de la página de la aplicación. El espacio de nombres de JavaScript para la biblioteca de SharePoint de cliente Object SP.js es **SP**. Dado que una aplicación de Project Server usa la biblioteca de PS.js, la aplicación utiliza el espacio de nombres **PS** para obtener el contexto de cliente y obtener acceso a la JSOM para Project Server. 
  
Las funciones de JavaScript en la aplicación **QuickStatus** incluyen los siguientes: 
  
- El controlador de eventos **ready** del documento se ejecuta al instanciar el modelo de objetos del documento (DOM). El controlador de eventos **ready** realiza los siguientes cuatro pasos: 
    
    1. Inicializa la variable global **projContext** con el contexto de cliente del JSOM de Project Server y la variable global **pwaWeb**. 
        
    2. Llama a la función **getUserInfo** para inicializar la variable global **projUser**. 
        
    3. Llama a la función **getAssignments**, que obtiene datos de asignación concretos del usuario. 
        
    4. Enlaza los controladores de eventos clic a la casilla de verificación del encabezado de la tabla y a las casillas de verificación de cada fila de la tabla. Los controladores de eventos clic administran el atributo **checked** de las casillas de verificación cuando el usuario activa o desactiva cualquier casilla de la tabla. 
    
- Si la función **getAssignments** es correcta, llama a la función **onGetAssignmentsSuccess**. Esa función inserta una fila en la tabla para cada asignación, inicializa los controles HTML de cada fila y, a continuación, inicializa las propiedades del botón inferior. 
    
- El controlador de eventos **onClick** del botón **Actualizar** llama a la función **updateAssignments**. Esa función obtiene el valor de porcentaje completado que se aplica a cada asignación seleccionada; si el cuadro de texto de porcentaje completado está vacío, la función obtiene el porcentaje completado de cada asignación seleccionada de la tabla. Entonces, la función **updateAssignments** guarda las actualizaciones de estado y las envía y escribe un mensaje sobre los resultados en la parte inferior de la página. 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a>Procedimiento 3. Crear las funciones JavaScript

1. En Visual Studio, abra el archivo App.js y elimine todo el contenido del mismo.
    
2. Agregue las variables globales y el controlador de eventos **ready** del documento. Al objeto **document** se obtiene acceso mediante una función jQuery. 
    
   El controlador de eventos clic de la casilla de verificación del encabezado de la tabla establece el estado activado de las casillas de fila. Si todas las casillas de fila están activadas o desactivadas, el controlador de eventos clic de las casillas de fila establece el estado activado de la casilla de encabezado. El controlador de eventos clic además establece el mensaje de resultados en la parte inferior de la página en una cadena vacía.
    
   ```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the checked state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
   ```

3. Agregue la función **getUserInfo**, que llama a **onGetUserNameSuccess** si la consulta es correcta. La función **onGetUserNameSuccess** sustituye el contenido del párrafo **caption** por un título de tabla que incluye el nombre de usuario. 
    
   ```js
        // Get information about the current user.
        function getUserInfo() {
            projUser = pwaWeb.get_currentUser();
            projContext.load(projUser);
            projContext.executeQueryAsync(onGetUserNameSuccess,
                // Anonymous function to execute if getUserInfo fails.
                function (sender, args) {
                    alert('Failed to get user name. Error: ' + args.get_message());
            });
        } 
        // This function is executed if the getUserInfo call is successful.
        function onGetUserNameSuccess() {
            var prefaceInfo = 'Assignments for ' + projUser.get_title();
            $('#tableCaption').text(prefaceInfo);
        }
   ```

4. Agregue la función **getAssignments**, que llama a **onGetAssignmentsSuccess** (paso 5) si la consulta de asignación es correcta. La opción **Include** limita la consulta a devolver únicamente los campos especificados. 
    
   ```js
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
   ```

5. Agregue la función **onGetAssignmentsSuccess**, que agrega una fila para cada asignación a la tabla. La variable **prevProjName** se usa para determinar si una fila es para otro proyecto. Si es así, el nombre del proyecto se muestra en negrita; si no, el nombre del proyecto se establece en una cadena vacía. 
    
   > [!NOTE]
   > El JSOM no incluye las propiedades de **TimeSpan** que incluye el CSOM, como **ActualWorkTimeSpan**. En su lugar, utiliza el JSOM de propiedades para el número de milisegundos, como el [PS. StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) (propiedad). Es el método para obtener dicha propiedad **obtener\_actualWorkMilliseconds**, que devuelve un valor entero. > El método **get_actualWork** devuelve una cadena como "h 3". Puede usar cualquiera de los valores de la aplicación **QuickStatus** , pero mostrar de forma diferente. La consulta de las asignaciones incluye las dos propiedades, por lo que puede probar el valor durante la depuración. Si se quita la variable **actualWork** , también puede quitar la propiedad **ActualWork** en la consulta de las asignaciones. 
  
   Por último, la función **onGetAssignmentsSuccess** inicializa el botón **Actualizar** y el botón **Actualizar** con controladores de eventos clic. El valor de texto del botón **Actualizar** también se podría establecer en el código HTML. 
    
   ```js
        // Get the enumerator, iterate through the assignment collection, 
        // and add each assignment to the table.
        function onGetAssignmentsSuccess(sender, args) {
            if (assignments.get_count() > 0) {
                var assignmentsEnumerator = assignments.getEnumerator();
                var projName = "";
                var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
                var taskNum = 0;
                var chkTask = "";
                var txtPctComplete = "";
                // Constants for creating input controls in the table.
                var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
                var LBLCHK = '<label for="chk';
                var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
                while (assignmentsEnumerator.moveNext()) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    projName = statusAssignment.get_project().get_name();
                    // Get an integer, such as 3600000.
                    var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds(); 
                    // Get a string, such as "1h". Not used here.
                    var actualWork = statusAssignment.get_actualWork();
                    if (projName === prevProjName) {
                        projName = "";
                    }
                    prevProjName = statusAssignment.get_project().get_name();
                    // Create a row for the assignment information.
                    var row = assignmentsTable.insertRow();
                    taskNum++;
                    // Create an HTML string with a check box and task name label, for example:
                    // <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> <label for="chk1">Task 1</label>
                    chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">' 
                        + statusAssignment.get_name() + '</label>';
                    txtPctComplete = INPUTTXT + taskNum + '" />';
                    // Insert cells for the assignment properties.
                    row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                    row.insertCell().innerHTML = chkTask;
                    row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                    row.insertCell().innerHTML = txtPctComplete;
                    row.insertCell().innerText = statusAssignment.get_remainingWork();
                    row.insertCell().innerText = statusAssignment.get_finish();
                    // Initialize the percent complete cell.
                    $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
                }
            }
            else {
                $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
                $get("message").innerText = projUser.get_title() + ' has no assignments'
            }
            // Initialize the button properties.
            $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
            $get("btnSubmitUpdate").innerText = 'Update';
            $get('btnRefresh').onclick = function () { window.location.reload(true); };
            $get('btnExit').onclick = function () { exitToPwa(); };
        }
   ```

6. Agregue el controlador de eventos clic **updateAssignments** del botón **Actualizar**. Si el usuario cambia un valor para el porcentaje completado de una tarea o agrega un valor en el cuadro de texto **percentComplete**, dicho valor podría especificarse en varios formatos, como "60", "60%" o "60 %". El método **getNumericValue** devuelve el valor numérico del texto de entrada. 
    
   > [!NOTE]
   > En una aplicación diseñada para uso en producción, los valores de entrada de la información numérica deben incluir validación de campos y comprobación de errores adicional. 
  
   El ejemplo **updateAssignments** incluye alguna comprobación de errores básica y muestra información en el párrafo **message** de la parte inferior de la página: verde si la consulta de actualización es correcta y roja si hay un error de entrada o la consulta de actualización no es correcta. 
    
   Antes de usar el método **submitAllStatusUpdates**, la aplicación tiene que guardar las actualizaciones en el servidor mediante el método **PS.StatusAssignmentCollection.update**. 
    
   ```js
        // Update all checked assignments. If the bottom percent complete field is blank,
        // use the value in the % complete field of each selected row in the table.
        function updateAssignments() {
            // Get percent complete from the bottom text box.
            var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
            var pctComplete = pctCompleteMain;
            var assignmentsEnumerator = assignments.getEnumerator();
            var taskNum = 0;
            var taskRow = "";
            var indexPercent = "";
            var doSubmit = true;
            while (assignmentsEnumerator.moveNext()) {
                var pctCompleteRow = "";
                taskRow = "chk" + ++taskNum;
                if ($get(taskRow).checked) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    if (pctCompleteMain === "") {
                        // Get percent complete from the text box field in the table row.
                        pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                        pctComplete = pctCompleteRow;
                    }
                    // If both percent complete fields are empty, show an error.
                    if (pctCompleteMain === "" && pctCompleteRow === "") {
                        $('p#message').attr('style', 'color: #e11500');     // Red text.
                        $get("message").innerHTML =
                            '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                            + taskNum
                            + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                            + '<p>Please refresh the page and try again.</p>';
                        doSubmit = false;
                        taskNum = 0;
                        break;
                    }
                    if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
                }
            } 
            // Save and submit the assignment updates.
            if (doSubmit) {
                assignments.update();
                assignments.submitAllStatusUpdates();
                projContext.executeQueryAsync(function (source, args) {
                    $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                    $get("message").innerText = 'Assignments have been updated.';
                }, function (source, args) {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerText = 'Error updating assignments: ' + args.get_message();
                });
            }
        }
        // Get the numeric part for percent complete, from a string. For example, with "20 %", return "20".
        function getNumericValue(pctComplete) {
            pctComplete = pctComplete.trim();
            pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
            indexPercent = pctComplete.indexOf('%', 0);
            if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
            return pctComplete;
        }
   ```

7. Agregar la función **exitToPwa** , que usa el parámetro de cadena de consulta de **SPHostUrl** para la dirección URL del sitio de Project Web App de host. Para volver a la página tareas, anexe `"/Tasks.aspx"` a la dirección URL. Por ejemplo, la variable **spHostUrl** se establecería en `https://ServerName/ProjectServerName/Tasks.aspx`.
    
   La función **getQueryStringParameter** divide la dirección URL de la página **QuickStatus** para extraer y devolver el parámetro especificado en las opciones de la dirección URL. El siguiente es un ejemplo del valor **document.URL** del documento **QuickStatus** (todo en una línea): 
    
   ```HTML
    https://app-ef98082fa37e3c.servername.officeapps.selfhost.corp.microsoft.com/pwa/
        QuickStatus/Pages/Default.aspx
        ?SPHostUrl=https%3A%2F%2Fsphvm%2D85178%2Fpwa
        &SPLanguage=en%2DUS
        &SPClientTag=1
        &SPProductNumber=15%2E0%2E4420%2E1022
        &SPAppWebUrl=https%3A%2F%2Fapp%2Def98082fa37e3c%2Eservername
            %2Eofficeapps%2Eselfhost%2Ecorp%2Emicrosoft%2Ecom%2Fpwa%2FQuickStatus
   ```

   Para la dirección URL anterior, la función **getQueryStringParameter** devuelve el valor de cadena de consulta de **SPHostUrl** , `https://ServerName/pwa`. 
    
   ```js
        // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
        function exitToPwa() {
            // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
            var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                            + "/Tasks.aspx";
            // Set the top window for the QuickStatus IFrame to the Tasks page.
            window.top.location.href = spHostUrl;
        }
        // Get a specified query string parameter from the {StandardTokens} URL option string.
        function getQueryStringParameter(urlParameterKey) {
            var docUrl = document.URL;
            var params = docUrl.split('?')[1].split('&');
            for (var i = 0; i < params.length; i++) {
                var theParam = params[i].split('=');
                if (theParam[0] == urlParameterKey)
                    return decodeURIComponent(theParam[1]);
            }
        }
   ```

Si publica la aplicación **QuickStatus** en este momento y agregarlo a Project Web App, se puede ejecutar la aplicación desde la página de contenido del sitio, pero no está fácilmente disponible para los usuarios. Para ayudar a los usuarios encontrar y ejecutar la aplicación, puede agregar un botón correspondiente a la cinta de opciones en la página tareas. Procedimiento 4 muestra cómo agregar una acción personalizada de la cinta de opciones. 

<a name="pj15_StatusingApp_ribbon"> </a>

### <a name="adding-a-ribbon-custom-action"></a>Adición de una acción personalizada de cinta

Las fichas de la cinta de opciones, grupos y controles para Project Web App se especifican en el archivo pwaribbon.xml, que está instalado en el `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` directorio en el equipo que ejecuta Project Server. Para ayudar a las acciones personalizadas de diseño para la cinta de opciones de Project Web App, la descarga del SDK de Project 2013 incluye una copia de pwaribbon.xml. 
  
Project Web App usa las definiciones de la cinta de opciones diferentes para la página de tareas, dependiendo de si la instancia de Project Web App usa el modo de entrada único que permite a los usuarios especificar valores para el estado de tareas y partes de horas. Si tiene permisos administrativos para Project Web App, para determinar el modo de entrada, elija **Configuración de PWA** en el menú de configuración de la lista desplegable en la esquina superior derecha de la página. En la página Configuración de PWA, elija **Configuración del parte de horas y valores predeterminados**y, a continuación, mire la casilla de verificación **Modo de entrada único** en la parte inferior de la página. 
  
Si el modo de entrada único está desactivado, la cinta de opciones de la página Tareas es definida por la región Mi trabajo de pwaribbon.xml: 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

Si el modo de entrada único está activado, la cinta de opciones de la página Tareas es definida por la región Modo vinculado de pwaribbon.xml: 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

Aunque los grupos y los controles de cada región parecen similares, un control del modo vinculado puede llamar a una función distinta que el mismo control del modo no vinculado. El procedimiento 4 muestra cómo agregar un control de botón para la aplicación **QuickStatus** si el modo de entrada único está desactivado (la casilla de verificación **Modo de entrada único** está desactivada). 
  
> [!NOTE]
> Para obtener información general acerca de cómo agregar acciones personalizadas en una cinta de opciones o en un menú en una aplicación de SharePoint, vea [crear acciones personalizadas para implementarlas con aplicaciones para SharePoint](https://msdn.microsoft.com/library/jj163954.aspx). 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a>Procedimiento 4. Agregar una acción personalizada de cinta de opciones a la página Tareas

1. Examine la cinta de opciones en la página de tareas en Project Web App. Seleccione la ficha **tareas** en la cinta de opciones y planee cómo modificarlo. Existen siete grupos, como **Enviar**, **tareas**y **período**. El grupo de **envío** tiene dos controles, un botón **Guardar** y un menú desplegable de **Enviar estado** . Puede agregar un control en cualquier ubicación en un grupo, agregar un grupo con un nuevo control en cualquier ubicación en la ficha **tareas** o agregar otra ficha de la cinta de opciones que tiene controles y grupos personalizados. En este ejemplo, se agrega un tercer botón de para el grupo de **envío** , donde el botón invoca la dirección URL de la aplicación **QuickStatus** . 
    
2. En el panel **Explorador de soluciones** en Visual Studio, haga clic en el proyecto **QuickStatus** y, a continuación, agregue un nuevo elemento. En el cuadro de diálogo **Agregar nuevo elemento** , elija **Acción personalizada de la cinta de opciones** (vea la figura 4). Por ejemplo, el nombre de la acción personalizada RibbonQuickStatusAction y, a continuación, elija **Agregar**.
    
   **Ilustración 4. Adición de una acción personalizada de cinta de opciones**

   ![Agregar una acción personalizada de la cinta de opciones] (media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Agregar una acción personalizada de la cinta de opciones")
  
3. En la primera página del asistente **Crear acción personalizada para cinta**, deje seleccionada la opción **Web host**, seleccione **Ninguno** en la lista desplegable del ámbito de acción personalizada y luego seleccione **Siguiente** (ilustración 5). Los elementos de las listas desplegables son relevantes para SharePoint, no para Project Server. Se sustituirá la mayor parte del XML generado para la acción personalizada de modo que se aplique a Project Server. 
    
   **Ilustración 5. Especificación de propiedades para la acción personalizada de la cinta de opciones**

   ![Especificación de propiedades de la acción personalizada de la cinta de opciones] (media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Especificación de propiedades de la acción personalizada de la cinta de opciones")
  
4. En la página siguiente del asistente **Crear acción personalizada para cinta**, deje todos los valores predeterminados de la configuración y luego seleccione **Finalizar** (ilustración 6). Visual Studio crea la carpeta **RibbonQuickStatusAction**, que contiene un archivo Elements.xml. 
    
   **Ilustración 6. Especificación de la configuración de un control de botón**

   ![Especificar la configuración de un control de botón] (media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Especificar la configuración de un control de botón")
  
5. Modifique el código predeterminado generado en el archivo Elements.xml para la acción personalizada de la cinta de opciones. Este es el código XML predeterminado:
    
   ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="https://schemas.microsoft.com/sharepoint/">
        <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon"
                    Sequence="10001"
                    Title="Invoke &apos;RibbonQuickStatusAction&apos; action">
        <CommandUIExtension>
            <!-- 
            Update the UI definitions below with the controls and the command actions
            that you want to enable for the custom action.
            -->
            <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ListItem.Actions.Controls._children">
                <Button Id="Ribbon.ListItem.Actions.RibbonQuickStatusActionButton"
                        Alt="Request RibbonQuickStatusAction"
                        Sequence="100"
                        Command="Invoke_RibbonQuickStatusActionButtonRequest"
                        LabelText="Request RibbonQuickStatusAction"
                        TemplateAlias="o1"
                        Image32by32="_layouts/15/images/placeholder32x32.png"
                        Image16by16="_layouts/15/images/placeholder16x16.png" />
            </CommandUIDefinition>
            </CommandUIDefinitions>
            <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_RibbonQuickStatusActionButtonRequest"
                                CommandAction="~appWebUrl/Pages/Default.aspx"/>
            </CommandUIHandlers>
        </CommandUIExtension >
        </CustomAction>
    </Elements>
   ```

   1. En el elemento **CustomAction**, elimine los atributos **Sequence** y **Title**. 
    
   2. Para agregar un control para el grupo de **envío** , busque el primer grupo de la `Ribbon.ContextualTabs.MyWork.Home.Groups` colección en el archivo pwaribbon.xml, que es el elemento que comienza, `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`. Para agregar un control secundario al grupo de **envío** , el siguiente código muestra el atributo de **ubicación** correcto del elemento **CommandUIDefinition** en el archivo Elements.xml: 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. Cambie los valores de atributo del elemento secundario **Button** de este modo: 
    
       ```XML
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invoke_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="QuickStatus"
                    ToolTipDescription="Run the QuickStatus app" />
       ```

       - Para hacer que el botón el tercer control en el grupo, el atributo de **secuencia** puede ser cualquier número mayor que el `Sequence="20"` valor del control **Enviar estado** existente (que es un elemento **FlyoutAnchor** en pwaribbon.xml). Por convención, los números de secuencia de grupos y controles son `10, 20, 30, …`, lo que permite que los elementos que va a insertarse en posiciones intermedias.
    
       - El atributo de **comando** especifica el comando para ejecutar en el elemento **CommandUIHandler** (vea el siguiente paso 5.d). Puede simplificar el nombre del comando para que sea más fácil para el desarrollador siguiente. Por ejemplo `Command="Invoke_QuickStatus"` es más fácil de leer que `Command="Invoke_RibbonQuickStatusActionButtonRequest"`.
    
       - Los atributos de imagen especifican el icono de 16 x 16 píxeles y el icono de 32 x 32 píxeles para el control de botón. En el archivo Elements.xml de forma predeterminada, `Image32by32="_layouts/15/images/placeholder32x32.png"` especifica un punto naranja. Puede extraer los iconos de los archivos de mapa de imagen (ps16x16.png y ps32x32.png) que se instalan en el `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` directorio en el equipo que ejecuta Project Server. Por ejemplo, el icono de 32 x 32 píxeles está en la segunda columna de iconos de la izquierda y la décima fila hacia abajo desde la parte superior del mapa de imagen ps32x32.png (la parte superior del icono es después de finalizar el noveno fila; 9 filas x 32 píxeles/fila = 288 píxeles). 
    
       - Para mostrar información sobre herramientas para el control de botón, agregue los atributos **ToolTipTitle** y **ToolTipDescription**. 
    
    4. Cambiar los atributos del elemento **CommandUIHandler** . Por ejemplo, asegúrese de que el atributo de **comando** coincide con el valor del atributo de **comando** para el elemento de **botón** . Para el atributo **CommandAction** , `~appWebUrl` es un marcador de posición para la dirección URL de la página Web de **QuickStatus** . Cuando el botón de la cinta de opciones, invoca la aplicación **QuickStatus** , el símbolo (token) **{StandardTokens}** se ha reemplazado por opciones de dirección URL que incluyen **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber**y **SPAppWebUrl **.
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. En el **Explorador de soluciones**, abra el diseñador **Feature1.feature** y mueva el elemento **RibbonQuickStatusAction** del panel **Elementos de la solución** al panel **Elementos de la característica**. Si a continuación abre el diseñador **Package.package**, el elemento **RibbonQuickStatusAction** estará en el panel **Elementos del paquete**. 
    
Al desarrollar la aplicación y agrega un botón de la cinta de opciones, normalmente probar la aplicación y establecer puntos de interrupción en el código JavaScript para la depuración. Al presionar **F5** para iniciar la depuración, Visual Studio compila la aplicación, lo implementa en el sitio que se especifica en la propiedad **Dirección URL del sitio** del proyecto **QuickStatus** y se muestra una página que le pregunta si confía en la aplicación. Al continuar y, a continuación, salga de la aplicación **QuickStatus** , devuelve a la página de tareas en Project Web App. 

> [!NOTE]
> La figura 7 muestra que el botón de **Estado rápido** en la ficha **tareas** de la cinta de opciones está deshabilitado. Una vez muchas depuración las implementaciones con Visual Studio, se pueden bloquear los controles de la cinta de opciones personalizada al continuar con la depuración o implementar la aplicación publicada en el mismo servidor de prueba. Para habilitar el botón, eliminar el elemento **RibbonQuickStatusAction** en Visual Studio y, a continuación, cree una nueva acción de la cinta de opciones que tiene un nombre diferente y el identificador. Si no se soluciona el problema, intente quitar la aplicación de la instancia de prueba de Project Web App y, a continuación, vuelva a crear la aplicación con un identificador de aplicación diferentes. 
  
**Ilustración 7. Visualización de la información sobre herramientas del botón Quick Status deshabilitado**

![Visualización de la información sobre herramientas del botón deshabilitado] (media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Visualización de la información sobre herramientas del botón deshabilitado")
  
El procedimiento 5 muestra cómo implementar e instalar la aplicación **QuickStatus**. El procedimiento 6 muestra algunos pasos adicionales a la hora de probar la aplicación una vez instalada. 

<a name="pj15_StatusingApp_Deploying"> </a>

## <a name="deploying-the-quickstatus-app"></a>Implementación de la aplicación QuickStatus

Hay varias maneras de implementar una aplicación en una aplicación web de SharePoint como Project Web App. Qué implementación que utilice dependerá de si desea publicar la aplicación en un catálogo privado de SharePoint o en la tienda de Office pública, y si está instalado SharePoint local o es un arrendamiento de en línea. Procedimiento 5 muestra cómo implementar la aplicación **QuickStatus** a una instalación local en un catálogo de aplicaciones privada. Para obtener más información, vea [instalar y administrar aplicaciones para SharePoint 2013](https://technet.microsoft.com/library/fp161232.aspx) y [publicar aplicaciones para SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)
  
> [!NOTE]
> La adición de una aplicación a un catálogo de SharePoint exige permisos de administrador de SharePoint. 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a>Procedimiento 5. Implementar la aplicación QuickStatus

1. En Visual Studio, guarde todos los archivos y luego haga clic con el botón secundario en el proyecto **QuickStatus** del **Explorador de soluciones** y seleccione **Publicar**.
    
2. Dado que la aplicación **QuickStatus** está hospedada por SharePoint, hay muy pocas opciones para publicar (ilustración 8). En el cuadro de diálogo **Publicar aplicaciones para Office y SharePoint**, seleccione **Finalizar**.
    
   **Ilustración 8. Publicación de la aplicación QuickStatus**

   ![Mediante el Asistente para publicación] (media/pj15_CreateStatusingApp_PublishWizard.gif "Mediante el Asistente para publicación")
  
3. Copie el archivo QuickStatus.app desde el `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` directorio a un directorio adecuado en el equipo local (o en el equipo de SharePoint para una instalación local). 
    
4. En Administración central de SharePoint, seleccione **Aplicaciones** en el Inicio rápido y, luego, **Administrar catálogo de aplicaciones**.
    
5. Si no existe un catálogo de aplicaciones, cree una colección de sitios para el catálogo de aplicaciones, siguiendo la sección *Configurar el sitio del catálogo de aplicaciones para una aplicación web* en [administrar el catálogo de aplicaciones en SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx).
    
   Si no existe un catálogo de aplicaciones, vaya a la dirección URL del sitio en la página Administrar catálogo de aplicaciones. Por ejemplo, en los pasos siguientes, el sitio del catálogo de aplicaciones es `https://ServerName/sites/TestApps`.
    
6. En la página del catálogo de aplicaciones, seleccione **Aplicaciones para SharePoint** en el Inicio rápido. En la página Aplicaciones para SharePoint, en la pestaña **ARCHIVOS** de la cinta de opciones, seleccione **Cargar documento**.
    
7. En el cuadro de diálogo **Agregar un documento**, busque el archivo QuickStatus.app, agregue comentarios de la versión y seleccione **Aceptar**.
    
8. Al agregar una aplicación, también puede agregar información local para la descripción de la aplicación, el icono y otra información. En el cuadro de diálogo **aplicaciones para SharePoint - QuickStatus.app** , agregue la información que desea mostrar para la aplicación en la colección de sitios de SharePoint. Por ejemplo, agregue la siguiente información: 
    
   1. Campo de **Descripción breve** : aplicación de prueba de estado rápido de tipo.
    
   2. Campo de **Descripción** : aplicación de prueba de tipo para actualizar el porcentaje completado de tareas en varios proyectos.
    
   3. Los campos de la **Dirección URL del icono** : agregar una imagen de 96 x 96 píxeles para el icono de la aplicación a los activos del sitio para el catálogo de aplicaciones. Por ejemplo, vaya a `https://ServerName/sites/TestApps`, elija **contenido del sitio** en el menú de lista desplegable **configuración** , elija **Activos del sitio**y, a continuación, agregue la imagen quickStatusApp.png. Haga clic en el elemento **quickStatusApp** , elija **Propiedades**y, a continuación, copie el valor de la **Dirección (URL)** en el cuadro de diálogo de **Propiedades** . Por ejemplo, copie `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`y, a continuación, pegue el valor en el campo de dirección **URL de icono** web. Escriba una descripción para el icono, por ejemplo (como se muestra en la figura 9), escriba el icono de la aplicación QuickStatus. Probar que la dirección URL es válida.
    
      **Ilustración 9. Adición de una dirección URL de icono para la aplicación QuickStatus**

      ![Establecer las propiedades de SharePoint para la aplicación] (media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Establecer las propiedades de SharePoint para la aplicación")
  
   4. Campo de **categoría** : elija una categoría existente, o especifique su propio valor. Por ejemplo, escriba estado.
    
      > [!NOTE]
      > Una categoría llamada **Estado** es solo para fines de prueba. Una categoría típica de las aplicaciones de Project Server es **Administración de proyectos**. 
  
   5. **Nombre del publicador de** campo: escriba el nombre del publicador. En este ejemplo, escriba SDK de Project.
    
   6. Campo **habilitado** : para que la aplicación sea visible para los administradores de sitios de Project Web App para la instalación, seleccione la casilla de verificación **habilitado** . 
    
   7. Los campos adicionales son opcionales. Por ejemplo, puede agregar una dirección URL de soporte y varias imágenes de ayuda para la página de detalles de la aplicación. En la ilustración 9, los campos **Dirección URL de la imagen 1** incluyen la dirección URL de una captura de pantalla de la aplicación y una descripción de la misma. 
    
   8. En el cuadro de diálogo **aplicaciones para SharePoint - QuickStatus.app** , elija **Guardar**. En la figura 9, el elemento **Rápida actualización del estado** de las aplicaciones para la biblioteca de SharePoint está desprotegida para su edición, así sucesivamente la ficha **Editar** de la cinta de opciones del cuadro de diálogo, decide **Proteger** para completar el proceso (vea la figura 10). 
    
      **Ilustración 10. La aplicación QuickStatus se agrega a la biblioteca Aplicaciones para SharePoint.**

      ![Aplicación del QuickStatus se agrega a SharePoint] (media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "Aplicación del QuickStatus se agrega a SharePoint")
  
9. En Project Web App, en el menú desplegable **configuración** , elija **Agregar una aplicación**. En la página de sus aplicaciones, en Inicio rápido, elija **De su organización**y, a continuación, elija **Detalles de la aplicación** para la aplicación de **Actualización de estado rápida** . La figura 11 muestra la página de detalles con el icono de la aplicación, captura de pantalla y otra información que agregó en el paso anterior. 
    
   **Ilustración 11. Empleo de la página de detalles Actualización de estado rápida en Project Web App**

   ![Adición de la aplicación QuickStatus a Project Web App] (media/pj15_CreateStatusingApp_AddAppToPWA.gif "Adición de la aplicación QuickStatus a Project Web App")
  
10. En la página de detalles de la actualización del estado rápido, seleccione **Agregar**. Project Web App muestra un cuadro de diálogo que muestra las operaciones que puede llevar a cabo la aplicación QuickStatus (vea la figura 12). La lista de operaciones se deriva de los elementos de **AppPermissionRequest** en el archivo AppManifest.xml. 
    
    **Ilustración 12. Verificación de la confianza en la aplicación Quick Status**

    ![Comprobar la confianza de la aplicación QuickStatus] (media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Comprobar la confianza de la aplicación QuickStatus")
  
11. En el cuadro de diálogo **¿confía rápida actualización de estado** , elija **Confianza**. La aplicación se agrega a la página contenido del sitio de Project Web App (vea la figura 13).
    
    **Ilustración 13. Visualización de la aplicación Quick Status en la página Contenido del sitio**

    ![Visualización de la aplicación QuickStatus en contenidos del sitio] (media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Visualización de la aplicación QuickStatus en contenidos del sitio")
  
En la página Contenido del sitio, puede seleccionar el icono **Actualización de estado rápida** para ejecutar la aplicación.

> [!NOTE]
> Para los comandos adicionales que proporcionan información acerca de la aplicación, en la página contenido del sitio, elija la región que contiene el nombre de la **Actualización de estado rápido** y los puntos suspensivos (...). Puede revisar la página acerca de la aplicación, ver la página de detalles de la aplicación que contiene información acerca de los errores de aplicación, revise la página de permisos de aplicación o quitar la aplicación de Project Web App. 
  
En la página de tareas en Project Web App (vea la figura 14), el botón **QuickStatus** debería estar habilitado en la cinta de opciones. Si se deshabilita el botón de **Estado rápida** , pruebe las acciones que se describen en la nota de la figura 7. 

**Ilustración 14. Inicio de la aplicación QuickStatus desde la pestaña TAREAS**

![Iniciar la aplicación QuickStatus desde la pestaña tareas] (media/pj15_CreateStatusingApp_TasksRibbon.gif "Iniciar la aplicación QuickStatus desde la pestaña tareas")
  
El procedimiento 6 muestra algunas pruebas que se pueden realizar con la aplicación QuickStatus.

<a name="pj15_StatusingApp_Testing"> </a>

## <a name="testing-the-quickstatus-app"></a>Prueba de la aplicación QuickStatus

Deben probar todas las operaciones que es posible que intente un usuario en la aplicación **QuickStatus** en una instalación de prueba de Project Server antes de implementar la aplicación en un servidor de producción o en un inquilino de producción de Project Online. Una instalación de prueba permite cambiar y eliminar las asignaciones para los usuarios sin que ello afecte a proyectos real. Las pruebas, también deben incluir a varios usuarios que tienen distintos conjuntos de permisos, como administrador, jefe de proyecto y miembro del equipo. Rigurosa comprobación puede revelar los cambios que se deben realizar en la aplicación, que no eran obvias en las pruebas durante el desarrollo. Procedimiento 6 muestra varias pruebas para la aplicación **QuickStatus** , pero no incluye una serie de pruebas exhaustiva. 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a>Procedimiento 6. Probar la aplicación QuickStatus

1. Ejecute la aplicación **QuickStatus** en un escenario en el que el usuario no tenga asignaciones. La aplicación debería mostrar un mensaje azul en la parte inferior de la página, por ejemplo, **El nombre de usuario no tiene asignaciones**.
    
   Seleccione **Actualizar** y el mensaje cambia a uno verde **Se han actualizado las asignaciones**.
    
   > [!NOTE]
   > El comportamiento de la aplicación debería cambiarse de modo que el botón **Actualizar** se deshabilite si no hay asignaciones. 
  
2. Ejecute la aplicación en un escenario en el que el usuario tenga varias asignaciones en varios proyectos distintos y algunas no estén terminadas. Observe el aspecto de la aplicación y realice las acciones siguientes (ilustración 15):
    
   1. La función **onGetAssignmentsSuccess** crea una fila en la tabla para cada asignación del usuario actual. El nombre del proyecto solo aparece una vez, en negrita, para la primera asignación de cada proyecto. 
    
   2. Desactive la casilla de verificación del encabezado de columna **Nombre de tarea**. El controlador de eventos clic del encabezado de columna desactiva las demás casillas de verificación de las filas de tareas. 
    
   3. Seleccione todas las tareas. El controlador de eventos clic de cada fila determina si se seleccionan todas las filas y, si es así, selecciona el encabezado de columna **Nombre de tarea**. 
    
   4. Vuelva a desactivar todas las casillas de verificación y seleccione una asignación que tenga algún trabajo restante. Por ejemplo, la ilustración 15 muestra que la tarea superior T1 tiene un 20 % de trabajo restante para finalizar.
    
   5. En el cuadro de texto **Establecer porcentaje completado** , escriba 80 y, a continuación, seleccione **Actualizar**. La parte inferior de la página debe mostrar un mensaje de verde, **se han actualizado las asignaciones**.
    
      **Ilustración 15. Actualización de una asignación en la aplicación QuickStatus**

      ![Actualizar una asignación en la aplicación QuickStatus] (media/pj15_CreateStatusingApp_Testing1Update.gif "Actualizar una asignación en la aplicación QuickStatus")
  
3. Seleccione **Actualizar** (ilustración 16). Todas las tareas están seleccionadas de nuevo y la tarea superior muestra 80 % completado. 
    
      **Ilustración 16. Actualización de la página Actualización de estado rápida**

      ![Actualizar la página de QuickStatus] (media/pj15_CreateStatusingApp_Testing2Refresh.gif "Actualizar la página de QuickStatus")
  
4. Desactive todas las casillas de verificación y luego seleccione otra tarea. Por ejemplo, seleccione **Nueva tarea de PWA**. Deje vacío el cuadro de texto **Establecer el porcentaje completado**, elimine todo el texto de la columna **% completado** de la tarea seleccionada y seleccione **Actualizar**. Dado que ambos cuadros de texto están vacíos, la aplicación muestra un mensaje de error rojo (ilustración 17).
    
      **Ilustración 17. Prueba del mensaje de error**

      ![El mensaje de error de la prueba] (media/pj15_CreateStatusingApp_Testing3Error.gif "El mensaje de error de la prueba")
  
5. Actualización de la tarea anterior al 80% completado y, a continuación, elija **Salir**. La función **exitToPwa** cambia la ubicación de la ventana de explorador a la página de tareas en la aplicación host de SharePoint (es decir, cambia la dirección URL a https://ServerName/pwa/Tasks.aspx). La figura 18 muestra que la tarea **T1** y la tarea **nueva tarea desde Project Web Access** muestran el 80% completado. 
    
      **Ilustración 18. Verificación de que las tareas están actualizadas en Project Web App**

      ![Comprobar las tareas actualizadas en Project Web App] (media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Comprobar las tareas actualizadas en Project Web App")
  
6. Antes de que se muestra el estado actualizado en Project Professional 2013, los cambios deben envían para su aprobación y, a continuación, aprobados por el jefe de proyecto.
    
Las pruebas revelan varios otros cambios que tendrían que realizarse en la aplicación **QuickStatus** para un mejor uso. Por ejemplo:

- Debería haber comprobaciones de errores adicionales y validación de valores de cuadros de texto. En la actualidad, un usuario puede especificar un valor no numérico o negativo como porcentaje completado, lo que da lugar a un mensaje de error poco descriptivo. Por ejemplo, con un valor negativo, el mensaje de error es **Error al actualizar las asignaciones: PJClientCallableException: StatusingSetDataValueInvalid**.
    
- El mensaje de error de los cuadros de texto en blanco podría enumerar el proyecto y la tarea, además del número de fila.
    
- El mensaje de correcto podría incluir una lista de las tareas actualizadas; o si la función **updateAssignments** es correcta, podría realizar una actualización de página automática y mostrar las tareas o los porcentajes actualizados en otro color y en negrita. 
    
- Para evitar una tabla muy grande, la tabla de asignaciones debería limitarse a las tareas que tienen menos de un 100 % completado. O bien, agregar una opción para mostrar todas las tareas. Este problema también se podría solucionar mediante el empleo de una cuadrícula basada en jQuery en lugar de una tabla, donde es posible implementar fácilmente el filtrado y la paginación de cuadrícula.
    
- Dado que la aplicación **QuickStatus** no envía el estado, el icono **Quick Status** de la pestaña **TAREAS** de la cinta de opciones sería más lógicamente el primer icono del grupo **Tareas**, en lugar del último del grupo **Enviar**. 
    
- Dado que la función **onGetAssignmentsSuccess** inicializa el texto del botón **btnSubmitUpdate**, pero los valores de texto de los otros botones son inicializados en HTML, la página se deja en un estado parcialmente inicializado mientras se ejecuta la función **getAssignments**. Los botones de la página parecerían más coherentes si todos los valores de texto se inicializaran en HTML. 
    
Lo que es más importante, el enfoque que emplea la aplicación **QuickStatus**, donde cambia el porcentaje completado de las asignaciones, debería revisarse en una aplicación de producción. Para obtener más información, consulte la sección [Siguientes pasos](#pj15_StatusingApp_NextSteps). 

<a name="pj15_StatusingApp_Example"> </a>

## <a name="example-code-for-the-quickstatus-app"></a>Código de ejemplo de la aplicación QuickStatus

### <a name="defaultaspx-file"></a>Archivo default.aspx

El siguiente código se encuentra en la `Pages\Default.aspx` archivo del proyecto **QuickStatus** : 
  
```HTML
    <%-- The following lines are ASP.NET directives needed when using SharePoint components --%>
    <%@ Page Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" MasterPageFile="~masterurl/default.master" Language="C#" %>
    <%@ Register TagPrefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%-- The markup and script in the following Content element will be placed in the <head> of the page.
        For production deployment, change the .debug.js JavaScript references to .js. --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
    <!-- CSS styles -->
    <link rel="Stylesheet" type="text/css" href="../Content/App.css" />
    <!-- Add your JavaScript to the following file -->
    <script type="text/javascript" src="../Scripts/App.js"></script>
    </asp:Content>
    <%-- The markup and script in the following Content element will be placed in the <body> of the page --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
    <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
    </div>
    </form>
    </asp:Content>
```

<br/>

### <a name="appjs-file"></a>Archivo app.js

El siguiente código se encuentra en la `Scripts\App.js` archivo del proyecto **QuickStatus** : 
  
```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the selected state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
    // Get information about the current user.
    function getUserInfo() {
        projUser = pwaWeb.get_currentUser();
        projContext.load(projUser);
        projContext.executeQueryAsync(onGetUserNameSuccess,
            // Anonymous function to execute if getUserInfo fails.
            function (sender, args) {
                alert('Failed to get user name. Error: ' + args.get_message());
        });
    }
    // This function is executed if the getUserInfo call is successful.
    // Replace the contents of the 'caption' paragraph with the project user name.
    function onGetUserNameSuccess() {
        var prefaceInfo = 'Assignments for ' + projUser.get_title();
        $('#tableCaption').text(prefaceInfo);
    }
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
    // Get the enumerator, iterate through the assignment collection, 
    // and add each assignment to the table.
    function onGetAssignmentsSuccess(sender, args) {
        if (assignments.get_count() > 0) {
            var assignmentsEnumerator = assignments.getEnumerator();
            var projName = "";
            var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
            var taskNum = 0;
            var chkTask = "";
            var txtPctComplete = "";
            // Constants for creating input controls in the table.
            var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
            var LBLCHK = '<label for="chk';
            var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
            while (assignmentsEnumerator.moveNext()) {
                var statusAssignment = assignmentsEnumerator.get_current();
                projName = statusAssignment.get_project().get_name();
                // Get an integer value for the number of milliseconds of actual work, such as 3600000.
                var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds();
                // Get a string value for the assignment actual work, such as "1h". Not used here.
                var actualWork = statusAssignment.get_actualWork();                         
                if (projName === prevProjName) {
                    projName = "";
                }
                prevProjName = statusAssignment.get_project().get_name();
                // Create a row for the assignment information.
                var row = assignmentsTable.insertRow();
                taskNum++;
                // Create an HTML string with a check box and task name label, for example:
                //     <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> 
                //     <label for="chk1">Task 1</label>
                chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">'
                    + statusAssignment.get_name() + '</label>';
                txtPctComplete = INPUTTXT + taskNum + '" />';
                // Insert cells for the assignment properties.
                row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                row.insertCell().innerHTML = chkTask;
                row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                row.insertCell().innerHTML = txtPctComplete;
                row.insertCell().innerText = statusAssignment.get_remainingWork();
                row.insertCell().innerText = statusAssignment.get_finish();
                // Initialize the percent complete cell.
                $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
            }
        }
        else {
            $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
            $get("message").innerText = projUser.get_title() + ' has no assignments'
        }
        // Initialize the button properties.
        $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
        $get("btnSubmitUpdate").innerText = 'Update';
        $get('btnRefresh').onclick = function () { window.location.reload(true); };
        $get('btnExit').onclick = function () { exitToPwa(); };
    }
    // Update all selected assignments. If the bottom percent complete field is blank,
    // use the value in the % complete field of each selected row in the table.
    function updateAssignments() {
        // Get percent complete from the bottom text box.
        var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
        var pctComplete = pctCompleteMain;
        var assignmentsEnumerator = assignments.getEnumerator();
        var taskNum = 0;
        var taskRow = "";
        var indexPercent = "";
        var doSubmit = true;
        while (assignmentsEnumerator.moveNext()) {
            var pctCompleteRow = "";
            taskRow = "chk" + ++taskNum;
            if ($get(taskRow).checked) {
                var statusAssignment = assignmentsEnumerator.get_current();
                if (pctCompleteMain === "") {
                    // Get percent complete from the text box field in the table row.
                    pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                    pctComplete = pctCompleteRow;
                }
                // If both percent complete fields are empty, show an error.
                if (pctCompleteMain === "" && pctCompleteRow === "") {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerHTML =
                        '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                        + taskNum
                        + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                        + '<p>Please refresh the page and try again.</p>';
                    doSubmit = false;
                    taskNum = 0;
                    break;
                }
                if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
            }
        } 
        // Save and submit the assignment updates.
        if (doSubmit) {
            assignments.update();
            assignments.submitAllStatusUpdates();
            projContext.executeQueryAsync(function (source, args) {
                $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                $get("message").innerText = 'Assignments have been updated.';
            }, function (source, args) {
                $('p#message').attr('style', 'color: #e11500');     // Red text.
                $get("message").innerText = 'Error updating assignments: ' + args.get_message();
            });
        }
    }
    // Get the numeric part for percent complete, from a string. 
    // For example, with "20 %", return "20".
    function getNumericValue(pctComplete) {
        pctComplete = pctComplete.trim();
        pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
        indexPercent = pctComplete.indexOf('%', 0);
        if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
        return pctComplete;
    }
    // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
    function exitToPwa() {
        // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
        var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                        + "/Tasks.aspx";
        // Set the top window for the QuickStatus IFrame to the Tasks page.
        window.top.location.href = spHostUrl;
    }
    // Get a specified query string parameter from the {StandardTokens} URL option string.
    function getQueryStringParameter(urlParameterKey) {
        var docUrl = document.URL;
        var params = docUrl.split('?')[1].split('&');
        for (var i = 0; i < params.length; i++) {
            var theParam = params[i].split('=');
            if (theParam[0] == urlParameterKey)
                return decodeURIComponent(theParam[1]);
        }
    }
```

<br/>

### <a name="appcss-file"></a>Archivo app.CSS

El siguiente código CSS se encuentra en la `Content\App.css` archivo del proyecto **QuickStatus** : 
  
```css
    /* Custom styles for the QuickStatus app. */
    /*============= Table elements ========================================*/
    table {
        width: 90%;
    }
    caption {
        font-size: 16px;
        padding-bottom: 5px;
        font-weight: bold;
        color: gray;
    }
    table th {
        background-color: gray;
        color: white;
    }
    table td, th {
        width: auto;
        text-align: left;
        padding: 2px;
        border: solid 1px whitesmoke;
        color: gray;
    }
    /*=== Class for check boxes added to rows 
    */
    .chkTask {
        width: 12px;
        height: 12px;
        color: gray;
    }
    /*========== DIV id for the Percent Complete text box ================*/
    #inputPercentComplete {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 20px;
        margin-left: 30px;
    }
    /*========== DIV id for the Submit Result button ====================*/
    #submitResult {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
    }
    /*========== DIV id for the Refresh Page button ====================*/
    #refreshPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 120px;
    }
    /*========== DIV id for the Exit Page button ====================*/
    #exitPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 240px;
    }
    /*========== Class for the buttons at the bottom of the page =======*/
    .bottomButtons {
        color: gray;
        font-weight: bold; 
        font-size: 12px; 
        border-color: darkgreen;
        border-width: thin;
    }
```

<br/>

### <a name="elementsxml-file-for-the-ribbon"></a>Archivo Elements.XML de la cinta de opciones

La siguiente definición de XML para el se ha agregado un botón en la ficha **tareas** en la cinta de opciones, que se encuentra en la `RibbonQuickStatusAction\Elements.xml` archivo del proyecto **QuickStatus** : 
  
```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="https://schemas.microsoft.com/sharepoint/">
    <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon">
        <CommandUIExtension>
        <!-- 
        Add a button that invokes the QuickStatus app. The Quick Status button is displayed as  
        the third control in the Page group (the group title is "Submit").
        -->
        <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invokae_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="Quick Status"
                    ToolTipDescription="Run the QuickStatus app" />
            </CommandUIDefinition>
        </CommandUIDefinitions>
        <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_QuickStatus"
                            CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
        </CommandUIHandlers>
        </CommandUIExtension >
    </CustomAction>
    </Elements>
```

<br/>

### <a name="appmanifestxml-file"></a>Archivo AppManifest.xml

El siguiente es el código XML para el manifiesto de la aplicación del proyecto **QuickStatus** , que incluye los dos ámbitos de solicitud de permisos que son necesarios para actualizar el estado de la asignación del usuario de la aplicación en varios proyectos: 
  
```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <!--Created:cb85b80c-f585-40ff-8bfc-12ff4d0e34a9-->
    <App xmlns="https://schemas.microsoft.com/sharepoint/2012/app/manifest"
        Name="QuickStatus"
        ProductID="{bbc497e7-1221-4d7b-a0ae-141a99546008}"
        Version="1.0.0.0"
        SharePointMinVersion="15.0.0.0"
    >
    <Properties>
        <Title>Quick Status Update</Title>
        <StartPage>~appWebUrl/Pages/Default.aspx?{StandardTokens}</StartPage>
    </Properties>
    <AppPrincipal>
        <Internal />
    </AppPrincipal>
    <AppPermissionRequests>
        <AppPermissionRequest Scope="https://sharepoint/projectserver/statusing" Right="SubmitStatus" />
        <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Read" />
    </AppPermissionRequests>
    </App>
```

<br/>

### <a name="appiconpng-file"></a>Archivo AppIcon.png

La solución de Visual Studio completa para la aplicación **QuickStatus** incluye un archivo AppIcon.png personalizado. La solución se incluirán en la descarga del SDK de Project 2013. 

<a name="pj15_StatusingApp_NextSteps"> </a>

## <a name="next-steps"></a>Siguientes pasos

La aplicación **QuickStatus** es un ejemplo de cómo escribir aplicaciones que se pueden instalar en Project Server 2013 y Project Online relativamente simple. La sección de [prueba de la aplicación QuickStatus](#pj15_StatusingApp_Testing) enumera varias mejoras que se pueden realizar para facilidad de uso. La aplicación **QuickStatus** utiliza las funciones de JavaScript para actualizar el estado de asignación de Project Web App. Pero, cambiar el porcentaje completado de la asignación no es una práctica de administración recomendado de proyecto. Otro enfoque sería actualizar la fecha de comienzo real y la duración restante de las tareas asignadas. Para obtener una descripción de los problemas, consulte [Actualización mejor](https://www.mpug.com/articles/update-better) en el boletín de seguridad MPUG. 

<a name="pj15_StatusingApp_AdditionalResources"> </a>

## <a name="see-also"></a>Vea también

- [Tareas de programación de Project Server ](project-programming-tasks.md)
- [Complementos de SharePoint](https://msdn.microsoft.com/library/jj163230.aspx)
- [Administración de actualizaciones de tareas en Project Web App](https://technet.microsoft.com/en-us/library/hh767481%28v=office.14%29.aspx)
- [Crear acciones personalizadas para implementar complementos de SharePoint](https://msdn.microsoft.com/library/jj163954.aspx)
    

