---
title: Crear un complemento COM para agregar características personalizadas a InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007, creación de complementos com, InfoPath 2007, adición de características personalizadas, complementos COM [InfoPath 2007]
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath admite complementos COM para extender la experiencia de usuario de edición de formularios. Aunque la compatibilidad con complementos COM se agregó por primera vez en InfoPath, otras aplicaciones de Office, como Microsoft Office Word y Microsoft Office Excel, han admitido complementos COM desde Office 2000.
ms.openlocfilehash: f8dd16b161c4ea862cf3b15e56e26a2547c1fc4c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303790"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Crear un complemento COM para agregar características personalizadas a InfoPath

Microsoft InfoPath admite complementos COM para extender la experiencia de usuario de edición de formularios. Aunque la compatibilidad con complementos COM se agregó por primera vez en InfoPath, otras aplicaciones de Office, como Microsoft Office Word y Microsoft Office Excel, han admitido complementos COM desde Office 2000.
  
La compatibilidad con complementos COM en InfoPath está disponible para el entorno de edición de formularios. El entorno de diseño de formularios no se puede extender mediante el uso de complementos COM.
  
## <a name="the-idtextensibility2-interface"></a>La interfaz IDTExtensibility2

El entorno de edición de InfoPath proporciona compatibilidad con la interfaz **IDTExtensibility2** , que deben implementar los desarrolladores de complementos com. **IDTExtensibility2** es un objeto de interfaz dual que proporciona cinco métodos que actúan como eventos dentro del entorno de edición. Estos métodos permiten que el complemento COM responda a las condiciones de inicio y cierre del entorno, que se enumeran en la tabla siguiente. 
  
|**Interfaz**|**Descripción**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal personalizado () as Variant)** <br/> |Se produce cuando un complemento se carga o descarga en el entorno.  <br/> |
|**OnBeginShutdown (ByVal Custom () as Variant)** <br/> |Se produce cuando se está cerrando el entorno.  <br/> |
|**OnConnection (ByVal aplicación As Object, ByVal ConnectMode as ext_ConnectMode, ByVal AddInInst As Object, ByVal Custom () as Variant)** <br/> |Se produce cuando se carga un complemento en el entorno.  <br/> |
|**OnDisconnection (ByVal RemoveMode as ext_DisconnectMode, ByVal Custom () as Variant)** <br/> |Se produce cuando se descarga un complemento del entorno.  <br/> |
|**OnStartupComplete (ByVal Custom () as Variant)** <br/> |Se produce cuando el entorno ha terminado de iniciarse.  <br/> |
   
## <a name="registering-com-add-ins"></a>Registrar complementos COM

Todas las aplicaciones de Office, incluidas InfoPath, usan el registro para enumerar los complementos de la colección de complementos COM, para almacenar el estado de conexión y almacenar la información de carga de demanda o inicio. Para los complementos COM de InfoPath, el nombre de cada complemento aparece en la siguiente clave:
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Para los complementos COM instalados para que los usen todos los usuarios del equipo cliente, la clave del registro se encuentra en el subárbol del registro HKLM:
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
El nombre de la clave del registro corresponde al **ProgIdAttribute** del complemento y contiene los siguientes valores. 
  
|**Name**|**Type**|**Descripción**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**String** <br/> |Nombre que se muestra en el cuadro de diálogo **Complementos com** y que aparece en la **** lista de la página complementos del **centro de confianza**.  <br/> |
|**Descripción** <br/> |**String** <br/> |La cadena que se muestra cuando se selecciona el complemento en el centro de **confianza**.  <br/> |
|**LoadBehavior** <br/> |**ÚLTIMAS** <br/> |Especifica la forma en que se carga el complemento COM. El valor puede ser una combinación de 0, 1, 2, 8 y 16. Consulte la tabla siguiente para obtener más información.  <br/> |
   
