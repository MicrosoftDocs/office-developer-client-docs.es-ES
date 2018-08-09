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
# <a name="external-automation-scenarios-and-examples"></a>Ejemplos y escenarios de automatización externa

Los miembros proporcionan por Microsoft Office InfoPath principal ensamblado de interoperabilidad (Microsoft.Office.Interop.InfoPath.dll) y el ensamblado de interoperabilidad XML de InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) admiten escribir código administrado para automatizar InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Establecimiento de referencias a los ensamblados de interoperabilidad primaria de Microsoft Office InfoPath y la interoperabilidad de XML de InfoPath

Para escribir código administrado para automatizar InfoPath, debe establecer referencias a los ensamblados de interoperabilidad XML de InfoPath y a la interoperabilidad primaria de Microsoft InfoPath. El ensamblado de interoperabilidad primario de Microsoft InfoPath ofrece compatibilidad para la interoperabilidad con el modelo de objetos COM expuesto por IPEDITOR. DLL mediante el uso de los miembros del espacio de nombres [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) . El ensamblado de interoperabilidad XML de InfoPath proporciona compatibilidad para la interoperabilidad con el modelo de objetos COM expuesto por Microsoft XML Core Services (MSXML) mediante el uso de los miembros del espacio de nombres [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) . 
  
> [!IMPORTANT]
> Los usuarios de aplicaciones de código administrado que automaticen InfoPath deben tener InfoPath, el ensamblado de interoperabilidad primario de Microsoft Office InfoPath y el ensamblado de interoperabilidad XML de InfoPath instalado en sus equipos. La opción de **Compatibilidad con programación de .NET** en el programa de instalación de InfoPath se establece en **Ejecutar desde Mi PC** para una instalación típica de InfoPath.
>  
> Como resultado, tal y como se instala siempre y cuando el paquete redistribuible de .NET Framework 1.1 o el Kit de desarrollo de Software (SDK) de .NET Framework 1.1 o posterior, estos ensamblados de interoperabilidad también se instalará de forma predeterminada. Si estos ensamblados de interoperabilidad no están disponibles en el equipo del usuario, debe confirmar que está instalada .NET Framework 1.1 o posterior y, a continuación, ejecutar **programas y características** en el **Panel de Control** para cambiar el programa de instalación y establecer la programación de .NET ** Compatibilidad con** opción de InfoPath para **Ejecutar desde Mi PC**. 
  
Los procedimientos siguientes describen cómo establecer los ensamblados de interoperabilidad de referencias a la interoperabilidad primaria de Microsoft Office InfoPath y el XML de InfoPath en un proyecto de Visual Studio.
  
Para establecer una referencia al ensamblado de interoperabilidad primario de Microsoft.Office.Interop.InfoPath, establezca una referencia a la **Biblioteca de tipos de Microsoft InfoPath 3.0** en la ficha **COM** del cuadro de diálogo **Agregar referencia** . Aunque se establece una referencia desde la ficha **COM** , se establece una referencia para el ensamblado de interoperabilidad primario de Microsoft.Office.Interop.InfoPath.dll que se instala en la caché de ensamblados Global (GAC) mediante el programa de instalación de InfoPath. 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Establecer una referencia al ensamblado de interoperabilidad primario de Microsoft.Office.Interop.InfoPath

1. Abra un proyecto de código administrado de Visual Studio.
    
2. En el **Explorador de soluciones**, haga clic en **referencias**y, a continuación, haga clic en **Agregar referencia**.
    
3. En la ficha **COM** , haga doble clic en la **Biblioteca de tipos de Microsoft InfoPath 3.0**y, a continuación, haga clic en **Aceptar**.
    
Para establecer una referencia al ensamblado de interoperabilidad Microsoft.Office.Interop.InfoPath.Xml, busque el archivo Microsoft.Office.Interop.InfoPath.Xml.dll que se instala de forma predeterminada en el < _unidad_>: \Program Office\OFFICE14 carpeta . Aunque especifique la copia del ensamblado en el sistema de archivos local, este procedimiento establece una referencia al ensamblado Microsoft.Office.Interop.InfoPath.Xml.dll que se instala en la caché de ensamblados Global (GAC) mediante el programa de instalación de InfoPath.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Establecer una referencia al ensamblado de interoperabilidad Microsoft.Office.Interop.InfoPath.Xml

1. Abra o cree un proyecto de código administrado de Visual Studio, como una **Aplicación de consola** o una **Aplicación de Windows**.
    
2. En el **Explorador de soluciones**, haga clic en **referencias**y, a continuación, haga clic en **Agregar referencia**.
    
3. En la ficha. **NET** , haga clic en **Examinar**, desplácese hasta la < _unidad_>: \Program Office\OFFICE14 carpeta y, a continuación, haga clic en Microsoft.Office.Interop.InfoPath.Xml.dll.
    
4. Haga clic en **Aceptar**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Automatizar al cambiar el valor de un campo

