---
title: Cómo filtrar una vista con una macro en una aplicación de Access
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: overview
ms.assetid: db4dbb71-1b22-4dfd-bc07-5f7d694fc038
description: Obtenga información sobre cómo filtrar una vista en una aplicación de Access con la acción de macro RequeryRecords y una macro de datos.
localization_priority: Priority
ms.openlocfilehash: 861851a3497f290fe0bcda38e51794194fbe7bbe
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726403"
---
# <a name="filter-a-view-by-using-a-macro-in-an-access-app"></a>Cómo filtrar una vista con una macro en una aplicación de Access

Obtenga información sobre cómo filtrar una vista en una aplicación de Access con la acción de macro RequeryRecords y una macro de datos.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 

La vista de lista predeterminada de una aplicación de Access permite filtrar los problemas de los valores que se encuentran en los campos. Puede haber ocasiones en que quiera filtrar una vista según un conjunto de condiciones, en lugar de que coincida con un valor. Para ello, debe crear una macro. En este artículo se muestra cómo crear una macro que filtre una vista para mostrar las tareas que están más allá de vencimiento o que vencerán en los próximos 7 días.
  
## <a name="prerequisites-for-building-an-app-with-access"></a>Requisitos previos para compilar una aplicación con Access
<a name="Access2013FilterViewByUsingMacro_Prerequisites"> </a>

Para seguir los pasos de este ejemplo, necesita:
  
- Access 2013
- Un entorno de desarrollo de SharePoint 2013.
    
