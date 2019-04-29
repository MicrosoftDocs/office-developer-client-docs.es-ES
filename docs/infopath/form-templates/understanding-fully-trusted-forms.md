---
title: Descripción de los formularios de plena confianza
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64d62990-6275-edef-c639-b6ba8d10c38c
description: InfoPath proporciona la capacidad de crear formularios de plena confianza, que son formularios que tienen más permisos de seguridad y que pueden tener acceso a recursos del sistema y a otros componentes en el equipo de un usuario. En este artículo se explica qué es y por qué se usa un formulario de plena confianza, así como la creación de un formulario de plena confianza mediante la conversión y el registro manual de un formulario estándar, o mediante la firma digital de un formulario estándar.
ms.openlocfilehash: 04560e0c844d6a6ff681fd366ca7da2e4db36ba1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430395"
---
# <a name="understanding-fully-trusted-forms"></a><span data-ttu-id="8e6a3-104">Descripción de los formularios de plena confianza</span><span class="sxs-lookup"><span data-stu-id="8e6a3-104">Understanding Fully Trusted Forms</span></span>

<span data-ttu-id="8e6a3-105">InfoPath proporciona la capacidad de crear formularios de plena confianza, que son formularios que tienen más permisos de seguridad y que pueden tener acceso a recursos del sistema y a otros componentes en el equipo de un usuario.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-105">InfoPath provides the ability to create fully trusted forms, which are forms that have greater security permissions and can access system resources and other components on a user's computer.</span></span> <span data-ttu-id="8e6a3-106">En este artículo se explica qué es y por qué se usa un formulario de plena confianza, así como la creación de un formulario de plena confianza mediante la conversión y el registro manual de un formulario estándar, o mediante la firma digital de un formulario estándar.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-106">This article describes what a fully trusted form is, and why it is used, and create a fully trusted form by manually converting and registering a standard form, or by digitally signing a standard form.</span></span>

<span data-ttu-id="8e6a3-p103">Las plantillas de formulario de InfoPath se pueden implementar con distintos niveles de seguridad. El nivel que se use dependerá del nivel de acceso a los recursos externos que vaya a tener el formulario. De forma predeterminada, las plantillas de formulario de InfoPath tienen restringido el acceso a los recursos del sistema y no se les permite usar ningún componente de software que no esté marcado como seguro para scripting. Sin embargo, este comportamiento se puede cambiar para que un formulario pueda tener acceso a los recursos del sistema y a otros recursos externos, incluidos los componentes de software que no están marcados como seguros para scripting.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p103">InfoPath form templates can be deployed with varying levels of security. The level you use is dictated by the level of access to external resources that you want a form to have. By default, InfoPath form templates are restricted from accessing system resources and are not allowed to use any software components that are not marked as safe for scripting. However, this behavior can be overridden so that a form can access system resources and other external resources, including software components that are not marked as safe for scripting.</span></span>
  
<span data-ttu-id="8e6a3-p104">Para que se pueda usar un formulario, InfoPath debe tener acceso a la plantilla de formulario en la que se basa el formulario. Cuando se crea una plantilla de formulario, InfoPath crea una entrada en el archivo de definición de formulario (.xsf) que contiene la dirección URL de la ubicación de la plantilla de formulario. Un formulario basado en URL se denomina *de espacio aislado*. Cuando un usuario lo rellena, el formulario se agrega a una memoria caché local y se le niega el acceso a los recursos del sistema. Este tipo de formulario hereda sus permisos del dominio en el que se abre.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p104">For a form to be used, InfoPath must be able to access the form template that the form is based on. When you create a form template, InfoPath creates an entry in the form definition (.xsf) file that contains the URL of the location of the form template. A URL-based form is said to be *sandboxed*. When a user fills it out, the form is added in a local cache and denied access to system resources. This kind of form inherits its permissions from the domain in which it is opened.</span></span> 
  
