---
title: Ejemplos y escenarios de automatización externa
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- automatizar InfoPath 2007, formularios [InfoPath 2007], agregar datos mediante programación, automatización [InfoPath 2007], escenarios externos
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Los miembros proporcionados por el ensamblado de interoperabilidad primario de Microsoft Office InfoPath (Microsoft. Office. Interop. InfoPath. dll) y el ensamblado de interoperabilidad XML de InfoPath (Microsoft. Office. Interop. InfoPath. Xml. dll) admiten la escritura de código administrado para automatizar InfoPath.
ms.openlocfilehash: 79fbc56033ffce639b5007874dabf56e8e286edb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537818"
---
# <a name="external-automation-scenarios-and-examples"></a><span data-ttu-id="e4eac-104">Ejemplos y escenarios de automatización externa</span><span class="sxs-lookup"><span data-stu-id="e4eac-104">External automation scenarios and examples</span></span>

<span data-ttu-id="e4eac-105">Los miembros proporcionados por el ensamblado de interoperabilidad primario de Microsoft Office InfoPath (Microsoft. Office. Interop. InfoPath. dll) y el ensamblado de interoperabilidad XML de InfoPath (Microsoft. Office. Interop. InfoPath. Xml. dll) admiten la escritura de código administrado para automatizar InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e4eac-105">The members provided by the Microsoft Office InfoPath primary interop assembly (Microsoft.Office.Interop.InfoPath.dll) and the InfoPath XML interop assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) support writing managed code for automating InfoPath.</span></span> 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a><span data-ttu-id="e4eac-106">Establecimiento de referencias a los ensamblados de interoperabilidad primarios de Microsoft Office InfoPath y la interoperabilidad XML de InfoPath</span><span class="sxs-lookup"><span data-stu-id="e4eac-106">Establishing references to the Microsoft Office InfoPath Primary Interop and InfoPath XML Interop assemblies</span></span>

<span data-ttu-id="e4eac-107">Para escribir código administrado para automatizar InfoPath, debe establecer referencias a la interoperabilidad principal de Microsoft InfoPath y a los ensamblados de interoperabilidad XML de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e4eac-107">To write managed code for automating InfoPath, you must establish references to the Microsoft InfoPath primary interop and the InfoPath XML interop assemblies.</span></span> <span data-ttu-id="e4eac-108">El ensamblado de interoperabilidad primario de Microsoft InfoPath proporciona compatibilidad con la interoperabilidad con el modelo de objetos COM expuesto por IPEDITOR. DLL con los miembros del espacio de nombres [Microsoft. Office. Interop. InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e4eac-108">The Microsoft InfoPath primary interop assembly provides support for interoperability with the COM object model exposed by IPEDITOR.DLL by using the members of the [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) namespace.</span></span> <span data-ttu-id="e4eac-109">El ensamblado de interoperabilidad XML de InfoPath proporciona compatibilidad con la interoperabilidad con el modelo de objetos COM expuesto por Microsoft XML Core Services (MSXML) mediante los miembros del espacio de nombres [Microsoft. Office. Interop. InfoPath. XML](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) .</span><span class="sxs-lookup"><span data-stu-id="e4eac-109">The InfoPath XML interop assembly provides support for interoperability with the COM object model exposed by Microsoft XML Core Services (MSXML) by using the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) namespace.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e4eac-110">Los usuarios de aplicaciones de código administrado que automatizan InfoPath deben tener InfoPath, el ensamblado de interoperabilidad primario de Microsoft Office InfoPath y el ensamblado de interoperabilidad XML de InfoPath instalado en sus equipos.</span><span class="sxs-lookup"><span data-stu-id="e4eac-110">Users of managed-code applications that automate InfoPath must have InfoPath, the Microsoft Office InfoPath primary interop assembly, and the InfoPath XML interop assembly installed on their computers.</span></span> <span data-ttu-id="e4eac-111">La opción **compatibilidad con programación de .net** en el programa de instalación de InfoPath se establece en **Ejecutar desde mi PC** para una instalación típica de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e4eac-111">The **.NET Programmability Support** option in the InfoPath setup program is set to **Run from My Computer** for a typical installation of InfoPath.</span></span>
>  
> <span data-ttu-id="e4eac-112">Como resultado, siempre que esté instalado el paquete redistribuible de .NET Framework 1,1 o el kit de desarrollo de software (SDK) de .NET Framework 1,1 o posterior, estos ensamblados de interoperabilidad también se instalarán de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e4eac-112">As a result, as long as the .NET Framework 1.1 Redistributable or .NET Framework 1.1 Software Development Kit (SDK) or later is installed, these interop assemblies will also be installed by default.</span></span> <span data-ttu-id="e4eac-113">Si estos ensamblados de interoperabilidad no están disponibles en el equipo de un usuario, debe confirmar que .NET Framework 1,1 o posterior está instalado y, a continuación, ejecutar **programas y características** desde el **Panel de control** para cambiar la configuración y establecer la capacidad de **programación de .net Admite** la opción de InfoPath para **Ejecutar desde mi PC**.</span><span class="sxs-lookup"><span data-stu-id="e4eac-113">If these interop assemblies are not available on a user's computer, you must confirm that the .NET Framework 1.1 or later is installed, and then run **Programs and Features** from the **Control Panel** to change setup and set the **.NET Programmability Support** option of InfoPath to **Run from My Computer**.</span></span> 
  
