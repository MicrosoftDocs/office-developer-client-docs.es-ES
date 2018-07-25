---
title: 'Tutorial: Crear una plantilla de formulario básica con código'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- plantillas de formulario [infopath 2007], crear código administrado, plantillas de formulario de código administrado [InfoPath 2007], crear, plantillas formulario [InfoPath 2007], tutoriales, InfoPath 2007, tutoriales
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: En Microsoft InfoPath, puede escribir lógica empresarial en Visual Basic o C# si abre una plantilla en el diseñador de InfoPath y, a continuación, usa uno de los comandos de la interfaz de usuario para agregar un controlador de eventos, que abrirá el entorno de desarrollo de Visual Studio 2012 para que se escriba el código.
ms.openlocfilehash: 8c98d71c26f8e56c532b2a4467218c366072b2ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815991"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a>Tutorial: Crear una plantilla de formulario básica con código

En Microsoft InfoPath, puede escribir lógica empresarial en Visual Basic o C# si abre una plantilla en el diseñador de InfoPath y, a continuación, usa uno de los comandos de la interfaz de usuario para agregar un controlador de eventos, que abrirá el entorno de desarrollo de Visual Studio 2012 para que se escriba el código. De manera predeterminada, los proyectos de plantilla de formulario creados con Visual Studio 2012 funcionan con el nuevo modelo de objetos de código administrado proporcionado por el espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . 
  
Este tutorial muestra en primer lugar cómo crear una sencilla aplicación denominada "Hola a todos" utilizando C# o Visual Basic en el entorno de desarrollo de Visual Studio 2012. El tutorial termina con un ejemplo de código que muestra cómo usar la propiedad [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) de la clase [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) para recuperar el nombre del usuario actual y rellenar un control de **Cuadro de texto** con ese valor. 
  
## <a name="prerequisites"></a>Requisitos previos

Para llevar a cabo este tutorial utilizando el entorno de desarrollo de Visual Studio 2012, necesitará:
  
- Microsoft InfoPath con Visual Studio 2012 instalado.
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a>"Hola a todos" en Visual Studio Tools for Applications

En el siguiente tutorial, aprenderá a escribir código en el entorno de desarrollo de Visual Studio 2012 para hacer que se muestre un sencillo cuadro de diálogo de alerta. Para ello, escribirá un controlador de eventos para el evento [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) de la clase [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) , que está asociada al control **Botón**. 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a>Crear un nuevo proyecto y especificar un lenguaje de programación

1. Inicie el diseñador de InfoPath y a continuación haga doble clic en la plantilla de formulario **En blanco (InfoPath Editor)**. 
    
2. Para especificar el lenguaje de programación que desea usar, haga clic en el **botón de Office**, haga clic en **Opciones de formulario**, haga clic en **Programación** en la lista **Categoría** y a continuación seleccione **Visual Basic** o **C#** de la lista desplegable **Lenguaje del código de la plantilla de formulario**. 
    
   > [!NOTE]
   > Las demás opciones de lenguaje de programación de la lista desplegable **Lenguaje del código de la plantilla de formulario** proporcionan compatibilidad con versiones anteriores de InfoPath. Las opciones **C# (compatible con InfoPath 2007)** y **Visual Basic (compatible con InfoPath 2007)** funcionarán con los procedimientos de este tema. Sin embargo, para utilizar las opciones **C# (compatible con InfoPath 2003)** y **Visual Basic (compatible con InfoPath 2003)**, vea [Tutorial: Crear y depurar una plantilla de formulario básica mediante el modelo de objetos de InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md). 
  
    Ya está todo preparado para agregar un control **Botón** y crear su controlador de eventos. 
    
### <a name="add-a-button-control-and-event-handler"></a>Agregar un control Botón y un controlador de eventos.

1. En el grupo **Controles**, haga clic en el control **Botón** para agregarlo al formulario. 
    