<span data-ttu-id="8e6a3-p105">Sin embargo, puede modificar un formulario para que se base en un nombre de recursos uniforme (URN), que permite el acceso a los recursos del sistema. Los formularios de este tipo se denominan *de plena confianza*.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p105">However, you can modify a form so that it is based on a Uniform Resource Name (URN) instead, which allows access to system resources. Forms of this kind are said to be *fully trusted*.</span></span> 
  
## <a name="why-use-a-fully-trusted-form"></a><span data-ttu-id="8e6a3-118">¿Por qué usar un formulario de plena confianza?</span><span class="sxs-lookup"><span data-stu-id="8e6a3-118">Why Use a Fully Trusted Form?</span></span>

<span data-ttu-id="8e6a3-p106">Los formularios de plena confianza tienen un mejor conjunto de permisos que los formularios de espacio aislado. Por ejemplo, pueden contener código de programación que use objetos externos para obtener acceso a los recursos del sistema, pueden usar componentes de software o controles de Microsoft ActiveX que no estén marcados como seguros para scripting y pueden usar lógica empresarial personalizada proporcionada por ensamblados .NET.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p106">Fully trusted forms have a better set of permissions than sandboxed forms. For example, they can contain programming code that uses external objects for accessing system resources, they can use software components or Microsoft ActiveX controls that are not marked as safe for scripting, and they can use custom business logic provided by .NET assemblies.</span></span>
  
<span data-ttu-id="8e6a3-p107">Además, algunos miembros del modelo de objetos de InfoPath se establecen en el nivel de seguridad 3, lo que significa que solo pueden usarse en un formulario de plena confianza. Por ejemplo, para obtener acceso al objeto Microsoft Office **CommandBars**, se puede usar la propiedad [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) de la clase [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) de InfoPath para establecer una referencia hacia él. Debido a que esta propiedad está establecida en el nivel de seguridad 3, no se puede usar en un formulario que no sea de plena confianza.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p107">In addition, some members of the InfoPath object model are set to security level 3, which means that they can only be used in a fully trusted form. For example, to access the Microsoft Office **CommandBars** object, you use the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the InfoPath [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class to set a reference to it. Because this property is set to security level 3, it cannot be used in a form that is not fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8e6a3-124">[!NOTA] El uso de la propiedad [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) de la clase [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) , o cualquier otro miembro del modelo de objetos con un nivel de seguridad 3, en un formulario que no sea de plena confianza devolverá un error de "permiso denegado".</span><span class="sxs-lookup"><span data-stu-id="8e6a3-124">Using the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class, or any other object model member that has a security level of 3, in a form that is not fully trusted will result in a "permission denied" error.</span></span> 
  
## <a name="what-makes-a-form-fully-trusted"></a><span data-ttu-id="8e6a3-125">¿Cómo hacer que un formulario sea de plena confianza?</span><span class="sxs-lookup"><span data-stu-id="8e6a3-125">What Makes a Form Fully Trusted?</span></span>

<span data-ttu-id="8e6a3-126">Se requieren las siguientes acciones, en las que participan tanto la interfaz de usuario de InfoPath como los archivos de formulario, para crear y usar un formulario de plena confianza:</span><span class="sxs-lookup"><span data-stu-id="8e6a3-126">The following actions, involving both the InfoPath user interface and the form files, are required to create and use a fully trusted form:</span></span>
  
- <span data-ttu-id="8e6a3-p108">Habilitar InfoPath para permitir el uso de formularios de plena confianza en la categoría **Editores de confianza** del cuadro de diálogo **Centro de confianza**. Esta opción debe estar habilitada para que los usuarios puedan abrir formularios de plena confianza.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p108">Enabling InfoPath to allow for the use of fully trusted forms on the **Trusted Publishers** category of the **Trust Center** dialog box. This option must be enabled for users to open fully trusted forms.</span></span> 
    
- <span data-ttu-id="8e6a3-129">Registrar el formulario de plena confianza en el equipo de destino usando el método **RegisterSolution** del objeto **Application** de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-129">Registering the fully trusted form on the target computer by using the **RegisterSolution** method of the InfoPath **Application** object.</span></span> 
    
