---
title: Crear un complemento COM para agregar características personalizadas a InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, creación de complementos com,InfoPath 2007, adición de características personalizadas,complementos COM [InfoPath 2007]
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath admite complementos COM para extender la experiencia de usuario de edición de formularios. Aunque la compatibilidad con complementos COM se agregó por primera vez en InfoPath, otras aplicaciones de Office como Microsoft Office Word y Microsoft Office Excel han admitido complementos COM desde Office 2000.
ms.openlocfilehash: f8dd16b161c4ea862cf3b15e56e26a2547c1fc4c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303790"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Crear un complemento COM para agregar características personalizadas a InfoPath

Microsoft InfoPath admite complementos COM para extender la experiencia de usuario de edición de formularios. Aunque la compatibilidad con complementos COM se agregó por primera vez en InfoPath, otras aplicaciones de Office como Microsoft Office Word y Microsoft Office Excel han admitido complementos COM desde Office 2000.
  
La compatibilidad con complementos COM en InfoPath está disponible para el entorno de edición de formularios. El entorno de diseño de formularios no se puede extender mediante complementos COM.
  
## <a name="the-idtextensibility2-interface"></a>Interfaz IDTExtensibility2

El entorno de edición de InfoPath proporciona compatibilidad con la interfaz **IDTExtensibility2,** que deben implementar los desarrolladores de complementos COM. **IDTExtensibility2** es un objeto de interfaz dual que proporciona cinco métodos que actúan como eventos dentro del entorno de edición. Estos métodos permiten que el complemento COM responda a las condiciones de inicio y cierre del entorno, que se enumeran en la tabla siguiente. 
  
|**Interfaz**|**Descripción**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal custom() As Variant)** <br/> |Se produce cuando se carga o descarga un complemento en el entorno.  <br/> |
|**OnBeginShutdown (ByVal custom() As Variant)** <br/> |Se produce cuando se está apagando el entorno.  <br/> |
|**OnConnection(ByVal Application As Object, ByVal ConnectMode As ext_ConnectMode, ByVal AddInInst As Object, ByVal custom() As Variant)** <br/> |Se produce cuando se carga un complemento en el entorno.  <br/> |
|**OnDisconnection (ByVal RemoveMode As ext_DisconnectMode, ByVal custom() As Variant)** <br/> |Se produce cuando un complemento se descarga del entorno.  <br/> |
|**OnStartupComplete (ByVal custom() As Variant)** <br/> |Se produce cuando se ha completado el inicio del entorno.  <br/> |
   
## <a name="registering-com-add-ins"></a>Registro de complementos COM

Todas las aplicaciones de Office, incluido InfoPath, usan el Registro para enumerar complementos en la colección COM Add-Ins, para almacenar el estado de conexión y para almacenar la información de carga de arranque o demanda. Para los complementos COM de InfoPath, el nombre de cada complemento aparece debajo de la siguiente clave:
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Para los complementos COM instalados para su uso por cada usuario del equipo cliente, la clave del Registro se encuentra en el subárbol del Registro HKLM:
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
El nombre de la clave del Registro corresponde al **ProgIdAttribute** del complemento y contiene los siguientes valores. 
  
|**Nombre**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**Cadena** <br/> |Nombre que se muestra en el cuadro de diálogo Complementos  **COM** y que aparece en la página Complementos del **Centro de confianza.**  <br/> |
|**Descripción** <br/> |**String** <br/> |Cadena que se muestra cuando se selecciona el complemento en el Centro **de confianza.**  <br/> |
|**LoadBehavior** <br/> |**DWORD** <br/> |Especifica la forma en que se carga el complemento COM. El valor puede ser una combinación de 0, 1, 2, 8 y 16. Consulta la tabla siguiente para obtener más información.  <br/> |
   