> [!NOTE]
> Para obtener más información sobre cómo configurar el entorno de desarrollo de SharePoint, consulte [Configurar un entorno de desarrollo general para SharePoint 2013](https://msdn.microsoft.com/library/08e4e4e1-d960-43fa-85df-f3c279ed6927%28Office.15%29.aspx). Para obtener más información sobre cómo conseguir Access 2013 y SharePoint 2013, consulte [Descargas](https://msdn.microsoft.com/office/apps/fp123627). 
  
## <a name="create-the-app"></a>Crear la aplicación
<a name="Access2013FilterViewByUsingMacro_CreateApp"> </a>

Suponga que quiere crear una aplicación de Access que siga las tareas de la empresa. Antes de empezar a crear las tablas y las vistas, debe buscar una plantilla de esquema.
  
### <a name="to-create-the-task-tracking-app"></a>Crear la aplicación de seguimiento de tareas

1. Abra Access y elija **Personalizar aplicación web**.
    
2. Especifique un nombre y una ubicación web de la aplicación. También puede elegir una ubicación de la lista **Ubicaciones** y seleccionar **Crear**.
    
3. Escriba **tareas** en el cuadro **Búsqueda** y presione ENTRAR. 
    
    En la figura 1 se muestra una lista de las plantillas que podría útiles para el seguimiento de tareas.
    
   **Figura 1. Plantillas que coinciden con la búsqueda de tareas**

   ![Plantillas que coinciden con la búsqueda de problemas](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Plantillas que coinciden con la búsqueda de problemas")
  
4. Seleccione **Tareas**.
    
Access crea un conjunto de tablas y vistas.
  
Introduzca varias tareas y empleados de ejemplo en la aplicación. Para ello, elija **Iniciar aplicación** para abrir la aplicación en el explorador web. Escriba un valor en el campo **Fecha de vencimiento** para cada tarea. Vuelva a Access cuando haya terminado. 
  
## <a name="plan-the-customizations"></a>Planear las personalizaciones
<a name="Access2013FilterViewByUsingMacro_PlanCustomizations"> </a>

Ahora tiene una aplicación que contiene varias tareas. La vista predeterminada permite buscar las tareas con elementos que se almacenan en los campos mostrados en la vista. Por ejemplo, puede buscar para problemas de alta prioridad o en curso. Suponga que quiere dar prioridad al trabajo mostrando problemas activos que vencen la semana siguiente. Para ello, debe crear una macro de interfaz de usuario (IU).
  
El comando de macro de interfaz de usuario que puede usar para filtrar la vista es [Acción de Macro RequeryRecords (acceso personalizado web app)](requeryrecords-macro-action-access-custom-web-app.md). La acción de macro **RequeryRecords** filtra la vista según el argumento  *Where*  , que se proporciona en forma de una cláusula WHERE de SQL. Para filtrar la vista, debe proporcionar varios datos en un formato específico para filtrar la vista. 
  
Los hechos importantes son:
  
- El campo o campos para comparar
    
- Cómo hacer referencia a la fecha de hoy
    
- Cómo hacer referencia a un día concreto en relación con la fecha de hoy
    
- Cómo determinar las tareas que están en curso
    
El campo **Fecha de vencimiento** proporciona información sobre el momento en que vence una tarea. El campo **Estado** proporciona información de estado de cada tarea. Para hacer referencia a un campo de una macro, use el formato **[*TableName*].[*FieldName*]**. Use **[Tareas].[Fecha de vencimiento]** para hacer referencia al campo **Fecha de vencimiento** y **[Tareas].[Estado]** para hacer referencia al campo **Estado**. 
  
La función [Función hoy (acceso personalizado web app)](today-function-access-custom-web-app.md) devuelve la fecha de hoy. La función [Función DateAdd (aplicación web personalizada de Access)](dateadd-function-access-custom-web-app.md) se puede usar para calcular una fecha que es un número determinado de días después de una fecha especificada. 
  
El campo **Estado** contiene varios valores posibles. Un valor **Completado** indica que la tarea ya no está activa. 
  
Estos datos se pueden combinar en la siguiente cláusula WHERE de SQL.
  
```sql
[Tasks].[Due Date]<DateAdd(Day,7,Today()) AND [Tasks].[Status]<>"Completed"
```

Esta cláusula WHERE de SQL se usa en la macro para filtrar la vista para mostrar los problemas activos que vencen en los próximos 7 días o que han vencido.
  
Para ejecutar la macro de interfaz de usuario, se debe adjuntar a un elemento o a un evento que ocurra en la vista. La **Barra de acciones** es un lugar cómodo para agregar un comando personalizado a la vista. La **Barra de acciones** es una barra de herramientas que se puede personalizar que aparece en la parte superior de cada vista. De forma predeterminada, la **Barra de acciones** contiene botones para agregar, editar, guardar, eliminar y cancelar las modificaciones. Puede agregar botones que realicen acciones personalizadas, como el filtrado de la vista. 
  
Si la vista contiene registros que cumplen con los criterios especificados, **RequeryRecords** filtra la vista. Sin embargo, si la vista no contiene ningún registro que cumpla con los criterios, se mostrará un nuevo registro vacío. Si no quiere que se muestre un registro vacío si no hay tareas que venzan en la próxima semana, debe buscar un método para comprobar las tareas antes de llamar a la acción de macro **RequeryRecords**. Para ello, cree una macro de datos para buscar registros que cumplan con los criterios. 
  
La macro de interfaz de usuario llamará a la macro de datos, que intentará buscar una tarea que venza la semana siguiente. Si la macro de datos encuentra la tarea, personaliza la aplicación.
  
## <a name="customize-the-app"></a>Personalizar la aplicación
<a name="Access2013FilterViewByUsingMacro_CustomizeApp"> </a>

Ahora que ha determinado las personalizaciones, impleméntelas. En primer lugar se debe crear la macro de datos. Algunas macros de datos se adjuntan directamente a tablas. Sin embargo, esta macro de datos es una macro de datos independiente.
  
### <a name="to-create-the-data-macro"></a>Crear la macro de datos

1. Abra la aplicación en Access.
    
2. En el grupo **Crear**, seleccione **Opciones avanzadas** y elija **Macro de datos**.
    
    Se abre una macro de datos vacía en la macro Vista Diseño.
    
3. En el cuadro de lista **Agregar nueva acción**, seleccione **LookupRecord**.
    
4. En el cuadro de lista **Buscar un registro en**, seleccione **Tareas**.
    
5. En el cuadro **Condición Where**, escriba **[Tasks].[Due Date]\<DateAdd(Day,7,Today()) AND [Tasks].[Status]\<\>"Completed"**. 
    
6. Seleccione **SetReturnVar** en el cuadro de lista **Agregar nueva acción**. 
    
    > [!NOTE]
    > Verá dos cuadros de lista **Agregar nueva acción**, un dentro del bloque **LookupRecord** y otro fuera del bloque **LookupRecord**. Debe elegir el cuadro de lista **Agregar nueva acción** del bloque **LookupRecord**, como se muestra en la figura 1. 
  
   **Figura 1. Cuadro de lista Agregar nueva acción**

   ![Lista desplegable Agregar nueva acción](media/odc_Access2013_FilterFormByUsingMacro_Figure01.jpg "Lista desplegable Agregar nueva acción")
  
7. En el cuadro **Nombre**, escriba **TaskFound**. 
    
8. En el cuadro **Expresión**, escriba **"Yes"**. 
    
9. Seleccione **Guardar**. Escriba **TasksDueSoon** en el cuadro **Nombre de macro** y seleccione **Aceptar**.
    
    La macro debería tener el aspecto de la macro que se muestra en la figura 2.
    
   **Figura 2. Macro de datos TasksDueSoon**

   ![Macro de datos TasksDueSoon](media/odc_Access2013_FilterFormByUsingMacro_Figure02.jpg "Macro de datos TasksDueSoon")
  
10. Cierre la macro Vista Diseño.
    
Ahora, estamos listos para agregar un botón personalizado a la barra de acciones.
  
### <a name="to-add-a-custom-button-to-the-action-bar"></a>Agregar un botón personalizado a la barra de acciones

1. Elija la tabla **Tareas**. Esto selecciona el formulario Lista de tareas. 
    
2. En el Selector de vistas, seleccione **Lista**, el icono **Configuración/Acción** y luego **Editar**.
    
    La vista se abre en la vista Diseño.
    
3. Ahora, estamos listos para agregar un botón personalizado a la barra de acciones. Para ello, seleccione **Agregar acción personalizada**, como se muestra en la figura 3. 
    
   **Figura 3. Botón Agregar acción personalizada**

   ![Botón Agregar acción personalizada](media/odc_Access2013_FilterFormByUsingMacro_Figure03.jpg "Botón Agregar acción personalizada")
  
    La nueva acción se muestra como un botón con un icono de estrella, como se muestra en la figura 4.
    
   **Figura 4. Botón Nueva barra de acciones**

   ![Botón Nueva barra de acciones](media/odc_Access2013_FilterFormByUsingMacro_Figure04.jpg "Botón Nueva barra de acciones")
  
4. Seleccione el botón Barra de acciones personalizado y luego elija el icono **Datos**. 
    
    aparece el cuadro de diálogo **Datos**. 
    
5. En el cuadro **Nombre del control**, escriba **FilterTasks**. 
    
6. En la **Información sobre herramientas**, escriba **Mostrar las tareas más allá de la fecha de vencimiento o que vencen la semana siguiente**. 
    
Ahora podemos crear la macro de interfaz de usuario que filtrará la vista.
  
### <a name="to-create-the-ui-macro-to-filter-the-view"></a>Crear la macro de interfaz de usuario para filtrar la vista

1. En el cuadro de diálogo **Datos**, elija **Al hacer clic**, como se muestra en la figura 5. 
    
   **Figura 5. Cuadro de diálogo Datos**

   ![Cuadro de diálogo Datos](media/odc_Access2013_FilterFormByUsingMacro_Figure05.jpg "Cuadro de diálogo Datos")
  
    Se abre una macro de interfaz de usuario vacía en la macro Vista Diseño.
    
2. En el cuadro de lista **Agregar nueva acción**, seleccione **RunDataMacro**. 
    
3. En el cuadro Nombre de la macro, escriba **TasksDueSoon**. 
    
    En el cuadro **SetLocalVar**, escriba **FilterRecords**. 
    
    La acción **RunDataMacro** llama a la macro de datos **TasksDueSoon** que creamos anteriormente y almacena los resultados en una variable denominada **FilterRecords**. 
    
4. En el cuadro de lista **Agregar nueva acción**, seleccione **If**. 
    
5. En el cuadro **If**, escriba **[FilterRecords]="Yes"**. 
    
6. En el cuadro de lista **Agregar nueva acción**, seleccione **RequeryRecords**. 
    
    > [!NOTE]
    > Verá dos cuadros de lista **Agregar nueva acción**, un dentro del bloque **If** y otro fuera del bloque **If**. Debe elegir el cuadro de lista **Agregar nueva acción** del bloque **If**, como se muestra en la figura 6. 
  
   **Figura 6. Cuadro de lista Agregar nueva acción**

   ![Lista desplegable Agregar nueva acción](media/odc_Access2013_FilterFormByUsingMacro_Figure06.jpg "Lista desplegable Agregar nueva acción")
  
7. En el cuadro **Where**, escriba **[Tasks].[Due Date]\<DateAdd(Day,7,Today()) AND [Tasks].[Status]\<\>"Completed"**. 
    
8. En el cuadro **Ordenar por**, escriba **[Due Date]**. 
    
9. Elija el vínculo **Agregar más** que aparece a la derecha del cuadro **Agregar nueva acción**, como se muestra en la figura 7. 
    
   **Figura 7. Vínculo Agregar Else**

   ![Vínculo Agregar Else](media/odc_Access2013_FilterFormByUsingMacro_Figure07.jpg "Vínculo Agregar Else")
  
    Se agrega una cláusula Else al bloque If.
    
10. En el cuadro de lista **Agregar nueva acción**, seleccione **MessageBox**. 
    
11. En el cuadro **Mensaje**, escriba **Ninguna tarea ha vencido o vence en los próximos 7 días**. 
    
12. Seleccione **Guardar**.
    
    La macro debería tener el aspecto de la macro que se muestra en la figura 8.
    
    **Figura 8. Macro de interfaz de usuario para filtrar la vista**

    ![Macro de interfaz de usuario para filtrar la vista](media/odc_Access2013_FilterFormByUsingMacro_Figure08.jpg "Macro de interfaz de usuario para filtrar la vista")
  
13. Cierre la macro Vista Diseño.
    
En este punto, hemos creado la macro de interfaz de usuario que filtra la vista Lista de tareas para mostrar las tareas urgentes. No sería correcto dejar la vista en un estado filtrado sin proporcionar un método para quitar el filtro. Para ello, agregue otro botón Barra de acciones y la macro de interfaz de usuario.
  
### <a name="to-add-an-action-bar-button-to-remove-the-filter"></a>Agregar un botón Barra de acciones para quitar el filtro

1. Seleccione **Agregar acción personalizada**.
    
    La nueva acción se muestra como un botón con un icono de estrella
    
2. Seleccione el botón Barra de acciones personalizada y elija el icono **Datos**. 
    
    Aparece el cuadro de diálogo **Datos**. 
    
3. En el cuadro **Nombre del control**, escriba **RemoveFilter**. 
    
4. En el cuadro **Información sobre herramientas**, escriba **Quitar todos los filtros aplicados a la vista**. 
    
Ahora podemos crear la macro de interfaz de usuario que quitará el filtro de la vista.
  
### <a name="to-create-the-ui-macro-to-remove-the-filter-from-the-view"></a>Crear la macro de interfaz de usuario para quitar el filtro de la vista

1. En el cuadro de diálogo **Datos**, elija **Al hacer clic**.
    
    Se abre una macro de interfaz de usuario vacía en la macro Vista Diseño.
    
2. En el cuadro de lista **Agregar nueva acción**, seleccione **RequeryRecords**. 
    
    En este momento, dejaremos los cuadros **Where** y **Order By** vacíos. Luego, se llama a la acción **RequeryRecords** sin parámetros, se quitan todos los filtros de la vista. 
    
3. Seleccione **Guardar**.
    
4. Cierre la macro Vista Diseño.
    
5. Cierre la vista Lista de tareas. Seleccione **Sí** cuando se le pida guardar los cambios. 
    
Ahora podemos personalizar el texto. Elija **Iniciar aplicación** para abrir la aplicación en el explorador web y seleccione el botón Barra de acciones FilterTasks personalizado. Se mostrarán las tareas que hayan vencido o que vencerán en los próximos 7 días. Si la aplicación no contiene tareas urgentes, se muestra un mensaje. 
  
## <a name="conclusion"></a>Conclusión

Puede usar la acción de macro **RequeryRecords** en una macro de interfaz de usuario para filtrar la vista según los criterios que elija. Dependiendo del comportamiento que quiera, es posible que quiera crear una macro de datos para comprobar que un registro cumple con los criterios antes de usar la acción de macro **RequeryRecords**. 
  
## <a name="see-also"></a>Vea también

- [Novedades para desarrolladores de Access 2013](https://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx)
    