## <a name="creating-a-fully-trusted-form"></a><span data-ttu-id="8e6a3-130">Creación de un formulario de plena confianza</span><span class="sxs-lookup"><span data-stu-id="8e6a3-130">Creating a Fully Trusted Form</span></span>

- <span data-ttu-id="8e6a3-131">Puede crear el formulario manualmente, lo que implica modificar directamente algunos de los archivos del formulario.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-131">You can create the form manually, which involves modifying some of the form files directly.</span></span>
    
- <span data-ttu-id="8e6a3-132">Puede firmar digitalmente la plantilla de formulario.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-132">You can digitally sign the form template.</span></span>
    
### <a name="manually-creating-a-fully-trusted-form"></a><span data-ttu-id="8e6a3-133">Creación manual de un formulario de plena confianza</span><span class="sxs-lookup"><span data-stu-id="8e6a3-133">Manually Creating a Fully Trusted Form</span></span>

#### <a name="to-manually-create-a-fully-trusted-form"></a><span data-ttu-id="8e6a3-134">Para crear manualmente un formulario de plena confianza</span><span class="sxs-lookup"><span data-stu-id="8e6a3-134">To manually create a fully trusted form</span></span>

1. <span data-ttu-id="8e6a3-135">Realice una copia de seguridad de la plantilla de formulario que desea que sea de plena confianza.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-135">Make a backup copy of the form template that you want to make fully trusted.</span></span>
    
2. <span data-ttu-id="8e6a3-136">Abra la plantilla de formulario en InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-136">Open the form template in InfoPath.</span></span>
    
3. <span data-ttu-id="8e6a3-137">Guarde los archivos de origen del formulario en una carpeta del disco duro; para ello, haga clic en la pestaña **Archivo**, en **Publicar** y, a continuación, en **Exportar archivos de origen**.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-137">Save the form source files to a folder on your hard disk by clicking the **File** tab, clicking **Publish**, and then clicking **Export Source Files**.</span></span>
    
4. <span data-ttu-id="8e6a3-138">Especifique la carpeta en la que desea guardar los archivos de origen del formulario, haga clic en **Aceptar** y, a continuación, salga de InfoPath Designer.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-138">Specify the folder in which to save the form source files, click **OK**, and then exit the InfoPath designer.</span></span>
    
5. <span data-ttu-id="8e6a3-139">En la carpeta en la que extrajo los archivos de formulario, abra el archivo de definición de formulario (.xsf), llamado  `manifest.xsf` de forma predeterminada, en un editor de texto como Bloc de notas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-139">In the folder in which you extracted the form files, open the form definition (.xsf) file, named  `manifest.xsf` by default, in a text editor such as Microsoft Notepad.</span></span> 
    
6. <span data-ttu-id="8e6a3-140">Agregue los siguientes atributos al elemento **xDocumentClass** en el archivo .xsf:</span><span class="sxs-lookup"><span data-stu-id="8e6a3-140">Add the following attributes to the **xDocumentClass** element in the .xsf file:</span></span> 
   
   `requireFullTrust="yes"`<br/>
   `name="urn:MyForm:MyCompany`

   > [!NOTE]
   > [!NOTA] Los valores usados para el URN pueden ser cualquier tipo de valor de cadena, siempre que este valor sea único. Debe haber al menos dos valores después del `urn:` prefijo, y estos valores deben estar separados por dos puntos. <span data-ttu-id="8e6a3-143">Además, el URN no debe exceder los 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-143">In addition, the URN should not exceed 255 characters.</span></span> 
  
7. <span data-ttu-id="8e6a3-144">Guarde y cierre el archivo .xsf y, a continuación, abra el archivo de plantilla XML (.xml) llamado  `Template.xml` de forma predeterminada, en un editor de texto como Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-144">Save and close the .xsf file, and then open the XML template (.xml) file that is named  `Template.xml` by default, in a text editor such as Notepad.</span></span> 
    
