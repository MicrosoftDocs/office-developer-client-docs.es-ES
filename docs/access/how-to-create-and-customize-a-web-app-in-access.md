---
title: Crear y personalizar una aplicación web en Access
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 628745f4-82e9-4838-9726-6f3e506a654f
localization_priority: Priority
ms.openlocfilehash: d7d27e98189a5b6784e4db48c81a545b85f01fc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306149"
---
# <a name="create-and-customize-a-web-app-in-access"></a><span data-ttu-id="23b24-102">Crear y personalizar una aplicación web en Access</span><span class="sxs-lookup"><span data-stu-id="23b24-102">Create and customize a web app in Access</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23b24-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/es-ES/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="23b24-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/es-ES/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
<span data-ttu-id="23b24-p102">Access 2013 incluye un nuevo modelo de aplicación que permite a los expertos en la materia crear rápidamente aplicaciones web. Con Access se incluye un conjunto de plantillas que puede usar para iniciar la creación de su aplicación.</span><span class="sxs-lookup"><span data-stu-id="23b24-p102">Access 2013 features a new application model that enables subject matter experts to quickly create web-based applications. Included with Access are a set of templates that you can use to jump start creating your application.</span></span>

<span data-ttu-id="23b24-107"><a name="ac15_CreateAndCustomizeWebApp_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="23b24-107"></span></span>

## <a name="prerequisites-for-building-an-app-with-access-2013"></a><span data-ttu-id="23b24-108">Requisitos previos para la creación de una aplicación con Access 2013</span><span class="sxs-lookup"><span data-stu-id="23b24-108">Prerequisites for building an app with Access 2013</span></span>

<span data-ttu-id="23b24-109">Para seguir los pasos de este ejemplo, necesita lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="23b24-109">To follow the steps in this example, you need the following:</span></span>
  
- <span data-ttu-id="23b24-110">Access</span><span class="sxs-lookup"><span data-stu-id="23b24-110">Access</span></span>
    
- <span data-ttu-id="23b24-111">Un entorno de desarrollo de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="23b24-111">A SharePoint development environment</span></span>
    
<span data-ttu-id="23b24-112">Para obtener más información sobre cómo configurar el entorno de desarrollo de SharePoint, vea [Configurar un entorno de desarrollo general para SharePoint](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint).</span><span class="sxs-lookup"><span data-stu-id="23b24-112">For more information about setting up your SharePoint development environment, see [Set up a general development environment for SharePoint](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint).</span></span> 
  