Suponga que uno de los clientes del usuario de una plantilla de formulario de informe de ventas de InfoPath que han cambiado recientemente su nombre de la empresa"A" a "Empresa B." Un desarrollador se le pida que escribir código que se actualice automáticamente los formularios de informe de ventas guardados desde esta plantilla de formulario para reflejar el cambio de nombre. El siguiente escenario se da por supuesto un formulario que contenga un cuadro de texto que está enlazado a un campo denominado customerName.
  
### <a name="create-the-sample-form-template-and-form"></a>Crear la plantilla de formulario de ejemplo y el formulario

1. Abra InfoPath y cree una plantilla de formulario en blanco.
    
2. Agregar un control de **Cuadro de texto** al formulario y el nombre del campo enlazado en el control customerName.
    
3. En el panel de tareas **campos** , haga clic en la carpeta **misCampos** y, a continuación, haga clic en **Propiedades**.
    
4. En la pestaña **Detalles** , seleccione y copie el siguiente valor **Namespace:** y, a continuación, pegue esto en el Bloc de notas o alguna otra ubicación donde se pueden recuperar. Necesitará este valor más adelante para establecer el valor de la propiedad **SelectionNamespaces** en el código. 
    
5. Publicar la plantilla de formulario en una carpeta denominada C:\Test y acepte el nombre predeterminado, Plantilla1. 
    
6. Abra la plantilla de formulario, agregue el nombre de "Empresa A" al cuadro de texto dependiente del campo NombreDeCliente y, a continuación, guarde el formulario como "Form1". 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Crear una aplicación de consola de código administrado para cambiar el nombre de la empresa' A' a 'Compañía B'

1. Abra Visual Studio y cree un nuevo Visual C# o Visual Basic aplicación de consola denominada UpdateCustomer.
    
2. Establecer referencias a los ensamblados de interoperabilidad de XML de InfoPath e interoperabilidad primaria de Microsoft Office InfoPath tal y como se ha descrito anteriormente.
    
3. Agregue el código siguiente en el archivo Program.cs o Module1.vb, asegurándose de que se actualice el valor del espacio de nombres en la configuración de la propiedad **SelectionNamespaces** con el valor que se copió al crear el formulario de ejemplo. 
    
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

4. En el menú **Depurar** para compilar y ejecutar la aplicación de consola, haga clic en **Iniciar depuración** . 
    
   La aplicación abre el formulario guardado como Form1.xml y recorre en bucle todos los elementos customerName que contienen el valor de la empresa A y cambia ese valor a la empresa B. Una vez finalizada la operación, se guarda una copia nueva del formulario como Form2.xml en la carpeta C:\Test. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Automatizar la apertura de un formulario y rellenar los valores de campo

En el ejemplo siguiente se automatiza la apertura de un formulario en blanco y rellenar el nombre, apellidos y campos de dirección en el formulario. En este escenario se da por supuesto un formulario que contiene tres cuadros de texto que están enlazados a campos denominados FirstName, LastName y dirección.
  
### <a name="create-the-sample-form-template-and-form"></a>Crear la plantilla de formulario de ejemplo y el formulario

1. Abra InfoPath y cree un formulario en blanco.
    
2. Agregue tres controles de cuadro de texto al formulario y el nombre de los campos enlazados a los controles: FirstName, LastName (apellidos) y la dirección. Agregue los otros campos que desee.
    
3. En el panel de tareas **campos** , haga clic en la carpeta **misCampos** y, a continuación, haga clic en **Propiedades**.
    
4. En la pestaña **Detalles** , seleccione y copie el siguiente valor **Namespace:** y, a continuación, pegue esto en el Bloc de notas o alguna otra ubicación donde se pueden recuperar. Necesitará este valor más adelante para establecer el valor de la propiedad **SelectionNamespaces** en el código. 
    
5. Publicar la plantilla de formulario en una carpeta denominada C:\Temp y acepte el nombre predeterminado, Plantilla1.
    
6. Abra la plantilla de formulario y guardar un formulario en blanco como "Form1" en C:\Temp.
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Crear una aplicación de consola de código administrado para abrir el formulario y rellene los campos

1. Abra Visual Studio y cree un nuevo Visual C# o Visual Basic aplicación de consola denominada OpenForm.
    
2. Establecer referencias a los ensamblados de interoperabilidad de XML de InfoPath e interoperabilidad primaria de Microsoft Office InfoPath tal y como se ha descrito anteriormente.
    
3. Agregue el código siguiente en el archivo Program.cs o Module1.vb, asegurándose de que se actualice el valor del espacio de nombres en la configuración de la propiedad **SelectionNamespaces** con el valor que se copió al crear el formulario de ejemplo. 
    
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

4. En el menú **Depurar** , haga clic en **Iniciar depuración** para compilar y ejecutar la aplicación de consola. 
    
   La aplicación de abrir el formulario guardado como Form1.xml, rellene los campos FirstName, LastName (apellidos) y la dirección con los valores especificados en el código y, a continuación, guarde el formulario, dejando InfoPath abierto. 
    
## <a name="see-also"></a>Vea también

- [Información sobre el conjunto de interoperabilidad principal de InfoPath de Microsoft Office](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [Información sobre el conjunto de interoperabilidad XML de InfoPath](about-the-infopath-xml-interop-assembly.md)