8. <span data-ttu-id="8e6a3-145">Quite el atributo **href** de la instrucción de procesamiento  `mso-infoPathSolution` y reemplácelo con el mismo atributo **name** que usó en el paso 6 para el archivo .xsf.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-145">Remove the **href** attribute from the  `mso-infoPathSolution` processing instruction and replace it with the same **name** attribute that you used in step 6 for the .xsf file.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="8e6a3-146">[!NOTA] Los valores del URN usados para el atributo **name** deben ser los mismos tanto en el archivo .xsf como en el archivo de plantilla XML.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-146">The URN values that are used for the **name** attribute must be the same in both the .xsf file and XML template file.</span></span> 
  
9. <span data-ttu-id="8e6a3-147">Guarde y cierre el archivo de plantilla XML.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-147">Save and close the XML template file.</span></span>
    
10. <span data-ttu-id="8e6a3-148">Vuelva a empaquetar los archivos en el formato CAB .xsn con una herramienta como makecab.exe.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-148">Repackage the files into the .xsn CAB format with a tool such as makecab.exe.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8e6a3-p110">[!NOTA] Si bien el diseñador de formularios de InfoPath admite volver a empaquetar los archivos de formulario en un archivo .xsn, si lo hace, revertirá el formulario a un formulario basado en URL. Por esta razón, debe volver a empaquetar los archivos manualmente para evitar que se sobrescriban los cambios en los archivos de formulario.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p110">Although InfoPath form designer supports repackaging the form files into an .xsn file, doing this will revert the form to a URL-based form. For this reason, you must repackage the files manually to avoid overwriting your changes to the form files.</span></span> 
  
11. <span data-ttu-id="8e6a3-p111">Cree un programa de instalación personalizado mediante el método **RegisterSolution** del objeto **Application** de InfoPath para instalar el formulario de plena confianza. Una forma fácil de hacerlo es crear un archivo de script que use las siguientes líneas de código (tanto en la sintaxis de Microsoft JScript como de VBScript):</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p111">Create a custom installation program by using the **RegisterSolution** method of the InfoPath **Application** object to install the fully trusted form. A simple way to do this is to create a script file that uses the following lines of code (in either Microsoft JScript or VBScript syntax):</span></span> 
    
    ```js
        objIPApp = new ActiveXObject("InfoPath.Application"); 
        objIPApp.RegisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
        objIPApp.Quit(); 
        objIPApp = null;
    ```
   
    ```vb
        Public Sub InstallForm()
            Dim objIPApp As Object
            ' Create a reference to the Application object.
            Set objIPApp = CreateObject("InfoPath.Application")
            ' Register the InfoPath form template.
            objIPApp.RegisterSolution ("C:\\My Forms\\MyFormTemplate.xsn")
            MsgBox "The InfoPath form template has been registered."
            Set objIPApp = Nothing
        End Sub
        
    ```

> [!NOTE] 
> <span data-ttu-id="8e6a3-p112">[!NOTA] Si bien en este ejemplo se usa un archivo de script simple, también puede usar un mecanismo de instalación más eficaz los como archivos (.msi) de Microsoft Windows Installer. Sin embargo, asegúrese de usar el método **RegisterSolution** para instalar correctamente el formulario de plena confianza en el equipo de destino. Para obtener acceso al método **RegisterSolution** del objeto **Application** de InfoPath desde Visual Basic o Visual Studio, establezca una referencia a la Biblioteca de tipos de Microsoft InfoPath 3.0, proporcionada por IPEDITOR.dll que está instalado en la carpeta C:\Program Files\Microsoft Office\Office14.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p112">Although this example uses a simple script file, you can also use a more robust installation mechanism such as Microsoft Windows Installer (.msi) files. Be sure, however, to use the **RegisterSolution** method to correctly install the fully trusted form on the target computer. To access the **RegisterSolution** method of the InfoPath the **Application** object from Visual Basic or Visual Studio, set a reference to the Microsoft InfoPath 3.0 Type Library, which is provided by IPEDITOR.dll that is installed in the C:\Program Files\Microsoft Office\Office14 folder.</span></span> 
  