El valor **DWORD** para **LoadBehavior** debe contener un valor que describa cómo se carga el complemento com en el entorno de edición. El valor puede ser de la tabla siguiente o una combinación de valores de la tabla. Por ejemplo, un complemento COM creado en Visual Studio 2005 tendrá un **LoadBehavior** de "3" cargado en el inicio de la aplicación y estará conectado. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|comprendi  <br/> |Desconectado. El complemento se muestra como inactivo en el cuadro de diálogo **complemento com** .  <br/> |
|1  <br/> |Asociada. El complemento se muestra como activo en el cuadro de diálogo **complemento com** .  <br/> |
|segundo  <br/> |Cargar al inicio. El complemento se carga y se conecta cuando se inicia la aplicación host.  <br/> |
|8,5  <br/> |Cargar a petición. El complemento se carga y se conecta cuando la aplicación host lo requiere, por ejemplo, cuando un usuario hace clic en un botón que usa funcionalidad en el complemento.  <br/> |
|16  <br/> |Conectar la primera vez. El complemento se cargará y se conectará la primera vez que el usuario ejecute la aplicación host después de registrar el complemento.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Creación de un complemento COM administrado con Visual Studio 2005 o Visual Studio 2008

Para crear un complemento COM administrado con Microsoft Visual Studio 2005 o Visual Studio 2008, cree un proyecto de complemento compartido como se indica a continuación: 
  
1. Inicie Visual Studio.
    
2. En el menú **Archivo**, haga clic en **Nuevo proyecto**.
    
3. En el panel **tipos de proyecto** del cuadro de diálogo **nuevo proyecto** , haga clic en la carpeta **otros tipos de proyectos** y, a continuación, haga clic en extensibilidad. ****
    
4. En el panel **plantillas** , haga clic en **complemento compartido**.
    
5. En el cuadro **nombre** , escriba un nombre para el proyecto. 
    
6. En el cuadro **Ubicación** , escriba una ruta de acceso de carpeta o haga clic en **examinar** y seleccione una ruta de acceso de carpeta y, a continuación, haga clic en **Aceptar**. Aparece el **Asistente para complementos** compartidos. 
    
7. Haga clic en **siguiente** en el **Asistente para complementos**compartidos. Aparece la página **seleccionar un lenguaje de programación** . 
    
8. Haga clic en **crear un complemento con Visual Basic**y, a continuación, haga clic en **siguiente**. Aparece la página **Seleccione una aplicación host** . 
    
9. Desactive las casillas situadas junto a cada aplicación excepto **Microsoft InfoPath**y, a continuación, haga clic en **siguiente**. Aparecerá la página **Escriba un nombre y una descripción** . 
    
10. En el cuadro **¿cuál es el nombre de su complemento** ?, escriba el nombre del complemento com. 
    
11. En el cuadro **¿cuál es la descripción de su complemento** ?, escriba la descripción del complemento com y haga clic en **siguiente**. Aparece la página **Elija las opciones del complemento** . 
    
12. Active las casillas **me gustaría que mi complemento se cargue cuando la aplicación host se cargue** y **mi complemento debe estar disponible para todos los usuarios del equipo en el que se instaló, no solo para la persona que lo instala** . 
    
13. Haga clic en **siguiente** para revisar la página de **Resumen** y, a continuación, haga clic en **Finalizar**.
    
Una vez que Visual Studio ha creado el proyecto, verá dos proyectos en la ventana Explorador de soluciones. El primer proyecto es el proyecto para el complemento COM; el segundo proyecto es un proyecto de instalación para implementar el complemento COM. El **Asistente** para complementos compartidos sólo inserta una referencia a la **biblioteca de objetos de Microsoft Office 14,0**, por lo que es necesario insertar una referencia a la biblioteca de objetos de InfoPath mediante los pasos siguientes:
  
1. Haga doble clic en **mi proyecto** para mostrar las propiedades del proyecto del complemento. Haga clic en la pestaña **referencias** para mostrar las referencias agregadas automáticamente al proyecto. 
    
2. Haga clic en el botón **Agregar** para mostrar el cuadro de diálogo **Agregar referencia** . 
    
3. En la pestaña **com** , haga doble clic en **biblioteca de tipos de Microsoft. InfoPath 2,0**y, a continuación, haga clic en **Aceptar**.
    
4. Al agregar una referencia a la **biblioteca de tipos de Microsoft InfoPath 3,0** , también se agregan referencias a tres ensamblados que deben quitarse: **ADODB**, **MSHTML**y **MSXML2**. En el **Explorador de soluciones** , en **referencias**, haga clic con el botón secundario en cada una de estas referencias y, a continuación, haga clic en **quitar**.
    
