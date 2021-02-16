---
title: Responder a eventos de formulario
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- order of events [infopath 207],events [InfoPath 2007], responding,events [InfoPath 2007], order,InfoPath 2007, reponding to events,EventArgs classes [InfoPath 2007]
localization_priority: Normal
ms.assetid: 754db64b-179f-4385-8dd9-c20c9407b186
description: Es posible escribir código que responda a diversos eventos que pueden ocurrir cuando un usuario rellena un formulario. Para trabajar con eventos en InfoPath, hay que agregar los controladores de eventos cuando se trabaja con una plantilla de formulario en el modo de diseño.
ms.openlocfilehash: 0db3209dfe005f2a87ad65f3fc89b1714ec7d95c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407686"
---
# <a name="respond-to-form-events"></a>Responder a eventos de formulario

Es posible escribir código que responda a diversos eventos que pueden ocurrir cuando un usuario rellena un formulario. Para trabajar con eventos en InfoPath, hay que agregar los controladores de eventos cuando se trabaja con una plantilla de formulario en el modo de diseño.
  
Los controladores de eventos de InfoPath se deberían crear siempre en modo de diseño porque InfoPath añade automáticamente la declaración correcta para recibir el evento en el método **InternalStartup** e inserta el esqueleto del código del controlador de eventos en un archivo de código del formulario (FormCode.cs o FormCode.vb). Una vez creado un controlador de eventos, no se debe modificar su declaración en el archivo de código del formulario. 
  
Para obtener información acerca de cómo crear los controladores de eventos de InfoPath, vea [Agregar un controlador de eventos](how-to-add-an-event-handler.md).
  
## <a name="overview-of-the-event-classes"></a>Información general sobre las clases Event

El modelo de InfoPath que proporciona el espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) implementa tres clases que implementan los 12 eventos que se pueden producir y controlar mediante la lógica empresarial de la plantilla de formulario. En la tabla siguiente, se enumera cada objeto de evento de InfoPath, los eventos con los que están asociados y una descripción de la funcionalidad que ofrecen. 
  
|**Nombre**|**Eventos**|**Descripción**|
|:-----|:-----|:-----|
|[ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) <br/> |[Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) <br/> |La clase **ButtonEvent** implementa el evento **Clicked** que se produce cuando se hace clic en un control **Botón** de un formulario.  <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) <br/> [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) <br/> [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) <br/> [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) <br/> [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) <br/> [VersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.VersionUpgrade.aspx) <br/> [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) <br/> |La clase **FormEvents** implementa los eventos que son específicos de una plantilla de formulario de InfoPath:  <br/> **ContextChanged** <br/> Se produce después de que cambie el nodo de contexto.  <br/> **Loading** <br/> Ocurre después de haber cargado una plantilla de formulario, pero antes de inicializar alguna vista.  <br/> **Merge** <br/> Se produce cuando se **invoca el** comando Combinar formularios desde la interfaz de usuario o infoPath se inicia con el modificador de línea  `/aggregate` de comandos.  <br/> **Save** <br/> Se produce cuando  **se** usan los comandos Guardar o Guardar como desde la interfaz de usuario, o cuando se usan los métodos [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx) y [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) de la clase [XmlForm.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)  <br/> **Sign** <br/> Ocurre después de que un conjunto de datos firmados se haya seleccionado por medio del cuadro de diálogo **Firmas digitales**.  <br/> **Submit** <br/> Se produce cuando **se usa el** comando Enviar desde la interfaz de usuario o se usa el método [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) de la clase **XmlForm.**  <br/> **VersionUpgrade** <br/> Ocurre cuando el número de versión del formulario que se ha abierto es más antiguo que el número de versión de la plantilla de formulario en que se basa.  <br/> **ViewSwitched** <br/> Ocurre después de haber cambiado de vista con éxito en un formulario.  <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) <br/> [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) <br/> [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) <br/> |Implementa los eventos que producen los cambios realizados en los datos del documento XML subyacente de una instancia de formulario.  <br/> **Changed** <br/> Tiene lugar después de aceptar los cambios efectuados en el documento XML subyacente de un formulario y una vez que haya ocurrido el evento **Validating**.  <br/> **Changing** <br/> Ocurre después de que se hayan efectuado los cambios en el documento XML subyacente de un formulario, pero antes de aceptarlos.  <br/> **Validating** <br/> Ocurre después de haber aceptado los cambios efectuados en el documento XML subyacente de un formulario, pero antes de que ocurra el evento **Changed**.  <br/> La **clase XmlEvent** también implementa la propiedad [RaiseUndoRedoForChanged,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.RaiseUndoRedoForChanged.aspx) que obtiene o establece si se producirá el evento **Changed** cuando se produzca una operación de deshacer o rehacer.  <br/> |
   
