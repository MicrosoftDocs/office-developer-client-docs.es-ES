---
title: Crear un complemento COM para agregar características personalizadas a InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007, creación de complementos com, InfoPath 2007, agregar características personalizadas, complementos de COM [InfoPath 2007]
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath admite complementos COM para ampliar la experiencia de usuario de edición de formularios. Aunque la compatibilidad con complementos COM en primer lugar se agregan en InfoPath, otras aplicaciones de Office, como Microsoft Office Word y Microsoft Office Excel, han admitido complementos COM desde Office 2000.
ms.openlocfilehash: 4c70dfb71cf7b15a0978b4567ffac02a8ba524c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815767"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Crear un complemento COM para agregar características personalizadas a InfoPath

Microsoft InfoPath admite complementos COM para ampliar la experiencia de usuario de edición de formularios. Aunque la compatibilidad con complementos COM en primer lugar se agregan en InfoPath, otras aplicaciones de Office, como Microsoft Office Word y Microsoft Office Excel, han admitido complementos COM desde Office 2000.
  
Add-compatibilidad con COM en InfoPath está disponible para el entorno de edición de formularios. No se puede extender el entorno de diseño de formulario mediante el uso de complementos COM.
  
## <a name="the-idtextensibility2-interface"></a>La interfaz IDTExtensibility2

El entorno de edición proporciona compatibilidad para la interfaz **IDTExtensibility2** , que debe ser implementada por los programadores de complementos COM. **IDTExtensibility2** de InfoPath es un objeto de doble interfaz que proporciona cinco métodos que actúan como eventos en el entorno de edición. Estos métodos permiten el complemento COM responder a inicio y cierre las condiciones del entorno, que aparecen en la siguiente tabla. 
  
|**Interfaz**|**Descripción**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal custom() como Variant)** <br/> |Se produce cuando un complemento se carga o descarga en el entorno.  <br/> |
|**OnBeginShutdown (ByVal custom() como Variant)** <br/> |Se produce cuando se cierra el entorno.  <br/> |
|**OnConnection (ByVal Application As Object, ByVal ConnectMode As ext_ConnectMode, ByVal AddInInst As Object, ByVal custom() As Variant)** <br/> |Se produce cuando un complemento se carga en el entorno.  <br/> |
|**OnDisconnection (ByVal RemoveMode As ext_DisconnectMode, ByVal custom() As Variant)** <br/> |Se produce cuando un complemento se descarga desde el entorno.  <br/> |
|**OnStartupComplete (ByVal custom() como Variant)** <br/> |Se produce cuando el entorno ha terminado de iniciarse.  <br/> |
   
## <a name="registering-com-add-ins"></a>Registrar complementos COM

Todas las aplicaciones de Office, incluida InfoPath, utilizan el registro para complementos de lista en la colección de complementos COM, para almacenar el estado de conexión y para almacenar la información de carga de demanda o arranque. Para InfoPath complementos COM, el nombre de cada complemento aparece bajo la siguiente clave:
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Para los complementos COM instalan para su uso por todos los usuarios del equipo cliente, la clave del registro se encuentra en el subárbol del registro HKLM:
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
Nombre de la clave del registro corresponde a **ProgIdAttribute** del complemento y contiene los siguientes valores. 
  
|**Nombre**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**String** <br/> |El nombre que se muestra en el cuadro de diálogo **complementos COM** y aparecen en la página **complementos** del **Centro de confianza**.  <br/> |
|**Descripción** <br/> |**String** <br/> |La cadena que se muestra cuando el complemento está seleccionado en el **Centro de confianza**.  <br/> |
|**LoadBehavior** <br/> |**DWORD** <br/> |Especifica el modo en que COM Add-in está cargado. El valor puede ser una combinación de 0, 1, 2, 8 y 16. Consulte la tabla siguiente para obtener más información.  <br/> |
   
