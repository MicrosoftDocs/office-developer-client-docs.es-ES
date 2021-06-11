---
title: Descripción de los formularios de plena confianza
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64d62990-6275-edef-c639-b6ba8d10c38c
description: InfoPath proporciona la capacidad de crear formularios de plena confianza, que son formularios que tienen permisos de seguridad mayores y pueden tener acceso a recursos del sistema y otros componentes en el equipo de un usuario. En este artículo se explica qué es y por qué se usa un formulario de plena confianza, así como la creación de un formulario de plena confianza mediante la conversión y el registro manual de un formulario estándar, o mediante la firma digital de un formulario estándar.
ms.openlocfilehash: 04560e0c844d6a6ff681fd366ca7da2e4db36ba1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430395"
---
# <a name="understanding-fully-trusted-forms"></a>Descripción de los formularios de plena confianza

InfoPath proporciona la capacidad de crear formularios de plena confianza, que son formularios que tienen permisos de seguridad mayores y pueden tener acceso a recursos del sistema y otros componentes en el equipo de un usuario. En este artículo se explica qué es y por qué se usa un formulario de plena confianza, así como la creación de un formulario de plena confianza mediante la conversión y el registro manual de un formulario estándar, o mediante la firma digital de un formulario estándar.

Las plantillas de formulario de InfoPath se pueden implementar con distintos niveles de seguridad. El nivel que se use dependerá del nivel de acceso a los recursos externos que vaya a tener el formulario. De forma predeterminada, las plantillas de formulario de InfoPath tienen restringido el acceso a los recursos del sistema y no se les permite usar ningún componente de software que no esté marcado como seguro para scripting. Sin embargo, este comportamiento se puede cambiar para que un formulario pueda tener acceso a los recursos del sistema y a otros recursos externos, incluidos los componentes de software que no están marcados como seguros para scripting.
  
Para que se pueda usar un formulario, InfoPath debe tener acceso a la plantilla de formulario en la que se basa el formulario. Cuando se crea una plantilla de formulario, InfoPath crea una entrada en el archivo de definición de formulario (.xsf) que contiene la dirección URL de la ubicación de la plantilla de formulario. Un formulario basado en URL se denomina *de espacio aislado*. Cuando un usuario lo rellena, el formulario se agrega a una memoria caché local y se le niega el acceso a los recursos del sistema. Este tipo de formulario hereda sus permisos del dominio en el que se abre. 
  
Sin embargo, puede modificar un formulario para que se base en un nombre de recursos uniforme (URN), que permite el acceso a los recursos del sistema. Los formularios de este tipo se denominan *de plena confianza*. 
  
## <a name="why-use-a-fully-trusted-form"></a>¿Por qué usar un formulario de plena confianza?

Los formularios de plena confianza tienen un mejor conjunto de permisos que los formularios de espacio aislado. Por ejemplo, pueden contener código de programación que use objetos externos para obtener acceso a los recursos del sistema, pueden usar componentes de software o controles de Microsoft ActiveX que no estén marcados como seguros para scripting y pueden usar lógica empresarial personalizada proporcionada por ensamblados .NET.
  
Además, algunos miembros del modelo de objetos de InfoPath se establecen en el nivel de seguridad 3, lo que significa que solo pueden usarse en un formulario de plena confianza. Por ejemplo, para obtener acceso al objeto Microsoft Office **CommandBars**, se puede usar la propiedad [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) de la clase [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) de InfoPath para establecer una referencia hacia él. Debido a que esta propiedad está establecida en el nivel de seguridad 3, no se puede usar en un formulario que no sea de plena confianza. 
  
> [!NOTE]
> [!NOTA] El uso de la propiedad [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) de la clase [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) , o cualquier otro miembro del modelo de objetos con un nivel de seguridad 3, en un formulario que no sea de plena confianza devolverá un error de "permiso denegado". 
  
## <a name="what-makes-a-form-fully-trusted"></a>¿Cómo hacer que un formulario sea de plena confianza?

Se requieren las siguientes acciones, en las que participan tanto la interfaz de usuario de InfoPath como los archivos de formulario, para crear y usar un formulario de plena confianza:
  
- Habilitar InfoPath para permitir el uso de formularios de plena confianza en la categoría **Editores de confianza** del cuadro de diálogo **Centro de confianza**. Esta opción debe estar habilitada para que los usuarios puedan abrir formularios de plena confianza. 
    
- Registrar el formulario de plena confianza en el equipo de destino usando el método **RegisterSolution** del objeto **Application** de InfoPath. 
    
## <a name="creating-a-fully-trusted-form"></a>Creación de un formulario de plena confianza

- Puede crear el formulario manualmente, lo que implica modificar directamente algunos de los archivos del formulario.
    