> [!NOTE]
>  [!NOTA] Los eventos **Changed** y **Changing** sólo se producen una vez cuando se hace un cambio en un campo que no está en blanco en el formulario, mientras que los eventos comparables de InfoPath y del modelo de objetos compatible con InfoPath 2003 proporcionado por el espacio de nombres [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) ( [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) y [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) ) se producen dos veces en los cambios de un campo que no está en blanco: una vez cuando el valor antiguo se borra y la segunda cuando se inserta el nuevo valor. 
  
## <a name="overview-of-the-eventargs-classes"></a>Información general sobre las clases EventArgs

Cada uno de los 12 eventos tienen un objeto **EventArgs** asociado al evento que se pasa al controlador de eventos para el evento para proporcionar información de estado y otra funcionalidad que se puede usar en el código del controlador de eventos. En la tabla siguiente, se enumeran los eventos de InfoPath con sus objetos **EventArgs** asociados y una breve descripción de la funcionalidad que proporcionan las propiedades y los métodos del objeto. Para obtener detalles sobre propiedades y métodos específicos del objeto, haga clic en el nombre de un objeto **EventArgs** en la tabla y, después, en el vínculo Miembros. 
  
|**Evento**|**Clase EventsArgs**|**Descripción**|
|:-----|:-----|:-----|
|**Clicked** <br/> |[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |Obtiene el identificador del control.  <br/> Obtiene un objeto **XPathNavigator** situado en el nodo XML más interno del documento XML subyacente del formulario que contiene el control **Botón**.  <br/> |
|**ContextChanged** <br/> |[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |Obtiene el tipo de cambio de contexto que se llevó a cabo cuando se produjo el evento.  <br/> Obtiene un valor que indica si el cambio de contexto se produjo como respuesta a una operación de deshacer o rehacer.  <br/> Obtiene una referencia a un objeto **XPathNavigator** situado en el nodo de contexto que produjo el evento.  <br/> |
|**Loading** <br/> |[LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) <br/> |Especifica la vista en que se debe abrir el formulario una vez que se carga.  <br/> Obtiene una referencia al objeto **XmlFormCancelEventArgs**.  <br/> Obtiene un **IDictionary** que contiene los parámetros de entrada especificados mediante la opción de línea de comandos, o especificado mediante parámetros de consulta en una  `/InputParameters` dirección URL para abrir el formulario.  <br/> |
|**Merge** <br/> |[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |Obtiene una referencia al objeto **XmlFormCancelEventArgs**.  <br/> Obtiene el recuento del número de formularios combinados en una operación de combinación.  <br/> Obtiene el índice basado en cero del formulario que está combinando actualmente.  <br/> Obtiene o establece un valor que se usa con la propiedad **Cancel** para determinar si se debe cancelar sólo el formulario actual o la operación de combinación completa.  <br/> Obtiene un objeto **XPathNavigator** situado en el nodo raíz del documento XML subyacente del formulario que se está combinando.  <br/> |
|**Save** <br/> |[SaveEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.aspx) <br/> |Lleva a cabo la operación de guardado solicitada por el usuario.  <br/> Obtiene una referencia al objeto **SaveCancelEventArgs** que se puede usar para cancelar el evento.  <br/> Obtiene el nombre de archivo utilizado en el controlador de eventos para el evento.  <br/> Obtiene si la operación de guardado se realizará como una operación "guardar" o "guardar como".  <br/> |
|**Sign** <br/> |[SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) <br/> |Obtiene o establece información sobre si se debe mostrar el cuadro de diálogo **Firmas digitales**.  <br/> Obtiene el conjunto de datos que se pueden firmar que provocó el evento.  <br/> |
|**Submit** <br/> |[SubmitEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.aspx) <br/> |Obtiene una referencia al objeto **XmlFormCancelEventArgs** para cancelar el evento.  <br/> |
|**VersionUpgrade** <br/> |[VersionUpgradeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.aspx) <br/> |Obtiene una referencia al objeto **XmlFormCancelEventArgs** para cancelar el evento.  <br/> Obtiene el número de versión del documento de formulario que se está actualizando.  <br/> Obtiene el número de versión de la plantilla de formulario asociada al formulario que se está actualizando.  <br/> |
|**ViewSwitched** <br/> |[ViewSwitchedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewSwitchedEventArgs.aspx) <br/> |La clase **ViewSwitchedEventArgs** no proporciona ninguna propiedad ni métodos para el evento salvo los heredados de **System.Object**.  <br/> |
|**Changed** <br/> |[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |Obtiene un objeto **XPathExpression** que contiene una expresión de XPath que devuelve el nodo que se está cambiando.  <br/> Obtiene el valor nuevo para el nodo que se está cambiando.  <br/> Obtiene un objeto **XPathNavigator** que indica el nodo principal del nodo que se va a eliminar.  <br/> Obtiene el valor original del nodo que se está cambiando.  <br/> Obtiene una [enumeración XmlOperation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.aspx) que indica el tipo de operación que se produjo cuando se cambió el nodo.  <br/> Obtiene un objeto **XPathNavigator** que indica el nodo que se está cambiando.  <br/> Obtiene un valor que indica si el nodo que se está cambiando forma parte de una operación de deshacer o rehacer.  <br/> |
|**Changing** <br/> |[XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) <br/> |Obtiene un objeto **XmlFormCancelEventArgs** asociado al evento.  <br/> Hereda toda la funcionalidad enumerada arriba para el objeto **XmlEventArgs**.  <br/> |
|**Validating** <br/> |[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |Crea un [objeto FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) que contiene información de error personalizada con los valores especificados y la agrega al objeto [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) del formulario.  <br/> Hereda toda la funcionalidad enumerada arriba para el objeto **XmlEventArgs**.  <br/> |
   
## <a name="using-the-eventargs-objects"></a>Uso de los objetos EventArgs

Al crear un controlador de eventos, InfoPath crea la declaración de éste en el código de formulario del proyecto. En la declaración del controlador de eventos, InfoPath utiliza **e** como nombre del parámetro que se transmite al controlador de eventos. Este parámetro contiene el objeto **EventArgs** que está asociado con el controlador de eventos para ofrecer la información de estado y otra funcionalidad cuando se provoca el evento. 
  
Por ejemplo, si se crea un controlador de eventos para el evento **Loading** en el modo de diseño (haciendo clic en el menú **Evento Loading** en la ficha **Programador**), InfoPath agrega la declaración del controlador de eventos que recibe el objeto [LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) al archivo de código de formulario y, después, abre el editor de código para que pueda agregar el código a la siguiente declaración del controlador de eventos. 
  
```cs
public void FormEvents_Loading(object sender, LoadingEventArgs e)
{
   // Write your code here.
}
```

```vb
Public Sub FormEvents_Loading(ByVal sender As Object, _
   ByVal e As LoadingEventArgs)
   ' Write your code here.
End Sub
```

Cuando se escribe código para un controlador de eventos, puede usar las propiedades y los métodos implementados por el objeto **EventArgs** que se pasa mediante el parámetro **e**. Por ejemplo, en el siguiente controlador de eventos **Changing**, la propiedad [NewValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.NewValue.aspx) del objeto [XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) (que se hereda de la clase [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) ) se utiliza para comprobar el valor del campo que se acaba de cambiar. Si el usuario cambió el campo y lo dejó en blanco, se tiene acceso a la propiedad [Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.Message.aspx) de la clase [XmlFormCancelEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.aspx) usando la propiedad [CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.CancelableArgs.aspx) del objeto **XmlChangingEventArgs** para mostrar un error al usuario; la propiedad **XmlFormCancelEventArgs.Cancel** se establece en **true** para cancelar el evento y deshacer los cambios hechos por el usuario.
  
```cs
public void field1_Changing(object sender, LoadingEventArgs e)
{
   // Determine whether there is a new value.
   if (e.NewValue == "")
   {
      // The value is blank, so display an error message
      // and roll back the changes.
      e.CancelableArgs.Message = 
         "You must supply a value for this field.";
      e.CancelableArgs.Cancel = true;
      return;
   }
}
```

```vb
Public Sub field1_Changing(ByVal sender As Object, _
   ByVal e As LoadingEventArgs)
   ' Determine whether there is a new value.
   If (e.NewValue = "") Then
      ' The value is blank, so display an error message 
      ' and roll back the changes.
      e.CancelableArgs.Message = _
         "You must supply a value for this field."
      e.CancelableArgs.Cancel = True
      Return
   End If
End Sub
```


