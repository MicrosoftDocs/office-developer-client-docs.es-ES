---
title: Ejemplos y escenarios de automatización externa
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- automatización de infopath 2007, formularios [InfoPath 2007], agregar datos mediante programación, automatización [InfoPath 2007], escenarios externos
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Los miembros proporcionan por Microsoft Office InfoPath principal ensamblado de interoperabilidad (Microsoft.Office.Interop.InfoPath.dll) y el ensamblado de interoperabilidad XML de InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) admiten escribir código administrado para automatizar InfoPath.
ms.openlocfilehash: 1c76e5cb659c9d3f39eec4a7e517ab57c98c858a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815761"
---
# <a name="external-automation-scenarios-and-examples"></a><span data-ttu-id="6651d-104">Ejemplos y escenarios de automatización externa</span><span class="sxs-lookup"><span data-stu-id="6651d-104">External automation scenarios and examples</span></span>

<span data-ttu-id="6651d-105">Los miembros proporcionan por Microsoft Office InfoPath principal ensamblado de interoperabilidad (Microsoft.Office.Interop.InfoPath.dll) y el ensamblado de interoperabilidad XML de InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) admiten escribir código administrado para automatizar InfoPath.</span><span class="sxs-lookup"><span data-stu-id="6651d-105">The members provided by the Microsoft Office InfoPath primary interop assembly (Microsoft.Office.Interop.InfoPath.dll) and the InfoPath XML interop assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) support writing managed code for automating InfoPath.</span></span> 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a><span data-ttu-id="6651d-106">Establecimiento de referencias a los ensamblados de interoperabilidad primaria de Microsoft Office InfoPath y la interoperabilidad de XML de InfoPath</span><span class="sxs-lookup"><span data-stu-id="6651d-106">Establishing references to the Microsoft Office InfoPath Primary Interop and InfoPath XML Interop assemblies</span></span>

