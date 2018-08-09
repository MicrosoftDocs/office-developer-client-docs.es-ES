---
title: Soluciones de espacio aislado de ejemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 415fa0fa-b7b7-4acb-a437-f54c34064004
description: En este tema, se presentan dos ejemplos que muestran el tipo de código que puede escribir en un solución de espacio aislado de InfoPath y cómo publicar la plantilla de formulario.
ms.openlocfilehash: b0874e34d843850df55eee87d689ce0d01112635
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815968"
---
# <a name="sample-sandboxed-solutions"></a><span data-ttu-id="ccb00-103">Soluciones de espacio aislado de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ccb00-103">Sample sandboxed solutions</span></span>

<span data-ttu-id="ccb00-p101">Los formularios de InfoPath con código administrado se pueden publicar en la infraestructura solución de espacio aislado de SharePoint desde InfoPath Designer. En este tema, se presentan dos ejemplos que muestran el tipo de código que puede escribir en un solución de espacio aislado de InfoPath y cómo publicar la plantilla de formulario.</span><span class="sxs-lookup"><span data-stu-id="ccb00-p101">InfoPath forms with managed code can be published to the SharePoint sandboxed solution infrastructure from the InfoPath Designer. This topic provides two examples that show the kind of code that you can write in an InfoPath sandboxed solution, and how to publish the form template.</span></span>
  
## <a name="example-1-sorting-data-in-an-order-form"></a><span data-ttu-id="ccb00-106">En el ejemplo 1: Ordenar datos en un formulario de pedido</span><span class="sxs-lookup"><span data-stu-id="ccb00-106">Example 1: Sorting data in an order form</span></span>

<span data-ttu-id="ccb00-p102">Una tarea útil que puede realizar con código en un formulario de InfoPath es ordenar datos en una tabla de repetición. Para esto, el código reordena los nodos en el documento XML subyacente que se muestra en el formulario de InfoPath. A pesar de que el caso descrito en este tema está destinado a su publicación directamente desde InfoPath como un solución de espacio aislado, también se puede implementar como una plantilla de formulario aprobada por administrador.</span><span class="sxs-lookup"><span data-stu-id="ccb00-p102">A useful task that you can perform by using code in an InfoPath form is to sort data in a repeating table. To do this, the code reorders the nodes in underlying XML document that is displayed in the InfoPath form. Although the scenario described in this topic is targeted for publishing directly from InfoPath as a sandboxed solution, it can also be deployed as an administrator-approved form template.</span></span>
  
<span data-ttu-id="ccb00-110">Antes de comenzar, asegúrese de que se cumplen los siguientes requisitos.</span><span class="sxs-lookup"><span data-stu-id="ccb00-110">Before you start, make sure that you meet the following requirements.</span></span>
  
- <span data-ttu-id="ccb00-111">Es administrador de colección de sitios en el sitio de SharePoint Server 2010 o SharePoint Foundation 2010 en donde desea publicar el formulario.</span><span class="sxs-lookup"><span data-stu-id="ccb00-111">You are a site collection administrator on the SharePoint Server 2010 or SharePoint Foundation 2010 site where you want to publish the form.</span></span>
    