El **valor DWORD** de **LoadBehavior** debe contener un valor que describa cómo se carga el complemento COM en el entorno de edición. El valor puede ser de la tabla siguiente o una combinación de valores de la tabla. Por ejemplo, un complemento COM creado en Visual Studio 2005 tendrá un **LoadBehavior** de "3" cargado en el inicio de la aplicación y se conectará. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Desconectado. El complemento se muestra como inactivo en el cuadro de **diálogo Complemento COM.**  <br/> |
|1   <br/> |Conectado. El complemento se muestra como Activo en el cuadro **de diálogo Complemento COM.**  <br/> |
|2   <br/> |Cargar al inicio. El complemento se carga y se conecta cuando se inicia la aplicación host.  <br/> |
|8   <br/> |Cargar a petición. El complemento se carga y se conecta cuando la aplicación host lo requiere, por ejemplo, cuando un usuario hace clic en un botón que usa funcionalidad en el complemento.  <br/> |
|16   <br/> |Conectar la primera vez. El complemento se cargará y conectará la primera vez que el usuario ejecute la aplicación host después de registrarlo.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Creación de un complemento COM administrado con Visual Studio 2005 o Visual Studio 2008

Para crear un complemento COM administrado con Microsoft Visual Studio 2005 o Visual Studio 2008, cree un proyecto de Add-In compartido de la siguiente manera: 
  
1. Inicie Visual Studio.
    
2. En el menú **Archivo**, haga clic en **Nuevo proyecto**.
    
3. En el **panel Tipos de proyecto** del cuadro **de** diálogo Nuevo proyecto, haga clic en la carpeta **Otros** tipos de proyectos y, a continuación, haga clic **en Extensibilidad.**
    
4. En el **panel Plantillas,** haga clic **en Complemento compartido.**
    
5. En el **cuadro** Nombre, escriba un nombre para el proyecto. 
    
6. En el **cuadro Ubicación,** escriba una ruta de acceso de carpeta o **haga** clic en Examinar, seleccione una ruta de carpeta y, a continuación, haga clic en **Aceptar.** Aparecerá **el Asistente para complementos compartidos.** 
    
7. Haga **clic en** Siguiente en el Asistente para complementos **compartidos.** Aparecerá **la página Seleccionar un lenguaje de** programación. 
    
8. Haga **clic en Crear un** complemento mediante Visual Basic y, a continuación, haga clic en **Siguiente.** Aparece **la página Seleccionar un host de** aplicación. 
    
9. Desactive las casillas situadas junto a cada aplicación excepto **Microsoft InfoPath** y, a continuación, haga clic en **Siguiente**. Aparece **la página Escribir un** nombre y una descripción. 
    
10. En el **cuadro ¿Cuál es el nombre del complemento?,** escriba el nombre del complemento COM. 
    
11. En el **cuadro ¿Cuál es la descripción** del complemento?, escriba la descripción del complemento COM y haga clic en **Siguiente.** Aparece **la página Add-In opciones.** 
    
12. Compruebe que me gustaría que mi complemento se cargara cuando la aplicación **host** se cargase y Mi complemento debería estar disponible para todos los usuarios del equipo en el que se **instaló,** no solo para la persona que lo instala. 
    
13. Haga **clic en Siguiente** para revisar la página **Resumen** y, a continuación, haga clic **en Finalizar.**
    
Después de crear el proyecto Visual Studio, verá dos proyectos en la ventana Explorador de soluciones. El primer proyecto es el proyecto del complemento COM; el segundo proyecto es un proyecto de configuración para implementar el complemento COM. El **Asistente** para complementos compartidos solo inserta una referencia a la biblioteca de objetos de **Microsoft Office 14.0,** por lo que es necesario insertar una referencia a la biblioteca de objetos de InfoPath siguiendo estos pasos:
  
1. Haga doble clic **en Mi proyecto** para mostrar las propiedades del proyecto de complemento. Haga clic **en la pestaña** Referencias para mostrar las referencias agregadas automáticamente al proyecto. 
    
2. Haga clic **en el botón** Agregar para mostrar el cuadro de **diálogo** Agregar referencia. 
    
