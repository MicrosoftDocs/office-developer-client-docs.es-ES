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
ms.openlocfilehash: af8bfbb0322b9d70fb85ba21a757a581ba423a44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310202"
---
# <a name="external-automation-scenarios-and-examples"></a>Ejemplos y escenarios de automatización externa

Los miembros proporcionados por el ensamblado de interoperabilidad primario de Microsoft Office InfoPath (Microsoft. Office. Interop. InfoPath. dll) y el ensamblado de interoperabilidad XML de InfoPath (Microsoft. Office. Interop. InfoPath. Xml. dll) admiten la escritura de código administrado para automatizar InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Establecimiento de referencias a los ensamblados de interoperabilidad primarios de Microsoft Office InfoPath y la interoperabilidad XML de InfoPath

Para escribir código administrado para automatizar InfoPath, debe establecer referencias a la interoperabilidad principal de Microsoft InfoPath y a los ensamblados de interoperabilidad XML de InfoPath. El ensamblado de interoperabilidad primario de Microsoft InfoPath proporciona compatibilidad con la interoperabilidad con el modelo de objetos COM expuesto por IPEDITOR. DLL con los miembros del espacio de nombres [Microsoft. Office. Interop. InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) . El ensamblado de interoperabilidad XML de InfoPath proporciona compatibilidad con la interoperabilidad con el modelo de objetos COM expuesto por Microsoft XML Core Services (MSXML) mediante los miembros del espacio de nombres [Microsoft. Office. Interop. InfoPath. XML](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) . 
  
> [!IMPORTANT]
> Los usuarios de aplicaciones de código administrado que automatizan InfoPath deben tener InfoPath, el ensamblado de interoperabilidad primario de Microsoft Office InfoPath y el ensamblado de interoperabilidad XML de InfoPath instalado en sus equipos. La opción **compatibilidad con programación de .net** en el programa de instalación de InfoPath se establece en **Ejecutar desde mi PC** para una instalación típica de InfoPath.
>  
> Como resultado, siempre que esté instalado el paquete redistribuible de .NET Framework 1,1 o el kit de desarrollo de software (SDK) de .NET Framework 1,1 o posterior, estos ensamblados de interoperabilidad también se instalarán de forma predeterminada. Si estos ensamblados de interoperabilidad no están disponibles en el equipo de un usuario, debe confirmar que .NET Framework 1,1 o posterior está instalado y, a continuación, ejecutar **programas y características** desde el **Panel de control** para cambiar la configuración y establecer la capacidad de **programación de .net Admite** la opción de InfoPath para **Ejecutar desde mi PC**. 
  
Los procedimientos siguientes describen cómo establecer referencias a la interoperabilidad principal de Microsoft Office InfoPath y los ensamblados de interoperabilidad XML de InfoPath en un proyecto de Visual Studio.
  
Para establecer una referencia al ensamblado de interoperabilidad primario Microsoft. Office. Interop. InfoPath, establezca una referencia a la **biblioteca de tipos de Microsoft InfoPath 3,0** en la ficha **com** del cuadro de diálogo **Agregar referencia** . Aunque se establezca una referencia desde la ficha **com** , se establece una referencia al ensamblado de interoperabilidad primario Microsoft. Office. Interop. InfoPath. dll que está instalado en la memoria caché de ensamblados global (GAC) mediante el programa de instalación de InfoPath. 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Establecer una referencia al ensamblado de interoperabilidad primario Microsoft. Office. Interop. InfoPath

1. Abra un proyecto de código administrado de Visual Studio.
    
2. En el **Explorador de soluciones**, haga clic con el botón secundario en **Referencias** y, a continuación, haga clic en **Agregar referencia**.
    
3. En la pestaña **com** , haga doble clic en **biblioteca de tipos de Microsoft InfoPath 3,0**y, a continuación, haga clic en **Aceptar**.
    
Para establecer una referencia al ensamblado de interoperabilidad Microsoft. Office. Interop. InfoPath. XML, vaya al archivo Microsoft. Office. Interop. InfoPath. Xml. dll que se instala de forma predeterminada en la _unidad_< >: \Archivos de programa\Microsoft Office\OFFICE14 . Aunque especifique la copia del ensamblado en el sistema de archivos local, este procedimiento establece una referencia al ensamblado Microsoft. Office. Interop. InfoPath. Xml. dll que está instalado en la memoria caché global de ensamblados (GAC) mediante el programa de instalación de InfoPath.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Establecer una referencia al ensamblado de interoperabilidad Microsoft. Office. Interop. InfoPath. XML

1. Abra o cree un proyecto de código administrado de Visual Studio, como una **aplicación de consola** o una aplicación de **Windows**.
    
2. En el **Explorador de soluciones**, haga clic con el botón secundario en **Referencias** y, a continuación, haga clic en **Agregar referencia**.
    
3. En la ficha **.net** , haga clic en **examinar**, vaya a __ la carpeta < >: \Archivos de programa\Microsoft Office\OFFICE14 y, a continuación, haga clic en Microsoft. Office. Interop. InfoPath. Xml. dll.
    
4. Haga clic en **Aceptar**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Automatizar el cambio de valor de un campo

SuPongamos que uno de los clientes del usuario de una plantilla de formulario de informe de ventas de InfoPath cambió recientemente su nombre de "compañía A" a "compañía B". Se pide a los desarrolladores que escriban código que actualice automáticamente los formularios de informes de ventas guardados desde esta plantilla de formulario para reflejar el cambio de nombre. El siguiente escenario asume un formulario que contiene un cuadro de texto enlazado a un campo denominado Nombre_cliente.
  