<span data-ttu-id="e4eac-114">Los procedimientos siguientes describen cómo establecer referencias a la interoperabilidad principal de Microsoft Office InfoPath y los ensamblados de interoperabilidad XML de InfoPath en un proyecto de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e4eac-114">The following procedures describe how to set references to the Microsoft Office InfoPath primary interop and the InfoPath XML interop assemblies in a Visual Studio project.</span></span>
  
<span data-ttu-id="e4eac-115">Para establecer una referencia al ensamblado de interoperabilidad primario Microsoft. Office. Interop. InfoPath, establezca una referencia a la **biblioteca de tipos de Microsoft InfoPath 3,0** en la ficha **com** del cuadro de diálogo **Agregar referencia** .</span><span class="sxs-lookup"><span data-stu-id="e4eac-115">To set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly, set a reference to **Microsoft InfoPath 3.0 Type Library** on the **COM** tab of the **Add Reference** dialog box.</span></span> <span data-ttu-id="e4eac-116">Aunque se establezca una referencia desde la ficha **com** , se establece una referencia al ensamblado de interoperabilidad primario Microsoft. Office. Interop. InfoPath. dll que está instalado en la memoria caché de ensamblados global (GAC) mediante el programa de instalación de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e4eac-116">Even though you set a reference from the **COM** tab, a reference is established to the Microsoft.Office.Interop.InfoPath.dll primary interop assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span> 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a><span data-ttu-id="e4eac-117">Establecer una referencia al ensamblado de interoperabilidad primario Microsoft. Office. Interop. InfoPath</span><span class="sxs-lookup"><span data-stu-id="e4eac-117">Set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly</span></span>

1. <span data-ttu-id="e4eac-118">Abra un proyecto de código administrado de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e4eac-118">Open a Visual Studio managed code project.</span></span>
    
2. <span data-ttu-id="e4eac-119">En el **Explorador de soluciones**, haga clic con el botón secundario en **Referencias** y, a continuación, haga clic en **Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="e4eac-119">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="e4eac-120">En la pestaña **com** , haga doble clic en **biblioteca de tipos de Microsoft InfoPath 3,0**y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e4eac-120">On the **COM** tab, double-click **Microsoft InfoPath 3.0 Type Library**, and then click **OK**.</span></span>
    