<span data-ttu-id="8e6a3-156">Si tiene que quitar un formulario de plena confianza, puede usar el método **UnregisterSolution** del objeto **Application** como se muestra en los siguientes ejemplos de JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-156">If you have to remove a fully trusted form, you can use the **UnregisterSolution** method of the **Application** object as shown in the following JScript and VBScript examples.</span></span> 
    
```js
    objIPApp = new ActiveXObject("InfoPath.Application"); 
    objIPApp.UnregisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
    objIPApp.Quit(); 
    objIPApp = null;
```

```vb
    Public Sub UninstallForm()
        Dim objIPApp As Object
        ' Create a reference to the Application object.
        Set objIPApp = CreateObject("InfoPath.Application")
        ' Unregister the InfoPath form template.
        objIPApp.UnregisterSolution ("C:\My Forms\MyFormTemplate.xsn")
        MsgBox ("The InfoPath form template has been unregistered.")
        Set objIPApp = Nothing
    End Sub
    
```

### <a name="digitally-signing-a-form-template-to-create-a-fully-trusted-form"></a><span data-ttu-id="8e6a3-157">Firmar digitalmente una plantilla de formulario para crear un formulario de plena confianza</span><span class="sxs-lookup"><span data-stu-id="8e6a3-157">Digitally Signing a Form Template to Create a Fully Trusted Form</span></span>

<span data-ttu-id="8e6a3-158">Firmar digitalmente una plantilla de formulario permite implementar una plantilla de formulario de plena confianza por correo electrónico o en un servidor Web, como un servidor que ejecuta Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-158">Digitally signing a form template enables you to deploy a fully trusted form template by email or on a Web server, such as a server that is running Microsoft SharePoint Foundation.</span></span> <span data-ttu-id="8e6a3-159">Realice los pasos de los tres procedimientos siguientes para crear un formulario de plena confianza mediante la especificación de plena confianza para el formulario, la estampación de una firma digital en él y, a continuación, su publicación.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-159">Use the steps in the following three procedures to make a form fully trusted by specifying full trust for the form, signing it digitally, and then publishing it.</span></span>
  
#### <a name="to-digitally-sign-a-form-template"></a><span data-ttu-id="8e6a3-160">Para firmar digitalmente una plantilla de formulario</span><span class="sxs-lookup"><span data-stu-id="8e6a3-160">To digitally sign a form template</span></span>

1. <span data-ttu-id="8e6a3-161">Abra el formulario en InfoPath Designer, haga clic en la pestaña **Archivo** y, a continuación, haga clic en **Opciones de formulario** en la ficha **Información**.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-161">Open the form in the InfoPath designer, click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
2. <span data-ttu-id="8e6a3-162">En el cuadro de diálogo **Opciones de formulario**, haga clic en la categoría **Seguridad y confianza**.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-162">In the **Form Options** dialog box, click the **Security and Trust** category.</span></span> 
    
3. <span data-ttu-id="8e6a3-163">Desactive **Determinar automáticamente el nivel de seguridad (recomendado)**.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-163">Clear the selection for **Automatically determine security level (recommended)**.</span></span>
    
4. <span data-ttu-id="8e6a3-164">Seleccione **Plena confianza (el formulario puede obtener acceso a los archivos y la configuración del equipo)**.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-164">Select **Full Trust (the form has access to files and settings on the user's computer)**.</span></span>
    
5. <span data-ttu-id="8e6a3-165">En **Firma de plantillas de formulario**, seleccione **Firmar esta plantilla de formulario**.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-165">Under **Form Template Signature**, select **Sign this form template**.</span></span>
    
6. <span data-ttu-id="8e6a3-166">Haga clic en **Seleccionar certificado** para seleccionar un certificado que previamente se haya descargado e instalado de una entidad emisora de certificados de confianza.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-166">Click **Select Certificate** to select a certificate that was previously downloaded and installed from a trusted certificate provider.</span></span> 
    
