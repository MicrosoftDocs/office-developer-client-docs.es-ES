---
title: 'Tutorial: crear y depurar una plantilla de formulario básica mediante el modelo de objetos de InfoPath'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- plantillas de formulario [InfoPath 2007], tutoriales, plantillas de formulario [InfoPath 2007], creación de InfoPath 2003, plantillas de formulario compatibles con InfoPath 2003, tutoriales
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: En este tema se proporciona un tutorial para crear una plantilla de formulario con código administrado de InfoPath básica que funcione con el modelo de objetos compatible con InfoPath 2003 que proporciona el espacio de nombres Microsoft. Office. Interop. InfoPath. semiTrust.
ms.openlocfilehash: c559aedad5c62134c796196c63c1a84f70c4dc3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414343"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a>Tutorial: crear y depurar una plantilla de formulario básica mediante el modelo de objetos de InfoPath

En este tema se proporciona un tutorial para crear una plantilla de formulario con código administrado de InfoPath básica que funcione con el modelo de objetos compatible con InfoPath 2003 que proporciona el espacio de nombres [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
## <a name="hello-world"></a>Hola a todos

En el siguiente ejemplo, aprenderá a mostrar un cuadro de diálogo de alerta simple mediante el método [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) del modelo de objetos compatible con InfoPath 2003. 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a>Crear una plantilla de formulario de InfoPath que funciona con el modelo de objetos compatible con InfoPath 2003

1. Cree una nueva plantilla de formulario que funcione con el modelo de objetos compatible con InfoPath 2003, tal y como se describe en [crear una plantilla de formulario con el modelo de objetos de infopath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).
    
2. Asigne al proyecto de plantilla de formulario el nombre HelloWorld y guárdelo. 
    
   El sistema de proyectos crea el código y los archivos del proyecto y, a continuación, abre una plantilla de formulario en blanco en el modo de diseño de InfoPath. Ya está listo para añadir controladores de eventos.
    
### <a name="add-a-button-with-an-onclick-event-handler"></a>Agregar un botón con un controlador de eventos OnClick

1. En la sección **Controles** de la ficha **Inicio**, haga clic en el control **Botón** para insertarlo en la vista. 
    
2. Haga clic con el botón secundario del mouse en el control y a continuación haga clic en **Propiedades del botón**.
    
3. Cambie la **etiqueta** a alerta.
    
4. Cambie el **identificador** a AlertID.
    
5. Haga clic en **Editar código del formulario**.
    
   Se crea un esqueleto de controlador de eventos para el evento [onclick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) y el foco se desplaza al editor de código en Visual Studio 2012. Para obtener más información sobre cómo trabajar con controladores de eventos, vea [Agregar un controlador de eventos mediante el modelo de objetos de InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md). 
    
   Ya está todo preparado para agregar el código de formulario al controlador de eventos del botón.
    
### <a name="add-form-code-to-the-event-handler"></a>Agregar código de formulario al controlador de eventos

1. En el controlador de eventos **OnClick**, escriba el código siguiente: 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   Observe que aparece una lista desplegable de Microsoft IntelliSense cada vez que se escribe un punto en la línea de código. La función completa del controlador de eventos debe tener el siguiente aspecto:
    
   ```cs
    [InfoPathEventHandler(MatchPath="AlertID", EventType=InfoPathEventType.OnClick)]
    public void AlertID_OnClick(DocActionEvent e)
    {
        thisXDocument.UI.Alert("Hello World!");
    }
   ```

   ```vb
    <InfoPathEventHandler(MatchPath:="AlertID", EventType:=InfoPathEventType.OnClick)>
    Public Sub AlertID_OnClick(ByVal e As DocActionEvent)
        thisXDocument.UI.Alert("Hello World!")
    End Sub
   ```

   > [!NOTE]
   > Como alternativa al método **Alert**, puede utilizar el método **MessageBox.Show** del espacio de nombres **System.Windows.Forms** para mostrar un cuadro de mensajes. Para ello, debe agregar una referencia al ensamblado System. Windows. Forms, Add `using System.Windows.Forms;` o `Imports System.Windows.Forms` a las directivas al principio del archivo de código y, a continuación, escribir una línea de código como la siguiente:`MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`
  
2. Cambie a la ventana de modo de diseño de InfoPath y haga clic en el botón **Vista previa** de la ficha **Inicio**. 
    
3. En la ventana **Vista previa**, haga clic en el botón **Aviso**. 
    
   Aparecerá un cuadro de mensaje con el texto "Hello World".
    
   El procedimiento siguiente muestra cómo agregar puntos de interrupción para depurar el código del formulario.
    
### <a name="debug-form-code"></a>Depurar el código del formulario

1. En el editor de código, haga clic en la barra gris que se encuentra a la izquierda de esta línea:
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   Aparecerá un círculo rojo y la línea de código se resaltará para indicar que se hará una pausa en el tiempo de ejecución al llegar a este punto de interrupción en el código del formulario.
    
2. En el menú **Depurar**, haga clic en **Iniciar depuración** (o presione F5). 
    
3. En la ventana **Vista previa** de InfoPath, haga clic en el botón **Aviso**. 
    
   El foco se desplazará al editor de código y se resaltará la línea en la que se encuentra el punto de interrupción.
    
4. En el menú **Depurar**, haga clic en **Paso a paso por procedimientos** (o presione Mayús+F8) para continuar depurando el código paso a paso. 
    
   Se ejecuta el código del método Alert y se ejecuta el **mensaje** "Hello World!". la alerta se muestra en la ventana **vista previa** de InfoPath. 
    
## <a name="getting-the-current-users-name"></a>Obtener el nombre del usuario actual

Puede utilizar las clases de .NET Framework para obtener acceso a funciones de las que no se puede disponer con facilidad en las secuencias de comandos. En este ejemplo, aprenderá cómo utilizar las clases de .NET Framework para recuperar el nombre del usuario actual.
  
### <a name="add-an-onload-event-handler"></a>Agregar un controlador de eventos OnLoad

1. Abra el proyecto HelloWorld de InfoPath que acaba de crear.
    
2. En la ficha **Ver**, haga clic en **Mostrar campos**.
    
3. Haga clic con el botón secundario en el nodo **myFields** y, a continuación, haga clic en **Agregar**.
    
4. En **Nombre**, escriba **empleado** y haga clic en **Aceptar**.
    
5. Arrastre el nodo **empleado** hasta la vista. 
    
6. En la ficha **Programador**, haga clic en **Evento Al cargar (OnLoad)**.
    
   De esta forma, se creará un controlador de eventos para el evento [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) y el foco se desplazará al editor de código. Se puede llamar al código de este controlador de eventos cada vez que se cargue el formulario. El procedimiento siguiente muestra cómo agregar código de formulario que recupere el nombre del usuario para el controlador de eventos. 
    
### <a name="add-form-code"></a>Agregar código de formulario

1. En el controlador de eventos **OnLoad**, escriba el código siguiente: 
    
   ```cs
    // Store an XML DOM node as a local variable.
    IXMLDOMNode nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    if(nodeEmployee != null)
    {
        if(nodeEmployee.text == "")
        {
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName;
        }
    }
   ```

   ```vb
    // Store an XML DOM node as a local variable.
    Dim nodeEmployee As IXMLDOMNode
    nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    If Not(nodeEmployee Is Nothing) Then
        If(nodeEmployee.text = "") Then
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName
        End If
    End If
   ```

2. Compile el formulario y obtenga una vista previa del mismo.
    
   El nombre de usuario debería aparecer ahora en el cuadro de texto Empleado. 
    
Para obtener información sobre cómo implementar una plantilla de formulario con código administrado, vea [deploy InfoPath Form templates with Code](how-to-deploy-infopath-form-templates-with-code.md). Para obtener información sobre el modelo de objetos de InfoPath y las tareas de programación comunes en plantillas de formulario con código administrado que funcionan con el modelo de objetos compatible con InfoPath 2003, consulte [Understanding the infopath 2003 Object Model](understanding-the-infopath-2003-object-model.md). 
  
## <a name="see-also"></a>Ver también

- [Utilizar código de limpieza e inicialización mediante el modelo de objetos de InfoPath 2003](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [Modelos de objetos compatibles con InfoPath 2003](infopath-2003-compatible-object-models.md)
- [Adición de un controlador de eventos mediante el modelo de objetos de InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

