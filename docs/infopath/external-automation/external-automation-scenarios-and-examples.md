---
title: Ejemplos y escenarios de automatización externa
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- automatizar infopath 2007,forms [InfoPath 2007], agregar datos mediante programación,automatización [InfoPath 2007], escenarios externos
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Los miembros proporcionados por el ensamblado de interoperabilidad principal de Microsoft Office InfoPath (Microsoft.Office.Interop.InfoPath.dll) y el ensamblado de interoperabilidad XML de InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) admiten la escritura de código administrado para automatizar InfoPath.
ms.openlocfilehash: 79fbc56033ffce639b5007874dabf56e8e286edb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537818"
---
# <a name="external-automation-scenarios-and-examples"></a>Ejemplos y escenarios de automatización externa

Los miembros proporcionados por el ensamblado de interoperabilidad principal de Microsoft Office InfoPath (Microsoft.Office.Interop.InfoPath.dll) y el ensamblado de interoperabilidad XML de InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) admiten la escritura de código administrado para automatizar InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Establecer referencias a los Microsoft Office interoperabilidad principal de InfoPath y los ensamblados de interoperabilidad XML de InfoPath

Para escribir código administrado para automatizar InfoPath, debe establecer referencias a la interoperabilidad principal de Microsoft InfoPath y a los ensamblados de interoperabilidad XML de InfoPath. El ensamblado de interoperabilidad principal de Microsoft InfoPath proporciona compatibilidad con la interoperabilidad con el modelo de objetos COM expuesto por IPEDITOR.DLL mediante los miembros del espacio de nombres [Microsoft.Office.Interop.InfoPath.](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) El ensamblado de interoperabilidad XML de InfoPath proporciona compatibilidad con la interoperabilidad con el modelo de objetos COM expuesto por Microsoft XML Core Services (MSXML) mediante los miembros del espacio de nombres [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) web. 
  
> [!IMPORTANT]
> Los usuarios de aplicaciones de código administrado que automatizan InfoPath deben tener InfoPath, el ensamblado de interoperabilidad principal de infoPath de Microsoft Office y el ensamblado de interoperabilidad XML de InfoPath instalado en sus equipos. La **opción .NET Programmability Support** del programa de instalación de InfoPath se establece en Ejecutar desde Mi **equipo** para una instalación típica de InfoPath.
>  
> Como resultado, siempre y cuando se instale el Kit de desarrollo de software (SDK) redistribuible o .NET Framework 1.1 de .NET Framework 1.1 o posterior, estos ensamblados de interoperabilidad también se instalarán de forma predeterminada. Si estos ensamblados de interoperabilidad no están disponibles en el equipo de un usuario, debe confirmar que el  .NET Framework 1.1 o posterior está instalado y, a continuación, ejecutar Programas y características desde el Panel de **control** para cambiar la configuración y establecer la opción Compatibilidad de programación **de .NET** de InfoPath en **Ejecutar desde Mi equipo**. 
  
Los siguientes procedimientos describen cómo establecer referencias a la interoperabilidad principal de Microsoft Office InfoPath y a los ensamblados de interoperabilidad XML de InfoPath en un Visual Studio proyecto.
  
Para establecer una referencia a Microsoft. Office.Interop.InfoPath ensamblado de interoperabilidad principal, establezca una referencia a biblioteca de tipos de  **Microsoft InfoPath 3.0** en la ficha **COM** del cuadro de diálogo Agregar referencia. Aunque establezca una referencia desde la pestaña **COM,** se establece una referencia al ensamblado de interoperabilidad principal de Microsoft.Office.Interop.InfoPath.dll instalado en la caché global de ensamblados (GAC) por el programa de instalación de InfoPath. 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Establezca una referencia a Microsoft. Office.Interop.InfoPath ensamblado de interoperabilidad principal

1. Abra un Visual Studio de código administrado.
    
2. En el **Explorador de soluciones**, haga clic con el botón secundario en **Referencias** y, a continuación, haga clic en **Agregar referencia**.
    
3. En la **pestaña COM,** haga doble clic en Biblioteca de tipos de **Microsoft InfoPath 3.0** y, a continuación, haga clic en **Aceptar**.
    
Para establecer una referencia al ensamblado de interoperabilidad de Microsoft.Office.Interop.InfoPath.Xml, vaya al archivo Microsoft.Office.Interop.InfoPath.Xml.dll que  está instalado de forma predeterminada en la carpeta> unidad <:\Archivos de programa\Microsoft Office\OFFICE14. Aunque especifique la copia del ensamblado en el sistema de archivos local, este procedimiento establece una referencia al ensamblado de Microsoft.Office.Interop.InfoPath.Xml.dll instalado en la caché global de ensamblados (GAC) por el programa de instalación de InfoPath.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Establecer una referencia al ensamblado Microsoft.Office.Interop.InfoPath.Xml de interoperabilidad

1. Abra o cree un proyecto Visual Studio código administrado, como una **aplicación** de consola **o Windows aplicación**.
    
2. En el **Explorador de soluciones**, haga clic con el botón secundario en **Referencias** y, a continuación, haga clic en **Agregar referencia**.
    
3. En la pestaña **.NET,** haga clic en **Examinar**, vaya _a_ la carpeta <> unidad>:\Archivos de programa\Microsoft Office\OFFICE14 y, a continuación, haga clic en Microsoft.Office.Interop.InfoPath.Xml.dll.
    