2. Haga doble clic en el control **Botón**, escriba Hola para la propiedad **Etiqueta** en la ficha **Propiedades** de la cinta y a continuación haga clic en **Código personalizado**. Cuando se le pida, guarde el formulario con el nombre "Hola a todos".
    
   Así se abrirá el entorno de **Visual Studio Tools for Applications** con el cursor situado en el controlador de eventos para el evento [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) del control **Botón**. 
    
   Ya está todo preparado para agregar el código de formulario al controlador de eventos del botón. 
    
### <a name="add-hello-world-code-to-the-event-handler-and-preview-the-form"></a>Agregue el código de "Hola a todos" al controlador de eventos y obtenga una vista previa del formulario.

1. En el esqueleto del controlador de eventos, escriba:
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   El código de la plantilla de formulario debe tener un aspecto parecido al siguiente:
    
   ```cs
    using Microsoft.Office.InfoPath;
    using System;
    using System.Windows.Forms;
    using System.Xml;
    using System.Xml.XPath;
    namespace HelloWorld
    {
        public partial class FormCode
        {
            public void InternalStartup()
            {
            ((ButtonEvent)EventManager.ControlEvents["CTRL1_5"]).Clicked += new ClickedEventHandler(CTRL1_5_Clicked);
            }
            public void CTRL1_5_Clicked(object sender, ClickedEventArgs e)
            {
            MessageBox.Show("Hello World!");
            }
        }
    }
   ```

   ```vb
    Imports Microsoft.Office.InfoPath
    Imports System
    Imports System.Windows.Forms
    Imports System.Xml
    Imports System.Xml.XPath
    Namespace HelloWorld
        Public Class FormCode
            Private Sub InternalStartup(ByVal sender As Object, ByVal e As EventArgs) Handles Me.Startup
            AddHandler DirectCast(EventManager.ControlEvents("CTRL1_5"), ButtonEvent).Clicked, AddressOf CTRL1_5_Clicked
            End Sub
            Public Sub CTRL1_5_Clicked(ByVal sender As Object, ByVal e As ClickedEventArgs)
            MessageBox.Show("Hello World!")
            End Sub
        End Class
    End Namespace
   ```

2. Cambie a la ventana de diseñador de InfoPath.
    
3. Haga clic en el botón **Vista previa** de la ficha **Inicio**. 
    
4. Haga clic en el botón Hola del formulario. 
    
   Aparecerá un cuadro de mensaje con el texto "Hola a todos".
    
   El procedimiento siguiente muestra cómo agregar puntos de interrupción para depurar el código del formulario.
    
### <a name="debug-form-code"></a>Depurar el código del formulario

1. Cambie a la ventana de Visual Studio 2012.
    
2. Haga clic en la barra gris situada a la izquierda de la línea:
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   Aparecerá un círculo rojo y la línea de código se resaltará para indicar que, en tiempo de ejecución, se hará una pausa al llegar a este punto de interrupción en el código del formulario.
    
3. En el menú **Depurar** haga clic en **Iniciar depuración** (o presione F5). 
    
4. En la ventana **Vista previa** de InfoPath, haga clic en el botón Hola del formulario. 
    
5. El foco se desplazará al editor de código de Visual Studio 2012 y se resaltará la línea en la que se encuentra el punto de interrupción.
    
6. En el menú **Depurar**, haga clic en **Paso a paso por procedimientos** (o presione Mayús+F8) para continuar paso a paso por los procedimientos del código. 
    
7. Se ejecuta el código del controlador de eventos y se muestra el mensaje "Hola a todos". 
    
8. Haga clic en **Aceptar** para volver al editor de código de Visual Studio de 2012 y después haga clic en **Detener depuración** en el menú **Depurar** (o presione Ctrl+Alt+Interrumpir). 
    
## <a name="getting-the-current-users-name"></a>Obtener el nombre del usuario actual

