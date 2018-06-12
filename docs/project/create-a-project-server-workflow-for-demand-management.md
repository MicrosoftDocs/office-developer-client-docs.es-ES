---
title: Crear un flujo de trabajo de Project Server para la administración de propuestas
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: b0e4a3b3-d1df-454d-b74c-b980b0b456f6
description: En este artículo se describe cómo crear un flujo de trabajo simple mediante el uso de SharePoint Designer 2013.
ms.openlocfilehash: d548cbc47585add2648396f4736e6ad36a00bcb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821324"
---
# <a name="create-a-project-server-workflow-for-demand-management"></a>Crear un flujo de trabajo de Project Server para la administración de propuestas

En este artículo se describe cómo crear un flujo de trabajo simple mediante el uso de SharePoint Designer 2013. Puede exportar el flujo de trabajo a Visio 2013 para la visualización y edición, o usar Visio 2013 para los flujos de trabajo de Project Server 2013 de diseño e importar el diseño en SharePoint Designer 2013 publicación para Project Web App. Para obtener más información acerca de la plataforma de flujo de trabajo de SharePoint y la creación de flujos de trabajo con Visio 2013 y SharePoint Designer 2013, vea los artículos de [flujos de trabajo en SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163986%28office.15%29.aspx) en la documentación para desarrolladores de SharePoint 2013. 
  
Para obtener información sobre la preparación de Project Server para flujos de trabajo, consulte [iniciar: establecer seguridad y configuración del Administrador de flujo de trabajo de SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163276%28office.15%29.aspx).

<a name="pj15_CreateWorkflowSPD_General"> </a>

## <a name="creating-a-general-workflow"></a>Crear un flujo de trabajo general

Use los siguientes pasos para crear un flujo de trabajo de Project Server 2013 mediante SharePoint Designer 2013. El flujo de trabajo está diseñado para la administración de propuestas de propuestas de proyectos.
  