El valor **DWORD** de **LoadBehavior** debe contener un valor que describe cómo se carga COM Add-in en el entorno de edición. El valor puede ser desde la tabla siguiente, o una combinación de valores de la tabla. Por ejemplo, un COM Add-in creado en Visual Studio 2005 tendrá un **LoadBehavior** de "3" cargar al inicio de la aplicación y estar conectado. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Desconectado. El complemento se muestra como inactivo en el cuadro de diálogo **complemento COM** .  <br/> |
|1  <br/> |Conectado. El complemento se muestra como activo en el cuadro de diálogo **complemento COM** .  <br/> |
|2  <br/> |Cargar al inicio. El complemento está cargado y conectado cuando se inicia la aplicación host.  <br/> |
|8  <br/> |Cargar a petición. El complemento está cargado y conectado cuando la aplicación host lo requiere, por ejemplo, cuando un usuario hace clic en un botón que utiliza funcionalidad en el complemento.  <br/> |
|16  <br/> |Conectar por primera vez. El complemento se carga y conecta la primera vez que el usuario ejecuta la aplicación host después de registrar el complemento.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Creación de un complemento COM administrado con Visual Studio 2005 o Visual Studio 2008

Para crear un complemento COM complemento mediante Microsoft Visual Studio 2005 o Visual Studio 2008, cree un proyecto de complemento compartido de la siguiente forma: 
  
1. Inicie Visual Studio.
    
2. En el menú **Archivo**, haga clic en **Nuevo proyecto**.
    
3. En el panel **Tipos de proyecto** del cuadro de diálogo **Nuevo proyecto** , haga clic en la carpeta de **Otros tipos de proyectos** y, a continuación, haga clic en **extensibilidad**.
    
4. En el panel **plantillas** , haga clic en **Complemento compartido**.
    
5. En el cuadro **nombre** , escriba un nombre para el proyecto. 
    
6. En el cuadro **ubicación** , escriba una ruta de acceso de carpeta o haga clic en **Examinar** y seleccione una ruta de acceso de la carpeta y, a continuación, haga clic en **Aceptar**. Aparecerá el **Shared Asistente para complementos** . 
    
7. Haga clic en **siguiente** en el **Asistente para agregar compartidos**. Aparecerá la página **Seleccione un lenguaje de programación** . 
    
8. Haga clic en **crear un complemento utilizando Visual Basic**y, a continuación, haga clic en **siguiente**. Aparecerá la página **Seleccione una aplicación Host** . 
    
9. Desactive las casillas junto a cada aplicación exceptuando **Microsoft InfoPath**y, a continuación, haga clic en **siguiente**. Aparece la página **Especifique un nombre y una descripción** . 
    
10. En el cuadro **¿Qué es el nombre de su complemento** , escriba el nombre de su COM Add-in. 
    
11. En el cuadro **¿Qué es la descripción de su complemento** , escriba la descripción para su COM Add-in y haga clic en **siguiente**. Aparecerá la página **Elija las opciones del complemento** . 
    
12. Comprobar los cuadros de **Mi complemento debe estar disponible para todos los usuarios del equipo en el que se instaló, no sólo para la persona que lo instala** y **me gustaría que mi complemento se cargue cuando lo haga la aplicación host** . 
    
13. Haga clic en **siguiente** para revisar la página de **Resumen** y, a continuación, haga clic en **Finalizar**.
    
Una vez creado el proyecto por Visual Studio, verá dos proyectos en la ventana Explorador de soluciones. El primer proyecto es el proyecto para el COM Add-in; el segundo proyecto es un proyecto de instalación para la implementación de COM Add-in. El **Shared Asistente para complementos** sólo inserta una referencia a la **Biblioteca de objetos de Microsoft Office 14.0**, por lo que es necesario insertar una referencia a la biblioteca de objetos de InfoPath mediante los pasos siguientes:
  
1. Haga doble clic en **Mi proyecto** para mostrar las propiedades del proyecto de complemento. Haga clic en la ficha **referencias** para que se muestren las referencias agregadas automáticamente al proyecto. 
    
