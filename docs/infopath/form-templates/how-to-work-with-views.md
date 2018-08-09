---
title: Trabajar con vistas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- view class [infopath 2007],InfoPath 2007, working with views,views [InfoPath 2007]
localization_priority: Normal
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: Cuando se trabaja con una plantilla de formulario de InfoPath, es posible escribir código para tener acceso a las vistas del formulario y, a continuación, efectuar diversas acciones con los datos contenidos en ellas. El modelo de objetos de InfoPath que proporciona el espacio de nombres Microsoft.Office.InfoPath admite el acceso a las vistas de los formularios mediante el uso de los miembros de la clase View .
ms.openlocfilehash: 84c32244454e388e50433922c007d556fbef806a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815899"
---
# <a name="work-with-views"></a>Trabajar con vistas

Cuando se trabaja con una plantilla de formulario de InfoPath, es posible escribir código para tener acceso a las vistas del formulario y, a continuación, efectuar diversas acciones con los datos contenidos en ellas. El modelo de objetos de InfoPath que proporciona el espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) admite el acceso a las vistas de los formularios mediante el uso de los miembros de la clase [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) . 
  
## <a name="overview-of-the-view-class"></a>Información general sobre la clase View

La clase [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) proporciona el método y las propiedades siguientes que los programadores de formularios pueden utilizar para interactuar con una vista de InfoPath. 
  
