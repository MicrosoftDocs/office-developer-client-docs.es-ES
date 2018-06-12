---
title: Crear y personalizar una aplicación web en Access
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 628745f4-82e9-4838-9726-6f3e506a654f
ms.openlocfilehash: 7a41bc4c9509f1d9cec49003fb775a3be2768703
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815360"
---
# <a name="create-and-customize-a-web-app-in-access"></a>Crear y personalizar una aplicación web en Access

> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
Access 2013 incluye un nuevo modelo de aplicación que permite a los expertos en la materia crear rápidamente aplicaciones web. Con Access se incluye un conjunto de plantillas que puede usar para iniciar la creación de su aplicación.

<a name="ac15_CreateAndCustomizeWebApp_Prerequisites"> </a>

## <a name="prerequisites-for-building-an-app-with-access-2013"></a>Requisitos previos para la creación de una aplicación con Access 2013

Para realizar los pasos de este ejemplo, necesita los elementos siguientes:
  
- Access
    
- Un entorno de desarrollo de SharePoint.
    
Para obtener más información acerca de cómo configurar el entorno de desarrollo de SharePoint, vea [configurar un entorno de desarrollo general de SharePoint](https://docs.microsoft.com/en-us/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint). 
  
Para obtener más información acerca de cómo obtener acceso y SharePoint, vea [descargas](http://msdn.microsoft.com/en-US/office/apps/fp123627).

<a name="ac15_CreateAndCustomizeWebApp_CreateTheApp"> </a>

## <a name="create-the-app"></a>Crear la aplicación

Supongamos que desea crear una aplicación de Access que hace un seguimiento de los problemas de su empresa. Antes de comenzar a crear las tablas y la vista desde cero, debería buscar una plantilla de esquema que se adapte a sus necesidades.
  
### <a name="to-create-the-issue-tracking-app"></a>Crear una aplicación de seguimiento de problemas

1. Abra Access y seleccione **Personalizar aplicación web**.
    
2. Especifique un nombre y una ubicación web de la aplicación. También puede elegir una ubicación de la lista **Ubicaciones** y seleccionar **Crear**.
    
3. Escriba **Problemas** en el cuadro **¿De qué elemento desea realizar un seguimiento?** y presione ENTRAR. 
    
   En la figura 1 se muestra una lista de las plantillas que podría ser de utilidad para el seguimiento de problemas.
    
   **Figura 1. Plantillas que coinciden con la búsqueda de problemas**

   ![Plantillas que coinciden con la búsqueda de problemas] (media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Plantillas que coinciden con la búsqueda de problemas")
  
4. Elija **Problemas**.
    
Access crea un conjunto de tablas y vistas.
  
## <a name="explore-the-app"></a>Explorar la aplicación
<a name="ac15_CreateAndCustomizeWebApp_ExploreTheApp"> </a>

Para comprender si el esquema y las vistas se ajustan a sus necesidades, debería examinarlos.
  
Las tablas que se crean al seleccionar el esquema Problemas se muestran en el panel de icono. Las tablas Problemas, Cliente y Empleados son el enfoque principal de la aplicación. En la tabla Problema se almacena información sobre cada problema. Cada problema lo abre un empleado, y está asignado a él, en nombre de un cliente. Las tablas Problemas relacionados y Comentarios sobre el problema sirven de apoyo para la aplicación. La tabla Problemas relacionados le permite vincular un problema con otro. La tabla Comentarios sobre el problema almacena varios comentarios sobre un solo problema.
  
En una base de datos de escritorio de Access (.accdb), las relaciones entre las tablas se administran en la ventana **Relaciones**. Las aplicaciones de Access 2013 administran las relaciones mediante campos establecidos en el tipo de datos **Búsqueda**. Examinemos las relaciones de la tabla Problemas. Para ello, haga clic con el botón secundario del mouse en el icono **Problemas** y seleccione **Editar tabla**.
  
El campo **Cliente** está relacionado con la tabla **Clientes**. Para examinar la relación, seleccione el campo **Cliente** y luego **Modificar búsquedas**. Aparecerá el **Asistente para búsquedas**, tal como se muestra en la figura 2. 
  
**Figura 2. Asistente para búsquedas que muestra la relación con la tabla Clientes**

![Asistente para búsquedas que muestra la relación] (media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Asistente para búsquedas que muestra la relación")
  
En el cuadro de diálogo Asistente para búsquedas se muestra que el campo **Cliente** está vinculado a la tabla **Clientes** y que se debe devolver el campo **Nombre para mostrar, Nombre Apellidos** de la tabla **Clientes**. 
  
Los campos **Abierto por**, **Asignada a** y **Cambiado por** están relacionados con la tabla **Empleados**. También se han establecido otros campos en el tipo de datos **Búsqueda**. En estos casos, el tipo de datos Búsqueda se usa para especificar valores concretos que se deben permitir en el campo. 
  
Cierre la tabla **Problemas** y examine el panel de icono. Los tres iconos superiores, para las tablas **Problemas**, **Clientes** y **Empleados**, se muestran de manera diferente que en los dos iconos inferiores de las tablas **Problemas relacionados** y **Comentarios sobre el problema**, tal como se muestra en la figura 3. 
  
**Figura 3. Panel de icono del esquema Problemas**

![Panel de icono para el esquema de problemas] (media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Panel de icono para el esquema de problemas")
  
Las tablas **Problemas relacionados** y **Comentarios sobre el problema** están atenuadas porque no deben mostrarse al usuario en el explorador web. 
  
Usemos la aplicación para hacer el seguimiento de algunos problemas. Para ello, haga clic en **Iniciar aplicación** para abrir la aplicación en el explorador web. 
  
La aplicación abre la vista **Lista de problemas** de la tabla Problemas. Antes de agregar un problema, se recomienda agregar algunos clientes y empleados. Haga clic en el icono **Clientes** para comenzar a agregar clientes. 
  
Use el Selector de vistas para elegir una de las tres vistas disponibles para la tabla **Clientes**, con las etiquetas **Lista**, **Hoja de datos** y **Grupos**, tal como se muestra en la figura 4. 
  
**Figura 4. Selector de vistas**

![Selector de vistas] (media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "Selector de vistas")
  
Si elige **Lista**, se activará la vista **Lista de clientes**, que es una vista de detalles de la lista. La vista de detalles de la lista es una de las vistas que Access genera automáticamente al crear una tabla. La principal característica que diferencia una vista de detalles de la lista es el panel de listas que aparecen en el lado izquierdo de la vista. El panel de vistas se usa para filtrar los registros de la vista y navegar por ellos. En una base de datos de escritorio de Access, la implementación de una vista de lista en la que se permiten búsquedas requeriría la redacción de código personalizado. 
  
Si selecciona **Hoja de datos**, se abrirá la vista **Hoja de datos Clientes**. La hoja de datos es otro tipo de vista que Access genera automáticamente al crear una tabla. Las vistas de hoja de datos son de utilidad para los usuarios que consideran más fácil especificar, ordenar y filtrar datos en forma de hoja de cálculo. 
  
Si selecciona Grupos, se abre una vista de resumen. Las vistas de resumen se pueden usar para agrupar registros según un campo y calcular opcionalmente una suma o un promedio.
  
A medida que agregue clientes, use la barra de acciones para agregar, editar, guardar y eliminar registros, así como para cancelar las modificaciones. La barra de acciones se puede personalizar y aparece en la parte superior de cada vista, tal como se muestra en la figura 5.
  
**Figura 5. Barra de acciones**

![Barra de acciones] (media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Barra de acciones")
  
Cuando haya agregado algunos clientes y empleados, abra la vista Lista de problemas y comience a agregar un problema. A medida que escriba el nombre de un cliente en el cuadro cliente, aparecerán uno o más nombres de cliente, tal como se muestra en la figura 6.
  
**Figura 6. Control Autocompletar**

![Control Autocompletar] (media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "Control Autocompletar")
  
El cuadro Cliente es un control de tipo autocompletar, que muestra una lista de registros que coinciden con lo que esté escribiendo en el cuadro. Esto ayuda a garantizar la precisión de la entrada de datos.
  
## <a name="customize-the-app"></a>Personalizar la aplicación
<a name="ac15_CreateAndCustomizeWebApp_CustomizeTheApp"> </a>

Tras dar un paseo por la aplicación, observará que la vista Lista de problemas no contiene información de contacto para el cliente. Personalicemos la aplicación para agregar el número de teléfono de trabajo del cliente a la tabla Problemas al crear el problema.
  
### <a name="to-add-a-field-to-the-issues-table"></a>Agregar un campo a la tabla Problemas

1. Abra la aplicación en Access.
    
2. Seleccione el icono **Problemas**, el icono **Configuración/Acción** y luego **Editar tabla**.
    
3. Especifique el **Número de contacto** en la primera celda vacía de la columna **Nombre del campo**. 
    
4. Seleccione **Texto corto** en la columna **Tipo de datos**. 
    
5. Seleccione **Guardar**.
    
6. Cierre la tabla Problemas.
    
Ahora que disponemos de un campo en el que almacenar el número de teléfono, creemos una macro de datos para buscar la información de contacto.
  
### <a name="to-create-the-data-macro-to-look-up-contact-information"></a>Crear la macro de datos que permite buscar información de contacto

1. En el grupo **Crear**, seleccione **Opciones avanzadas** y elija **Macro de datos**.
    
2. Seleccione **Crear parámetro**.
    
3. En el cuadro **Nombre**, especifique **CustID**. En la lista desplegable **Tipo**, seleccione **Número (decimal flotante).**
    
4. En la lista desplegable **Agregar nueva acción**, seleccione **LookupRecord**. 
    
5. En la lista desplegable **Buscar un registro en**, seleccione **Clientes**. 
    
6. En el cuadro **Condición WHERE**, especifique **[Clientes].[ID]=[CustID]**. 
    
7. Seleccione **SetReturnVar** de la lista desplegable **Agregar nueva acción**. 
    
    > [!NOTE]
    > [!NOTA] Verá dos listas desplegables **Agregar nueva acción**, una en el bloque **LookupRecord** y otra fuera del bloque **LookupRecord**. Debería elegir la lista desplegable **Agregar nueva acción** dentro del bloque **LookupRecord**, tal como se muestra en la figura 7. 
  
   **Figura 7. Lista desplegable Agregar nueva acción**

   ![Lista desplegable Agregar nueva acción] (media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Lista desplegable Agregar nueva acción")
  
8. En el cuadro **Nombre**, escriba **ContactPhone**. 
    
9. En el cuadro **Expresión**, escriba **[Clientes].[Teléfono de trabajo]**. 
    
10. Seleccione **Guardar**. Escriba **GetContactPhone** en el cuadro **Nombre de macro** y haga clic en **Aceptar**.
    
    La macro debería tener el aspecto de la macro que se muestra en la figura 8.
    
    **Figura 8. Macro de datos GetContactPhone**

    ![Macro de datos GetContactPhone] (media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "Macro de datos GetContactPhone")
  
11. Cierre la macro Vista Diseño.
    
Ahora estamos listos para agregar el campo **Número de contacto** al formulario Lista de problemas. 
  
### <a name="to-add-the-contact-number-field-to-the-issues-list-form"></a>Agregar el campo Número de contacto al formulario Lista de problemas

1. Seleccione la tabla **Problemas** para elegir el formulario Lista de problemas. 
    
2. En el Selector de vistas, seleccione **Lista**, el icono **Configuración/Acción** y luego **Editar**.
    
3. Arrastre el campo **Número de contacto** del panel **Lista de campos** a la ubicación del formulario en la que desee mostrar el número de contacto. 
    
4. Seleccione el cuadro de texto **Número de contacto** y haga clic en **Datos**. 
    
5. En el cuadro **Nombre del control**, escriba **CustomerContact** y cierre la ventana emergente **Datos**. 
    
6. Seleccione **Guardar**.
    
Ahora debemos escribir una macro de interfaz de usuario (UI) que copia el campo **Teléfono de trabajo** de la tabla **Clientes** al campo **Número de contacto** de la tabla **Problemas**. El evento **Después de actualizar** del control **CustomerAutocomplete** es una buena ubicación para la macro. 
  
### <a name="to-create-the-afterupdate-macro"></a>Crear la macro Después de actualizar

1. Seleccione el control **CustomerAutocomplete**, el botón **Acciones** y luego **Después de actualizar**. 
    
    Se abre una macro vacía en la macro Vista Diseño.
    
2. En la lista desplegable **Agregar nueva acción**, seleccione **RunDataMacro**. 
    
3. En la lista desplegable **Nombre de macro**, seleccione **GetContactPhone**. 
    
4. En el cuadro **CustID**, escriba **[CustomerAutocomplete]**. 
    
5. En el cuadro **SetLocalVar**, escriba **Teléfono**. 
    
    Cuando elija la macro de datos GetContactPhone creada anteriormente, Access completó automáticamente el nombre del parámetro y la variable devuelta de la macro.
    
    El número de teléfono del cliente se almacena en la variable denominada Phone.
    
6. En la lista desplegable **Agregar nueva acción**, seleccione **SetProperty**. 
    
7. En el cuadro **Nombre del control**, escriba **CustomerContact**. 
    
8. En la lista desplegable **Propiedad**, seleccione **Valor**. 
    
9. En el cuadro **Valor**, escriba **=[Teléfono]**. 
    
10. Haga clic en **Guardar**.
    
    La macro debería tener el aspecto de la macro que se muestra en la figura 9.
    
    **Figura 9. Macro Después de actualizar**

    ![Macro después de actualizar] (media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "Macro después de actualizar")
  
11. Cerrar macro Vista Diseño.
    
12. Cierre la vista Lista de problemas. Seleccione **Sí** cuando se le solicite guardar los cambios. 
    
Ahora está listo para la personalización. Haga clic en **Iniciar aplicación** para abrir la aplicación en el explorador web y luego agregue un problema nuevo. El **Número de contacto** cuadro se actualiza automáticamente después de especifica el nombre del cliente, tal como se muestra en la figura 10. 
  
**Figura 10. Vista Problemas actualizada con el número de teléfono**

![Vista de problemas actualizada con el número de teléfono] (media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "Vista de problemas actualizada con el número de teléfono")
  
## <a name="conclusion"></a>Conclusión

El uso de una de las plantillas de esquema incluidas con es una buena manera de iniciar la creación de una aplicación web de Access. Las vistas que se crean automáticamente incluyen funciones avanzadas que requieren código personalizado que se debe implementar en una base de datos de escritorio de Access. 
  
## <a name="see-also"></a>Ver también

- [Nuevo en Access para desarrolladores](http://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx) 
- [Referencia de la aplicación de acceso web personalizados](access-custom-web-app-reference.md)
  