<span data-ttu-id="6651d-107">Para escribir código administrado para automatizar InfoPath, debe establecer referencias a los ensamblados de interoperabilidad XML de InfoPath y a la interoperabilidad primaria de Microsoft InfoPath.</span><span class="sxs-lookup"><span data-stu-id="6651d-107">To write managed code for automating InfoPath, you must establish references to the Microsoft InfoPath primary interop and the InfoPath XML interop assemblies.</span></span> <span data-ttu-id="6651d-108">El ensamblado de interoperabilidad primario de Microsoft InfoPath ofrece compatibilidad para la interoperabilidad con el modelo de objetos COM expuesto por IPEDITOR. DLL mediante el uso de los miembros del espacio de nombres [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6651d-108">The Microsoft InfoPath primary interop assembly provides support for interoperability with the COM object model exposed by IPEDITOR.DLL by using the members of the [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) namespace.</span></span> <span data-ttu-id="6651d-109">El ensamblado de interoperabilidad XML de InfoPath proporciona compatibilidad para la interoperabilidad con el modelo de objetos COM expuesto por Microsoft XML Core Services (MSXML) mediante el uso de los miembros del espacio de nombres [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) .</span><span class="sxs-lookup"><span data-stu-id="6651d-109">The InfoPath XML interop assembly provides support for interoperability with the COM object model exposed by Microsoft XML Core Services (MSXML) by using the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) namespace.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="6651d-110">Los usuarios de aplicaciones de código administrado que automaticen InfoPath deben tener InfoPath, el ensamblado de interoperabilidad primario de Microsoft Office InfoPath y el ensamblado de interoperabilidad XML de InfoPath instalado en sus equipos.</span><span class="sxs-lookup"><span data-stu-id="6651d-110">Users of managed-code applications that automate InfoPath must have InfoPath, the Microsoft Office InfoPath primary interop assembly, and the InfoPath XML interop assembly installed on their computers.</span></span> <span data-ttu-id="6651d-111">La opción de **Compatibilidad con programación de .NET** en el programa de instalación de InfoPath se establece en **Ejecutar desde Mi PC** para una instalación típica de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="6651d-111">The **.NET Programmability Support** option in the InfoPath setup program is set to **Run from My Computer** for a typical installation of InfoPath.</span></span>
>  
> <span data-ttu-id="6651d-112">Como resultado, tal y como se instala siempre y cuando el paquete redistribuible de .NET Framework 1.1 o el Kit de desarrollo de Software (SDK) de .NET Framework 1.1 o posterior, estos ensamblados de interoperabilidad también se instalará de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6651d-112">As a result, as long as the .NET Framework 1.1 Redistributable or .NET Framework 1.1 Software Development Kit (SDK) or later is installed, these interop assemblies will also be installed by default.</span></span> <span data-ttu-id="6651d-113">Si estos ensamblados de interoperabilidad no están disponibles en el equipo del usuario, debe confirmar que está instalada .NET Framework 1.1 o posterior y, a continuación, ejecutar **programas y características** en el **Panel de Control** para cambiar el programa de instalación y establecer la programación de .NET ** Compatibilidad con** opción de InfoPath para **Ejecutar desde Mi PC**.</span><span class="sxs-lookup"><span data-stu-id="6651d-113">If these interop assemblies are not available on a user's computer, you must confirm that the .NET Framework 1.1 or later is installed, and then run **Programs and Features** from the **Control Panel** to change setup and set the **.NET Programmability Support** option of InfoPath to **Run from My Computer**.</span></span> 
  
<span data-ttu-id="6651d-114">Los procedimientos siguientes describen cómo establecer los ensamblados de interoperabilidad de referencias a la interoperabilidad primaria de Microsoft Office InfoPath y el XML de InfoPath en un proyecto de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6651d-114">The following procedures describe how to set references to the Microsoft Office InfoPath primary interop and the InfoPath XML interop assemblies in a Visual Studio project.</span></span>
  
<span data-ttu-id="6651d-115">Para establecer una referencia al ensamblado de interoperabilidad primario de Microsoft.Office.Interop.InfoPath, establezca una referencia a la **Biblioteca de tipos de Microsoft InfoPath 3.0** en la ficha **COM** del cuadro de diálogo **Agregar referencia** .</span><span class="sxs-lookup"><span data-stu-id="6651d-115">To set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly, set a reference to **Microsoft InfoPath 3.0 Type Library** on the **COM** tab of the **Add Reference** dialog box.</span></span> <span data-ttu-id="6651d-116">Aunque se establece una referencia desde la ficha **COM** , se establece una referencia para el ensamblado de interoperabilidad primario de Microsoft.Office.Interop.InfoPath.dll que se instala en la caché de ensamblados Global (GAC) mediante el programa de instalación de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="6651d-116">Even though you set a reference from the **COM** tab, a reference is established to the Microsoft.Office.Interop.InfoPath.dll primary interop assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span> 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a><span data-ttu-id="6651d-117">Establecer una referencia al ensamblado de interoperabilidad primario de Microsoft.Office.Interop.InfoPath</span><span class="sxs-lookup"><span data-stu-id="6651d-117">Set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly</span></span>

1. <span data-ttu-id="6651d-118">Abra un proyecto de código administrado de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6651d-118">Open a Visual Studio managed code project.</span></span>
    
2. <span data-ttu-id="6651d-119">En el **Explorador de soluciones**, haga clic en **referencias**y, a continuación, haga clic en **Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="6651d-119">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="6651d-120">En la ficha **COM** , haga doble clic en la **Biblioteca de tipos de Microsoft InfoPath 3.0**y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="6651d-120">On the **COM** tab, double-click **Microsoft InfoPath 3.0 Type Library**, and then click **OK**.</span></span>
    
<span data-ttu-id="6651d-121">Para establecer una referencia al ensamblado de interoperabilidad Microsoft.Office.Interop.InfoPath.Xml, busque el archivo Microsoft.Office.Interop.InfoPath.Xml.dll que se instala de forma predeterminada en el < _unidad_>: \Program Office\OFFICE14 carpeta .</span><span class="sxs-lookup"><span data-stu-id="6651d-121">To set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly, browse to the Microsoft.Office.Interop.InfoPath.Xml.dll file that is installed by default in the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder.</span></span> <span data-ttu-id="6651d-122">Aunque especifique la copia del ensamblado en el sistema de archivos local, este procedimiento establece una referencia al ensamblado Microsoft.Office.Interop.InfoPath.Xml.dll que se instala en la caché de ensamblados Global (GAC) mediante el programa de instalación de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="6651d-122">Even though you specify the copy of the assembly in the local file system, this procedure establishes a reference to the Microsoft.Office.Interop.InfoPath.Xml.dll assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span>
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a><span data-ttu-id="6651d-123">Establecer una referencia al ensamblado de interoperabilidad Microsoft.Office.Interop.InfoPath.Xml</span><span class="sxs-lookup"><span data-stu-id="6651d-123">Set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly</span></span>

1. <span data-ttu-id="6651d-124">Abra o cree un proyecto de código administrado de Visual Studio, como una **Aplicación de consola** o una **Aplicación de Windows**.</span><span class="sxs-lookup"><span data-stu-id="6651d-124">Open or create a Visual Studio managed code project, such as a **Console Application** or **Windows Application**.</span></span>
    
2. <span data-ttu-id="6651d-125">En el **Explorador de soluciones**, haga clic en **referencias**y, a continuación, haga clic en **Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="6651d-125">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="6651d-126">En la ficha. **NET** , haga clic en **Examinar**, desplácese hasta la < _unidad_>: \Program Office\OFFICE14 carpeta y, a continuación, haga clic en Microsoft.Office.Interop.InfoPath.Xml.dll.</span><span class="sxs-lookup"><span data-stu-id="6651d-126">On the **.NET** tab, click **Browse**, navigate to the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder, and then click Microsoft.Office.Interop.InfoPath.Xml.dll.</span></span>
    
4. <span data-ttu-id="6651d-127">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="6651d-127">Click **OK**.</span></span>
    
## <a name="automate-changing-the-value-of-a-field"></a><span data-ttu-id="6651d-128">Automatizar al cambiar el valor de un campo</span><span class="sxs-lookup"><span data-stu-id="6651d-128">Automate changing the value of a field</span></span>

<span data-ttu-id="6651d-129">Suponga que uno de los clientes del usuario de una plantilla de formulario de informe de ventas de InfoPath que han cambiado recientemente su nombre de la empresa"A" a "Empresa B."</span><span class="sxs-lookup"><span data-stu-id="6651d-129">Suppose one of the customers of the user of an InfoPath sales report form template recently changed its name from "Company A" to "Company B."</span></span> <span data-ttu-id="6651d-130">Un desarrollador se le pida que escribir código que se actualice automáticamente los formularios de informe de ventas guardados desde esta plantilla de formulario para reflejar el cambio de nombre.</span><span class="sxs-lookup"><span data-stu-id="6651d-130">A developer is asked to write code that will automatically update the sales report forms saved from this form template to reflect the name change.</span></span> <span data-ttu-id="6651d-131">El siguiente escenario se da por supuesto un formulario que contenga un cuadro de texto que está enlazado a un campo denominado customerName.</span><span class="sxs-lookup"><span data-stu-id="6651d-131">The following scenario assumes a form that contains a text box that is bound to a field named customerName.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="6651d-132">Crear la plantilla de formulario de ejemplo y el formulario</span><span class="sxs-lookup"><span data-stu-id="6651d-132">Create the sample form template and form</span></span>

1. <span data-ttu-id="6651d-133">Abra InfoPath y cree una plantilla de formulario en blanco.</span><span class="sxs-lookup"><span data-stu-id="6651d-133">Open InfoPath and create a blank form template.</span></span>
    
2. <span data-ttu-id="6651d-134">Agregar un control de **Cuadro de texto** al formulario y el nombre del campo enlazado en el control customerName.</span><span class="sxs-lookup"><span data-stu-id="6651d-134">Add a **Text Box** control to the form, and name the field bound to the control customerName.</span></span>
    
3. <span data-ttu-id="6651d-135">En el panel de tareas **campos** , haga clic en la carpeta **misCampos** y, a continuación, haga clic en **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="6651d-135">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="6651d-136">En la pestaña **Detalles** , seleccione y copie el siguiente valor **Namespace:** y, a continuación, pegue esto en el Bloc de notas o alguna otra ubicación donde se pueden recuperar.</span><span class="sxs-lookup"><span data-stu-id="6651d-136">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="6651d-137">Necesitará este valor más adelante para establecer el valor de la propiedad **SelectionNamespaces** en el código.</span><span class="sxs-lookup"><span data-stu-id="6651d-137">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="6651d-138">Publicar la plantilla de formulario en una carpeta denominada C:\Test y acepte el nombre predeterminado, Plantilla1.</span><span class="sxs-lookup"><span data-stu-id="6651d-138">Publish the form template to a folder named C:\Test and accept the default name, Template1.</span></span> 
    
6. <span data-ttu-id="6651d-139">Abra la plantilla de formulario, agregue el nombre de "Empresa A" al cuadro de texto dependiente del campo NombreDeCliente y, a continuación, guarde el formulario como "Form1".</span><span class="sxs-lookup"><span data-stu-id="6651d-139">Open the form template, add the name "Company A" to text box bound to the customerName field, and then save the form as "Form1".</span></span> 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a><span data-ttu-id="6651d-140">Crear una aplicación de consola de código administrado para cambiar el nombre de la empresa' A' a 'Compañía B'</span><span class="sxs-lookup"><span data-stu-id="6651d-140">Create a managed code console application to change the name from 'Company A' to 'Company B'</span></span>

1. <span data-ttu-id="6651d-141">Abra Visual Studio y cree un nuevo Visual C# o Visual Basic aplicación de consola denominada UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="6651d-141">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named UpdateCustomer.</span></span>
    
2. <span data-ttu-id="6651d-142">Establecer referencias a los ensamblados de interoperabilidad de XML de InfoPath e interoperabilidad primaria de Microsoft Office InfoPath tal y como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6651d-142">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="6651d-143">Agregue el código siguiente en el archivo Program.cs o Module1.vb, asegurándose de que se actualice el valor del espacio de nombres en la configuración de la propiedad **SelectionNamespaces** con el valor que se copió al crear el formulario de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6651d-143">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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

4. <span data-ttu-id="6651d-144">En el menú **Depurar** para compilar y ejecutar la aplicación de consola, haga clic en **Iniciar depuración** .</span><span class="sxs-lookup"><span data-stu-id="6651d-144">Click **Start Debugging** on the **Debug** menu to compile and run the console application.</span></span> 
    
   <span data-ttu-id="6651d-145">La aplicación abre el formulario guardado como Form1.xml y recorre en bucle todos los elementos customerName que contienen el valor de la empresa A y cambia ese valor a la empresa B. Una vez finalizada la operación, se guarda una copia nueva del formulario como Form2.xml en la carpeta C:\Test.</span><span class="sxs-lookup"><span data-stu-id="6651d-145">The application opens the form saved as Form1.xml and loops through all customerName elements that contain the value Company A and changes that value to Company B. When the operation is complete, a new copy of the form is saved as Form2.xml in the C:\Test folder.</span></span> 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a><span data-ttu-id="6651d-146">Automatizar la apertura de un formulario y rellenar los valores de campo</span><span class="sxs-lookup"><span data-stu-id="6651d-146">Automate opening a form and populating field values</span></span>

<span data-ttu-id="6651d-147">En el ejemplo siguiente se automatiza la apertura de un formulario en blanco y rellenar el nombre, apellidos y campos de dirección en el formulario.</span><span class="sxs-lookup"><span data-stu-id="6651d-147">The following example automates opening a blank form and populating the first name, last name, and address fields in the form.</span></span> <span data-ttu-id="6651d-148">En este escenario se da por supuesto un formulario que contiene tres cuadros de texto que están enlazados a campos denominados FirstName, LastName y dirección.</span><span class="sxs-lookup"><span data-stu-id="6651d-148">This scenario assumes a form that contains three text boxes that are bound to fields named FirstName, LastName, and Address.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="6651d-149">Crear la plantilla de formulario de ejemplo y el formulario</span><span class="sxs-lookup"><span data-stu-id="6651d-149">Create the sample form template and form</span></span>

1. <span data-ttu-id="6651d-150">Abra InfoPath y cree un formulario en blanco.</span><span class="sxs-lookup"><span data-stu-id="6651d-150">Open InfoPath and create a blank form.</span></span>
    
2. <span data-ttu-id="6651d-151">Agregue tres controles de cuadro de texto al formulario y el nombre de los campos enlazados a los controles: FirstName, LastName (apellidos) y la dirección.</span><span class="sxs-lookup"><span data-stu-id="6651d-151">Add three text box controls to the form, and name the fields bound to the controls: FirstName, LastName, and Address.</span></span> <span data-ttu-id="6651d-152">Agregue los otros campos que desee.</span><span class="sxs-lookup"><span data-stu-id="6651d-152">Add any other fields you want.</span></span>
    
3. <span data-ttu-id="6651d-153">En el panel de tareas **campos** , haga clic en la carpeta **misCampos** y, a continuación, haga clic en **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="6651d-153">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="6651d-154">En la pestaña **Detalles** , seleccione y copie el siguiente valor **Namespace:** y, a continuación, pegue esto en el Bloc de notas o alguna otra ubicación donde se pueden recuperar.</span><span class="sxs-lookup"><span data-stu-id="6651d-154">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="6651d-155">Necesitará este valor más adelante para establecer el valor de la propiedad **SelectionNamespaces** en el código.</span><span class="sxs-lookup"><span data-stu-id="6651d-155">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="6651d-156">Publicar la plantilla de formulario en una carpeta denominada C:\Temp y acepte el nombre predeterminado, Plantilla1.</span><span class="sxs-lookup"><span data-stu-id="6651d-156">Publish the form template to a folder named C:\Temp and accept the default name, Template1.</span></span>
    
6. <span data-ttu-id="6651d-157">Abra la plantilla de formulario y guardar un formulario en blanco como "Form1" en C:\Temp.</span><span class="sxs-lookup"><span data-stu-id="6651d-157">Open the form template and save a blank form as "Form1" to C:\Temp.</span></span>
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a><span data-ttu-id="6651d-158">Crear una aplicación de consola de código administrado para abrir el formulario y rellene los campos</span><span class="sxs-lookup"><span data-stu-id="6651d-158">Create a managed code console application to open the form and populate the fields</span></span>

1. <span data-ttu-id="6651d-159">Abra Visual Studio y cree un nuevo Visual C# o Visual Basic aplicación de consola denominada OpenForm.</span><span class="sxs-lookup"><span data-stu-id="6651d-159">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named OpenForm.</span></span>
    
2. <span data-ttu-id="6651d-160">Establecer referencias a los ensamblados de interoperabilidad de XML de InfoPath e interoperabilidad primaria de Microsoft Office InfoPath tal y como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6651d-160">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="6651d-161">Agregue el código siguiente en el archivo Program.cs o Module1.vb, asegurándose de que se actualice el valor del espacio de nombres en la configuración de la propiedad **SelectionNamespaces** con el valor que se copió al crear el formulario de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6651d-161">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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

4. <span data-ttu-id="6651d-162">En el menú **Depurar** , haga clic en **Iniciar depuración** para compilar y ejecutar la aplicación de consola.</span><span class="sxs-lookup"><span data-stu-id="6651d-162">On the **Debug** menu, click **Start Debugging** to compile and run the console application.</span></span> 
    
   <span data-ttu-id="6651d-163">La aplicación de abrir el formulario guardado como Form1.xml, rellene los campos FirstName, LastName (apellidos) y la dirección con los valores especificados en el código y, a continuación, guarde el formulario, dejando InfoPath abierto.</span><span class="sxs-lookup"><span data-stu-id="6651d-163">The application will open the form saved as Form1.xml and fill in the FirstName, LastName, and Address fields with the values specified in the code, and then save the form, leaving InfoPath open.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6651d-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="6651d-164">See also</span></span>

- [<span data-ttu-id="6651d-165">Información sobre el conjunto de interoperabilidad principal de InfoPath de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="6651d-165">About the Microsoft Office InfoPath Primary Interop Assembly</span></span>](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [<span data-ttu-id="6651d-166">Información sobre el conjunto de interoperabilidad XML de InfoPath</span><span class="sxs-lookup"><span data-stu-id="6651d-166">About the InfoPath XML Interop Assembly</span></span>](about-the-infopath-xml-interop-assembly.md)