## <a name="viewing-the-registry-settings"></a>Visualización de la configuración del registro

Para ver la configuración del registro que se creará cuando se instale el complemento COM, siga estos pasos:
  
1. Haga clic con el botón secundario en el nodo raíz del proyecto de instalación en el **Explorador de soluciones**, haga clic en **Ver**, **Editor**y, a continuación, en **registro**.
    
2. En el panel izquierdo, haga clic en el signo más para expandir **HKEY_LOCAL_MACHINE**, **software**, **Microsoft**, **InfoPath**y **AddIns**.
    
3. Haga clic en el nombre correspondiente al **ProgID**del proyecto de complemento compartido.
    
Para cambiar cualquiera de estas propiedades, haga clic con el botón secundario en la propiedad, haga clic en **ventana Propiedades**y cambie el cuadro **valor** en la **ventana Propiedades**.
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>ComPilar y distribuir el complemento compartido

Para compilar el complemento COM administrado para realizar pruebas en el equipo en el que se desarrolló el proyecto de complemento compartido, haga clic con el botón secundario en el nodo raíz del proyecto de complemento compartido en el explorador de soluciones y haga clic en generar. Si el proyecto se compila sin errores, puede iniciar el entorno de edición de InfoPath y empezar a usar el complemento COM administrado. Si tiene una instancia de InfoPath en ejecución, ciérrela antes de compilar el proyecto. También es posible que sea necesario abrir el cuadro de diálogo de complementos COM para comprobar que el complemento COM está registrado. Para abrir el cuadro de diálogo de complementos COM, siga estos pasos:
  
1. Abra el entorno de edición de InfoPath. La forma más sencilla de hacerlo es abrir una plantilla de formulario existente, que creará un nuevo formulario basado en esa plantilla de formulario.
    
2. Haga clic en **centro de confianza** en el menú **herramientas** . 
    
3. Haga clic **** en la categoría complementos a la izquierda. 
    
4. En la sección **administrar** situada cerca de la parte inferior del cuadro de diálogo **centro de confianza** , seleccione complementos **com** en la lista y haga clic en el botón **ir** . 
    
5. En el cuadro de diálogo **Complementos com** , verá el nombre del complemento que ha creado recientemente y debe haber una casilla de verificación junto a él. Si no hay ninguna casilla de verificación junto a ella, el complemento COM no se pudo cargar debido a un error, que se mostrará en la sección **comportamiento de carga** del cuadro de diálogo. 
    
Para compilar el complemento COM administrado para usarlo en un equipo distinto del equipo en el que se desarrolló el proyecto de complemento compartido, debe seguir pasos adicionales para proteger el código. Para obtener información sobre cómo proteger proyectos de complementos comPartidos para usarlos en otros equipos, vea los tres artículos siguientes:
  