<span data-ttu-id="23b24-113">Para obtener más información sobre cómo conseguir Access y SharePoint, vea [Descargas](https://msdn.microsoft.com/office/apps/fp123627).</span><span class="sxs-lookup"><span data-stu-id="23b24-113">For more information about obtaining Access and SharePoint, see [Downloads](https://msdn.microsoft.com/office/apps/fp123627).</span></span>

<span data-ttu-id="23b24-114"><a name="ac15_CreateAndCustomizeWebApp_CreateTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="23b24-114"></span></span>

## <a name="create-the-app"></a><span data-ttu-id="23b24-115">Crear la aplicación</span><span class="sxs-lookup"><span data-stu-id="23b24-115">Create the app</span></span>

<span data-ttu-id="23b24-p103">Supongamos que desea crear una aplicación de Access que hace un seguimiento de los problemas de su empresa. Antes de comenzar a crear las tablas y la vista desde cero, debería buscar una plantilla de esquema que se adapte a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="23b24-p103">Suppose you want to create an Access app that tracks issues for your business. Before you start creating the tables and view from scratch, you should search for a schema template that meets your needs.</span></span>
  
### <a name="to-create-the-issue-tracking-app"></a><span data-ttu-id="23b24-118">Crear una aplicación de seguimiento de problemas</span><span class="sxs-lookup"><span data-stu-id="23b24-118">To create the issue tracking app</span></span>

1. <span data-ttu-id="23b24-119">Abra Access y seleccione **Personalizar aplicación web**.</span><span class="sxs-lookup"><span data-stu-id="23b24-119">Open Access and choose **Custom web app**.</span></span>
    
2. <span data-ttu-id="23b24-p104">Especifique un nombre y una ubicación web de la aplicación. También puede elegir una ubicación de la lista **Ubicaciones** y seleccionar **Crear**.</span><span class="sxs-lookup"><span data-stu-id="23b24-p104">Enter a name and the web location for your app. You can also choose a location from the **Locations** list and choose **Create**.</span></span>
    
3. <span data-ttu-id="23b24-122">Escriba **Problemas** en el cuadro **¿De qué elemento desea realizar un seguimiento?** y presione ENTRAR.</span><span class="sxs-lookup"><span data-stu-id="23b24-122">Type **Issues** into the **What would you like to track?** box and then press ENTER.</span></span> 
    
   <span data-ttu-id="23b24-123">En la figura 1 se muestra una lista de las plantillas que podría ser de utilidad para el seguimiento de problemas.</span><span class="sxs-lookup"><span data-stu-id="23b24-123">A list of templates that might be useful for tracking issues is displayed in Figure 1.</span></span>
    
   <span data-ttu-id="23b24-124">**Figura 1. Plantillas que coinciden con la búsqueda de problemas**</span><span class="sxs-lookup"><span data-stu-id="23b24-124">**Figure 1. Templates that match the search for issues**</span></span>

   <span data-ttu-id="23b24-125">![Plantillas que coinciden con la búsqueda de problemas](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Plantillas que coinciden con la búsqueda de problemas")</span><span class="sxs-lookup"><span data-stu-id="23b24-125">![Templates that match the search for issues](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Templates that match the search for issues")</span></span>
  
4. <span data-ttu-id="23b24-126">Elija **Problemas**.</span><span class="sxs-lookup"><span data-stu-id="23b24-126">Choose **Issues**.</span></span>
    
<span data-ttu-id="23b24-127">Access crea un conjunto de tablas y vistas.</span><span class="sxs-lookup"><span data-stu-id="23b24-127">Access creates a set of tables and views.</span></span>
  
## <a name="explore-the-app"></a><span data-ttu-id="23b24-128">Explorar la aplicación</span><span class="sxs-lookup"><span data-stu-id="23b24-128">Explore the app</span></span>
<span data-ttu-id="23b24-129"><a name="ac15_CreateAndCustomizeWebApp_ExploreTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="23b24-129"></span></span>

<span data-ttu-id="23b24-130">Para comprender si el esquema y las vistas se ajustan a sus necesidades, debería examinarlos.</span><span class="sxs-lookup"><span data-stu-id="23b24-130">To understand whether the schema and views meet your needs, you should examine them.</span></span>
  
<span data-ttu-id="23b24-p105">Las tablas que se crean al seleccionar el esquema Problemas se muestran en el panel de icono. Las tablas Problemas, Cliente y Empleados son el enfoque principal de la aplicación. En la tabla Problema se almacena información sobre cada problema. Cada problema lo abre un empleado, y está asignado a él, en nombre de un cliente. Las tablas Problemas relacionados y Comentarios sobre el problema sirven de apoyo para la aplicación. La tabla Problemas relacionados le permite vincular un problema con otro. La tabla Comentarios sobre el problema almacena varios comentarios sobre un solo problema.</span><span class="sxs-lookup"><span data-stu-id="23b24-p105">The tables created by selecting the Issues schema are displayed in the Tile Pane. The Issues, Customer, and Employees tables are the main focus of the app. The Issues table stores information about each issue. Each issue is opened by and assigned to an employee on behalf of a customer. The Related Issues and Issue Comments tables play a supporting role in the app. The Related Issues table enables you to link one issue to another. The Issue Comments table stores multiple comments for a single issue.</span></span>
  
<span data-ttu-id="23b24-p106">En una base de datos de escritorio de Access (.accdb), las relaciones entre las tablas se administran en la ventana **Relaciones**. Las aplicaciones de Access 2013 administran las relaciones mediante campos establecidos en el tipo de datos **Búsqueda**. Examinemos las relaciones de la tabla Problemas. Para ello, haga clic con el botón secundario del mouse en el icono **Problemas** y seleccione **Editar tabla**.</span><span class="sxs-lookup"><span data-stu-id="23b24-p106">In an Access desktop (.accdb) database, the relationships between tables are managed in the **Relationships** window. Access 2013 apps manage relationships by using fields set to the **Lookup** data type. Let's examine the relationships for the Issues table by right-clicking the **Issues** tile and selecting **Edit Table**.</span></span>
  
<span data-ttu-id="23b24-p107">El campo **Cliente** está relacionado con la tabla **Clientes**. Para examinar la relación, seleccione el campo **Cliente** y luego **Modificar búsquedas**. Aparecerá el **Asistente para búsquedas**, tal como se muestra en la figura 2.</span><span class="sxs-lookup"><span data-stu-id="23b24-p107">The **Customer** field is related to the **Customers** table. To examine the relationship, select the **Customer** field and then select **Modify Lookups**. The **Lookup Wizard** is displayed, as shown in Figure 2.</span></span> 
  
<span data-ttu-id="23b24-144">**Figura 2. Asistente para búsquedas que muestra la relación con la tabla Clientes**</span><span class="sxs-lookup"><span data-stu-id="23b24-144">**Figure 2. Lookup Wizard displaying the relationship to the Customers table**</span></span>

<span data-ttu-id="23b24-145">![Asistente para búsquedas que muestra la relación](media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Asistente para búsquedas que muestra la relación")</span><span class="sxs-lookup"><span data-stu-id="23b24-145">![Lookup Wizard displaying the relationship](media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Lookup Wizard displaying the relationship")</span></span>
  
<span data-ttu-id="23b24-146">En el cuadro de diálogo Asistente para búsquedas se muestra que el campo **Cliente** está vinculado a la tabla **Clientes** y que se debe devolver el campo **Nombre para mostrar, Nombre Apellidos** de la tabla **Clientes**.</span><span class="sxs-lookup"><span data-stu-id="23b24-146">The Lookup Wizard dialog box shows that the **Customer** field is linked to the **Customers** table and to return the **Display Name First Last** field from the **Customers** table.</span></span> 
  
<span data-ttu-id="23b24-p108">Los campos **Abierto por**, **Asignada a** y **Cambiado por** están relacionados con la tabla **Empleados**. También se han establecido otros campos en el tipo de datos **Búsqueda**. En estos casos, el tipo de datos Búsqueda se usa para especificar valores concretos que se deben permitir en el campo.</span><span class="sxs-lookup"><span data-stu-id="23b24-p108">The **Opened By**, **Assigned To**, and **Changed By** fields are related to the **Employees** table. Several other fields are also set to the **Lookup** data type. In these cases, the Lookup data type is used to specify the specific values to allow for in the field.</span></span> 
  
<span data-ttu-id="23b24-p109">Cierre la tabla **Problemas** y examine el panel de icono. Los tres iconos superiores, para las tablas **Problemas**, **Clientes** y **Empleados**, se muestran de manera diferente que en los dos iconos inferiores de las tablas **Problemas relacionados** y **Comentarios sobre el problema**, tal como se muestra en la figura 3.</span><span class="sxs-lookup"><span data-stu-id="23b24-p109">Close the **Issues** table and examine the Tile Pane. The top three tiles, for the **Issues**, **Customers**, and **Employees** tables, are displayed differently than the bottom two tiles for the **Related Issues** and **Issue Comments** table, as shown in Figure 3.</span></span> 
  
<span data-ttu-id="23b24-152">**Figura 3. Panel de icono del esquema Problemas**</span><span class="sxs-lookup"><span data-stu-id="23b24-152">**Figure 3. Tile Pane for the Issues schema**</span></span>

<span data-ttu-id="23b24-153">![Panel de icono del esquema Problemas](media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Panel de icono del esquema Problemas")</span><span class="sxs-lookup"><span data-stu-id="23b24-153">![Tile Pane for the Issues schema](media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Tile Pane for the Issues schema")</span></span>
  
<span data-ttu-id="23b24-154">Las tablas **Problemas relacionados** y **Comentarios sobre el problema** están atenuadas porque no deben mostrarse al usuario en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="23b24-154">The **Related Issues** and **Issue Comments** tables are dimmed because they are to be hidden from the user in the web browser.</span></span> 
  
<span data-ttu-id="23b24-p110">Usemos la aplicación para hacer el seguimiento de algunos problemas. Para ello, haga clic en **Iniciar aplicación** para abrir la aplicación en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="23b24-p110">Let's use the app to track some issues. To do this, click **Launch App** to open the app in your web browser.</span></span> 
  
<span data-ttu-id="23b24-p111">La aplicación abre la vista **Lista de problemas** de la tabla Problemas. Antes de agregar un problema, se recomienda agregar algunos clientes y empleados. Haga clic en el icono **Clientes** para comenzar a agregar clientes.</span><span class="sxs-lookup"><span data-stu-id="23b24-p111">The app opens the **Issues List** view of the Issues table. Before adding an issue, it would be a good idea to add some customers and employees. Click the **Customers** tile to start adding customers.</span></span> 
  
<span data-ttu-id="23b24-160">Use el Selector de vistas para elegir una de las tres vistas disponibles para la tabla **Clientes**, con las etiquetas **Lista**, **Hoja de datos** y **Grupos**, tal como se muestra en la figura 4.</span><span class="sxs-lookup"><span data-stu-id="23b24-160">Use the View Selector to choose one of three views available for the **Customers** table, labeled **List**, **Datasheet**, and **Groups** as shown in Figure 4.</span></span> 
  
<span data-ttu-id="23b24-161">**Figura 4. Selector de vistas**</span><span class="sxs-lookup"><span data-stu-id="23b24-161">**Figure 4. View Selector**</span></span>

<span data-ttu-id="23b24-162">![Selector de vistas](media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "Selector de vistas")</span><span class="sxs-lookup"><span data-stu-id="23b24-162">![View Selector](media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "View Selector")</span></span>
  
<span data-ttu-id="23b24-p112">Si elige **Lista**, se activará la vista **Lista de clientes**, que es una vista de detalles de la lista. La vista de detalles de la lista es una de las vistas que Access genera automáticamente al crear una tabla. La principal característica que diferencia una vista de detalles de la lista es el panel de listas que aparecen en el lado izquierdo de la vista. El panel de vistas se usa para filtrar los registros de la vista y navegar por ellos. En una base de datos de escritorio de Access, la implementación de una vista de lista en la que se permiten búsquedas requeriría la redacción de código personalizado.</span><span class="sxs-lookup"><span data-stu-id="23b24-p112">Choosing **List** activates the **Customers List** view, which is a List Details view. List Details is one of the views Access automatically generates when you create a table. The main feature that distinguishes a List Details view is the list pane that appears on the left side of the view. The list pane is used to filter and navigate the records contained in the view. In an Access desktop database, implementing a searchable list view would require writing custom code.</span></span> 
  
<span data-ttu-id="23b24-p113">Si selecciona **Hoja de datos**, se abrirá la vista **Hoja de datos Clientes**. La hoja de datos es otro tipo de vista que Access genera automáticamente al crear una tabla. Las vistas de hoja de datos son de utilidad para los usuarios que consideran más fácil especificar, ordenar y filtrar datos en forma de hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="23b24-p113">Choosing **Datasheet** opens the **Customers Datasheet** view. Datasheet is the other kind of view Access automatically generates when you create a table. Datasheet views are useful for those who find it easier to enter, sort, and filter data in a spreadsheet-like manner.</span></span> 
  
<span data-ttu-id="23b24-p114">Si selecciona Grupos, se abre una vista de resumen. Las vistas de resumen se pueden usar para agrupar registros según un campo y calcular opcionalmente una suma o un promedio.</span><span class="sxs-lookup"><span data-stu-id="23b24-p114">Choosing Groups opens a Summary view. Summary views can be used to group records based on a field and optionally calculate a sum or average.</span></span>
  
<span data-ttu-id="23b24-p115">A medida que agregue clientes, use la barra de acciones para agregar, editar, guardar y eliminar registros, así como para cancelar las modificaciones. La barra de acciones se puede personalizar y aparece en la parte superior de cada vista, tal como se muestra en la figura 5.</span><span class="sxs-lookup"><span data-stu-id="23b24-p115">As you're adding customers, use the Action Bar to add records, edit records, save records, delete records, and cancel edits. The Action Bar is a customizable toolbar that appears at the top of each view, as shown in Figure 5.</span></span>
  
<span data-ttu-id="23b24-175">**Figura 5. Barra de acciones**</span><span class="sxs-lookup"><span data-stu-id="23b24-175">**Figure 5. Action Bar**</span></span>

<span data-ttu-id="23b24-176">![Barra de acciones](media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Barra de acciones")</span><span class="sxs-lookup"><span data-stu-id="23b24-176">![Action Bar](media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Action Bar")</span></span>
  
<span data-ttu-id="23b24-p116">Cuando haya agregado algunos clientes y empleados, abra la vista Lista de problemas y comience a agregar un problema. A medida que escriba el nombre de un cliente en el cuadro cliente, aparecerán uno o más nombres de cliente, tal como se muestra en la figura 6.</span><span class="sxs-lookup"><span data-stu-id="23b24-p116">Once you've added some customers and employees open the Issues List view and start adding an issue. As you type the name of a customer into the into the Customer box, one or more of the customer names will appear, as shown in Figure 6.</span></span>
  
<span data-ttu-id="23b24-179">**Figura 6. Control Autocompletar**</span><span class="sxs-lookup"><span data-stu-id="23b24-179">**Figure 6. AutoComplete control**</span></span>

<span data-ttu-id="23b24-180">![Control Autocompletar](media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "Control Autocompletar")</span><span class="sxs-lookup"><span data-stu-id="23b24-180">![AutoComplete control](media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "AutoComplete control")</span></span>
  
<span data-ttu-id="23b24-p117">El cuadro Cliente es un control de tipo autocompletar, que muestra una lista de registros que coinciden con lo que esté escribiendo en el cuadro. Esto ayuda a garantizar la precisión de la entrada de datos.</span><span class="sxs-lookup"><span data-stu-id="23b24-p117">The Customer box is an AutoComplete control. The AutoComplete control displays a list of records that match what you're typing into the box. This helps ensure the accuracy of data entry.</span></span>
  
## <a name="customize-the-app"></a><span data-ttu-id="23b24-184">Personalizar la aplicación</span><span class="sxs-lookup"><span data-stu-id="23b24-184">Customize the app</span></span>
<span data-ttu-id="23b24-185"><a name="ac15_CreateAndCustomizeWebApp_CustomizeTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="23b24-185"></span></span>

<span data-ttu-id="23b24-p118">Tras dar un paseo por la aplicación, observará que la vista Lista de problemas no contiene información de contacto para el cliente. Personalicemos la aplicación para agregar el número de teléfono de trabajo del cliente a la tabla Problemas al crear el problema.</span><span class="sxs-lookup"><span data-stu-id="23b24-p118">Now that you've taken a tour of the app, you notice that the Issues List view doesn't contain contact information for the customer. Let's customize the app to add the customer's work phone to the Issues table as the issue is being created.</span></span>
  
### <a name="to-add-a-field-to-the-issues-table"></a><span data-ttu-id="23b24-188">Agregar un campo a la tabla Problemas</span><span class="sxs-lookup"><span data-stu-id="23b24-188">To add a field to the Issues table</span></span>

1. <span data-ttu-id="23b24-189">Abra la aplicación en Access.</span><span class="sxs-lookup"><span data-stu-id="23b24-189">Open the app in Access.</span></span>
    
2. <span data-ttu-id="23b24-190">Seleccione el icono **Problemas**, el icono **Configuración/Acción** y luego **Editar tabla**.</span><span class="sxs-lookup"><span data-stu-id="23b24-190">Choose the **Issues** tile, choose the **Settings/Action** icon, and then choose **Edit Table**.</span></span>
    
3. <span data-ttu-id="23b24-191">Especifique el **Número de contacto** en la primera celda vacía de la columna **Nombre del campo**.</span><span class="sxs-lookup"><span data-stu-id="23b24-191">Enter **Contact Number** in the first blank cell in the **Field Name** column.</span></span> 
    
4. <span data-ttu-id="23b24-192">Seleccione **Texto corto** en la columna **Tipo de datos**.</span><span class="sxs-lookup"><span data-stu-id="23b24-192">Choose **Short Text** in the **Data Type** column.</span></span> 
    
5. <span data-ttu-id="23b24-193">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="23b24-193">Choose **Save**.</span></span>
    
6. <span data-ttu-id="23b24-194">Cierre la tabla Problemas.</span><span class="sxs-lookup"><span data-stu-id="23b24-194">Close the Issues table.</span></span>
    
<span data-ttu-id="23b24-195">Ahora que disponemos de un campo en el que almacenar el número de teléfono, creemos una macro de datos para buscar la información de contacto.</span><span class="sxs-lookup"><span data-stu-id="23b24-195">Now that we have field in which to store the phone number, let's create a data macro to look up the contact information.</span></span>
  
### <a name="to-create-the-data-macro-to-look-up-contact-information"></a><span data-ttu-id="23b24-196">Crear la macro de datos que permite buscar información de contacto</span><span class="sxs-lookup"><span data-stu-id="23b24-196">To create the data macro to look up contact information</span></span>

1. <span data-ttu-id="23b24-197">En el grupo **Crear**, seleccione **Opciones avanzadas** y elija **Macro de datos**.</span><span class="sxs-lookup"><span data-stu-id="23b24-197">In the **Create** group, choose **Advanced**, and then choose **Data Macro**.</span></span>
    
2. <span data-ttu-id="23b24-198">Seleccione **Crear parámetro**.</span><span class="sxs-lookup"><span data-stu-id="23b24-198">Choose **Create Parameter**.</span></span>
    
3. <span data-ttu-id="23b24-p119">En el cuadro **Nombre**, especifique **CustID**. En la lista desplegable **Tipo**, seleccione **Número (decimal flotante).**</span><span class="sxs-lookup"><span data-stu-id="23b24-p119">In the **Name** box, enter **CustID**. In the **Type** dropdown, choose **Number (Floating Decimal).**</span></span>
    
4. <span data-ttu-id="23b24-201">En la lista desplegable **Agregar nueva acción**, seleccione **LookupRecord**.</span><span class="sxs-lookup"><span data-stu-id="23b24-201">From the **Add New Action** dropdown, choose **LookupRecord**.</span></span> 
    
5. <span data-ttu-id="23b24-202">En la lista desplegable **Buscar un registro en**, seleccione **Clientes**.</span><span class="sxs-lookup"><span data-stu-id="23b24-202">In the **Look Up A Record In** dropdown, choose **Customers**.</span></span> 
    
6. <span data-ttu-id="23b24-203">En el cuadro **Condición WHERE**, especifique **[Clientes].[ID]=[CustID]**.</span><span class="sxs-lookup"><span data-stu-id="23b24-203">In the **Where Condition** box, enter **[Customers].[ID]=[CustID]**.</span></span> 
    
7. <span data-ttu-id="23b24-204">Seleccione **SetReturnVar** de la lista desplegable **Agregar nueva acción**.</span><span class="sxs-lookup"><span data-stu-id="23b24-204">Choose **SetReturnVar** from the **Add New Action** dropdown.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="23b24-p120">Verá dos listas desplegables **Agregar nueva acción**, una en el bloque **LookupRecord** y otra fuera del bloque **LookupRecord**. Debería elegir la lista desplegable **Agregar nueva acción** dentro del bloque **LookupRecord**, tal como se muestra en la figura 7.</span><span class="sxs-lookup"><span data-stu-id="23b24-p120">You'll see two **Add New Action** dropdowns, one within the **LookupRecord** block, and another outside the **LookupRecord** block. You should choose the **Add New Action** dropdown within the **LookupRecord** block, as shown in Figure 7.</span></span> 
  
   <span data-ttu-id="23b24-207">**Figura 7. Lista desplegable Agregar nueva acción**</span><span class="sxs-lookup"><span data-stu-id="23b24-207">**Figure 7. Add New Action dropdown**</span></span>

   <span data-ttu-id="23b24-208">![Lista desplegable Agregar nueva acción](media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Lista desplegable Agregar nueva acción")</span><span class="sxs-lookup"><span data-stu-id="23b24-208">![Add New Action dropdown](media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Add New Action dropdown")</span></span>
  
8. <span data-ttu-id="23b24-209">En el cuadro **Nombre**, escriba **ContactPhone**.</span><span class="sxs-lookup"><span data-stu-id="23b24-209">In the **Name** box, enter **ContactPhone**.</span></span> 
    
9. <span data-ttu-id="23b24-210">En el cuadro **Expresión**, escriba **[Clientes].[Teléfono de trabajo]**.</span><span class="sxs-lookup"><span data-stu-id="23b24-210">In the **Expression** box, enter **[Customers].[Work Phone]**.</span></span> 
    
10. <span data-ttu-id="23b24-p121">Seleccione **Guardar**. Escriba **GetContactPhone** en el cuadro **Nombre de macro** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="23b24-p121">Choose **Save**. Enter **GetContactPhone** in the **Macro Name** box and then choose **OK**.</span></span>
    
    <span data-ttu-id="23b24-213">La macro debería tener el aspecto de la macro que se muestra en la figura 8.</span><span class="sxs-lookup"><span data-stu-id="23b24-213">The macro should resemble the macro shown in Figure 8.</span></span>
    
    <span data-ttu-id="23b24-214">**Figura 8. Macro de datos GetContactPhone**</span><span class="sxs-lookup"><span data-stu-id="23b24-214">**Figure 8. GetContactPhone data macro**</span></span>

    <span data-ttu-id="23b24-215">![Macro de datos GetContactPhone](media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "Macro de datos GetContactPhone")</span><span class="sxs-lookup"><span data-stu-id="23b24-215">![GetContactPhone data macro](media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "GetContactPhone data macro")</span></span>
  
11. <span data-ttu-id="23b24-216">Cierre la macro Vista Diseño.</span><span class="sxs-lookup"><span data-stu-id="23b24-216">Close macro Design View.</span></span>
    
<span data-ttu-id="23b24-217">Ahora estamos listos para agregar el campo **Número de contacto** al formulario Lista de problemas.</span><span class="sxs-lookup"><span data-stu-id="23b24-217">Now we're ready to add the **Contact Number** field to the Issues List form.</span></span> 
  
### <a name="to-add-the-contact-number-field-to-the-issues-list-form"></a><span data-ttu-id="23b24-218">Agregar el campo Número de contacto al formulario Lista de problemas</span><span class="sxs-lookup"><span data-stu-id="23b24-218">To add the Contact Number field to the Issues List form</span></span>

1. <span data-ttu-id="23b24-p122">Seleccione la tabla **Problemas** para elegir el formulario Lista de problemas.</span><span class="sxs-lookup"><span data-stu-id="23b24-p122">Choose the **Issues** table. This chooses the Issues list form.</span></span> 
    
2. <span data-ttu-id="23b24-221">En el Selector de vistas, seleccione **Lista**, el icono **Configuración/Acción** y luego **Editar**.</span><span class="sxs-lookup"><span data-stu-id="23b24-221">In the View selector, choose **List**, choose the **Settings/Action** icon, and then choose **Edit**.</span></span>
    
3. <span data-ttu-id="23b24-222">Arrastre el campo **Número de contacto** del panel **Lista de campos** a la ubicación del formulario en la que desee mostrar el número de contacto.</span><span class="sxs-lookup"><span data-stu-id="23b24-222">Drag the **Contact Number** field form the **Field List** pane to the location on the form where you want the contact number to be displayed.</span></span> 
    
4. <span data-ttu-id="23b24-223">Seleccione el cuadro de texto **Número de contacto** y haga clic en **Datos**.</span><span class="sxs-lookup"><span data-stu-id="23b24-223">Choose the **Contact Number** text box, and then click **Data**.</span></span> 
    
5. <span data-ttu-id="23b24-224">En el cuadro **Nombre del control**, escriba **CustomerContact** y cierre la ventana emergente **Datos**.</span><span class="sxs-lookup"><span data-stu-id="23b24-224">In the **Control Name** box, enter **CustomerContact** and then close the **Data** popup.</span></span> 
    
6. <span data-ttu-id="23b24-225">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="23b24-225">Choose **Save**.</span></span>
    
<span data-ttu-id="23b24-p123">Ahora debemos escribir una macro de interfaz de usuario (UI) que copia el campo **Teléfono de trabajo** de la tabla **Clientes** al campo **Número de contacto** de la tabla **Problemas**. El evento **Después de actualizar** del control **CustomerAutocomplete** es una buena ubicación para la macro.</span><span class="sxs-lookup"><span data-stu-id="23b24-p123">Now we should write a user interface (UI) macro that copies the **Work Phone** field from the **Customers** table into the **Contact Phone** field of the **Issues** table. The **After Update** event of the **CustomerAutocomplete** control is a good location for the macro.</span></span> 
  
### <a name="to-create-the-afterupdate-macro"></a><span data-ttu-id="23b24-228">Crear la macro Después de actualizar</span><span class="sxs-lookup"><span data-stu-id="23b24-228">To create the AfterUpdate macro</span></span>

1. <span data-ttu-id="23b24-229">Seleccione el control **CustomerAutocomplete**, el botón **Acciones** y luego **Después de actualizar**.</span><span class="sxs-lookup"><span data-stu-id="23b24-229">Choose the **CustomerAutocomplete** control, choose the **Actions** button, and then choose **After Update**.</span></span> 
    
    <span data-ttu-id="23b24-230">Se abre una macro vacía en la macro Vista Diseño.</span><span class="sxs-lookup"><span data-stu-id="23b24-230">A blank macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="23b24-231">En la lista desplegable **Agregar nueva acción**, seleccione **RunDataMacro**.</span><span class="sxs-lookup"><span data-stu-id="23b24-231">From the **Add New Action** dropdown, choose **RunDataMacro**.</span></span> 
    
3. <span data-ttu-id="23b24-232">En la lista desplegable **Nombre de macro**, seleccione **GetContactPhone**.</span><span class="sxs-lookup"><span data-stu-id="23b24-232">In the **Macro Name** dropdown, choose **GetContactPhone**.</span></span> 
    
4. <span data-ttu-id="23b24-233">En el cuadro **CustID**, escriba **[CustomerAutocomplete]**.</span><span class="sxs-lookup"><span data-stu-id="23b24-233">In the **CustID** box, enter **[CustomerAutocomplete]**.</span></span> 
    
5. <span data-ttu-id="23b24-234">En el cuadro **SetLocalVar**, escriba **Teléfono**.</span><span class="sxs-lookup"><span data-stu-id="23b24-234">In the **SetLocalVar** box, enter **Phone**.</span></span> 
    
    <span data-ttu-id="23b24-235">Cuando elija la macro de datos GetContactPhone creada anteriormente, Access completó automáticamente el nombre del parámetro y la variable devuelta de la macro.</span><span class="sxs-lookup"><span data-stu-id="23b24-235">When you chose the GetContactPhone data macro that was created earlier, Access automatically filled in the parameter name and return variable for the macro.</span></span>
    
    <span data-ttu-id="23b24-236">El número de teléfono del cliente se almacena en la variable denominada Phone.</span><span class="sxs-lookup"><span data-stu-id="23b24-236">The phone number for the customer is stored in a variable named Phone.</span></span>
    
6. <span data-ttu-id="23b24-237">En la lista desplegable **Agregar nueva acción**, seleccione **SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="23b24-237">From the **Add New Action** dropdown, choose **SetProperty**.</span></span> 
    
7. <span data-ttu-id="23b24-238">En el cuadro **Nombre del control**, escriba **CustomerContact**.</span><span class="sxs-lookup"><span data-stu-id="23b24-238">In the **Control Name** box, enter **CustomerContact**.</span></span> 
    
8. <span data-ttu-id="23b24-239">En la lista desplegable **Propiedad**, seleccione **Valor**.</span><span class="sxs-lookup"><span data-stu-id="23b24-239">In the **Property** dropdown, choose **Value**.</span></span> 
    
9. <span data-ttu-id="23b24-240">En el cuadro **Valor**, escriba **=[Teléfono]**.</span><span class="sxs-lookup"><span data-stu-id="23b24-240">In the **Value** box, enter **=[Phone]**.</span></span> 
    
10. <span data-ttu-id="23b24-241">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="23b24-241">Choose **Save**.</span></span>
    
    <span data-ttu-id="23b24-242">La macro debería tener el aspecto de la macro que se muestra en la figura 9.</span><span class="sxs-lookup"><span data-stu-id="23b24-242">The macro should resemble the macro shown in Figure 9.</span></span>
    
    <span data-ttu-id="23b24-243">**Figura 9. Macro Después de actualizar**</span><span class="sxs-lookup"><span data-stu-id="23b24-243">**Figure 9. After Update macro**</span></span>

    <span data-ttu-id="23b24-244">![Macro Después de actualizar](media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "Macro Después de actualizar")</span><span class="sxs-lookup"><span data-stu-id="23b24-244">![After Update macro](media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "After Update macro")</span></span>
  
11. <span data-ttu-id="23b24-245">Cierre la macro Vista Diseño.</span><span class="sxs-lookup"><span data-stu-id="23b24-245">Close macro Design View.</span></span>
    
12. <span data-ttu-id="23b24-p124">Cierre la vista Lista de problemas. Seleccione **Sí** cuando se le solicite guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="23b24-p124">Close the Issues List view. Choose **Yes** when you are prompted to save your changes.</span></span> 
    
<span data-ttu-id="23b24-248">Ahora tiene todo preparado para escribir la personalización.</span><span class="sxs-lookup"><span data-stu-id="23b24-248">Now we're ready to text the customization.</span></span> <span data-ttu-id="23b24-249">Haga clic en **Iniciar aplicación** para abrir la aplicación en el explorador web y después agregue un nuevo problema.</span><span class="sxs-lookup"><span data-stu-id="23b24-249">Click **Launch App** to open the app in your web browser and then add a new issue.</span></span> <span data-ttu-id="23b24-250">El cuadro **Número de contacto** se actualizará automáticamente después de que escriba el nombre del cliente, tal como se muestra en la figura 10.</span><span class="sxs-lookup"><span data-stu-id="23b24-250">The **Contact Number** box updates automatically after the customer name is entered,  as shown in Figure 10.</span></span> 
  
<span data-ttu-id="23b24-251">**Figura 10. Vista Problemas actualizada con el número de teléfono**</span><span class="sxs-lookup"><span data-stu-id="23b24-251">**Figure 10. Issues view updated with phone number**</span></span>

<span data-ttu-id="23b24-252">![Vista Problemas actualizada con el número de teléfono](media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "Vista Problemas actualizada con el número de teléfono")</span><span class="sxs-lookup"><span data-stu-id="23b24-252">![Issues view updated with phone number](media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "Issues view updated with phone number")</span></span>
  
## <a name="conclusion"></a><span data-ttu-id="23b24-253">Conclusión</span><span class="sxs-lookup"><span data-stu-id="23b24-253">Conclusion</span></span>

<span data-ttu-id="23b24-p126">El uso de una de las plantillas de esquema incluidas con es una buena manera de iniciar la creación de una aplicación web de Access. Las vistas que se crean automáticamente incluyen funciones avanzadas que requieren código personalizado que se debe implementar en una base de datos de escritorio de Access.</span><span class="sxs-lookup"><span data-stu-id="23b24-p126">Using one of the schema templates included with is a good way to jump start the creation of an Access web app. The views that are automatically created for you contain advanced functionally that requires custom code to implement in a Access desktop database.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="23b24-256">Vea también</span><span class="sxs-lookup"><span data-stu-id="23b24-256">See also</span></span>

- [<span data-ttu-id="23b24-257">Novedades para desarrolladores de Access 2013</span><span class="sxs-lookup"><span data-stu-id="23b24-257">What's new for Access 2013 developers</span></span>](https://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx) 
- [<span data-ttu-id="23b24-258">Referencia de la aplicación de acceso web personalizados</span><span class="sxs-lookup"><span data-stu-id="23b24-258">Access custom web app reference</span></span>](access-custom-web-app-reference.md)
  