En el ejemplo siguiente, aprenderá a utilizar la propiedad [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) de la clase [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) para recuperar el nombre del usuario actual y rellenar el valor de un control **Cuadro de texto** mediante un controlador de eventos para el evento [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) . 
  
El control **Cuadro de texto** se rellena usando una instancia de la clase [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) para escribir el nombre del usuario actual en el nodo XML al que está enlazado el control. 
  
En primer lugar se llama a la propiedad [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) para recuperar una instancia de la clase [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) que representa el documento XML subyacente del formulario. A continuación, el objeto [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) llama al método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) , que crea el objeto **XPathNavigator** y lo coloca en el nodo raíz del origen de datos principal del formulario. 
  
Se llama al método [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) de la clase **XPathNavigator** para seleccionar el campo empleado en el origen de datos del formulario. Finalmente, se llama al método [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) para establecer el valor del campo con la propiedad [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) . 
  
Para obtener más información sobre cómo trabajar con **System.Xml** en plantillas de formulario de código administrado, vea [Trabajar con las clases XPathNavigator y XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="add-a-loading-event-handler"></a>Agregar un cuadro controlador de eventos de carga

1. Abra la plantilla de formulario "Hola a todos" que ha creado en el tutorial anterior en el diseñador de InfoPath.
    
2. En la ficha **Ver**, seleccione **Mostrar campos**.
    
3. Haga clic con el botón secundario en la carpeta **misCampos** y, a continuación, haga clic en **Agregar**.
    
4. En **Nombre**, escriba empleado y haga clic en **Aceptar**.
    
5. Arrastre el campo empleado a la vista. 
    
6. En la ficha **Programador**, haga clic en **Evento Loading**.
    
   Así se creará un controlador de eventos para el evento [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) y el foco se desplazará a dicho controlador de eventos en el editor de código. 
    
7. En el editor de código, escriba lo siguiente:
    
   ```cs
    public void FormEvents_Loading(object sender, LoadingEventArgs e)
    {
        XPathNavigator dataSource;
        dataSource = this.MainDataSource.CreateNavigator();
        dataSource.SelectSingleNode(
            "/my:myFields/my:employee", NamespaceManager).SetValue(this.User.UserName);
    }
   ```
 
   ```vb
    Public Sub FormEvents_Loading(ByVal sender As Object, ByVal e As LoadingEventArgs)
        Dim dataSource As XPathNavigator
        dataSource = Me.MainDataSource.CreateNavigator
        dataSource.SelectSingleNode( _
            "/my:myFields/my:employee", NamespaceManager).SetValue(Me.User.UserName)
    End Sub
   ```

8. Cambie a la ventana de diseño de formulario de InfoPath y a continuación haga clic en el botón **Vista previa** de la ficha **Inicio** para obtener la vista previa del formulario. 
    
   El campo empleado debe rellenarse automáticamente con el nombre de usuario. 
    
## <a name="next-steps"></a>Siguientes pasos

- Para obtener información sobre cómo trabajar con controladores de eventos para otros controles y eventos, vea [Agregar un controlador de eventos](how-to-add-an-event-handler.md).
    
- Para obtener información sobre la vista previa y la depuración de código de las plantillas de formulario, vea [Obtener una vista previa y depurar plantillas de formulario de InfoPath con código](how-to-preview-and-debug-infopath-form-templates-with-code.md).
    
- Para obtener información sobre cómo implementar plantillas de formulario con código administrado, vea [Implementar plantillas de formulario de InfoPath con código](how-to-deploy-infopath-form-templates-with-code.md).
    
- Para obtener información sobre el modelo de objetos de InfoPath y las tareas de programación más comunes en la plantillas de formulario con código administrado, vea [Comprender el modelo de objetos de InfoPath y las tareas de programación más comunes](understanding-the-infopath-object-model-and-common-developer-tasks.md)
    
## <a name="see-also"></a>Vea también

- [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)