7. <span data-ttu-id="8e6a3-167">Haga clic en Aceptar dos veces para salir completamente.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-167">Click OK two times to exit completely.</span></span>
    
#### <a name="to-publish-the-form-template-to-a-sharepoint-document-library"></a><span data-ttu-id="8e6a3-168">Para publicar la plantilla de formulario en una biblioteca de documentos de SharePoint</span><span class="sxs-lookup"><span data-stu-id="8e6a3-168">To publish the form template to a SharePoint Document Library</span></span>

1. <span data-ttu-id="8e6a3-169">Haga clic en la pestaña **Archivo**, haga clic en **Publicar** y, a continuación, en **SharePoint Server**.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-169">Click the **File** tab, click **Publish**, and then click **SharePoint Server**.</span></span>
    
2. <span data-ttu-id="8e6a3-170">Siga las instrucciones del **Asistente para la publicación** para publicar la plantilla de formulario en una biblioteca de documentos de SharePoint nueva o existente.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-170">Follow the instructions in the **Publishing Wizard** to publish the form template to a new or existing SharePoint document library.</span></span> 
    
#### <a name="to-a-create-a-form-that-is-based-on-your-fully-trusted-digitally-signed-form-template"></a><span data-ttu-id="8e6a3-171">Para crear un formulario basado en la plantilla de formulario de plena confianza, firmada digitalmente</span><span class="sxs-lookup"><span data-stu-id="8e6a3-171">To a create a form that is based on your fully trusted, digitally signed form template</span></span>

1. <span data-ttu-id="8e6a3-172">En la biblioteca de documentos de SharePoint, haga clic en **Rellenar el formulario**.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-172">In the SharePoint document library, click **Fill Out the Form**.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="8e6a3-p114">[!NOTA] Una vez publicada la plantilla de formulario en una biblioteca de documentos de SharePoint mediante el **Asistente para la publicación**, la plantilla no se mostrará como un elemento de la biblioteca de formularios. Cuando cree un formulario en esa biblioteca de documentos, la plantilla se usará de forma predeterminada como la plantilla para el nuevo formulario.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p114">After publishing the form template to a SharePoint document library using the **Publishing Wizard**, the template is not displayed as an item in the form library. When you create a form in that document library, the template will be used by default as the template for the new form.</span></span> 
  
2. <span data-ttu-id="8e6a3-p115">Si la plantilla de formulario predeterminada se firmó digitalmente, InfoPath mostrará una advertencia de seguridad sobre la plantilla de formulario firmada digitalmente. Seleccione **Confiar siempre en los archivos de este editor y abrirlos automáticamente** y, a continuación, haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p115">If the default form template was digitally signed, InfoPath displays a security warning about the digitally signed form template. Select **Always trust files from this publisher and open them automatically**, and then click **Open**.</span></span>
    
## <a name="using-a-fully-trusted-form"></a><span data-ttu-id="8e6a3-177">Usar un formulario de plena confianza</span><span class="sxs-lookup"><span data-stu-id="8e6a3-177">Using a Fully Trusted Form</span></span>

<span data-ttu-id="8e6a3-p116">Usar un formulario de plena confianza es muy similar a usar un formulario estándar. Las únicas diferencias significativas son que el formulario puede tener acceso a recursos restringidos y que ya no se mostrarán advertencias.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p116">Using a fully trusted form is very similar to using a standard form. The only significant differences are that the form can access restricted resources and warnings will no longer be displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8e6a3-p117">[!NOTA] Para permitir que InfoPath use un formulario de plena confianza, los usuarios deben asegurarse de que la casilla de verificación **Permitir que se ejecuten en mi equipo formularios de plena confianza** está activada en la categoría **Editores de confianza** del cuadro de diálogo **Centro de confianza**. Para abrir el cuadro de diálogo **Centro de confianza**, haga clic en la pestaña **Archivo**, en **Opciones** (debajo de la pestaña **InfoPath**), en **Centro de confianza** y, a continuación, en **Configuración del Centro de confianza**.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p117">To enable InfoPath to use a fully trusted form, users must ensure that the **Allow fully trusted forms to run on my computer** check box is selected on the **Trusted Publishers** category of the **Trust Center** dialog box. To open the **Trust Center** dialog box, click the **File** tab, click **Options** (below the **InfoPath** tab), click **Trust Center**, and then click **Trust Center Settings**.</span></span> 
  