- [Implementación de complementos COM administrados en Office XP](https://go.microsoft.com/fwlink/?LinkID=73473)
  
- [Uso de la solución de corrección para complementos COM para implementar complementos COM administrados en Office XP](https://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Aislamiento de extensiones de Office con el Asistente para la corrección de COM](https://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> Si no se aísla el complemento COM, es posible que se produzcan pérdidas de memoria e inestabilidad de la aplicación. 
  
> [!NOTE]
> Si .NET Framework u otros ensamblados necesarios del proyecto de instalación aún no están instalados en los equipos de destino, es posible que el archivo. msi no se instale correctamente. Además, no puede distribuir el archivo. msi y, a continuación, intentar instalar el archivo. msi. También debe distribuir los demás archivos auxiliares en la misma carpeta que el archivo. msi original generado por Visual Studio. 
  
## <a name="coding-in-the-com-add-in"></a>Codificación en el complemento COM

Los eventos de aplicación que se producen en el entorno de edición de formularios de InfoPath se pueden capturar mediante un complemento COM. El complemento COM puede usar los siguientes eventos del objeto [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) para responder a las acciones del usuario: 
  
|**Event**|**Descripción**|
|:-----|:-----|
|[NewXDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx) Click  <br/> |Se produce cuando se crea un nuevo formulario.  <br/> |
|[Salir](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx) Click  <br/> |Se produce cuando el usuario sale de InfoPath.  <br/> |
|[WindowActivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx) Click  <br/> |Este evento se produce cuando se activa cualquier ventana de documento.  <br/> |
|[WindowDeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx) Click  <br/> |Este evento se produce cuando se desactiva cualquier ventana de documento.  <br/> |
|[Windows](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx) Click  <br/> |Se produce cuando se mueve una ventana de documento o se cambia su tamaño.  <br/> |
|[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx) Click  <br/> |Este evento se produce antes de que se cierre cualquier documento.  <br/> |
|[XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx) Click  <br/> |Se produce inmediatamente antes de que se imprima un documento abierto.  <br/> |
|[XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx) Click  <br/> |Se produce inmediatamente antes de que se guarde un documento abierto.  <br/> |
|[XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx) Click  <br/> |Se produce cuando se crea un nuevo formulario, cuando se abre un formulario existente o cuando otro formulario se convierte en el formulario activo.  <br/> |
|[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx) Click  <br/> |Este evento se produce al abrir un documento.  <br/> |
   
Para capturar estos eventos en el complemento COM, debe declarar las siguientes variables de nivel de clase en la clase **Connect** : 
  
```vb
InfoPathApplication = DirectCast( _
   application, Microsoft.Office.Interop.InfoPath._Application3)
InfoPathApplicationEvents = DirectCast( _
   InfoPathApplication.Events, _
   Microsoft.Office.Interop.InfoPath.ApplicationEvents)
```

```cs
InfoPathApplication =
   (Microsoft.Office.Interop.InfoPath._Application3)application;
InfoPathApplicationEvents =
   (Microsoft.Office.Interop.InfoPath.ApplicationEvents)
   InfoPathApplication.Events;
```

La primera línea convierte el **objeto** de aplicación genérica recibido por el complemento en el objeto [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) . La segunda línea convierte la propiedad [Events](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) del objeto **_Application3** (representada por la variable **InfoPathApplication** ) en el objeto [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) . 
  
Para crear controladores de eventos, seleccione **InfoPathApplicationEvents** en el cuadro de lista desplegable **nombre de clase** en la parte superior de la ventana de Visual Studio y, a continuación, seleccione el evento que desea controlar en el cuadro de lista desplegable **nombre de método** en la parte superior del visual. Ventana de estudio. Por ejemplo, si necesita controlar el momento en que se guarda un formulario, puede controlar el evento **XDocumentBeforeSave** . Al seleccionar **XDocumentBeforeSave** en la lista desplegable **nombre de método** , se inserta automáticamente el siguiente procedimiento: 
  
```vb
Private Sub InfoPathApplicationEvents_XDocumentBeforeSave( _
   ByVal pDocument As Microsoft.Office.Interop.InfoPath._XDocument, _
   ByRef pfCancel As Boolean) _
   Handles InfoPathApplicationEvents.XDocumentBeforeSave
End Sub
```

```cs
private void InfoPathApplicationEvents_XDocumentBeforeSave(
   Microsoft.Office.Interop.InfoPath._XDocument pDocument, ref bool pfCancel)
{
}

```

Cualquiera de los eventos del objeto **ApplicationEvents** puede ser controlado por el complemento com mediante el mismo método. 
  
## <a name="see-also"></a>Vea también

- [Creación de un complemento COM de Microsoft Office 2000](https://go.microsoft.com/fwlink/?LinkID=73468) 
- [Crear complementos COM administrados de Office con Visual Studio .NET](https://go.microsoft.com/fwlink/?LinkID=73470)
- [Trabajar con los procedimientos de evento IDTExtensibility2](https://go.microsoft.com/fwlink/?LinkID=73471)
- [ComPilar un complemento COM de Office con Visual Basic .NET](https://go.microsoft.com/fwlink/?LinkID=73469)
- [Crear un complemento COM de Office con Visual C# .NET](https://support.microsoft.com/en-us/help/302901/how-to-build-an-office-com-add-in-by-using-visual-c-net)
- [Crear complementos de InfoPath 2007 con las herramientas de Visual Studio 2005 para Office System SE](https://msdn.microsoft.com/library/bb968857%28office.12%29.aspx)