3. En la **ficha COM,** haga doble clic en Biblioteca de **tipos de Microsoft.InfoPath 2.0** y, a continuación, haga clic en **Aceptar**.
    
4. Agregar una referencia a la biblioteca de tipos de **Microsoft InfoPath 3.0** también agrega referencias a tres ensamblados que deben quitarse: **ADODB**, **MSHTML** y **MSXML2**. En **el Explorador de soluciones,** en **Referencias,** haga clic con el botón secundario en cada una de estas referencias y, a continuación, haga clic en **Quitar**.
    
## <a name="viewing-the-registry-settings"></a>Visualización de la configuración del Registro

Para ver la configuración del Registro que se creará cuando se instale el complemento COM, siga estos pasos:
  
1. Haga clic con el botón secundario en el nodo raíz del proyecto de instalación en el Explorador de soluciones **,** haga clic en Ver **y,** a continuación, haga clic en El **Registro.**
    
2. En el panel izquierdo, haga clic en el signo más para expandir **HKEY_LOCAL_MACHINE**, **Software**, **Microsoft**, **InfoPath** y, a continuación, **AddIns**.
    
3. Haga clic en el nombre correspondiente al ProgID del proyecto de complemento **compartido.**
    
Para cambiar cualquiera de estas propiedades, haga clic con el botón secundario en la propiedad, haga clic en ventana Propiedades y cambie el cuadro **Valor** en la ventana **Propiedades**.
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>Compilar y distribuir el servicio compartido Add-In

Para compilar el complemento COM administrado para realizar pruebas en el equipo en el que se desarrolló el proyecto de Add-In compartido, haga clic con el botón secundario en el nodo raíz del proyecto Add-In compartido en el Explorador de soluciones y haga clic en Generar. Si el proyecto se genera sin errores, puede iniciar el entorno de edición de InfoPath y empezar a usar el complemento COM administrado. Si tiene una instancia de InfoPath en ejecución, cieciela antes de compilar el proyecto. También puede ser necesario abrir el cuadro de diálogo Complementos COM para comprobar que el complemento COM está registrado. Para abrir el cuadro de diálogo Complementos COM, siga estos pasos:
  
1. Abra el entorno de edición de InfoPath. La forma más sencilla de hacerlo es abrir una plantilla de formulario existente, que creará un nuevo formulario basado en esa plantilla de formulario.
    
2. Haga **clic en Centro de** confianza en el **menú** Herramientas. 
    
3. Haga clic **en la categoría Complementos** de la izquierda. 
    
4. En la **sección Administrar,**  cerca de la parte inferior del cuadro de diálogo Centro de confianza, seleccione Complementos **COM** en la lista y haga clic en el **botón** Ir. 
    
5. En el cuadro de diálogo Complementos **COM,** verá el nombre del complemento creado recientemente y debería haber una casilla al lado. Si no hay ninguna casilla al lado, el complemento COM no se pudo cargar  debido a un error, que aparecerá en la sección Comportamiento de carga del cuadro de diálogo. 
    
Para compilar el complemento COM administrado para usarlo en un equipo distinto del equipo en el que se desarrolló el proyecto Add-In compartido, debe seguir pasos adicionales para proteger el código. Para obtener información sobre la protección de proyectos Add-In compartidos para su uso en otros equipos, vea los tres artículos siguientes:
  