- Puede firmar digitalmente la plantilla de formulario.
    
### <a name="manually-creating-a-fully-trusted-form"></a>Creación manual de un formulario de plena confianza

#### <a name="to-manually-create-a-fully-trusted-form"></a>Para crear manualmente un formulario de plena confianza

1. Realice una copia de seguridad de la plantilla de formulario que desea que sea de plena confianza.
    
2. Abra la plantilla de formulario en InfoPath.
    
3. Guarde los archivos de origen del formulario en una carpeta del disco duro; para ello, haga clic en la pestaña **Archivo**, en **Publicar** y, a continuación, en **Exportar archivos de origen**.
    
4. Especifique la carpeta en la que desea guardar los archivos de origen del formulario, haga clic en **Aceptar** y, a continuación, salga de InfoPath Designer.
    
5. En la carpeta en la que extrajo los archivos de formulario, abra el archivo de definición de formulario (.xsf), llamado  `manifest.xsf` de forma predeterminada, en un editor de texto como Bloc de notas de Microsoft. 
    
6. Agregue los siguientes atributos al elemento **xDocumentClass** en el archivo .xsf: 
   
   `requireFullTrust="yes"`<br/>
   `name="urn:MyForm:MyCompany`

   > [!NOTE]
   > [!NOTA] Los valores usados para el URN pueden ser cualquier tipo de valor de cadena, siempre que este valor sea único. Debe haber al menos dos valores después del prefijo y estos `urn:` valores deben estar separados por dos puntos. Además, el URN no debe exceder los 255 caracteres. 
  
7. Guarde y cierre el archivo .xsf y, a continuación, abra el archivo de plantilla XML (.xml) llamado  `Template.xml` de forma predeterminada, en un editor de texto como Bloc de notas. 
    
8. Quite el atributo **href** de la instrucción de procesamiento  `mso-infoPathSolution` y reemplácelo con el mismo atributo **name** que usó en el paso 6 para el archivo .xsf. 
    
   > [!NOTE]
   > [!NOTA] Los valores del URN usados para el atributo **name** deben ser los mismos tanto en el archivo .xsf como en el archivo de plantilla XML. 
  
9. Guarde y cierre el archivo de plantilla XML.
    
10. Vuelva a empaquetar los archivos en el formato CAB .xsn con una herramienta como makecab.exe.
    
    > [!NOTE]
    > [!NOTA] Si bien el diseñador de formularios de InfoPath admite volver a empaquetar los archivos de formulario en un archivo .xsn, si lo hace, revertirá el formulario a un formulario basado en URL. Por esta razón, debe volver a empaquetar los archivos manualmente para evitar que se sobrescriban los cambios en los archivos de formulario. 
  
11. Cree un programa de instalación personalizado mediante el método **RegisterSolution** del objeto **Application** de InfoPath para instalar el formulario de plena confianza. Una forma fácil de hacerlo es crear un archivo de script que use las siguientes líneas de código (tanto en la sintaxis de Microsoft JScript como de VBScript): 
    
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
> [!NOTA] Si bien en este ejemplo se usa un archivo de script simple, también puede usar un mecanismo de instalación más eficaz los como archivos (.msi) de Microsoft Windows Installer. Sin embargo, asegúrese de usar el método **RegisterSolution** para instalar correctamente el formulario de plena confianza en el equipo de destino. Para obtener acceso al método **RegisterSolution** del objeto **Application** de InfoPath desde Visual Basic o Visual Studio, establezca una referencia a la Biblioteca de tipos de Microsoft InfoPath 3.0, proporcionada por IPEDITOR.dll que está instalado en la carpeta C:\Program Files\Microsoft Office\Office14. 
  
Si tiene que quitar un formulario de plena confianza, puede usar el método **UnregisterSolution** del objeto **Application** como se muestra en los siguientes ejemplos de JScript y VBScript. 
    
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

### <a name="digitally-signing-a-form-template-to-create-a-fully-trusted-form"></a>Firmar digitalmente una plantilla de formulario para crear un formulario de plena confianza

La firma digital de una plantilla de formulario permite implementar una plantilla de formulario de plena confianza por correo electrónico o en un servidor web, como un servidor que ejecuta Microsoft SharePoint Foundation. Realice los pasos de los tres procedimientos siguientes para crear un formulario de plena confianza mediante la especificación de plena confianza para el formulario, la estampación de una firma digital en él y, a continuación, su publicación.
  
#### <a name="to-digitally-sign-a-form-template"></a>Para firmar digitalmente una plantilla de formulario

1. Abra el formulario en InfoPath Designer, haga clic en la pestaña **Archivo** y, a continuación, haga clic en **Opciones de formulario** en la ficha **Información**. 
    