<span data-ttu-id="e4eac-121">Para establecer una referencia al ensamblado de interoperabilidad Microsoft. Office. Interop. InfoPath. XML, vaya al archivo Microsoft. Office. Interop. InfoPath. Xml. dll que se instala de forma predeterminada en la _unidad_< >: \Archivos de programa\Microsoft Office\OFFICE14 .</span><span class="sxs-lookup"><span data-stu-id="e4eac-121">To set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly, browse to the Microsoft.Office.Interop.InfoPath.Xml.dll file that is installed by default in the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder.</span></span> <span data-ttu-id="e4eac-122">Aunque especifique la copia del ensamblado en el sistema de archivos local, este procedimiento establece una referencia al ensamblado Microsoft. Office. Interop. InfoPath. Xml. dll que está instalado en la memoria caché global de ensamblados (GAC) mediante el programa de instalación de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e4eac-122">Even though you specify the copy of the assembly in the local file system, this procedure establishes a reference to the Microsoft.Office.Interop.InfoPath.Xml.dll assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span>
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a><span data-ttu-id="e4eac-123">Establecer una referencia al ensamblado de interoperabilidad Microsoft. Office. Interop. InfoPath. XML</span><span class="sxs-lookup"><span data-stu-id="e4eac-123">Set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly</span></span>

1. <span data-ttu-id="e4eac-124">Abra o cree un proyecto de código administrado de Visual Studio, como una **aplicación de consola** o una aplicación de **Windows**.</span><span class="sxs-lookup"><span data-stu-id="e4eac-124">Open or create a Visual Studio managed code project, such as a **Console Application** or **Windows Application**.</span></span>
    
2. <span data-ttu-id="e4eac-125">En el **Explorador de soluciones**, haga clic con el botón secundario en **Referencias** y, a continuación, haga clic en **Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="e4eac-125">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="e4eac-126">En la ficha **.net** , haga clic en **examinar**, vaya a __ la carpeta < >: \Archivos de programa\Microsoft Office\OFFICE14 y, a continuación, haga clic en Microsoft. Office. Interop. InfoPath. Xml. dll.</span><span class="sxs-lookup"><span data-stu-id="e4eac-126">On the **.NET** tab, click **Browse**, navigate to the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder, and then click Microsoft.Office.Interop.InfoPath.Xml.dll.</span></span>
    
4. <span data-ttu-id="e4eac-127">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e4eac-127">Click **OK**.</span></span>
    
## <a name="automate-changing-the-value-of-a-field"></a><span data-ttu-id="e4eac-128">Automatizar el cambio de valor de un campo</span><span class="sxs-lookup"><span data-stu-id="e4eac-128">Automate changing the value of a field</span></span>

<span data-ttu-id="e4eac-129">Supongamos que uno de los clientes del usuario de una plantilla de formulario de informe de ventas de InfoPath cambió recientemente su nombre de "compañía A" a "compañía B".</span><span class="sxs-lookup"><span data-stu-id="e4eac-129">Suppose one of the customers of the user of an InfoPath sales report form template recently changed its name from "Company A" to "Company B."</span></span> <span data-ttu-id="e4eac-130">Se pide a los desarrolladores que escriban código que actualice automáticamente los formularios de informes de ventas guardados desde esta plantilla de formulario para reflejar el cambio de nombre.</span><span class="sxs-lookup"><span data-stu-id="e4eac-130">A developer is asked to write code that will automatically update the sales report forms saved from this form template to reflect the name change.</span></span> <span data-ttu-id="e4eac-131">El siguiente escenario asume un formulario que contiene un cuadro de texto enlazado a un campo denominado Nombre_cliente.</span><span class="sxs-lookup"><span data-stu-id="e4eac-131">The following scenario assumes a form that contains a text box that is bound to a field named customerName.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="e4eac-132">Crear el formulario y la plantilla de formulario de ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4eac-132">Create the sample form template and form</span></span>

1. <span data-ttu-id="e4eac-133">Abra InfoPath y cree una plantilla de formulario en blanco.</span><span class="sxs-lookup"><span data-stu-id="e4eac-133">Open InfoPath and create a blank form template.</span></span>
    