Para obtener instrucciones detalladas, vea la sección [creación de un flujo de trabajo de bifurcación](#pj15_CreateWorkflowSPD_Detailed) . 
  
### <a name="to-create-a-project-server-workflow-general-procedure"></a>Crear un flujo de trabajo de Project Server (procedimiento general)

1. Determine los requisitos y, después, diseñe el flujo de trabajo. Organícelo en fases y etapas y determine los campos personalizados que va a usar el flujo de trabajo.
    
2. En Project Web App, cree las entidades que requiere el flujo de trabajo:
    
    1. Revise las fases existentes del flujo de trabajo; cree fases según sea necesario.
        
    2. Cree los campos personalizados de empresa que va a usar el flujo de trabajo. Para estar disponibles en una etapa del flujo de trabajo, los campos personalizados deben estar controlados por un flujo de trabajo.
        
    3. Edite o cree las páginas de detalle del proyecto (PDP) que usarán las etapas del flujo de trabajo para recopilar información para el proyecto. En este ejemplo, las etapas usan PDP predeterminadas que se editan para incluir un nuevo campo personalizado.
        
    4. Cree las etapas necesarias del flujo de trabajo y después asocie cada etapa del flujo de trabajo con la fase correcta.
    
3. En SharePoint Designer 2013, construya el flujo de trabajo mediante el uso de instrucciones declarativas en el **Diseñador basado en texto**:
    
    > [!NOTE]
    > También puede cambiar el **Diseñador Visual** en SharePoint Designer 2013 o importar un flujo de trabajo existente de Visio 2013. Siga estos pasos para usar el **Diseñador basado en texto**: 
    > 
    > 1. Abra el sitio de Project Web App y, a continuación, cree un flujo de trabajo de sitio que usa la plataforma de flujo de trabajo de **Flujo de trabajo de SharePoint 2013 - Project Server** . 
    > 2. Agregue las etapas que usa el flujo de trabajo.
    > 3. Inserte los pasos, condiciones, acciones y bucles del flujo de trabajo que se necesitan en cada etapa.
    > 4. Busque si hay errores en el flujo de trabajo y corrija los que encuentre.
    > 5. (Opcional) Cambiar la vista para el **Diseñador Visual**o exportar el flujo de trabajo a un archivo de Visio 2013. Puede modificar la vista de Visio y guardar los cambios en el flujo de trabajo actual. Puede editar el archivo de Visio e importarlo en SharePoint Designer 2013 para crear otros flujos de trabajo.
    > 6. Publicar el flujo de trabajo. Después de publicar, el flujo de trabajo se muestra en la lista de flujos de trabajo para el sitio de Project Web App.
    
4. En Project Web App, use el flujo de trabajo para la administración de propuestas de propuestas de proyectos:
    
    1. Cree una plantilla de proyecto empresarial (EPT) que use el flujo de trabajo.
        
    2. En la página Centro de proyectos, cree un proyecto que use la plantilla EPT para el flujo de trabajo y siga las etapas del flujo de trabajo.
        
    3. Pruebe el flujo de trabajo a fondo.
        
    4. Implemente el flujo de trabajo en un servidor de producción.

<a name="pj15_CreateWorkflowSPD_Detailed"> </a>

## <a name="creating-a-branching-workflow"></a>Crear un flujo de trabajo de bifurcación

Antes de que puede usar SharePoint Designer 2013 para crear un flujo de trabajo de Project Server, el servicio 1.0 de cliente del Administrador de flujo de trabajo debe configurarse para usar las actividades de flujo de trabajo de Project Server 2013. Para obtener información acerca de cómo configurar el flujo de trabajo de administrador de Client 1.0, vea los artículos de [flujos de trabajo en SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163986%28office.15%29.aspx) en la documentación para desarrolladores de SharePoint Server 2013. 
  
El siguiente procedimiento detallado incluye los mismos pasos que en la sección [creación de un flujo de trabajo general](#pj15_CreateWorkflowSPD_General) . 
  
### <a name="to-create-a-project-server-branching-workflow-detailed-procedure"></a>Procedimiento para crear un flujo de trabajo de bifurcación de Project Server (procedimiento detallado)

#### <a name="1-plan-and-design-the-workflow"></a>1. planear y diseñar el flujo de trabajo.

Un flujo de trabajo de Project Server se puede integrar con varias etapas y fases de un proceso de administración de propuestas. Debido a que los flujos de trabajo pueden ser complicadas, debe comprender los requisitos de negocio y planear cuidadosamente un flujo de trabajo. Para obtener un ejemplo simple, diseñar un flujo de trabajo de bifurcación que utiliza el costo estimado de una propuesta de proyecto para determinar si se acepta la propuesta. Si el costo estimado es mayor que $ 25.000, rechazar la propuesta; de lo contrario, acepte la propuesta y crear el proyecto.
    
Debido a que puede usar Visio 2013 y SharePoint Designer 2013 para ayudarle a diseñar y crear flujos de trabajo de Project Server 2013, puede experimentar más fácilmente con los flujos de trabajo que es posible con Project Server 2010. El diseño de flujo de trabajo de ejemplo en este artículo es la misma que en el artículo [crear un flujo de trabajo de bifurcación](http://msdn.microsoft.com/library/a02cafdc-d881-4271-b446-d8b2cd456a52%28Office.15%29.aspx) en el SDK de Project 2010. Puede diseñar y crear un flujo de trabajo de prueba en un equipo remoto mediante una instancia de prueba de Project Web App: no es necesario que crear flujos de trabajo directamente en un equipo de Project Server 2013. 
    
#### <a name="2-create-the-entities-that-your-workflow-requires"></a>2. Cree las entidades que requiere el flujo de trabajo.

En Project Web App, revise las fases de flujo de trabajo disponibles y las fases y los campos personalizados de empresa que están disponibles. Si es necesario, cree las entidades que requiere el flujo de trabajo, como se muestra en los siguientes pasos:
    
1. **Fases de flujo de trabajo** La instalación predeterminada de Project Web App incluye la creación, seleccionar, fases de planeación, administrar y terminadas. Para el ejemplo de flujo de trabajo de bifurcación, no es necesario crear otras fases. 
        
2. **Campos personalizados de empresa** El flujo de trabajo de bifurcación requiere un campo personalizado de costo de proyecto que está controlado por el flujo de trabajo. El valor de un campo personalizado controlado por el flujo de trabajo se establece en un PDP que usa el flujo de trabajo. Por ejemplo, elija el icono de **configuración** en la parte superior derecha de una página de Project Web App, elija **Configuración de PWA**y, a continuación, elija los **campos personalizados de empresa y tablas de búsqueda**.
        
   Crear un campo personalizado denominado costo de la propuesta para la entidad de **proyecto** y seleccione el tipo de **costo**. Para la descripción, escriba el costo estimado de una propuesta de proyecto. En la sección **comportamiento** , seleccione el **comportamiento controlado por flujo de trabajo**.
        
3. **Páginas de detalles del proyecto** Editar o crear el PDP que va a usar las etapas de flujo de trabajo. Por ejemplo, realice los siguientes pasos: 
        
    1. Elija **Páginas de detalles del proyecto** en la página Configuración del servidor y, a continuación, elija la PDP **ProjectInformation** . 
            
    2. En **la ficha de la cinta de opciones, en el grupo **Editar** ,** elija **Editar página**.
            
    3. Elija la flecha hacia abajo en la esquina superior derecha del elemento web **Información básica** y, a continuación, elija **Editar elemento web**. O bien, en la ficha de **Elemento WEB** de la cinta de opciones, en el grupo **Propiedades** , elija **el elemento web propiedades** para mostrar el elemento de editor. 
            
    4. En los **Campos de proyecto mostrados** sección del editor part (vea la figura 1), seleccione **Modificar**.
            
    5. Agregue el campo personalizado de **Costo de la propuesta** , muévalo encima del campo de **propietario** en la lista de **Campos de proyecto seleccionados** y, a continuación, elija **Aceptar** (vea la figura 1).
      
    6. En el elemento de editor, haga **clic en Aceptar**y, a continuación, elija **Detener la edición** en el grupo **Editar** , en la ficha de **página** de la cinta de opciones. La figura 2 muestra el campo personalizado de **Costo de la propuesta** que se agrega a la PDP de información del proyecto. 

    **En la figura 1. Edición del elemento web de los campos de proyecto en un PDP**

    ![Modificar los campos de proyecto de elemento en un PDP web] (media/pj15_CreateWorkflowSPD_EditPDP.gif "Modificar los campos de proyecto de elemento en un PDP web")

    **La figura 2. El PDP editado incluye el campo personalizado de costo de la propuesta**

    ![El PDP editado incluye el campo Costo de la propuesta] (media/pj15_CreateWorkflowSPD_EditedPDP.gif "El PDP editado incluye el campo Costo de la propuesta")
  
4. **Etapas de flujo de trabajo** Cree las etapas que son necesarias para cada fase del flujo de trabajo. En la página Configuración del servidor, elija **Etapas de flujo de trabajo**y, a continuación, elija **Nueva etapa de flujo de trabajo**. La figura 3 muestra parte de la página Agregar etapa de flujo de trabajo.
    
    **La figura 3. Adición de una etapa de flujo de trabajo en Project Web App**

    ![Adición de una etapa de flujo de trabajo en Project Web App] (media/pj15_CreateWorkflowSPD_AddWorkflowStage.gif "Adición de una etapa de flujo de trabajo en Project Web App")
  
    El ejemplo de flujo de trabajo de bifurcación utiliza las cuatro etapas que se muestran en la tabla 1. En la sección de **Configuración adicional para la página de detalles del proyecto Visible** de la página Agregar etapa de flujo de trabajo (no se muestra en la figura 3), los valores son opcionales; proporcionan más información en la página Estado del flujo de trabajo. Por ejemplo, debido a que el PDP de detalles de propuesta inicial requiere la intervención del usuario, active la casilla de verificación de **la página de detalles del proyecto requiere atención** y, a continuación, agregue una descripción específica, como establece el nombre del proyecto y el costo para este PDP.
    
    En la Figura 4 se muestran las cuatro etapas completadas en la página Etapas de flujo del trabajo.
    
    **La tabla 1. Etapas del flujo de trabajo de bifurcación**

    |Nombre|Descripción|Descripción para envío|Fase|PDP visibles|Campos personalizados|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |Detalles de la propuesta iniciales  <br/> |Establezca el nombre y el costo del proyecto.  <br/> |Envíe el proyecto como propuesta.  <br/> |Crear  <br/> |Información del proyecto  <br/> Detalles de proyecto  <br/> |Costo de la propuesta (necesario)  <br/> |
    |Detalles de proyecto  <br/> |Proporcione detalles del proyecto propuesto.  <br/> |Envíe detalles para continuar con el proyecto.  <br/> |Crear  <br/> |Información del proyecto  <br/> Detalles de proyecto  <br/> |Costo de la propuesta (solo lectura)  <br/> |
    |Rechazo automatizado  <br/> |La propuesta se rechaza a partir de la información proporcionada.  <br/> | <br/> |Crear  <br/> |Información del proyecto  <br/> |Costo de la propuesta (solo lectura)  <br/> |
    |Ejecución  <br/> |La propuesta se acepta y está lista para la administración del proyecto.  <br/> | <br/> |Administrar  <br/> |Información del proyecto  <br/> Detalles de proyecto  <br/> |Costo de la propuesta (solo lectura)  <br/> |
   
    **La figura 4. Lista de las fases de flujo de trabajo en Project Web App**

    ![Lista de las fases de flujo de trabajo en Project Web App] (media/pj15_CreateWorkflowSPD_WorkflowStages.gif "Lista de las fases de flujo de trabajo en Project Web App")
  
#### <a name="3-construct-the-workflow-in-the-text-based-designer"></a>3. construir el flujo de trabajo en el diseñador basado en texto.

En SharePoint Designer 2013, construya el flujo de trabajo mediante el uso de instrucciones declarativas en el diseñador basado en texto. Puede comenzar a escribir en la línea de inserción naranja para obtener instrucciones de autocompletado sensible al contexto para la lógica de flujo de trabajo y los pasos, o puede insertar la lógica y los pasos mediante el uso de controles en el grupo **Insertar** en la ficha **flujo de trabajo** de la cinta de opciones. 
    
1. En la vista Backstage de SharePoint Designer 2013, elija **Abrir sitio**. Por ejemplo, abra `http://ServerName/pwa`. En el panel de **navegación** , elija **los flujos de trabajo**. A continuación, en la pestaña **flujos de trabajo** de la cinta de opciones, en el grupo **nuevo** , elija **Flujo de trabajo de sitio**. Para este ejemplo, el nombre del flujo de trabajo de flujo de trabajo de bifurcación. Asegúrese de que el **Flujo de trabajo de SharePoint 2013 - Project Server** esté seleccionado en la lista desplegable **Tipo de plataforma** (vea la figura 5). 
    
    **La figura 5. Creación de un flujo de trabajo del sitio de Project Server**

    ![Creación de un flujo de trabajo del sitio de Project Server] (media/pj15_CreateWorkflowSPD_CreateSiteWorkflow.gif "Creación de un flujo de trabajo del sitio de Project Server")
  
2. Seleccione la ficha **Flujo de trabajo de bifurcación** . A continuación, en la ficha **flujo de trabajo** de la cinta de opciones, en el grupo **Administrar** , en la lista desplegable de **vistas** , elija **Diseñador basado en texto**. Para mostrar la vista con el naranja intermitente de inserción línea (vea la figura 6), haga clic en dentro de la vista.
    
    **La figura 6. Uso de la vista de diseñador basado en texto para el flujo de trabajo**

    ![Uso de la vista Diseñador basado en texto] (media/pj15_CreateWorkflowSPD_TextBasedDesigner.gif "Uso de la vista Diseñador basado en texto")
  
3. En la vista **Diseñador basado en texto** , agregue las etapas que usa el flujo de trabajo. En la pestaña de **flujo de trabajo** de la cinta de opciones, en el grupo **Insertar** , en la lista desplegable de **fase** en **crear**, elija **Detalles de la propuesta iniciales**.
    
    De forma similar, coloque la línea de inserción naranja debajo del **etapa: detalles de la propuesta iniciales** cuadro y agregue las otras etapas que usa el flujo de trabajo: **Detalles del proyecto**, **Rechazo automatizado**y **ejecución** (vea la figura 7). 
    
    **La figura 7. Adición de una fase a un flujo de trabajo en SharePoint Designer**

    ![Adición de una fase a un flujo de trabajo en SPD] (media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Adición de una fase a un flujo de trabajo en SPD")
  
4. Agregue los pasos del flujo de trabajo y la lógica dentro de cada etapa: 
    
    1. En la etapa de **Detalles de la propuesta iniciales** , coloque la línea de inserción naranja en la parte superior del cuerpo del escenario. En el grupo **Insertar** de la cinta de opciones, elija **acción**, desplácese hacia abajo hasta **Acciones de Project Web App**y, a continuación, elija **esperar el evento del proyecto**. Elija **este evento de proyecto**y, a continuación, seleccione **evento: cuando se envía un proyecto** en la lista desplegable. 
    
    2. En la sección de **transición a la fase** de la fase de **Detalles de la propuesta iniciales** , inserte **Si cualquier valor es igual al valor**. Puede comenzar a escribir la instrucción o usar el control de **condición** en el grupo **Insertar** en la cinta de opciones. 
    
    3. Elija el primer control de **valor** y, a continuación, elija **fx** para mostrar el cuadro de diálogo **Definir búsqueda de flujo de trabajo** (vea la figura 8). En la lista desplegable **origen de datos** , seleccione **Datos del proyecto**. En la lista desplegable del **campo del origen** , seleccione el **Costo de la propuesta**.
    
       **La figura 8. Definición de un valor de búsqueda en el flujo de trabajo**

       ![Definición de un valor de búsqueda en el flujo de trabajo] (media/pj15_CreateWorkflowSPD_DefineWorkflowLookup.gif "Definición de un valor de búsqueda en el flujo de trabajo")
  
    4. Completar la `If` instrucción de modo que muestre lo siguiente: **costo de datos: propuesta de proyecto si es mayor que 25000**
    
       > [!NOTE]
       > Como alternativa, podría crear una variable de flujo de trabajo, establezca la variable en el valor de campo personalizado y, a continuación, compare la variable con un valor. Por ejemplo, en la lista desplegable de **Las Variables locales** en la cinta de opciones, cree una variable con el nombre **TotalCost** (sin espacios) del tipo **Number**. En el cuadro de diálogo **Definir búsqueda de flujo de trabajo** , seleccione **flujo de trabajo Variables y parámetros** para el origen de datos y, a continuación, seleccione **Variable: TotalCost** como el campo. La instrucción **If** , a continuación, sería: **If Variable: TotalCost es mayor que 25000**
  
    5. Coloque la línea de inserción naranja dentro de la `If` de sucursales y, a continuación, inserte **va a una fase** mediante el control de la **acción** , en el grupo **Insertar** en la cinta de opciones. Seleccione el control de lista desplegable de **una fase** y seleccione la fase de **Rechazo automático** . 
    
       De forma similar, en la `Else` de sucursales, inserte la instrucción **vaya a detalles del proyecto** . La figura 9 muestra la fase de **Detalles de la propuesta iniciales** completada. 
    
       **En la figura 9. Lógica completada para la fase de detalles de la propuesta iniciales**

       ![Lógica completada para detalles de la propuesta iniciales] (media/pj15_CreateWorkflowSPD_InitialStageLogic.gif "Lógica completada para detalles de la propuesta iniciales")
  
    6. En la fase de **Rechazo automático** , a menos que desea pausar el flujo de trabajo y mostrar algunos datos en un PDP, deje la primera sección vacía. La sección **transición a fase** debe contener una transición; debido a que no hay ningún otro fase siguiendo un rechazo, escriba Go al final del flujo de trabajo para la instrucción. 
    
    7. En la fase de **Detalles del proyecto** , agregue ir a la ejecución en la sección **realizar la transición a fase** . A menos que no hay datos adicionales para agregar o que desea pausar el flujo de trabajo, no es necesario esperar un evento enviado. 
    
    8. En la etapa de **ejecución** , a menos que desea pausar el flujo de trabajo, deje la sección acción de fase vacío. En la sección de **transición a fase** , agregue **Ir al final del flujo de trabajo**.
    
5. En el grupo **Guardar** en la cinta de opciones, elija **Buscar errores** para comprobar los errores de flujo de trabajo (vea la figura 10). Corrija los errores y, a continuación, elija **Guardar**.
    
    **La figura 10. Comprobar el flujo de trabajo para errores en SharePoint Designer**

    ![Comprobación de errores en el flujo de trabajo] (media/pj15_CreateWorkflowSPD_SPDCheckForErrors.gif "Comprobación de errores en el flujo de trabajo")
  
6. (Opcional) En el grupo **Administrar** de la cinta de opciones, en el menú desplegable de **vistas** , elija **Diseñador Visual**. En la figura 11, se acerca o aleja la vista de en el 50%.
    
    Puede editar elementos en el flujo de trabajo mediante el diseñador Visual. Por ejemplo, seleccione la condición **Si cualquier valor es igual al valor** , elija el icono de herramienta en la parte inferior izquierda de la condición y, a continuación, seleccione el **valor** para mostrar las condiciones de la comparación en el cuadro de diálogo **Propiedades** . 
    
    **La figura 11. Con el diseñador Visual para un flujo de trabajo**

    ![Uso de la vista de diseño de Visio del flujo de trabajo] (media/pj15_CreateWorkflowSPD_SwitchView.gif "Uso de la vista de diseño de Visio del flujo de trabajo")
  
    Cuando el flujo de trabajo está en la vista de diseñador Visual, para guardar el flujo de trabajo en un archivo de Visio 2013 (.vsdx) como una copia de seguridad o para utilizarlo más adelante, se puede elegir **Exportar a Visio**.
    
7. Publicar el flujo de trabajo. Al usar SharePoint Designer 2013 para publicar el flujo de trabajo en el sitio de Project Web App activo, el flujo de trabajo está registrado en el sitio de SharePoint o en Azure y pasa a estar disponible en Project Web App para EPT nuevo.

#### <a name="4-create-an-ept-for-the-workflow-and-then-test-the-workflow"></a>4. Cree una EPT para el flujo de trabajo y, a continuación, pruebe el flujo de trabajo.

En Project Web App, cree una EPT para el flujo de trabajo y, a continuación, pruebe el flujo de trabajo mediante la creación de una propuesta de proyecto:
    
1. En la página Configuración de PWA, elija **Tipos de proyecto empresarial**y, a continuación, cree una EPT con el nombre de flujo de trabajo de bifurcación de prueba. Desactive la casilla de verificación **crear nuevos proyectos como proyectos de lista de tareas de SharePoint** para que Project Server va a mantener el control total de los proyectos que se crean mediante la plantilla EPT. Seleccione **Flujo de trabajo de bifurcación** en la lista desplegable de **Asociación de flujo de trabajo de sitio** y, a continuación, seleccione la PDP **Información del proyecto** en la lista desplegable **Nueva página de proyecto** para que la primera página que se muestra el flujo de trabajo. 
    
    **La figura 12. Adición de un EPT para el flujo de trabajo**

    ![Adición de un EPT para el flujo de trabajo] (media/pj15_CreateWorkflowSPD_EPTs.gif "Adición de un EPT para el flujo de trabajo")
  
    > [!NOTE]
    > Un valor **Sí** en la columna **Proyecto de lista de tareas de SharePoint** en la tabla de tipos de proyecto empresarial hace referencia a una EPT que crea una lista de tareas de SharePoint, donde la lista de tareas está visible en Project Web App, pero SharePoint mantiene el control del proyecto . Para obtener más información acerca de la administración de proyectos como listas de tareas de SharePoint, vea [arquitectura de Project Server 2013](project-server-2013-architecture.md). 
  
2. Abra la página de proyectos en Project Web App y, a continuación, cree un proyecto mediante el uso de la nueva etp (vea la figura 13). Debido a que el **Flujo de trabajo de bifurcación de prueba** está asociada con el **Flujo de trabajo de bifurcación**, se inicia la creación del proyecto bajo el control del flujo de trabajo.
    
    **La figura 13. Creación de un proyecto con el EPT de flujo de trabajo de bifurcación de prueba**

    ![Creación de un proyecto con el EPT] (media/pj15_CreateWorkflowSPD_NewProject.gif "Creación de un proyecto con el EPT")
  
3. Cuando el flujo de trabajo muestra la **Información del proyecto** PDP, agregar datos a los campos del proyecto. Por ejemplo, escriba un valor de **Costo de la propuesta** de 30000. La versión en inglés de Estados Unidos de Project Server cambia el campo para mostrar 30.000 USD (vea la figura 14).
    
    **La figura 14. Uso de la PDP modificada de información de proyecto**

    ![Uso de la PDP modificada de información de proyecto] (media/pj15_CreateWorkflowSPD_NewProjectStage1.gif "Uso de la PDP modificada de información de proyecto")
  
4. En la ficha **proyecto** de la cinta de opciones, en el grupo de **proyectos** , elija **Guardar**. Project Server agrega los datos en el PDP al proyecto y, a continuación, se muestra la página Estado del flujo de trabajo (vea la figura 15). Para ver la descripción completa de la región de detalles de la propuesta iniciales en el diagrama de estado de flujo de trabajo, sitúe el puntero sobre el escenario en el diagrama de visualización del flujo de trabajo.
    
    La cuadrícula de **Todas las fases de flujo de trabajo** usa una flecha verde para mostrar que la región de detalles de la propuesta iniciales está esperando entrada. Esto es debido a que espera a que el flujo de trabajo para un evento de envío en la fase de detalles de la propuesta iniciales. Si el flujo de trabajo no esperaba a un evento de envío, podría elegir **siguiente** en el grupo de **página** para ir a la siguiente PDP. 
    
    **La figura 15. Uso de la página Estado del flujo de trabajo en la fase de detalles de la propuesta iniciales**

    ![Página de estado de flujo de trabajo después de la primera fase] (media/pj15_CreateWorkflowSPD_NewProjectStage1Status.gif "Página de estado de flujo de trabajo después de la primera fase")
  
    El diagrama de visualización de flujo de trabajo muestra la etapa actual en un color verde. En la fase de **creación** , la fase de detalles de la propuesta iniciales es la etapa actual. 
    
5. En la cinta de opciones, en el grupo de **flujo de trabajo** , elija **Enviar**.
    
    > [!TIP]
    > Si está deshabilitado el control **Enviar** , actualice la página. 
  
    Si el valor de **Costo de la propuesta** es mayor que 25.000 dólares, el flujo de trabajo se mueve a la fase de rechazo automático. La figura 16 muestra el estado de fase de rechazo automático cuando elija **Enviar** de nuevo. Si el **Costo de la propuesta** es de 25.000 dólares o menos, el flujo de trabajo se mueve a la fase de detalles del proyecto (vea la figura 17). 
    
    **La figura 16. El flujo de trabajo se completa en la fase de rechazo automático**

    ![El flujo de trabajo se completa en rechazo automatizado] (media/pj15_CreateWorkflowSPD_AutomatedRejectionCompleted.gif "El flujo de trabajo se completa en rechazo automatizado")
  
    La figura 17 muestra otra prueba con una propuesta de proyecto denominada **probar 2 - bifurcación**, donde es actual en la fase de crear la etapa de detalles del proyecto. La fase de administración se muestra en una luz azul del color, que indica la fase no está activa.
    
    **La figura 17. El flujo de trabajo continúa a la fase de detalles del proyecto si el costo es inferior a 25.000 $**

    ![Estado de flujo de trabajo en la fase de detalles del proyecto] (media/pj15_CreateWorkflowSPD_ProjectDetailsStage.gif "Estado de flujo de trabajo en la fase de detalles del proyecto")
  
6. Si hace avanzar a la fase de detalles del proyecto, no hay ningún dato adicional para agregar en la página predeterminada. Elija **Enviar** nuevo para avanzar a la fase de ejecución (vea la figura 18). 
    
    **La figura 18. El flujo de trabajo está listo para administrar en la fase de ejecución**

    ![Estado de flujo de trabajo en la fase de ejecución] (media/pj15_CreateWorkflowSPD_ExecutionStage.gif "Estado de flujo de trabajo en la fase de ejecución")
  
En la etapa de detalles del proyecto, el flujo de trabajo no se espera para un evento de envío. Si el PDP de detalles del proyecto incluye campos obligatorios adicionales, Project Server espera hasta que se agregan datos a los campos antes de continuar con la fase de ejecución. Tal como se define en el flujo de trabajo de bifurcación, la etapa ejecución también no esperar a que un evento de envío. En la etapa de ejecución, puede editar el proyecto como un jefe de proyecto o elija **Cerrar** en la ficha **proyecto** de la cinta de opciones. Cuando se elige **Cerrar**, puede comprobar en el proyecto y editarlo más adelante o dejar el proyecto desprotegido.

El proyecto de **Flujo de trabajo de bifurcación** es un ejemplo sencillo que tiene sólo una comparación de prueba. El flujo de trabajo implica tres fases en la fase de creación y una fase en la fase de administración de la administración de propuestas. Para probar exhaustivamente un flujo de trabajo, debe probar todas las ramas del flujo de trabajo y use valores extremos y típicos para ver si el comportamiento es como se esperaba. 

<a name="pj15_CreateWorkflowSPD_ImportingVromVisio"> </a>

## <a name="importing-a-workflow-from-visio"></a>Importar un flujo de trabajo desde Visio

Para cambiar el flujo de trabajo, puede crear o modificar los campos personalizados con flujo de trabajo controlado y crear o modificar etapas y fases de flujo de trabajo. Puede usar SharePoint Designer 2013 para agregar condiciones, acciones, bucles y fases y, a continuación, guarde y vuelva a publicar el flujo de trabajo. Para volver a usar o conservar una copia de seguridad de un flujo de trabajo, puede exportarla a un archivo de Visio 2013. 
  
También puede crear o editar el flujo de trabajo en Visio 2013 e importar el archivo a SharePoint Designer 2013 para su uso por Project Web App. Para usar un flujo de trabajo sin modificar, la instancia de Project Web App debe incluir las propiedades de la fase de flujo de trabajo que son los mismos que los de la instancia de Project Web App original. Para obtener más información acerca del uso de Visio para ayudar a crear flujos de trabajo, vea [desarrollo de flujo de trabajo en SharePoint Designer 2013 y Visio 2013](http://msdn.microsoft.com/en-us/library/jj163272%28office.15%29.aspx).
  
> [!NOTE]
> Cuando se importa un archivo de Visio 2013 a una instancia diferente de Project Web App, las fases tienen diferentes etapas GUID, incluso si los nombres de región son los mismos. Después de importar el flujo de trabajo, debe configurar las propiedades de acción y la fase para utilizar los valores que son específicos de la instancia de Project Web App. 
> 
> Si crea un flujo de trabajo en Visio 2013, las fases y las acciones no tienen propiedades que son específicos de una instancia de Project Web App porque Visio no conectar con Project Web App. Cuando se conecta SharePoint Designer 2013 con Project Web App, crear un flujo de trabajo y, a continuación, importar el archivo VSDX, sobrescribir el flujo de trabajo activo. A continuación, debe configurar las propiedades de acción y la fase para que coincidan con los valores que SharePoint Designer 2013 obtiene desde Project Web App. 
  
### <a name="to-import-a-workflow-from-visio-to-sharepoint-designer"></a>Procedimiento para importar un flujo de trabajo de Visio a SharePoint Designer

1. En Visio 2013, cree un flujo de trabajo simple. Por ejemplo, realice los siguientes pasos:
    
   1. Abra Visio y, a continuación, cree un flujo de trabajo. Elija el panel de **categorías** para un nuevo flujo de trabajo, elija **diagrama de flujo**, elija la plantilla de **Flujo de trabajo de Microsoft SharePoint 2013** en el panel de **nuevo** y, a continuación, elija **crear**. Se abre el flujo de trabajo con una forma de fase denominada **etapa 1**. El flujo de trabajo incluye un componente de inicio y una forma de ENTRAR y forma salir como parte de la forma etapa.
    
      Cuando mantenga el mouse sobre la forma de fase y elija el icono de **Propiedades** , se deshabilita la selección. Puede establecer las propiedades de acción y la fase después de importar el diagrama de flujo de trabajo en SharePoint Designer 2013. 
    
      > [!NOTE]
      >  Las únicas galerías de símbolos de formas que debe usar son las que se recogen en la siguiente lista de formas de Diagrama de flujo: 
      > - **Acciones - flujo de trabajo de SharePoint 2013**
      > - **Componentes: flujo de trabajo de SharePoint 2013**
      > - **Condiciones: flujo de trabajo de SharePoint 2013**
  
   2. En el panel **formas** , elija **Formas rápidas**y, a continuación, arrastre la forma condición denominada **Si cualquier valor es igual al valor** a la derecha de la forma etapa. 
    
   3. En la ficha **página principal** de la cinta de opciones, elija la herramienta **conector** y, a continuación, conecte la forma de salir de la etapa con la forma condición (vea la figura 19). 
    
      **La figura 19. Conectar una forma de etapa con una forma de condición en un diagrama de flujo de trabajo de Visio**

      ![Creación de un diagrama de flujo de trabajo en Visio] (media/pj15_CreateWorkflowSPD_NewVisioWorkflow.gif "Creación de un diagrama de flujo de trabajo en Visio")
  
   4. Arrastre dos formas de fase más a la derecha de la forma de condición. Las formas se denominan **fase 2** y **3 de la fase**.
    
   5. Mediante la herramienta **conector** , conectar el lado derecho de la forma de condición con la forma de ENTRAR de la **fase 2**. Elija la herramienta **puntero** , haga doble clic en la conexión para mostrar un cuadro de texto para el nombre y, a continuación, nombre de la conexión de sí.
    
   6. Conectar la parte inferior de la forma de condición con la forma de ENTRAR de la **fase 3**. Con la herramienta **puntero** , haga clic en la conexión y, a continuación, elija **No**. Cualquiera de los métodos funciona para asignar nombres a los conectores de **Sí** o **No**.
    
   7. En el panel **formas** , elija **acciones - flujo de trabajo de SharePoint 2013**y, a continuación, arrastre la acción **esperar el evento de project** a la mitad de la forma **Etapa** 1 (vea la figura 20). 
    
      **La figura 20. Completar el flujo de trabajo en Visio**

      ![Completar el flujo de trabajo en Visio] (media/pj15_CreateWorkflowSPD_CompletedVisioWorkflow.gif "Completar el flujo de trabajo en Visio")
  
   8. En la ficha **proceso** de la cinta de opciones, en el grupo de **Validación del diagrama** , elija **Comprobar diagrama**. Corrija los errores y, a continuación, guarde el dibujo. Por ejemplo, el nombre del flujo de trabajo de prueba de archivo de Visio.vsdx.
    
      Para obtener información acerca de cómo corregir errores de flujo de trabajo, vea [errores de validación de flujo de trabajo de solución de problemas de SharePoint Server 2013 en Visio 2013](http://msdn.microsoft.com/en-us/library/jj163971%28v=office.15%29.aspx).
    
2. Abra SharePoint Designer 2013 y, a continuación, abra el mismo sitio de Project Web App que usa para el ejemplo de **Flujo de trabajo de bifurcación** . 
    
3. Elija **los flujos de trabajo** en el panel de **navegación** y, a continuación, cree un flujo de trabajo de sitio (seleccione **Flujo de trabajo de sitio** en la ficha **flujos de trabajo** de la cinta de opciones). Por ejemplo, el nombre del flujo de trabajo Simple de flujo de trabajo desde Visio.
    
   En el cuadro de diálogo **Crear flujo de trabajo de sitio** , asegúrese de que el tipo de plataforma es el **Flujo de trabajo de SharePoint 2013 - Project Server**. Elija **crear**, y SharePoint Designer se abre el panel **Diseñador basado en texto** para el nuevo flujo de trabajo. 
    
4. En el grupo **Administrar** de la ficha **flujo de trabajo** de la cinta de opciones, elija **Configuración de flujo de trabajo**.
    
5. En el grupo **Administrar** de la pestaña **Configuración de flujo de trabajo** de la cinta de opciones, elija **Importar desde Visio**y, a continuación, importar el archivo de **flujo de trabajo de prueba desde Visio.vsdx** que guardó anteriormente. Un cuadro de diálogo de **Microsoft SharePoint Designer** le advierte que el diagrama que está importando no contiene las propiedades de ningún flujo de trabajo y pregunta si desea sobrescribir el flujo de trabajo actual. Elija **Sí**; SharePoint Designer se importa el diagrama de flujo de trabajo, se genera las galerías de símbolos para las formas y se muestra el panel de **Diseñador Visual** que contiene el flujo de trabajo importado. 
    
6. Establecer las propiedades de cada forma de la fase del flujo de trabajo. Por ejemplo, la primera forma de la fase se denomina **etapa 1 (no válido)**, ya que no representa una fase válida en la instancia de Project Web App conectada. Cuando se activa o se mantenga el mouse sobre el escenario, puede elegir el icono de **Propiedades** en la parte inferior izquierda de la forma de fase para mostrar el cuadro de diálogo **Propiedades de fase** cuadro (consulte la figura 21). Seleccione la fase de **Detalles de la propuesta iniciales** en la lista desplegable de **Fase de proyecto** y, a continuación, elija **Aceptar**. SharePoint Designer cambia el nombre de la región.
    
   **La figura 21. Establecer la propiedad fase en SharePoint Designer**

   ![Establecer las propiedades de un flujo de trabajo importado] (media/pj15_CreateWorkflowSPD_ImportFromVisio1.gif "Establecer las propiedades de un flujo de trabajo importado")
  
   Para la segunda etapa, establezca la propiedad de **Fase de proyecto** en **Rechazo automatizado**. Para la tercera fase, establezca la propiedad de **Fase de proyecto** en **ejecución**.
    
7. De forma similar, para la acción **esperar el evento de proyecto** , establezca la propiedad de **Nombre de evento** en **evento: cuando se envía un proyecto**.
    
8. De forma similar, establezca las propiedades de la condición **Si cualquier valor es igual al valor** . Por ejemplo, puede establecer la primera propiedad de **valor** a **Costo de proyecto de datos: propuesta**. Establezca la propiedad **Operator** en **es menor que**. Establezca la propiedad **Value** segundo a 5000.
    
9. Compruebe el flujo de trabajo para los errores y, a continuación, guarde el flujo de trabajo. Si no hay errores, puede cambiar la vista para el **Diseñador basado en texto** (vea la figura 22). 
    
   **La figura 22. Visualización del flujo de trabajo importado en el diseñador basado en texto**

   ![Visualización del flujo de trabajo importado] (media/pj15_CreateWorkflowSPD_WorkflowFromVisio.gif "Visualización del flujo de trabajo importado")
  
10. Publique el flujo de trabajo. Si guarda el flujo de trabajo pero no lo publica, este no estará disponible cuando cree un tipo de proyecto empresarial.
    
11. Para probar el importados **flujo de trabajo Simple de Visio** en Project Web App, cree una EPT que usa el flujo de trabajo y, a continuación, crear proyectos que emplean el nuevo etp tal como hizo para el ejemplo de **Flujo de trabajo de bifurcación** . En este caso, sin embargo, se rechazan los proyectos que son menores que el costo de 5000 $. 
    
En el trabajo a través de este artículo, creado y probado un trabajo de bifurcación sencillo mediante el uso de SharePoint Designer 2013 para establecer directamente las fases, condiciones y acciones que usa el flujo de trabajo. También se crea un diagrama de un flujo de trabajo de bifurcación incluso más sencilla mediante el uso de Visio 2013. Importar el diagrama de flujo de trabajo de Visio en SharePoint Designer 2013, donde se establecen las propiedades de cada etapa, la condición y la acción de la conexión con Project Web App.
  
Visio 2013 y SharePoint Designer juntos proporcionan sencillos para diseñadores, los jefes de proyecto, los desarrolladores de flujo de trabajo y los evaluadores crear, compartir y personalizar los diseños de flujo de trabajo para las diferentes instalaciones de Project Server 2013 y Project Online. Para flujos de trabajo que requieren acceso mediante programación a Project Server que no proporcionan SharePoint Designer, puede usar Visual Studio 2012 con el modelo de objetos de cliente (COM).
  
## <a name="see-also"></a>Ver también

- [Arquitectura de Project Server 2013](project-server-2013-architecture.md)
- [Inicio: Instalar y configurar el Administrador de flujo de trabajo de SharePoint de 2013](http://msdn.microsoft.com/en-us/library/jj163276%28office.15%29.aspx)
- [Descripción de cómo empaquetar e implementar el flujo de trabajo en SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj819316%28office.15%29.aspx)
- [Flujos de trabajo en SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163986%28office.15%29.aspx)
- [Desarrollo de flujo de trabajo en SharePoint Designer 2013 y Visio 2013](http://msdn.microsoft.com/en-us/library/jj163272%28office.15%29.aspx)
- [Solución de problemas de errores de validación de flujo de trabajo de SharePoint Server 2013 en Visio 2013](http://msdn.microsoft.com/en-us/library/jj163971%28v=office.15%29.aspx)
- [Flujo de trabajo y administración de propuestas](http://msdn.microsoft.com/library/cf7433a3-a531-4467-ac0c-df0c5d6881ae%28Office.15%29.aspx)