> [!NOTE]
> [!NOTA] Los métodos y las propiedades de la clase [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) no están disponibles durante el evento [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) . 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|Método [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)  <br/> |Deshabilita la sincronización automática entre el documento XML subyacente de un formulario y la vista asociada.  <br/> |
|Método [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)  <br/> |Habilita la sincronización automática entre el documento XML subyacente de un formulario y la vista asociada.  <br/> |
|[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) (método)  <br/> |Ejecuta un comando de edición en el documento XML subyacente de un formulario, de acuerdo con los datos seleccionados actualmente en la vista.  <br/> |
|Método [ExecuteAction (ActionType, cadena)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Ejecuta un comando de edición en el documento XML subyacente de un formulario, en función del campo o grupo especificados.  <br/> |
|Método [Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)  <br/> |Exporta la vista a un archivo con el formato especificado.  <br/> |
|[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) (método)  <br/> |Fuerza la sincronización automática entre el documento XML subyacente de un formulario y la vista asociada.  <br/> |
|[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) (método)  <br/> |Obtiene una referencia a un objeto **XPathNodeIterator** para realizar una iteración en los nodos XML devueltos, empezando en el nodo especificado.  <br/> |
|Método [GetContextNodes (XPathNavigator, cadena)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Obtiene una referencia a un objeto **XPathNodeIterator** para recorrer en iteración los nodos XML devueltos de la selección actual dentro del control enlazado al control especificado.  <br/> |
|Método [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |Obtiene una referencia a un objeto **XPathNodeIterator** para recorrer en iteración todos los nodos XML de los elementos seleccionados de una vista.  <br/> |
|[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) (método)  <br/> |Selecciona un intervalo de nodos en una vista partiendo del nodo XML inicial especificado.  <br/> |
|Método [SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Selecciona un intervalo de nodos en una vista partiendo del nodo XML inicial especificado y terminando en el nodo XML final.  <br/> |
|Método [SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Selecciona un intervalo de nodos de una vista partiendo del nodo XML inicial especificado, terminando en el nodo XML final y en el control especificado.  <br/> |
|[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) (método)  <br/> |Selecciona el texto que se encuentra en un control modificable enlazado al nodo especificado por el objeto **XPathNavigator** pasado a este método.  <br/> |
|Método [SelectText (XPathNavigator, cadena)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Selecciona el texto que se encuentra en un control modificable enlazado al nodo especificado por el objeto **XPathNavigator** pasado a este método y el control especificado.  <br/> |
|Método [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)  <br/> |Crea un mensaje de correo electrónico que contiene la vista actual.  <br/> |
|[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) (propiedad)  <br/> |Obtiene una referencia a un objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) asociado a la vista.  <br/> |
|[Ventana](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) (propiedad)  <br/> |Obtiene una referencia a un objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) asociado a la vista.  <br/> |
   
> [!NOTE]
> [!NOTA] El modelo de objetos de InfoPath también proporciona las clases [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) y [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , que se pueden usar para conseguir información sobre todas las vistas implementadas en un formulario. 
  
## <a name="using-the-view-class"></a>Uso de la clase View

Se tiene acceso a la clase [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) a través de la propiedad [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , a la que se tiene acceso mediante la palabra clave **this** (C#) o **Me** (Visual Basic). Para obtener acceso al nombre de la vista, debe tener acceso al objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) asociado a la vista. En el siguiente ejemplo se muestra cómo mostrar un cuadro de mensaje con el nombre de la vista que está actualmente activa. 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

Todas las plantillas de formulario de InfoPath contienen al menos una vista predeterminada; sin embargo, InfoPath admite también la creación de varias vistas del documento XML subyacente de un formulario. Cuando tiene varias vistas, puede usar [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) para trabajar con todas las vistas implementadas en la plantilla de formulario. Para tener acceso a la [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) de una plantilla de formulario, use la propiedad [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Puede cambiar mediante programación la vista activa usando el método [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) de [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , como se muestra en el siguiente ejemplo de código. 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

El ejemplo anterior (cambiar de vista) solo funcionará una vez abierto el formulario. Para establecer una vista predeterminada durante el evento [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , use la propiedad [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) de la clase [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) como se muestra en el siguiente ejemplo. Observe, sin embargo, que este valor sólo surtirá efecto después de que se haya cerrado y abierto de nuevo el formulario. 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a>Seleccionar controles en una vista

InfoPath proporciona dos métodos de la clase [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) . Ambos están sobrecargados para seleccionar mediante programación un control en la vista actual: los métodos [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) y [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) . El método [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) se usa para los controles de entrada de datos, como **Cuadro de texto**, y el método **SelectNodes** se usa para controles estructurales, como **Sección opcional**. Para seleccionar un control específico en la vista, debe proporcionar el nodo y, de manera opcional, el identificador de ViewContext del control. El identificador de ViewContext es necesario cuando hay varios controles dependientes del mismo nodo del origen de datos. InfoPath proporciona la información del identificador de ViewContext al diseñar el formulario.
  
El identificador de ViewContext de un control se muestra en la ficha **Avanzadas** del cuadro de diálogo de propiedades del control. Para obtener acceso a este cuadro de diálogo, haga clic con el botón secundario del mouse en el control, haga clic en _Propiedades_ de  **nombreDeControl** y después haga clic en la pestaña **Avanzadas**. El identificador de ViewContext del control aparece en la sección **Código** de la ficha **Avanzadas**. 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a>Cuándo utilizar SelectText y SelectNodes

Es posible seleccionar mediante programación los siguientes controles de entrada de datos mediante el método [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) : 
  
- Cuadro de texto
    
- Cuadro de texto enriquecido
    
- Selector de fecha
    
Es posible seleccionar los siguientes controles estructurales mediante programación utilizando el método [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) : 
  
- Sección opcional
    
- Sección de opciones
    
- Sección extensible (elementos)
    
- Tabla extensible (filas)
    
- Sección recursiva extensible
    
- Lista con viñetas, numerada y simple
    
- Tabla extensible horizontal
    
No es posible seleccionar mediante programación ni establecer el foco en los controles siguientes:
  
- Cuadro de lista desplegable
    
- Cuadro de lista
    
- Casilla de verificación
    
- Botón de opción
    
- Botón
    
- Imagen (vinculada o incorporada)
    
- Imagen de lápiz
    
- Hipervínculo
    
- Cuadro de expresión
    
- Etiqueta vertical
    
- Sección de ActiveX
    
- Zona horizontal
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a>Utilizar los métodos SelectText y SelectNodes

En el siguiente ejemplo, la sobrecarga de [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) del método **SelectText**, que proporciona un parámetro  _xmlNode_, se usa para seleccionar un **cuadro de texto** dependiente de "my:field1". 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

Si tiene varios controles dependientes de "my:field1", debe usar la sobrecarga de [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) del método **SelectText**, que proporciona un parámetro de  _viewContext_ adicional para seleccionar un control determinado. El ejemplo siguiente da por supuesto que hay dos controles **Cuadro de texto** dependientes de "my:field1". El identificador de ViewContext del primer control es "CTRL1" y el identificador de ViewContext del segundo control es "CTRL8". El segundo control está seleccionado. 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

En el ejemplo siguiente, la sobrecarga de [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) del método **SelectNodes**, que proporciona sólo un parámetro de  _startNode_, se utiliza para seleccionar la primera fila de una tabla extensible dependiente del grupo extensible "my:employee". 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

También es posible seleccionar varias filas en una tabla extensible. En el ejemplo siguiente, las tres primeras filas de una tabla extensible dependiente del grupo extensible "my:employee" se seleccionan mediante la sobrecarga de [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) del método de **SelectNodes**, que proporciona los parámetros  _startNode_ y  _endNode_: 
  
```cs
// Create XPathNavigators to specify range of nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
XPathNavigator repeatingTableRow3 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:myemployee[3]", NamespaceManager);
// Select range of nodes in specified XPathNavigators.
CurrentView.SelectNodes(repeatingTableRow1, repeatingTableRow3);
```