4. Haga clic en **Aceptar**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Automatizar el cambio del valor de un campo

Supongamos que uno de los clientes del usuario de una plantilla de formulario de informe de ventas de InfoPath cambió recientemente su nombre de "Empresa A" a "Empresa B". Se pide a un desarrollador que escriba código que actualice automáticamente los formularios de informe de ventas guardados desde esta plantilla de formulario para reflejar el cambio de nombre. En el siguiente escenario se supone que un formulario contiene un cuadro de texto enlazado a un campo denominado customerName.
  
### <a name="create-the-sample-form-template-and-form"></a>Crear la plantilla de formulario y el formulario de ejemplo

1. Abra InfoPath y cree una plantilla de formulario en blanco.
    
2. Agregue un **control Cuadro de** texto al formulario y asigne un nombre al campo enlazado al control customerName.
    
3. En el panel de tareas **Campos,** haga clic con el botón secundario en la **carpeta myFields** y, a continuación, haga clic en **Propiedades**.
    
4. En la **pestaña Detalles,** seleccione y copie el valor siguiente Espacio de **nombres:** y, a continuación, pegue esto en Bloc de notas o en otra ubicación donde pueda recuperarlo. Necesitará este valor más adelante para establecer el valor de la **propiedad SelectionNamespaces** en el código. 
    
5. Publique la plantilla de formulario en una carpeta denominada C:\Test y acepte el nombre predeterminado, Template1. 
    
6. Abra la plantilla de formulario, agregue el nombre "Empresa A" al cuadro de texto enlazado al campo customerName y, a continuación, guarde el formulario como "Form1". 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Crear una aplicación de consola de código administrado para cambiar el nombre de "Empresa A" a "Empresa B"

1. Abra Visual Studio y cree un nuevo objeto Visual C# o una Visual Basic de consola denominada UpdateCustomer.
    
2. Establezca referencias a los ensamblados Microsoft Office interoperabilidad principal de InfoPath y a los ensamblados de interoperabilidad XML de InfoPath, como se describió anteriormente.
    
3. Agregue el siguiente código al archivo Program.cs o Module1.vb, asegurándose de actualizar el valor del espacio de nombres en la configuración de la propiedad **SelectionNamespaces** con el valor que copió al crear el formulario de ejemplo. 
    
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

4. Haga **clic en Iniciar depuración** en el menú **Depurar** para compilar y ejecutar la aplicación de consola. 
    
   La aplicación abre el formulario guardado como Form1.xml y recorre en bucle todos los elementos customerName que contienen el valor Empresa A y cambia ese valor a la empresa B. Una vez completada la operación, se guarda una nueva copia del formulario como Form2.xml en la carpeta C:\Test. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Automatizar la apertura de un formulario y rellenar valores de campo

En el ejemplo siguiente se automatiza la apertura de un formulario en blanco y la rellenar los campos de nombre, apellido y dirección del formulario. En este escenario se supone que un formulario contiene tres cuadros de texto enlazados a campos denominados FirstName, LastName y Address.
  
### <a name="create-the-sample-form-template-and-form"></a>Crear la plantilla de formulario y el formulario de ejemplo

1. Abra InfoPath y cree un formulario en blanco.
    
2. Agregue tres controles de cuadro de texto al formulario y asigne un nombre a los campos enlazados a los controles: FirstName, LastName y Address. Agregue cualquier otro campo que desee.
    
3. En el panel de tareas **Campos,** haga clic con el botón secundario en la **carpeta myFields** y, a continuación, haga clic en **Propiedades**.
    
4. En la **pestaña Detalles,** seleccione y copie el valor siguiente Espacio de **nombres:** y, a continuación, pegue esto en Bloc de notas o en otra ubicación donde pueda recuperarlo. Necesitará este valor más adelante para establecer el valor de la **propiedad SelectionNamespaces** en el código. 
    
5. Publique la plantilla de formulario en una carpeta denominada C:\Temp y acepte el nombre predeterminado, Template1.
    
6. Abra la plantilla de formulario y guarde un formulario en blanco como "Form1" en C:\Temp.
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Crear una aplicación de consola de código administrado para abrir el formulario y rellenar los campos

1. Abra Visual Studio y cree un nuevo objeto Visual C# o Visual Basic de consola denominado OpenForm.
    
2. Establezca referencias a los ensamblados Microsoft Office interoperabilidad principal de InfoPath y a los ensamblados de interoperabilidad XML de InfoPath, como se describió anteriormente.
    
3. Agregue el siguiente código al archivo Program.cs o Module1.vb, asegurándose de actualizar el valor del espacio de nombres en la configuración de la propiedad **SelectionNamespaces** con el valor que copió al crear el formulario de ejemplo. 
    
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

4. En el **menú Depurar,** haga clic **en Iniciar depuración** para compilar y ejecutar la aplicación de consola. 
    
   La aplicación abrirá el formulario guardado como Form1.xml y rellenará los campos FirstName, LastName y Address con los valores especificados en el código y, a continuación, guardará el formulario, dejando InfoPath abierto. 
    
## <a name="see-also"></a>Vea también

- [Información sobre el conjunto de interoperabilidad principal de InfoPath de Microsoft Office](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [Información sobre el conjunto de interoperabilidad XML de InfoPath](about-the-infopath-xml-interop-assembly.md)

