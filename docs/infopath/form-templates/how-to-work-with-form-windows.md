---
title: Trabajar con formularios Windows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- windowscollection [infopath 2007],form windows [InfoPath 2007],Window class [InfoPath 2007]
localization_priority: Normal
ms.assetid: 32ae2427-882b-45f8-8754-0e8c27fc23ba
description: Cuando se trabaja con un formulario de InfoPath mediante programación, es posible escribir código para tener acceso a las ventanas del formulario y personalizar algunos de los elementos que contienen. El modelo de objetos de InfoPath proporcionado por el espacio de nombres Microsoft.Office.InfoPath admite el acceso a las ventanas de los formularios mediante el uso de la clase Window en asociación con la clase WindowCollection .
ms.openlocfilehash: 018357519e27629c29b2611bd0a88b8d64f0a1eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431067"
---
# <a name="work-with-form-windows"></a>Trabajar con formularios Windows

Cuando se trabaja con un formulario de InfoPath mediante programación, es posible escribir código para tener acceso a las ventanas del formulario y personalizar algunos de los elementos que contienen. El modelo de objetos de InfoPath proporcionado por el espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) admite el acceso a las ventanas de los formularios mediante el uso de la clase [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) en asociación con la clase [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) . 
  
> [!NOTE]
> [!NOTA] Las clases para trabajar con las ventanas de un formulario sólo están disponibles al trabajar con un **formulario de InfoPath Editor**. Si la configuración **Compatibilidad** de una plantilla de formulario es **Formulario de explorador web**, estas clases no están disponibles. 
  
Hay dos tipos de ventanas en InfoPath: 
  
- La ventana de edición, que se usa cuando un usuario rellena un formulario.
    
- La ventana de diseño, que se usa cuando un usuario diseña una plantilla de formulario.
    
Cuando se escribe código en una plantilla de formulario, la ventana de edición es la que proporciona la funcionalidad más práctica, puesto que permite utilizar un objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) que representa la ventana activa para tener acceso a gran variedad de propiedades y métodos para personalizar la experiencia de rellenar un formulario. 
  
## <a name="overview-of-the-windowscollection-class"></a>Información general sobre la clase WindowsCollection

La clase [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) proporciona las siguientes propiedades que los programadores de plantillas de formulario pueden utilizar para administrar los objetos [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) que contienen. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|Propiedad [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx)  <br/> |Obtiene un recuento del número de [objetos Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) contenidos en la colección.  <br/> |
|Propiedad [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx)  <br/> |Obtiene una referencia al objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) especificado.  <br/> |
   
## <a name="overview-of-the-window-class"></a>Información general sobre la clase Window

La clase [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) proporciona el método y las propiedades siguientes, que los desarrolladores de formularios pueden utilizar para interactuar con una ventana de InfoPath. La compatibilidad con estos métodos y propiedades varía según el tipo de ventana ( [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) ) con el que se esté trabajando. Algunos métodos y propiedades sólo funcionan con el tipo de ventana de editor (**WindowType.Editor**). Los demás métodos y propiedades funcionan tanto con el tipo de ventana de editor como con el tipo de ventana de diseñador (**WindowType.Designer**). Asimismo, como sucede con todos los miembros del modelo de objetos de InfoPath, cuando se llama desde una plantilla de formulario, la compatibilidad con métodos y propiedades varía según el nivel de seguridad y la forma en que se haya implementado el formulario.
  