2. En el cuadro de diálogo **Opciones de formulario**, haga clic en la categoría **Seguridad y confianza**. 
    
3. Desactive **Determinar automáticamente el nivel de seguridad (recomendado)**.
    
4. Seleccione **Plena confianza (el formulario puede obtener acceso a los archivos y la configuración del equipo)**.
    
5. En **Firma de plantillas de formulario**, seleccione **Firmar esta plantilla de formulario**.
    
6. Haga clic en **Seleccionar certificado** para seleccionar un certificado que previamente se haya descargado e instalado de una entidad emisora de certificados de confianza. 
    
7. Haga clic en Aceptar dos veces para salir completamente.
    
#### <a name="to-publish-the-form-template-to-a-sharepoint-document-library"></a>Para publicar la plantilla de formulario en una biblioteca de documentos de SharePoint

1. Haga clic en la pestaña **Archivo**, haga clic en **Publicar** y, a continuación, en **SharePoint Server**.
    
2. Siga las instrucciones del **Asistente para la publicación** para publicar la plantilla de formulario en una biblioteca de documentos de SharePoint nueva o existente. 
    
#### <a name="to-a-create-a-form-that-is-based-on-your-fully-trusted-digitally-signed-form-template"></a>Para crear un formulario basado en la plantilla de formulario de plena confianza, firmada digitalmente

1. En la biblioteca de documentos de SharePoint, haga clic en **Rellenar el formulario**.
    
   > [!NOTE]
   > [!NOTA] Una vez publicada la plantilla de formulario en una biblioteca de documentos de SharePoint mediante el **Asistente para la publicación**, la plantilla no se mostrará como un elemento de la biblioteca de formularios. Cuando cree un formulario en esa biblioteca de documentos, la plantilla se usará de forma predeterminada como la plantilla para el nuevo formulario. 
  
2. Si la plantilla de formulario predeterminada se firmó digitalmente, InfoPath mostrará una advertencia de seguridad sobre la plantilla de formulario firmada digitalmente. Seleccione **Confiar siempre en los archivos de este editor y abrirlos automáticamente** y, a continuación, haga clic en **Abrir**.
    
## <a name="using-a-fully-trusted-form"></a>Usar un formulario de plena confianza

Usar un formulario de plena confianza es muy similar a usar un formulario estándar. Las únicas diferencias significativas son que el formulario puede tener acceso a recursos restringidos y que ya no se mostrarán advertencias.
  
> [!NOTE]
> [!NOTA] Para permitir que InfoPath use un formulario de plena confianza, los usuarios deben asegurarse de que la casilla de verificación **Permitir que se ejecuten en mi equipo formularios de plena confianza** está activada en la categoría **Editores de confianza** del cuadro de diálogo **Centro de confianza**. Para abrir el cuadro de diálogo **Centro de confianza**, haga clic en la pestaña **Archivo**, en **Opciones** (debajo de la pestaña **InfoPath**), en **Centro de confianza** y, a continuación, en **Configuración del Centro de confianza**. 
  
Se puede abrir un formulario de plena confianza en InfoPath desde el cuadro de diálogo **Rellenar un formulario**. 
  
El cuadro de diálogo **Rellenar un formulario** se abre al hacer clic en **Más formularios** en el panel de tareas **Rellenar un formulario** o al hacer clic en **Rellenar un formulario** en el menú **Archivo**. 
  
### <a name="making-changes-to-a-fully-trusted-form"></a>Realizar cambios en un formulario de plena confianza

Si solo tiene que realizar cambios en el archivo .xsn, puede hacer que los usuarios reemplacen sus archivos .xsn existentes con el nuevo, después de que se realicen los cambios. No tendrán que volver a instalarlo mediante un programa de instalación personalizado.
  
Sin embargo, si realiza cambios en los archivos de formulario que contiene el archivo .xsn, deberá volver a empaquetar los archivos, como se explicó anteriormente y, a continuación, pedir a los usuarios que vuelvan a instalar el formulario de plena confianza.
  
> [!NOTE]
> El mejor enfoque es volver a guardar la plantilla de formulario en formato .xsn desde InfoPath Designer y, a continuación, seguir los pasos de este artículo para crear un formulario de plena confianza. 
  
## <a name="conclusion"></a>Conclusión

En función de los requisitos empresariales y las necesidades de los usuarios, es posible que tenga que crear un formulario con un conjunto de permisos superior al del formulario de InfoPath estándar. InfoPath permite modificar un formulario de modo que pueda obtener acceso a los recursos del sistema y a otros recursos externos que no estén marcados como seguros para scripting. Puede hacerlo manualmente, mediante la modificación de los archivos de formulario que contiene una plantilla de formulario y la ejecución de un script de instalación, o mediante la firma digital de la plantilla de formulario.
  