2. Haga clic en el botón **Agregar** para mostrar el cuadro de diálogo **Agregar referencia** . 
    
3. En la ficha **COM** , haga doble clic en la **Biblioteca de tipos Microsoft.InfoPath 2.0**y haga clic en **Aceptar**.
    
4. Agregar una referencia a la **Biblioteca de tipos de Microsoft InfoPath 3.0** , también agrega referencias a tres ensamblados que se deben quitar: **ADODB**, **MSHTML**y **MSXML2**. En **El Explorador de soluciones** , en **referencias**, haga clic en cada una de estas referencias y, a continuación, haga clic en **Quitar**.
    
## <a name="viewing-the-registry-settings"></a>Visualización de la configuración del registro

Para ver la configuración del registro que se creará cuando se instala COM Add-in, siga estos pasos:
  
1. Haga clic en el nodo raíz del proyecto del programa de instalación en el **Explorador de soluciones**, haga clic en **Ver**, a continuación, el **Editor**, a continuación, haga clic en **el registro**.
    
2. En el panel izquierdo, haga clic en el signo más para ** ** ** **expandir **HKEY_LOCAL_MACHINE**********.
    
3. Haga clic en el nombre correspondiente al **ProgID**de compartida complemento del proyecto.
    
Para cambiar alguna de estas propiedades, haga clic en la propiedad, haga clic en **Ventana Propiedades**y cambie el cuadro **valor** en la **Ventana Propiedades**.
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>Compilar y distribuir el complemento compartido

Para compilar el administradas COM Add-in para realizar pruebas en el equipo en el que se desarrolló el proyecto de complemento compartido, haga clic en el nodo raíz del proyecto complemento compartido en el Explorador de soluciones y haga clic en generar. Si el proyecto se compila sin errores, puede iniciar el entorno de edición de InfoPath y empezar a usar el administradas COM Add-in. Si tiene una instancia de InfoPath ejecutándose, ciérrela antes de generar el proyecto. También puede ser necesario abrir el cuadro de diálogo Complementos COM para comprobar que está registrado COM Add-in. Para abrir el cuadro de diálogo Complementos COM, siga estos pasos:
  
1. Abra el entorno de edición de InfoPath. La forma más sencilla de hacer esto es abrir una plantilla de formulario existente, que se va a crear un nuevo formulario basado en esa plantilla de formulario.
    
2. En el menú **Herramientas** , haga clic en **Centro de confianza** . 
    
3. Haga clic en la categoría **complementos** en el lado izquierdo. 
    
4. En la sección **Administrar** cerca de la parte inferior del cuadro de diálogo **Centro de confianza** , seleccione **complementos COM** en la lista y haga clic en el botón **Ir** . 
    
5. En el cuadro de diálogo **complementos COM** , verá el nombre de su complemento creadas recientemente y debe haber una casilla de verificación situada junto a él. Si no hay ninguna casilla de verificación situada junto a él, COM Add-in no se pudo cargar debido a un error, que se enumerarán en la sección **Comportamiento de carga** del cuadro de diálogo. 
    
Para compilar el complemento COM administrado para su uso en un equipo distinto del equipo en el que se desarrolló el proyecto de complemento compartido, debe seguir pasos adicionales para proteger el código. Para obtener información acerca de cómo proteger proyectos de complemento compartido para su uso en otros equipos, vea los tres artículos siguientes:
  
