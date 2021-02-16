---
title: Trabajar con ventanas de formulario mediante el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, form windows,form windows [InfoPath 2007], InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: fbcf3a04-ee0f-40a6-8edd-583ae203e2e1
description: Cuando se trabaja con un formulario de InfoPath mediante programación, es posible escribir código para tener acceso a las ventanas del formulario y, a continuación, personalizar algunos de los elementos que contienen. El modelo de objetos compatible con InfoPath 2003 admite el acceso a las ventanas de los formularios mediante la interfaz WindowObject en asociación con la interfaz WindowsCollection .
ms.openlocfilehash: f8939fc562cf16c1bce0f6f88bba659e895254f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427580"
---
# <a name="work-with-form-windows-using-the-infopath-2003-object-model"></a>Trabajar con ventanas de formulario mediante el modelo de objetos de InfoPath 2003

Cuando se trabaja con un formulario de InfoPath mediante programación, es posible escribir código para tener acceso a las ventanas del formulario y, a continuación, personalizar algunos de los elementos que contienen. El modelo de objetos compatible con InfoPath 2003 admite el acceso a las ventanas de los formularios mediante la interfaz [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) en asociación con la interfaz [WindowsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowsCollection.aspx) . 
  
Hay dos tipos de ventanas en InfoPath:
  
- La ventana de edición, que se usa cuando un usuario rellena un formulario.
    
- La ventana de diseño, que se usa cuando un usuario diseña una plantilla de formulario.
    
Cuando se escribe código en una plantilla de formulario, la ventana de edición es la que proporciona la funcionalidad más práctica, puesto que permite utilizar una instancia de **WindowObject** que haga referencia al mismo para tener acceso a gran variedad de propiedades y métodos para personalizar la experiencia de edición del formulario. 
  
## <a name="overview-of-the-windowscollection-interface"></a>Información general sobre la interfaz WindowsCollection

La interfaz **WindowsCollection** proporciona las siguientes propiedades que los programadores de plantillas pueden utilizar para administrar las instancias de **WindowObject** que contiene. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|Propiedad [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Count.aspx)  <br/> |Devuelve el número de objetos **Window** que contiene una colección.  <br/> |
|Propiedad [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Item.aspx)  <br/> |Devuelve una referencia al objeto **Window** especificado.  <br/> **NOTA:** Visual C# tiene acceso a las colecciones mediante un indizador en lugar de llamar a la **propiedad Item.** Por ejemplo, `thisApplication.Windows[0].Caption`.           |
   
## <a name="overview-of-the-window-object"></a>Información general del objeto Window

La interfaz **WindowObject** proporciona el método y las propiedades siguientes que los programadores de formularios pueden utilizar para interactuar con una ventana de InfoPath. La compatibilidad con estos métodos y propiedades varía según el tipo de ventana ( [XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) ) con el que se esté trabajando. Algunos métodos y propiedades sólo funcionan con el tipo de ventana de editor (**XdWindowType.xdEditorWindow**). Los demás métodos y propiedades funcionan tanto con el tipo de ventana de editor como con el tipo de ventana de diseñador (**XdWindowType.xdDesignerWindow**). Asimismo, como sucede con todos los miembros del modelo de objetos de InfoPath, cuando se llama desde una plantilla de formulario, la compatibilidad con métodos y propiedades varía según el nivel de seguridad y la forma en que se haya implementado el formulario.
  