- [Implementación de aplicaciones COM administradas Add-Ins en Office XP](https://go.microsoft.com/fwlink/?LinkID=73473)
  
- [Uso de la solución de correcciones de compatibilidad de complemento COM para implementar complementos COM administrados en Office XP](https://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Aislamiento de extensiones de Office con el Asistente para correcciones de compatibilidad (SHIM) de COM](https://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> No aislar el complemento COM puede provocar pérdidas de memoria e inestabilidad de la aplicación. 
  
> [!NOTE]
> Si .NET Framework u otros ensamblados necesarios del proyecto de instalación aún no están instalados en los equipos de destino, es posible que el archivo .msi no se instale correctamente. Además, no puede distribuir el archivo .msi y, a continuación, intentar instalar el archivo .msi. También debe distribuir los demás archivos de soporte técnico en la misma carpeta que el archivo .msi original generado por Visual Studio. 
  
## <a name="coding-in-the-com-add-in"></a>Codificación en el complemento COM

Un complemento COM puede capturar los eventos de aplicación que se producen en el entorno de edición de formularios de InfoPath. El complemento COM puede usar los siguientes eventos del objeto [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) para responder a las acciones del usuario: 
  
|**Evento**|**Descripción**|
|:-----|:-----|
|[NewXDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx) Evento  <br/> |Se produce cuando se crea un nuevo formulario.  <br/> |
|[Salir](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx) Evento  <br/> |Se produce cuando el usuario sale de InfoPath.  <br/> |
|[WindowActivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx) Evento  <br/> |Este evento se produce cuando se activa cualquier ventana de documento.  <br/> |
|[WindowDeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx) Evento  <br/> |Este evento se produce cuando se desactiva cualquier ventana de documento.  <br/> |
|[WindowSize](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx) Evento  <br/> |Se produce cuando se mueve una ventana de documento o se cambia su tamaño.  <br/> |
|[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx) Evento  <br/> |Este evento se produce antes de que se cierre cualquier documento.  <br/> |
|[XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx) Evento  <br/> |Se produce inmediatamente antes de que se imprima un documento abierto.  <br/> |
|[XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx) Evento  <br/> |Se produce inmediatamente antes de que se guarde un documento abierto.  <br/> |
|[XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx) Evento  <br/> |Se produce cuando se crea un nuevo formulario, cuando se abre un formulario existente o cuando otro formulario se convierte en el formulario activo.  <br/> |
|[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx) Evento  <br/> |Este evento se produce al abrir un documento.  <br/> |
   
Para capturar estos eventos en el complemento COM, debe declarar las siguientes variables de nivel de clase en la **clase Connect:** 
  
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

La primera línea convierte la aplicación genérica **Object** recibida por el complemento en [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) objeto. La segunda línea convierte la propiedad [Events](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) del **objeto _Application3** (representado por la variable **InfoPathApplication)** al [objeto ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) . 
  
Para crear controladores de eventos, seleccione **InfoPathApplicationEvents** en el cuadro desplegable Nombre de clase en la parte superior de  la ventana Visual Studio y, a continuación, seleccione el evento que desea controlar en el cuadro desplegable Nombre de método en la parte superior de la ventana Visual Studio.  Por ejemplo, si necesita controlar cuándo se guarda un formulario, controle el evento **XDocumentBeforeSave.** Al seleccionar **XDocumentBeforeSave en** la lista desplegable Nombre del método, se inserta automáticamente el siguiente procedimiento:  
  
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

Cualquiera de los eventos del **objeto ApplicationEvents** puede controlarse mediante el complemento COM mediante el mismo método. 
  
## <a name="see-also"></a>Consulte también

- [Creación de Microsoft Office complemento COM de 2000](https://go.microsoft.com/fwlink/?LinkID=73468) 
- [Crear archivos COM administrados de Office Add-Ins con Visual Studio .NET](https://go.microsoft.com/fwlink/?LinkID=73470)
- [Trabajar con los procedimientos de evento IDTExtensibility2](https://go.microsoft.com/fwlink/?LinkID=73471)
- [Crear un complemento COM de Office con Visual Basic .NET](https://go.microsoft.com/fwlink/?LinkID=73469)
- [Crear un complemento COM de Office con Visual C# .NET](https://support.microsoft.com/en-us/help/302901/how-to-build-an-office-com-add-in-by-using-visual-c-net)
- [Creación de herramientas de InfoPath 2007 Add-Ins mediante Visual Studio 2005 Tools for the Office System SE](https://msdn.microsoft.com/library/bb968857%28office.12%29.aspx)