2. <span data-ttu-id="e4eac-134">Agregue un control de **cuadro de texto** al formulario y asigne un nombre al campo enlazado al control customerName.</span><span class="sxs-lookup"><span data-stu-id="e4eac-134">Add a **Text Box** control to the form, and name the field bound to the control customerName.</span></span>
    
3. <span data-ttu-id="e4eac-135">En el panel de tareas **campos** , haga clic con el botón secundario en la carpeta Mis **campos** y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="e4eac-135">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="e4eac-136">En la pestaña **detalles** , seleccione y copie el valor que sigue al **espacio de nombres:** y, a continuación, péguelo en el Bloc de notas o en otra ubicación en la que pueda recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="e4eac-136">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="e4eac-137">Este valor será necesario más adelante para establecer el valor de la propiedad **SelectionNamespaces** en el código.</span><span class="sxs-lookup"><span data-stu-id="e4eac-137">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="e4eac-138">Publique la plantilla de formulario en una carpeta denominada C:\Test y acepte el nombre predeterminado, Template1.</span><span class="sxs-lookup"><span data-stu-id="e4eac-138">Publish the form template to a folder named C:\Test and accept the default name, Template1.</span></span> 
    
6. <span data-ttu-id="e4eac-139">Abra la plantilla de formulario, agregue el nombre "compañía A" al cuadro de texto enlazado al campo Nombre_cliente y, a continuación, guarde el formulario como "Form1".</span><span class="sxs-lookup"><span data-stu-id="e4eac-139">Open the form template, add the name "Company A" to text box bound to the customerName field, and then save the form as "Form1".</span></span> 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a><span data-ttu-id="e4eac-140">Crear una aplicación de consola de código administrado para cambiar el nombre de ' Company A ' a ' Company B '</span><span class="sxs-lookup"><span data-stu-id="e4eac-140">Create a managed code console application to change the name from 'Company A' to 'Company B'</span></span>

1. <span data-ttu-id="e4eac-141">Abra Visual Studio y cree una nueva aplicación de consola de Visual C# o Visual Basic denominada UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="e4eac-141">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named UpdateCustomer.</span></span>
    