|**Nombre**|**Descripción**|**Compatibilidad con el tipo de ventana**|
|:-----|:-----|:-----|
|[Método Activate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Activate.aspx)  <br/> |Designa la ventana como la que está activa en ese momento.  <br/> |Tanto el tipo **xdDesignWindow** como el tipo **xdEditorWindow**  <br/> |
|[Active (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Active.aspx)  <br/> |Devuelve un valor **Boolean** que indica si la ventana es la que está activa en ese momento  <br/> |Los tipos **xdDesignWindow y** **xdEditorWindow**  <br/> |
|[Caption (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Caption.aspx)  <br/> |Propiedad de lectura y escritura que devuelve o establece el texto del título de la ventana representada por el objeto **Window**.  <br/> |Sólo el tipo **xdEditorWindow**  <br/> |
|Método [Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Close.aspx)  <br/> |Cierra una ventana.  <br/> |Sólo el tipo **xdEditorWindow**  <br/> |
|[CommandBars (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.CommandBars.aspx)  <br/> |Devuelve una referencia al objeto **CommandBars** de Microsoft Office.  <br/> |Los tipos **xdDesignWindow y** **xdEditorWindow**  <br/> |
|[Height (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Height.aspx)  <br/> |Una propiedad de lectura y escritura del tipo de entero largo que especifica el alto de la ventana representada por el objeto **Window** se mide en puntos.  <br/> |Los tipos **xdDesignWindow y** **xdEditorWindow**  <br/> |
|[Left (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Left.aspx)  <br/> |Una propiedad de lectura y escritura del tipo de entero largo que especifica la posición horizontal de la ventana representada por el objeto **Window** se mide en puntos.  <br/> |Los tipos **xdDesignWindow y** **xdEditorWindow**  <br/> |
|[MailEnvelope (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.MailEnvelope.aspx)  <br/> |Devuelve una referencia al [objeto MailEnvelopeObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MailEnvelopeObject.aspx) .  <br/> |Sólo el tipo **xdEditorWindow**  <br/> |
|[Propiedad TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.TaskPanes.aspx)  <br/> |Devuelve una referencia a la [colección TaskPanesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.TaskPanesCollection.aspx) .  <br/> |Los tipos **xdDesignWindow y** **xdEditorWindow**  <br/> |
|[Top (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Top.aspx)  <br/> |Una propiedad de lectura y escritura del tipo de entero largo que especifica la posición vertical de la ventana representada por el objeto **Window** se mide en puntos.  <br/> |Los tipos **xdDesignWindow y** **xdEditorWindow**  <br/> |
|[WindowType (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowType.aspx)  <br/> |Devuelve un número que indica el tipo de la ventana, basándose en la enumeración [XdWindowType.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx)  <br/> |Los tipos **xdDesignWindow y** **xdEditorWindow**  <br/> |
|[Width (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Width.aspx)  <br/> |Una propiedad de lectura y escritura del tipo de entero largo que especifica el ancho de la ventana representada por el objeto **Window**, se mide en puntos.  <br/> |Los tipos **xdDesignWindow y** **xdEditorWindow**  <br/> |
|[WindowState (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowState.aspx)  <br/> |Propiedad de lectura y escritura de tipo [XdWindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowState.aspx) que devuelve o establece el estado de la ventana representada por el **objeto Window** .  <br/> |Los tipos **xdDesignWindow y** **xdEditorWindow**  <br/> |
|[XDocument (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.XDocument.aspx)  <br/> |Devuelve una referencia al objeto [_XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.aspx) asociado a la ventana.  <br/> |Sólo el tipo **xdEditorWindow**  <br/> |
   
## <a name="using-the-windowscollection-and-window-interfaces"></a>Uso de las interfaces WindowsCollection y Window

El acceso a la interfaz **WindowsCollection** se puede obtener a través de la propiedad [Windows](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Windows.aspx) de la interfaz [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . Al utilizar la interfaz **WindowsCollection** para obtener acceso a las ventanas de un formulario, se utiliza un indizador (en Visual C#) o se transmite un número entero largo a la propiedad **Item** (en Visual Basic) para devolver una referencia a una instancia de la interfaz **WindowObject**. Por ejemplo, el código siguiente establece una referencia a la primera interfaz **WindowObject** contenida en la interfaz **WindowsCollection**.
  
```cs
WindowObject objWindow = thisApplication.Windows[0];
```

```vb
Dim objWindow As WindowObject = thisApplication.Windows(0)
```

No obstante, se puede tener acceso a la ventana que está actualmente abierta directamente mediante la propiedad [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.ActiveWindow.aspx) de la interfaz **Application**, sin tener que utilizar la interfaz ** WindowsCollection **, como se muestra en el siguiente ejemplo de código:
  
```cs
WindowObject objWindow = thisApplication.ActiveWindow;
```

```vb
Dim objWindow As WindowObject = thisApplication.ActiveWindow
```

> [!NOTE]
> [!NOTA] Al depurar un proyecto de código administrado de InfoPath, la propiedad **ActiveWindow** devuelve siempre el valor **null** porque la ventana de depuración está activa. 
  
El acceso a la interfaz **WindowObject** se puede obtener mediante la propiedad [Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) de la interfaz [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.aspx) , que está asociada al documento XML subyacente del formulario. La propiedad **View** de la interfaz **XDocument** se utiliza para obtener acceso al objeto **View**. Por ejemplo, el código siguiente establece una referencia a la interfaz **WindowObject** asociada a la vista del documento XML subyacente de un formulario: 
  
```cs
WindowObject objWindow = thisXDocument.View.Window;
```

```vb
Dim objWindow As WindowObject = thisXDocument.View.Window
```

> [!NOTE]
> [!NOTA] Algunos de los métodos y las propiedades del objeto **Window** se utilizan sólo para editar el tipo de ventana; si se utilizan con el tipo de ventana de diseño, devolverán un error. Los métodos y propiedades que admite cada tipo de ventana se muestran en la tabla anterior. Puede utilizar la propiedad **WindowType** en el código para averiguar con qué tipo de ventana está trabajando. 
  