### <a name="create-the-sample-form-template-and-form"></a>Crear el formulario y la plantilla de formulario de ejemplo

1. Abra InfoPath y cree una plantilla de formulario en blanco.
    
2. Agregue un control de **cuadro de texto** al formulario y asigne un nombre al campo enlazado al control customerName.
    
3. En el panel de tareas **campos** , haga clic con el botón secundario en la carpeta Mis **campos** y, a continuación, haga clic en **propiedades**.
    
4. En la pestaña **detalles** , seleccione y copie el valor que sigue al **espacio de nombres:** y, a continuación, péguelo en el Bloc de notas o en otra ubicación en la que pueda recuperarlo. Este valor será necesario más adelante para establecer el valor de la propiedad **SelectionNamespaces** en el código. 
    
5. Publique la plantilla de formulario en una carpeta denominada C:\Test y acepte el nombre predeterminado, Template1. 
    
6. Abra la plantilla de formulario, agregue el nombre "compañía A" al cuadro de texto enlazado al campo Nombre_cliente y, a continuación, guarde el formulario como "Form1". 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Crear una aplicación de consola de código administrado para cambiar el nombre de ' Company A ' a ' Company B '

1. Abra Visual Studio y cree una nueva aplicación de consola de Visual C# o Visual Basic denominada UpdateCustomer.
    
2. Establezca referencias a los ensamblados de interoperabilidad primario de Microsoft Office InfoPath y de la interoperabilidad XML de InfoPath como se ha descrito anteriormente.
    
3. Agregue el siguiente código al archivo Program.cs o Module1. VB, asegurándose de actualizar el valor del espacio de nombres en el valor de la propiedad **SelectionNamespaces** con el valor que ha copiado al crear el formulario de ejemplo. 
    
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
    "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
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
    "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
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

4. Haga clic en **iniciar** depuración en el menú Depurar para compilar y ejecutar la aplicación de consola. **** 
    
   La aplicación abre el formulario guardado como Form1. XML y recorre todos los elementos Nombre_cliente que contienen el valor Company a y cambia ese valor a Company B. Una vez completada la operación, se guarda una nueva copia del formulario como Form2. XML en la carpeta C:\Test. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Automatizar la apertura de un formulario y el relleno de los valores de los campos

En el siguiente ejemplo se automatiza la apertura de un formulario en blanco y se rellenan los campos nombre, apellidos y dirección del formulario. Este escenario presupone un formulario que contiene tres cuadros de texto enlazados a campos denominados FirstName, LastName y Address.
  
### <a name="create-the-sample-form-template-and-form"></a>Crear el formulario y la plantilla de formulario de ejemplo

1. Abra InfoPath y cree un formulario en blanco.
    
2. Agregue tres controles de cuadro de texto al formulario y asigne a los campos un nombre enlazado a los controles: FirstName, LastName y Address. Agregue los demás campos que desee.
    
3. En el panel de tareas **campos** , haga clic con el botón secundario en la carpeta Mis **campos** y, a continuación, haga clic en **propiedades**.
    
4. En la pestaña **detalles** , seleccione y copie el valor que sigue al **espacio de nombres:** y, a continuación, péguelo en el Bloc de notas o en otra ubicación en la que pueda recuperarlo. Este valor será necesario más adelante para establecer el valor de la propiedad **SelectionNamespaces** en el código. 
    
5. Publique la plantilla de formulario en una carpeta llamada C:\Temp y acepte el nombre predeterminado, Template1.
    
6. Abra la plantilla de formulario y guarde un formulario en blanco como "Form1" en C:\Temp.
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Crear una aplicación de consola de código administrado para abrir el formulario y rellenar los campos

1. Abra Visual Studio y cree una nueva aplicación de consola de Visual C# o Visual Basic llamada AbrirFormulario.
    
2. Establezca referencias a los ensamblados de interoperabilidad primario de Microsoft Office InfoPath y de la interoperabilidad XML de InfoPath como se ha descrito anteriormente.
    
3. Agregue el siguiente código al archivo Program.cs o Module1. VB, asegurándose de actualizar el valor del espacio de nombres en el valor de la propiedad **SelectionNamespaces** con el valor que ha copiado al crear el formulario de ejemplo. 
    
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
            doc.setProperty("SelectionNamespaces","xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
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
          doc.setProperty("SelectionNamespaces", "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Pre-populate the fields with specified values.
          doc.selectSingleNode("//my:FirstName").text = "My Name"
          doc.selectSingleNode("//my:LastName").text = "My LastName"
          doc.selectSingleNode("//my:Address").text = "My Address"
          ' Save the form, leaving InfoPath open.
          myXDoc.Save()
      End Sub
    End Module
    
   ```

4. En el **** menú Depurar, haga clic en **iniciar** depuración para compilar y ejecutar la aplicación de consola. 
    
   La aplicación abrirá el formulario guardado como Form1. XML y rellenará los campos FirstName, LastName y address con los valores especificados en el código y, a continuación, guarda el formulario, dejando abierto InfoPath. 
    
## <a name="see-also"></a>Vea también

- [Información sobre el conjunto de interoperabilidad principal de InfoPath de Microsoft Office](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [Información sobre el conjunto de interoperabilidad XML de InfoPath](about-the-infopath-xml-interop-assembly.md)