- [Implementación de complementos COM administrados en Office XP](http://go.microsoft.com/fwlink/?LinkID=73473)
  
- [Uso de la solución de compatibilidad (shim) de complemento COM para implementar administrado complementos COM de Office XP](http://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Aislar las extensiones de Office con el Asistente de compatibilidad (shim) de COM](http://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> Si no se aísla COM Add-in puede provocar pérdidas de memoria e inestabilidad en la aplicación. 
  
> [!NOTE]
> Si .NET Framework u otros ensamblados requeridos del proyecto del programa de instalación aún no están instalados en los equipos de destino, es posible que el archivo .msi no se instale correctamente. Además, no se puede distribuir el archivo .msi y, a continuación, intente instalar el archivo .msi. También debe distribuir los archivos de compatibilidad con otras en la misma carpeta que el archivo .msi original generado por Visual Studio. 
  
## <a name="coding-in-the-com-add-in"></a>Codificación en el complemento COM

Eventos de aplicación que se producen en el entorno de edición de formularios de InfoPath se pueden capturar por un COM Add-in. Los siguientes eventos del objeto [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) pueden usarse por COM Add-in para responder a las acciones del usuario: 
  
|**Evento**|**Descripción**|
|:-----|:-----|
|[NewXDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx) (Evento)  <br/> |Se produce cuando se crea un nuevo formulario.  <br/> |
|[Salga de](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx) (Evento)  <br/> |Se produce cuando el usuario sale de InfoPath.  <br/> |
|[WindowActivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx) (Evento)  <br/> |Este evento se produce cuando se activa cualquier ventana de documento.  <br/> |
|[WindowDeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx) (Evento)  <br/> |Este evento se produce cuando se desactiva cualquier ventana de documento.  <br/> |
|[WindowSize](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx) (Evento)  <br/> |Se produce cuando se mueve una ventana de documento o se cambia su tamaño.  <br/> |
|[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx) (Evento)  <br/> |Tiene lugar inmediatamente antes de que se cierre un documento.  <br/> |
|[XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx) (Evento)  <br/> |Se produce inmediatamente antes de que se imprima un documento abierto.  <br/> |
|[XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx) (Evento)  <br/> |Se produce inmediatamente antes de que se guarde un documento abierto.  <br/> |
|[XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx) (Evento)  <br/> |Se produce cuando se crea un nuevo formulario, cuando se abre un formulario existente o cuando otro formulario se convierte en el formulario activo.  <br/> |
|[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx) (Evento)  <br/> |Este evento se produce al abrir un documento.  <br/> |
   
Para capturar estos eventos en COM Add-in, debe declarar las siguientes variables de nivel de clase en la clase **Connect** : 
  
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

La primera línea convierte el **objeto** recibido por el complemento en el objeto [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) de aplicación genérica. La segunda línea convierte la propiedad [Events](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) del objeto **_Application3** (representado por la variable **InfoPathApplication** ) en el objeto [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) . 
  
Para crear controladores de eventos, seleccione **InfoPathApplicationEvents** en el cuadro de lista desplegable **Nombre de clase** en la parte superior de la ventana de Visual Studio y, a continuación, seleccione el evento que desea controlar en el cuadro de lista desplegable **Nombre de método** en la parte superior del objeto Visual Ventana de Studio. Por ejemplo, si necesita controlar cuándo se guarda un formulario, debe controlar el evento **XDocumentBeforeSave** . Automáticamente, se selecciona **XDocumentBeforeSave** en la lista desplegable **Nombre de método** , inserta el siguiente procedimiento: 
  
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

Cualquiera de los eventos del objeto **ApplicationEvents** puede ser controlado por el COM Add-in utilizando el mismo método. 
  
## <a name="see-also"></a>Vea también

- [Creación de una Microsoft Office 2000 COM Add-in](http://go.microsoft.com/fwlink/?LinkID=73468) 
- [Creación de Office Managed COM Add-Ins con Visual Studio .NET](http://go.microsoft.com/fwlink/?LinkID=73470)
- [Trabajar con los procedimientos del evento IDTExtensibility2](http://go.microsoft.com/fwlink/?LinkID=73471)
- [Crear un complemento COM de Office con Visual Basic .NET](http://go.microsoft.com/fwlink/?LinkID=73469)
- [Crear un complemento COM de Office con Visual C# .NET](http://go.microsoft.com/fwlink/?LinkID=73472)
- [Creación de complementos de 2007 de InfoPath mediante el uso de Visual Studio 2005 Tools para Office System SE](http://msdn.microsoft.com/en-us/library/bb968857%28office.12%29.aspx)