|**Nombre**|**Descripción**|**Compatibilidad con el tipo de ventana**|
|:-----|:-----|:-----|
|[Activate (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx)  <br/> |Activa (lleva el foco a) la ventana.  <br/> |Tanto el **Designer** como el tipo **Editor**  <br/> |
|[Active (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx)  <br/> |Obtiene un valor **Boolean** que indica si la ventana es la que está activa en ese momento.  <br/> |Tanto el **Designer** como el tipo **Editor**  <br/> |
|[Caption (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx)  <br/> |Obtiene o establece el texto del título de la ventana representada por el [objeto Window.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx)  <br/> |Sólo el tipo **Editor**  <br/> |
|[Método Close()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Cierra la ventana y pide que se guarden los cambios de todos los formularios sin guardar o de formularios con cambios que no se han guardado.  <br/> |Sólo el tipo **Editor**  <br/> |
|[Método Close(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Cierra la ventana y opcionalmente fuerza que se cierre un formulario que no se ha guardado o cuyos cambios no se han guardado.  <br/> |Sólo el tipo **Editor**  <br/> |
|[CommandBars (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx)  <br/> |Obtiene una referencia a la colección **CommandBars** de Microsoft Office que está asociada al objeto window.  <br/> |Tanto el **Designer** como el tipo **Editor**  <br/> |
|[Height (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx)  <br/> |Obtiene o establece el alto de la ventana, medido en puntos.  <br/> |Tanto el **Designer** como el tipo **Editor**  <br/> |
|[Left (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx)  <br/> |Obtiene o establece la posición horizontal de la ventana, medida en puntos.  <br/> |Tanto el **Designer** como el tipo **Editor**  <br/> |
|[MailEnvelope (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx)  <br/> |Obtiene una referencia a la [clase MailEnvelope.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx)  <br/> |Sólo el tipo **Editor**  <br/> |
|[Propiedad TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx)  <br/> |Obtiene una referencia a la [colección TaskPaneCollection.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx)  <br/> |Tanto el **Designer** como el tipo **Editor**  <br/> |
|[Top (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx)  <br/> |Obtiene o establece la posición vertical de la ventana, medida en puntos.  <br/> |Tanto el **Designer** como el tipo **Editor**  <br/> |
|[Width (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx)  <br/> |Obtiene o establece el ancho de la ventana, medido en puntos.  <br/> |Tanto el **Designer** como el tipo **Editor**  <br/> |
|[WindowState (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx)  <br/> |Obtiene o establece el estado de la ventana como [un valor WindowState.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx)  <br/> |Tanto el **Designer** como el tipo **Editor**  <br/> |
|[WindowType (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx)  <br/> |Obtiene el tipo de la ventana como un [valor de enumeración WindowType.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx)  <br/> |Tanto el **Designer** como el tipo **Editor**  <br/> |
|[XmlForm (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx)  <br/> |Devuelve una referencia al [objeto XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) asociado a la ventana.  <br/> |Sólo el tipo **Editor**  <br/> |
   
## <a name="using-the-windowscollection-and-window-classes"></a>Uso de las clases WindowsCollection y Window

El acceso a la clase [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) se puede obtener a través de la propiedad [Windows](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) de la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . Al utilizar la clase [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) para obtener acceso a las ventanas de un formulario, se utiliza un indizador (en Visual C#) o se transmite un número entero largo a la propiedad **Item** (en Visual Basic) para devolver una referencia a una instancia del objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) . Por ejemplo, en el código siguiente se establece una referencia al primer objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) contenido en [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) para la sesión en curso de InfoPath. 
  
```cs
Window myWindow = this.Application.Windows[0];
```

```vb
Dim myWindow As Window = Me.Application.Windows(0)
```

Se puede tener acceso a la ventana que está actualmente abierta directamente mediante la propiedad [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) de la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) , sin tener que utilizar la clase [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) , como se muestra en el siguiente ejemplo de código. 
  
```cs
Window myWindow = this.Application.ActiveWindow;
```

```vb
Dim myWindow As Window = Me.Application.ActiveWindow
```

El acceso al objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) también se puede obtener mediante la propiedad [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) de la clase [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , que representa la vista activa que se usa para trabajar con el documento XML subyacente del formulario. La propiedad [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) se utiliza para obtener acceso al objeto [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) que representa la vista activa. Por ejemplo, en el código siguiente se establece una referencia a [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) que se asocia a la vista activa. 
  
```cs
Window myWindow = this.CurrentView.Window;
```

```vb
Dim myWindow As Window = Me.CurrentView.Window
```

> [!NOTE]
> [!NOTA] Algunos de los métodos y de las propiedades de la clase [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) se utilizan sólo para editar el tipo de ventana; si se utilizan con el tipo de ventana de diseño, devolverán un error. Los métodos y propiedades que admite cada tipo de ventana se muestran en la lista de la tabla anterior. Puede utilizar la propiedad [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) en el código para averiguar con qué tipo de ventana está trabajando. 
  