<span data-ttu-id="8e6a3-182">Se puede abrir un formulario de plena confianza en InfoPath desde el cuadro de diálogo **Rellenar un formulario**.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-182">A fully trusted form can be opened in InfoPath from the **Fill Out a Form** dialog box.</span></span> 
  
<span data-ttu-id="8e6a3-183">El cuadro de diálogo **Rellenar un formulario** se abre al hacer clic en **Más formularios** en el panel de tareas **Rellenar un formulario** o al hacer clic en **Rellenar un formulario** en el menú **Archivo**.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-183">The **Fill Out a Form** dialog box opens when you click **More Forms** in the **Fill Out a Form** task pane, or you click **Fill Out a Form** on the **File** menu.</span></span> 
  
### <a name="making-changes-to-a-fully-trusted-form"></a><span data-ttu-id="8e6a3-184">Realizar cambios en un formulario de plena confianza</span><span class="sxs-lookup"><span data-stu-id="8e6a3-184">Making Changes to a Fully Trusted Form</span></span>

<span data-ttu-id="8e6a3-p118">Si solo tiene que realizar cambios en el archivo .xsn, puede hacer que los usuarios reemplacen sus archivos .xsn existentes con el nuevo, después de que se realicen los cambios. No tendrán que volver a instalarlo mediante un programa de instalación personalizado.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p118">If you only have to make changes to the .xsn file, you can have users replace their existing .xsn file with the new one after the changes are made. They will not have to reinstall it by using a custom installation program.</span></span>
  
<span data-ttu-id="8e6a3-187">Sin embargo, si realiza cambios en los archivos de formulario que contiene el archivo .xsn, deberá volver a empaquetar los archivos, como se explicó anteriormente y, a continuación, pedir a los usuarios que vuelvan a instalar el formulario de plena confianza.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-187">However, if you are making changes to the form files that the .xsn file contains, you must repackage the files, as explained earlier, and then have users reinstall the fully trusted form.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8e6a3-188">El mejor enfoque es volver a guardar la plantilla de formulario en formato .xsn desde InfoPath Designer y, a continuación, seguir los pasos de este artículo para crear un formulario de plena confianza.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-188">The best approach is to save the form template back to the .xsn format from the InfoPath designer, and then follow the steps in this article to create a fully trusted form.</span></span> 
  
## <a name="conclusion"></a><span data-ttu-id="8e6a3-189">Conclusión</span><span class="sxs-lookup"><span data-stu-id="8e6a3-189">Conclusion</span></span>

<span data-ttu-id="8e6a3-p119">En función de los requisitos empresariales y las necesidades de los usuarios, es posible que tenga que crear un formulario con un conjunto de permisos superior al del formulario de InfoPath estándar. InfoPath permite modificar un formulario de modo que pueda obtener acceso a los recursos del sistema y a otros recursos externos que no estén marcados como seguros para scripting. Puede hacerlo manualmente, mediante la modificación de los archivos de formulario que contiene una plantilla de formulario y la ejecución de un script de instalación, o mediante la firma digital de la plantilla de formulario.</span><span class="sxs-lookup"><span data-stu-id="8e6a3-p119">Depending on your business requirements and the needs of your users, you may have to create a form that has a higher set of permissions than the standard InfoPath form. InfoPath provides the ability to modify a form so that it can access system resources and other external resources that are not marked as safe for scripting. This can be done manually by making modifications to the form files that a form template contains and running an installation script, or by digitally signing the form template.</span></span>
  