2. <span data-ttu-id="e4eac-142">Establezca referencias a los ensamblados de interoperabilidad primario de Microsoft Office InfoPath y de la interoperabilidad XML de InfoPath como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e4eac-142">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="e4eac-143">Agregue el siguiente código al archivo Program.cs o Module1. VB, asegurándose de actualizar el valor del espacio de nombres en el valor de la propiedad **SelectionNamespaces** con el valor que ha copiado al crear el formulario de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e4eac-143">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Text;
    using Microsoft.Office.Interop.InfoPath;
    using Microsoft.Office.Interop.InfoPath.Xml;
    namespace UpdateCustomer
    {
      class Program
      {
          static void Main(string[] args)
          {
            // Create an InfoPath Application object.
            Application myApp = 
                new Microsoft.Office.Interop.InfoPath.Application();
            // Get a reference the XDocuments collection 
            // and open the sample form.
            XDocumentsCollection myXDocs = myApp.XDocuments;
            XDocument myXDoc = myXDocs.Open("C:\\Test\\Form1.xml",
                (int) XdDocumentVersionMode.xdFailOnVersionOlder);
            
            // Access the XML DOM for the underlying XML document using
            // the DOM property. Note that you must cast to the 
            // IXMLDOMDocument2 type from the
            // Microsoft.Office.Interop.InfoPath.Xml namespace
            // to access the XML DOM.
            IXMLDOMDocument2 myXMLDoc = myXDoc.DOM as IXMLDOMDocument2;
            // Set the MSXML SelectionNamespaces property to the my
            // namespace of the form. IMPORTANT:Replace the namespace 
            // value below with that of your sample form.
            myXMLDoc.setProperty("SelectionNamespaces",
    "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
            // Select all instances of customerName that contain 
            //'Company A'.
            IXMLDOMNodeList myNames = 
                myXMLDoc.selectNodes(
                "//my:customerName[. = 'Company A']");
            // Check to determine if any nodes were returned.
            if (myNames.length < 1)
            Console.WriteLine(
                "No elements containing 'Company A' were found.");
            // Loop through the list updating to 'Company B'.
            IXMLDOMNode myName = myNames.nextNode();
            while (myName != null)
            {
                myName.text = "Company B";
                myName = myNames.nextNode();
            }
            // Save the updated form as Form2.xml and close out.
            myXDoc.SaveAs("C:\\Test\\Form2.xml");
            myXDocs.Close(0);
            myApp.Quit(false);
            Console.WriteLine("Finished!");
          }
      }
    }
   ```

   ```vb
    Imports Microsoft.Office.Interop.InfoPath
    Imports Microsoft.Office.Interop.InfoPath.Xml
    Module Module1
      Sub Main()
          ' Create an InfoPath Application object.
          Dim myApp As Application = _
            New Microsoft.Office.Interop.InfoPath.Application()
          ' Get a reference the XDocuments collection 
          ' and open the sample form.
          Dim myXDocs As XDocumentsCollection = myApp.XDocuments
          Dim myXDoc As XDocument = myXDocs.Open( _
            "C:\\Test\\Form1.xml", _
            XdDocumentVersionMode.xdFailOnVersionOlder)
          ' Access the XML DOM for the underlying XML document using
          ' the DOM property. Note that you must cast to the 
          ' IXMLDOMDocument2 type from the
          ' Microsoft.Office.Interop.InfoPath.Xml namespace
          ' to access the XML DOM.
          Dim myXMLDoc As IXMLDOMDocument2 = _
            DirectCast(myXDoc.DOM, IXMLDOMDocument2)
          ' Set the MSXML SelectionNamespaces property to the my
          ' namespace of the form. IMPORTANT:Replace the namespace 
          ' value below with that of your sample form.
          myXMLDoc.setProperty("SelectionNamespaces", _
    "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Select all instances of customerName that contain 
          ''Company A'.
          Dim myNames As IXMLDOMNodeList = _
      myXMLDoc.selectNodes("//my:customerName[. = 'Company A']")
          ' Check to determine if any nodes were returned.
          If (myNames.length < 1) Then
            Console.WriteLine( _
                "No elements containing 'Company A' were found.")
          Else
            ' Loop through the list updating to 'Company B'.
            Dim myName As IXMLDOMNode = myNames.nextNode()
            While (myName IsNot Nothing)
                myName.text = "Company B"
                myName = myNames.nextNode()
            End While
          End If
          ' Save the updated form as Form2.xml and close out.
          myXDoc.SaveAs("C:\\Test\\Form2.xml")
          myXDocs.Close(0)
          myApp.Quit(False)
          Console.WriteLine("Finished!")
      End Sub
    End Module
    
   ```

4. <span data-ttu-id="e4eac-144">Haga clic en **iniciar** depuración en el menú Depurar para compilar y ejecutar la aplicación de consola. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e4eac-144">Click **Start Debugging** on the **Debug** menu to compile and run the console application.</span></span> 
    
   <span data-ttu-id="e4eac-145">La aplicación abre el formulario guardado como Form1. XML y recorre todos los elementos Nombre_cliente que contienen el valor Company a y cambia ese valor a Company B. Una vez completada la operación, se guarda una nueva copia del formulario como Form2. XML en la carpeta C:\Test.</span><span class="sxs-lookup"><span data-stu-id="e4eac-145">The application opens the form saved as Form1.xml and loops through all customerName elements that contain the value Company A and changes that value to Company B. When the operation is complete, a new copy of the form is saved as Form2.xml in the C:\Test folder.</span></span> 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a><span data-ttu-id="e4eac-146">Automatizar la apertura de un formulario y el relleno de los valores de los campos</span><span class="sxs-lookup"><span data-stu-id="e4eac-146">Automate opening a form and populating field values</span></span>

<span data-ttu-id="e4eac-147">En el siguiente ejemplo se automatiza la apertura de un formulario en blanco y se rellenan los campos nombre, apellidos y dirección del formulario.</span><span class="sxs-lookup"><span data-stu-id="e4eac-147">The following example automates opening a blank form and populating the first name, last name, and address fields in the form.</span></span> <span data-ttu-id="e4eac-148">Este escenario presupone un formulario que contiene tres cuadros de texto enlazados a campos denominados FirstName, LastName y Address.</span><span class="sxs-lookup"><span data-stu-id="e4eac-148">This scenario assumes a form that contains three text boxes that are bound to fields named FirstName, LastName, and Address.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="e4eac-149">Crear el formulario y la plantilla de formulario de ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4eac-149">Create the sample form template and form</span></span>

1. <span data-ttu-id="e4eac-150">Abra InfoPath y cree un formulario en blanco.</span><span class="sxs-lookup"><span data-stu-id="e4eac-150">Open InfoPath and create a blank form.</span></span>
    
2. <span data-ttu-id="e4eac-151">Agregue tres controles de cuadro de texto al formulario y asigne a los campos un nombre enlazado a los controles: FirstName, LastName y Address.</span><span class="sxs-lookup"><span data-stu-id="e4eac-151">Add three text box controls to the form, and name the fields bound to the controls: FirstName, LastName, and Address.</span></span> <span data-ttu-id="e4eac-152">Agregue los demás campos que desee.</span><span class="sxs-lookup"><span data-stu-id="e4eac-152">Add any other fields you want.</span></span>
    
3. <span data-ttu-id="e4eac-153">En el panel de tareas **campos** , haga clic con el botón secundario en la carpeta Mis **campos** y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="e4eac-153">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="e4eac-154">En la pestaña **detalles** , seleccione y copie el valor que sigue al **espacio de nombres:** y, a continuación, péguelo en el Bloc de notas o en otra ubicación en la que pueda recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="e4eac-154">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="e4eac-155">Este valor será necesario más adelante para establecer el valor de la propiedad **SelectionNamespaces** en el código.</span><span class="sxs-lookup"><span data-stu-id="e4eac-155">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="e4eac-156">Publique la plantilla de formulario en una carpeta llamada C:\Temp y acepte el nombre predeterminado, Template1.</span><span class="sxs-lookup"><span data-stu-id="e4eac-156">Publish the form template to a folder named C:\Temp and accept the default name, Template1.</span></span>
    
6. <span data-ttu-id="e4eac-157">Abra la plantilla de formulario y guarde un formulario en blanco como "Form1" en C:\Temp.</span><span class="sxs-lookup"><span data-stu-id="e4eac-157">Open the form template and save a blank form as "Form1" to C:\Temp.</span></span>
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a><span data-ttu-id="e4eac-158">Crear una aplicación de consola de código administrado para abrir el formulario y rellenar los campos</span><span class="sxs-lookup"><span data-stu-id="e4eac-158">Create a managed code console application to open the form and populate the fields</span></span>

1. <span data-ttu-id="e4eac-159">Abra Visual Studio y cree una nueva aplicación de consola de Visual C# o Visual Basic llamada AbrirFormulario.</span><span class="sxs-lookup"><span data-stu-id="e4eac-159">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named OpenForm.</span></span>
    
2. <span data-ttu-id="e4eac-160">Establezca referencias a los ensamblados de interoperabilidad primario de Microsoft Office InfoPath y de la interoperabilidad XML de InfoPath como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e4eac-160">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="e4eac-161">Agregue el siguiente código al archivo Program.cs o Module1. VB, asegurándose de actualizar el valor del espacio de nombres en el valor de la propiedad **SelectionNamespaces** con el valor que ha copiado al crear el formulario de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e4eac-161">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Text;
    using Microsoft.Office.Interop.InfoPath;
    using Microsoft.Office.Interop.InfoPath.Xml;
    namespace OpenForm
    {
      class Program
      {
          static void Main(string[] args)
          {
            // Create an InfoPath Application object.
            Application myApp=
                new Microsoft.Office.Interop.InfoPath.Application();
            // Create an InfoPath XDocument variable and open 
            // the blank form.
            XDocument myXDoc = myApp.XDocuments.Open(
                "c:\\temp\\Form1.xml",
                (int) XdDocumentVersionMode.xdFailOnVersionOlder);
            
            // Create an IXMLDOMDocument2 variable and access 
            // the XML DOM from the underlying XML document
            // using the DOM property of the XDocument object. 
            // Note that you must cast to IXMLDOMDocument2 to do so.
            IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
            // Set the MSXML SelectionNamespaces property to the my
            // namespace of the form. IMPORTANT:Replace the namespace
            // value below with that of your sample form.
            doc.setProperty("SelectionNamespaces","xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
            // Pre-populate the fields with specified values.
            doc.selectSingleNode("//my:FirstName").text="My Name";
            doc.selectSingleNode("//my:LastName").text="My LastName";
            doc.selectSingleNode("//my:Address").text="My Address";
            // Save the form, leaving InfoPath open.
            myXDoc.Save();
            
          }
      }
    }
   ```

   ```vb
    Imports Microsoft.Office.Interop.InfoPath
    Imports Microsoft.Office.Interop.InfoPath.Xml
    Module Module1
      Sub Main()
          ' Create an InfoPath Application object.
          Dim myApp As Application = _
            New Microsoft.Office.Interop.InfoPath.Application
          ' Create an InfoPath XDocument variable and open 
          ' the blank form.
          Dim myXDoc As XDocument = myApp.XDocuments.Open( _
            "c:\\temp\\Form1.xml", _
            XdDocumentVersionMode.xdFailOnVersionOlder)
          ' Create an IXMLDOMDocument2 variable and access 
          ' the XML DOM from the underlying XML document
          ' using the DOM property of the XDocument object.
          Dim doc As IXMLDOMDocument2 = myXDoc.DOM
          ' Set the MSXML SelectionNamespaces property to the my
          ' namespace of the form. IMPORTANT:Replace the namespace
          ' value below with that of your sample form.
          doc.setProperty("SelectionNamespaces", "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Pre-populate the fields with specified values.
          doc.selectSingleNode("//my:FirstName").text = "My Name"
          doc.selectSingleNode("//my:LastName").text = "My LastName"
          doc.selectSingleNode("//my:Address").text = "My Address"
          ' Save the form, leaving InfoPath open.
          myXDoc.Save()
      End Sub
    End Module
    
   ```

4. <span data-ttu-id="e4eac-162">En el \*\*\*\* menú Depurar, haga clic en **iniciar** depuración para compilar y ejecutar la aplicación de consola.</span><span class="sxs-lookup"><span data-stu-id="e4eac-162">On the **Debug** menu, click **Start Debugging** to compile and run the console application.</span></span> 
    
   <span data-ttu-id="e4eac-163">La aplicación abrirá el formulario guardado como Form1. XML y rellenará los campos FirstName, LastName y address con los valores especificados en el código y, a continuación, guarda el formulario, dejando abierto InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e4eac-163">The application will open the form saved as Form1.xml and fill in the FirstName, LastName, and Address fields with the values specified in the code, and then save the form, leaving InfoPath open.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e4eac-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4eac-164">See also</span></span>

- [<span data-ttu-id="e4eac-165">Información sobre el conjunto de interoperabilidad principal de InfoPath de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="e4eac-165">About the Microsoft Office InfoPath Primary Interop Assembly</span></span>](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [<span data-ttu-id="e4eac-166">Información sobre el conjunto de interoperabilidad XML de InfoPath</span><span class="sxs-lookup"><span data-stu-id="e4eac-166">About the InfoPath XML Interop Assembly</span></span>](about-the-infopath-xml-interop-assembly.md)