- <span data-ttu-id="ccb00-p103">Consulte con el administrador de la granja de servidores para asegurarse de que el Servicio de código de espacio aislado de Microsoft SharePoint Foundation esté en uso en el servidor. Para más información, vea [Publicar formularios con código](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="ccb00-p103">Check with the farm administrator to make sure that the Microsoft SharePoint Foundation Sandboxed Code Service is running on the server. For more information, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span>
    
- <span data-ttu-id="ccb00-114">El lenguaje de programación que seleccionó para la plantilla de formulario es **C#** o **Visual Basic** sin ningún nombre de versión anterior que lo siga.</span><span class="sxs-lookup"><span data-stu-id="ccb00-114">The programming language that you have selected for the form template is either **C#** or **Visual Basic** without any earlier version name after it.</span></span> <span data-ttu-id="ccb00-115">Las versiones compatibles con InfoPath 2007 y InfoPath 2003 de los lenguajes de programación y los modelos de objetos no se admiten para soluciones de espacio aislado.</span><span class="sxs-lookup"><span data-stu-id="ccb00-115">The InfoPath 2007-compatible and InfoPath 2003-compatible versions of the programming languages and object models are not supported for sandboxed solutions.</span></span> <span data-ttu-id="ccb00-116">Para obtener más información acerca de cómo especificar el lenguaje de programación, vea [desarrollar con Visual Studio](how-to-develop-with-visual-studio.md).</span><span class="sxs-lookup"><span data-stu-id="ccb00-116">For more information about how to specify the programming language, see [Develop with Visual Studio](how-to-develop-with-visual-studio.md).</span></span>
    
<span data-ttu-id="ccb00-117">Realice los siguientes pasos para crear una plantilla de formulario que ordene los datos en un control de **Tabla de repetición** en el formulario.</span><span class="sxs-lookup"><span data-stu-id="ccb00-117">Perform the following steps to create a form template that sorts the data in a **Repeating Table** control on the form.</span></span> 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a><span data-ttu-id="ccb00-118">Para crear una plantilla de formulario que ordena datos mediante programación en el formulario</span><span class="sxs-lookup"><span data-stu-id="ccb00-118">To create a form template that programmatically sorts data in the form</span></span>

1. <span data-ttu-id="ccb00-p105">Cree una nueva plantilla de formulario en el diseñador de InfoPath y agregue un control de **Tabla de repetición** al formulario. El código de muestra para este ejemplo ordena las filas basadas en la primera columna de la tabla, pero puede modificar fácilmente el código para trabajar con cualquier columna.</span><span class="sxs-lookup"><span data-stu-id="ccb00-p105">Create a new form template in the InfoPath designer, and add a **Repeating Table** control to the form. The sample code for this example sorts the rows based on the first column in the table, but you can easily modify the code to work with any column.</span></span> 
    
2. <span data-ttu-id="ccb00-p106">Agregue un control **Botón** al formulario. El código para ordenar la tabla se agregará en el controlador de eventos para el evento **Clicked** del botón, pero también puede usar otro evento para este propósito.</span><span class="sxs-lookup"><span data-stu-id="ccb00-p106">Add a **Button** control to the form. The code to sort the table will be added to the event handler for the button's **Clicked** event, but you could also use another event for this purpose.</span></span> 
    
3. <span data-ttu-id="ccb00-p107">Seleccione el botón, haga clic en la pestaña **Propiedades** y, a continuación, en **Código personalizado**. Si el formulario no se guardó aún, se le solicitará hacerlo, y el Editor de código se abrirá con el cursor en el controlador de eventos del botón.</span><span class="sxs-lookup"><span data-stu-id="ccb00-p107">Select the button, click the **Properties** tab, and then click **Custom Code**. If your form hasn't been saved yet, you are prompted to save it, and then the Code Editor will open with the cursor in the button's event handler.</span></span>
    
4. <span data-ttu-id="ccb00-p108">Pegue el siguiente código en el controlador de eventos del botón. El código coloca los elementos de la primera columna en una matriz, ordena la matriz y vuelve a ordenar la tabla basada en la matriz ordenada. Este código asume que los datos que se ordenan son datos de cadena.</span><span class="sxs-lookup"><span data-stu-id="ccb00-p108">Paste the following code into the button's event handler. The code puts the elements from the first column into an array, sorts the array, and then reorders the table based on the sorted array. This code assumes that the data being sorted is string data.</span></span>
    
   ```cs
    // Put the elements from the first column into an array.
    XPathNavigator root = this.CreateNavigator();
        
    // Create a node iterator which contains only the values that you want to sort.
    // For this form, the entire table is in "group1", each row is a "group2"
    // and the rows are "field1", "field2" and "field3" respectively.
    XPathNodeIterator nodeIterator = root.Select(
        "/my:myFields/my:group1/my:group2/my:field1", this.NamespaceManager);
        
    // Create arrays to use for sorting.
    string[] sortArrayWords = new string[nodeIterator.Count + 1];
    int[] sortArrayKeys = new int[nodeIterator.Count + 1];
    int arrayPosition = 1;
        
    // Populate the arrays for sorting.
    while (nodeIterator.MoveNext()) 
    {
        // Loop until there are no more elements
        sortArrayWords[arrayPosition] = nodeIterator.Current.Value;
        sortArrayKeys[arrayPosition] = arrayPosition;
        arrayPosition += 1;
    }
        
    // Sort the array.
    Array.Sort(sortArrayWords, sortArrayKeys);
    arrayPosition = 0;
        
    // Create new XML to update the table.
    string newTableXML = "";
    // Iterate through the sorted array of keys.
    for (int i = 1; i <= sortArrayWords.Length - 1; i++) 
    {
        nodeIterator = root.Select(
            "/my:myFields/my:group1/my:group2", this.NamespaceManager);
            
        // Go to the right position in the table.
        for (int j = 1; j <= sortArrayKeys[i]; j++) 
        {
            nodeIterator.MoveNext();
        }
            
        // Add the row to the XML.
        newTableXML += nodeIterator.Current.OuterXml;
    }
        
    // Set the table to use the new XML.
    root.SelectSingleNode(
        "/my:myFields/my:group1", this.NamespaceManager).InnerXml = newTableXML;
    
   ```

   ```vb
    ' Put the elements from the first column into an array.
    Dim root As XPathNavigator = Me.CreateNavigator
    ' Create a node iterator which contains only the values that you want to sort
    ' For this form, the entire table is in "group1",
    ' each row is a "group2"
    ' and the rows are "field1", "field2" and "field3" respectively.
    Dim nodeIterator As XPathNodeIterator = root.Select( _
        "/my:myFields/my:group1/my:group2/my:field1", Me.NamespaceManager)
    ' Create arrays to use for sorting.
    Dim sortArrayWords(nodeIterator.Count) As String
    Dim sortArrayKeys(nodeIterator.Count) As Integer
    Dim arrayPosition As Integer = 1
    ' Populate the arrays for sorting.
    While nodeIterator.MoveNext() ' Loop until there are no more elements
        sortArrayWords(arrayPosition) = nodeIterator.Current.Value
        sortArrayKeys(arrayPosition) = arrayPosition
        arrayPosition += 1
    End While
    ' Sort the array.
    Array.Sort(sortArrayWords, sortArrayKeys)
    arrayPosition = 0
    ' Create new XML to update the table.
    Dim newTableXML As String = ""
    ' Iterate through the sorted array of keys.
    For i As Integer = 1 To sortArrayWords.Length - 1
        nodeIterator = root.Select( _
            "/my:myFields/my:group1/my:group2", Me.NamespaceManager)
        ' Go to the right position in the table.
        For j As Integer = 1 To sortArrayKeys(i)
        nodeIterator.MoveNext()
        Next
    ' Add the row to the XML.
    newTableXML &amp;= nodeIterator.Current.OuterXml
    Next
    ' Set the table to use the new XML.
    root.SelectSingleNode("/my:myFields/my:group1", _
        Me.NamespaceManager).InnerXml = newTableXML
   ```

5. <span data-ttu-id="ccb00-128">Publicar el formulario mediante el uso de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="ccb00-128">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="ccb00-129">Haga clic en **SharePoint Server**, en la ficha **Publicar**, en Backstage.</span><span class="sxs-lookup"><span data-stu-id="ccb00-129">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="ccb00-130">Escriba la dirección URL del sitio de SharePoint en donde desea publicar el formulario y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-130">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="ccb00-131">[!IMPORTANTE] Debe ser administrador de una colección de sitios en este sitio para publicar esta plantilla de formulario como un solución de espacio aislado.</span><span class="sxs-lookup"><span data-stu-id="ccb00-131">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="ccb00-132">Seleccione **Biblioteca de formularios** y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-132">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="ccb00-133">Seleccione **Crear una nueva biblioteca de formularios** y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-133">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="ccb00-134">Escriba el nombre y las descripciones de la biblioteca de formularios y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-134">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="ccb00-135">Haga clic en **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-135">Click **Publish**.</span></span>
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a><span data-ttu-id="ccb00-136">Ejemplo 2: Administrar proveedores en una lista de SharePoint</span><span class="sxs-lookup"><span data-stu-id="ccb00-136">Example 2: Managing vendors in a SharePoint list</span></span>

<span data-ttu-id="ccb00-p109">Este ejemplo implica la programación con el modelo de objetos de Microsoft SharePoint Foundation 2010. Para esto, debe establecer una referencia al ensamblado de Microsoft.SharePoint.dll, que está instalado con una copia con licencia de SharePoint Server 2010.</span><span class="sxs-lookup"><span data-stu-id="ccb00-p109">This example involves programming against the Microsoft SharePoint Foundation 2010 object model. To do that, you must establish a reference to the Microsoft.SharePoint.dll assembly which is installed with a licensed copy of SharePoint Server 2010.</span></span>
  
<span data-ttu-id="ccb00-p110">Microsoft.SharePoint.Server.dll está instalado en C:\Archivos de programa\Archivos comunes\Microsoft Shared\Web Server Extensions\14\ISAPI de manera predeterminada. Este archivo DLL debe incluirse en los proyectos cuando programe en un modelo de objetos de SharePoint. Para establecer una referencia a Microsoft.SharePoint.dll en un proyecto de Visual Studio 2012, abra el **Editor de código** y haga clic en **Agregar referencia** en el menú **Herramientas**. En el cuadro de diálogo **Agregar referencia**, haga clic en la pestaña **Explorar**, especifique la ubicación del archivo Microsoft.SharePoint.dll y haga clic en **Aceptar**. El archivo Microsoft.SharePoint.dll se copiará en el directorio del proyecto para que pueda usar los miembros del modelo de objetos de SharePoint Foundation 2010 en la solución InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ccb00-p110">Microsoft.SharePoint.Server.dll is installed in C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI by default. This DLL must be included in projects where you program against the SharePoint object model. To establish a reference to the Microsoft.SharePoint.dll in a Visual Studio 2012 project, open the **Code Editor**, and then click **Add Reference** on the **Tools** menu. In the **Add Reference** dialog box, click the **Browse** tab, specify the location of the Microsoft.SharePoint.dll file, and then click **OK**. This will copy the Microsoft.SharePoint.dll into the project directory so that you can use SharePoint Foundation 2010 object model members in your InfoPath solution.</span></span>
  
### <a name="designing-the-form-and-developing-the-code"></a><span data-ttu-id="ccb00-144">Diseñar el formulario y desarrollar el código</span><span class="sxs-lookup"><span data-stu-id="ccb00-144">Designing the form and developing the code</span></span>

<span data-ttu-id="ccb00-p111">Del código de un formulario de InfoPath, puede usar el modelo de objetos de SharePoint para crear elementos en listas de búsqueda. Esto resulta útil cuando rellena el cuadro desplegable de una lista de SharePoint y desea agregar nuevos valores a ella sin crear un formulario independiente. En este ejemplo, se usa un cuadro combinado para mostrar todos los valores que están actualmente en la lista y crea lógica de programación para agregar el valor a la lista si aún no existe.</span><span class="sxs-lookup"><span data-stu-id="ccb00-p111">From code in an InfoPath form, you can use the SharePoint object model to create items in lookup lists. This is useful when you populate a drop-down box from a SharePoint list and want to add new values to it without creating a separate form. This example uses a combo box to show all the values currently in the list and creates programming logic to add the value to the list if it does not already exist.</span></span>
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a><span data-ttu-id="ccb00-148">Para crear una plantilla de formulario que pueda agregar nuevos elementos a un cuadro combinado basado en una lista de SharePoint</span><span class="sxs-lookup"><span data-stu-id="ccb00-148">To create a form template that can add new items to a combo box based on a SharePoint list</span></span>

1. <span data-ttu-id="ccb00-p112">Cree una lista personalizada simple en un servidor de SharePoint Server 2010 y cambie el nombre a MiLista. El ejemplo siguiente usa un **Cuadro combinado** vinculado al campo **Título** para esta lista.</span><span class="sxs-lookup"><span data-stu-id="ccb00-p112">Create a simple custom list on a SharePoint Server 2010 server, and name it MyList. The following example uses a **Combo Box** bound to the **Title** field of this list.</span></span> 
    
2. <span data-ttu-id="ccb00-151">Cree un nuevo **Formulario en blanco** en InfoPath Designer, inserte un control de **Cuadro combinado** en el formulario y cambie el nombre del campo enlazado al cuadro combinado en myCombo.</span><span class="sxs-lookup"><span data-stu-id="ccb00-151">Create a new **Blank Form** in InfoPath Designer, insert a **Combo Box** control on your form, and rename the field bound to the combo box to myCombo.</span></span>
    
3. <span data-ttu-id="ccb00-152">Crear la conexión de datos a la lista que se usará para rellenar el cuadro combinado mediante el uso de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="ccb00-152">Create the data connection to the list that will be used to populate the combo box by using the following steps:</span></span>
    
    1. <span data-ttu-id="ccb00-153">En la ficha **Datos**, haga clic en el botón **Desde la lista de SharePoint** en el grupo **Obtener datos externos**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-153">On the **Data** tab, click **From SharePoint List** button in the **Get External Data** group.</span></span> 
        
    2. <span data-ttu-id="ccb00-154">Escriba la dirección URL del sitio que contiene la lista y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-154">Enter the URL for the site that contains the list, and then click **Next**.</span></span>
        
    3. <span data-ttu-id="ccb00-155">Seleccione la lista y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-155">Select the list, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="ccb00-p113">Seleccione los campos que desea incluir, para este ejemplo, seleccione Título e Id.. Título contiene los valores de búsqueda. Haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-p113">Select the fields that you want to include, for this example, select Title and ID. Title contains the values for lookup. Click **Next**.</span></span>
        
    5. <span data-ttu-id="ccb00-159">Haga clic en **Siguiente** en la pantalla a continuación.</span><span class="sxs-lookup"><span data-stu-id="ccb00-159">Click **Next** on the following screen.</span></span> 
        
    6. <span data-ttu-id="ccb00-160">Denomine la conexión de datos LookupList y haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-160">Name the data connection LookupList, and then click **Finish**.</span></span>
    
4. <span data-ttu-id="ccb00-161">Rellenar los valores en el cuadro combinado de la lista mediante el uso de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="ccb00-161">Populate the values in the combo box from the list by using the following steps:</span></span>
    
    1. <span data-ttu-id="ccb00-162">Seleccione el cuadro combinado que creó en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="ccb00-162">Select the combo box that you created in step 1.</span></span>
        
    2. <span data-ttu-id="ccb00-163">Haga clic en **Editar opciones** en la ficha **Propiedades de herramientas de control** de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="ccb00-163">Click **Edit Choices** on the **Control Tools Properties** tab of the ribbon.</span></span> 
        
    3. <span data-ttu-id="ccb00-164">Seleccione **Obtener opciones desde un origen de datos externo**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-164">Select **Get choices from an external data source**.</span></span>
        
    4. <span data-ttu-id="ccb00-165">Asegúrese de que el **Origen de datos** esté establecido en la conexión de datos que creó en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="ccb00-165">Make sure that **Data source** is set to the data connection that you created in step 2.</span></span> 
        
    5. <span data-ttu-id="ccb00-166">Establezca el valor y el nombre para mostrar en Título.</span><span class="sxs-lookup"><span data-stu-id="ccb00-166">Set the value and display name to Title.</span></span>
        
    6. <span data-ttu-id="ccb00-167">En la pestaña **Formularios de explorador**, seleccione **Siempre** en **Configuración de devolución** y haga clic en **Aceptar** para cerrar el cuadro de diálogo de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ccb00-167">On the **Browser forms** tab, select **Always** under **Postback settings**, and then click **OK** to close the properties dialog box.</span></span> 
    
5. <span data-ttu-id="ccb00-168">Asegúrese de que el cuadro combinado esté seleccionado y haga clic en **Evento cambiado** en la pestaña **Programador** de la cinta.</span><span class="sxs-lookup"><span data-stu-id="ccb00-168">Make sure the combo box is still selected, and then click **Changed Event** on the **Developer** tab of the ribbon.</span></span> 
    
    <span data-ttu-id="ccb00-p114">Si el formulario aún no se ha guardado, se le pedirá que lo haga. A continuación, se abrirá la ventana del editor de código con el cursor en el controlador de eventos  `myCombo_Changed`.</span><span class="sxs-lookup"><span data-stu-id="ccb00-p114">If your form is not saved yet, you are prompted to save it. And then, the code editor window opens with the cursor in the  `myCombo_Changed` event handler.</span></span> 
    
6. <span data-ttu-id="ccb00-171">Agregue una referencia al ensamblado Microsoft.SharePoint.dll como se describió anteriormente en este tema.</span><span class="sxs-lookup"><span data-stu-id="ccb00-171">Add a reference to the Microsoft.SharePoint.dll assembly as described earlier in this topic.</span></span> <span data-ttu-id="ccb00-172">Para obtener más información sobre cómo hacer referencia del ensamblado de Microsoft.SharePoint, vea [Miembros del modelo de objetos de SharePoint de uso](how-to-use-sharepoint-object-model-members.md).</span><span class="sxs-lookup"><span data-stu-id="ccb00-172">For more information about referencing the Microsoft.SharePoint assembly, see [Use SharePoint Object Model Members](how-to-use-sharepoint-object-model-members.md).</span></span>
    
7. <span data-ttu-id="ccb00-173">Pegue el código siguiente en el controlador de eventos  `myCombo_Changed`.</span><span class="sxs-lookup"><span data-stu-id="ccb00-173">Paste the following code into the  `myCombo_Changed` event handler.</span></span> 
    
   ```cs
    // Use InfoPath OM's ServerInfo.SharePointSiteUrl property to programmatically
    // specify the site where the form is published.
    using (SPSite FormSite = new SPSite(ServerInfo.SharePointSiteUrl.ToString()))
    {
        using (SPWeb FormWeb = FormSite.OpenWeb())
        {
            // Get the SharePoint list.
            SPList LookupList = FormWeb.Lists["MyList"];
            // Query for the item.
            SPQuery MyQuery = new SPQuery();
            // "Title" is the field (column) to search in the SharePoint list.
            // /my:myFields/my:myCombo is the xpath to the field bound to the Combo Box in the form.
            MyQuery.Query = "<Where><Eq><FieldRef Name='Title' /><Value Type='Text'>" + 
                GetDomValue("/my:myFields/my:myCombo") + "</Value></Eq></Where>";
            SPListItemCollection ReturnedItems = LookupList.GetItems(MyQuery);
            // Add the item to the SharePoint list if no items were returned in the query.
            if (ReturnedItems.Count == 0)
            {
                SPListItem NewItem = LookupList.Items.Add();
                // Set the value of the Title field in the list to the value in Combo Box on the form.
                NewItem["Title"] = GetDomValue("/my:myFields/my:myCombo");
                // Set AllowUnsafeUpdates to 'true' to temporarily allow updates to the database.
                FormWeb.AllowUnsafeUpdates = true;
                NewItem.Update();
                // Set AllowUnsafeUpdates back to 'false' to prevent further updates to the database.
                FormWeb.AllowUnsafeUpdates = false;
            }
        }
    }
   ```

   ```vb
    ' Use InfoPath OM's ServerInfo.SharePointSiteUrl property to specify the site where the form is published.
    Using FormSite As New SPSite(ServerInfo.SharePointSiteUrl.ToString())
        Using FormWeb As SPWeb = FormSite.OpenWeb()
            ' Get the SharePoint list.
            Dim LookupList As SPList = FormWeb.Lists("MyList")
            ' Query for the item.
            Dim MyQuery As New SPQuery()
            ' "Title" is the field (column) to search in the SharePoint list.
            ' my:myFields/my:myCombo is the xpath to the field bound to the Combo Box in the form.
            MyQuery.Query = "<Where><Eq><FieldRef Name='Title' /><Value Type='Text'>" &amp; _
                GetDomValue("/my:myFields/my:myCombo") &amp; "</Value></Eq></Where>"
            Dim ReturnedItems As SPListItemCollection = LookupList.GetItems(MyQuery)
            ' Add the item to the lookup list if no items were returned in the query.
            If ReturnedItems.Count = 0 Then
                Dim NewItem As SPListItem = LookupList.Items.Add()
                ' Set the value of the Title field in the list to the value in Combo Box on the form.
                NewItem("Title") = GetDomValue("/my:myFields/my:myCombo")
                ' Set AllowUnsafeUpdates to 'true' to temporarily allow updates to the database.
                FormWeb.AllowUnsafeUpdates = True
                NewItem.Update()
                ' Set AllowUnsafeUpdates back to 'false' to prevent further updates to the database.
                FormWeb.AllowUnsafeUpdates = False
            End If
        End Using
    End Using
   ```

8. <span data-ttu-id="ccb00-p116">El ejemplo de código anterior depende de la función auxiliar  `GetDomValue`. Pegue el código siguiente para la función auxiliar  `GetDomValue` debajo de la función del controlador de eventos  `myCombo_Changed`.</span><span class="sxs-lookup"><span data-stu-id="ccb00-p116">The preceding code example depends on the  `GetDomValue` helper function. Paste the following code for the  `GetDomValue` helper function below the  `myCombo_Changed` event handler function.</span></span> 
    
   ```cs
    private string GetDomValue(string XpathToGet)
    {
        return this.CreateNavigator().SelectSingleNode(XpathToGet, this.NamespaceManager).Value;
    }
   ```

   ```vb
    Private Function GetDomValue(XpathToGet As String) As String
        Return Me.CreateNavigator().SelectSingleNode(XpathToGet, Me.NamespaceManager).Value
    End Function
   ```

9. <span data-ttu-id="ccb00-176">Publicar el formulario mediante el uso de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="ccb00-176">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="ccb00-177">Haga clic en **SharePoint Server**, en la ficha **Publicar**, en Backstage.</span><span class="sxs-lookup"><span data-stu-id="ccb00-177">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="ccb00-178">Escriba la dirección URL del sitio de SharePoint en donde desea publicar el formulario y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-178">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="ccb00-179">[!IMPORTANTE] Debe ser administrador de una colección de sitios en este sitio para publicar esta plantilla de formulario como un solución de espacio aislado.</span><span class="sxs-lookup"><span data-stu-id="ccb00-179">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="ccb00-180">Seleccione **Biblioteca de formularios** y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-180">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="ccb00-181">Seleccione **Crear una nueva biblioteca de formularios** y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-181">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="ccb00-182">Escriba el nombre y las descripciones de la biblioteca de formularios y haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-182">Enter the name and description for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="ccb00-183">Haga clic en **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="ccb00-183">Click **Publish**.</span></span>
        
    7. <span data-ttu-id="ccb00-p117">Una vez publicado el formulario, abra el formulario desde la biblioteca y agregue un nuevo valor en el cuadro combinado para probar el código. Cuando salga del campo myCombo, el nuevo valor se escribirá en la lista de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ccb00-p117">After the form is successfully published, open the form from the form library and add a new value into the combo box to test the code. When you exit the myCombo field, the new value will be written to the SharePoint list.</span></span> 
    

