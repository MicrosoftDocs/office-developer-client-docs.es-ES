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
# <a name="work-with-views"></a><span data-ttu-id="73cc8-105">Trabajar con vistas</span><span class="sxs-lookup"><span data-stu-id="73cc8-105">Work with Views</span></span>

<span data-ttu-id="73cc8-p102">Cuando se trabaja con una plantilla de formulario de InfoPath, es posible escribir código para tener acceso a las vistas del formulario y, a continuación, efectuar diversas acciones con los datos contenidos en ellas. El modelo de objetos de InfoPath que proporciona el espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) admite el acceso a las vistas de los formularios mediante el uso de los miembros de la clase [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) .</span><span class="sxs-lookup"><span data-stu-id="73cc8-p102">When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain. The InfoPath object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace supports access to a form's views through the use of the members of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class.</span></span> 
  
## <a name="overview-of-the-view-class"></a><span data-ttu-id="73cc8-108">Información general sobre la clase View</span><span class="sxs-lookup"><span data-stu-id="73cc8-108">Overview of the View Class</span></span>

<span data-ttu-id="73cc8-109">La clase [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) proporciona el método y las propiedades siguientes que los programadores de formularios pueden utilizar para interactuar con una vista de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="73cc8-109">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class provides the following methods and properties, which form developers can use to interact with an InfoPath view.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="73cc8-110">[!NOTA] Los métodos y las propiedades de la clase [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) no están disponibles durante el evento [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) .</span><span class="sxs-lookup"><span data-stu-id="73cc8-110">The methods and properties of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class are not available during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
|<span data-ttu-id="73cc8-111">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="73cc8-111">**Name**</span></span>|<span data-ttu-id="73cc8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="73cc8-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73cc8-113">Método [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="73cc8-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-114">Deshabilita la sincronización automática entre el documento XML subyacente de un formulario y la vista asociada.</span><span class="sxs-lookup"><span data-stu-id="73cc8-114">Disables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="73cc8-115">Método [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="73cc8-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-116">Habilita la sincronización automática entre el documento XML subyacente de un formulario y la vista asociada.</span><span class="sxs-lookup"><span data-stu-id="73cc8-116">Enables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="73cc8-117">[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) (método)</span><span class="sxs-lookup"><span data-stu-id="73cc8-117">[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-118">Ejecuta un comando de edición en el documento XML subyacente de un formulario, de acuerdo con los datos seleccionados actualmente en la vista.</span><span class="sxs-lookup"><span data-stu-id="73cc8-118">Executes an editing command against a form's underlying XML document, based on the data currently selected in the view.</span></span>  <br/> |
|<span data-ttu-id="73cc8-119">Método [ExecuteAction (ActionType, cadena)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="73cc8-119">[ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-120">Ejecuta un comando de edición en el documento XML subyacente de un formulario, en función del campo o grupo especificados.</span><span class="sxs-lookup"><span data-stu-id="73cc8-120">Executes an editing command against a form's underlying XML document, based on the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="73cc8-121">Método [Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)</span><span class="sxs-lookup"><span data-stu-id="73cc8-121">[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-122">Exporta la vista a un archivo con el formato especificado.</span><span class="sxs-lookup"><span data-stu-id="73cc8-122">Exports the view to a file of the specified format.</span></span>  <br/> |
|<span data-ttu-id="73cc8-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) (método)</span><span class="sxs-lookup"><span data-stu-id="73cc8-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-124">Fuerza la sincronización automática entre el documento XML subyacente de un formulario y la vista asociada.</span><span class="sxs-lookup"><span data-stu-id="73cc8-124">Forces synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="73cc8-125">[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) (método)</span><span class="sxs-lookup"><span data-stu-id="73cc8-125">[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-126">Obtiene una referencia a un objeto **XPathNodeIterator** para realizar una iteración en los nodos XML devueltos, empezando en el nodo especificado.</span><span class="sxs-lookup"><span data-stu-id="73cc8-126">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes starting from the specified node.</span></span>  <br/> |
|<span data-ttu-id="73cc8-127">Método [GetContextNodes (XPathNavigator, cadena)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="73cc8-127">[GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-128">Obtiene una referencia a un objeto **XPathNodeIterator** para recorrer en iteración los nodos XML devueltos de la selección actual dentro del control enlazado al control especificado.</span><span class="sxs-lookup"><span data-stu-id="73cc8-128">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes in the current selection within the control bound to the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="73cc8-129">Método [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="73cc8-129">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-130">Obtiene una referencia a un objeto **XPathNodeIterator** para recorrer en iteración todos los nodos XML de los elementos seleccionados de una vista.</span><span class="sxs-lookup"><span data-stu-id="73cc8-130">Gets a reference to an **XPathNodeIterator** object for iterating over all XML nodes in the current selection of items in a view.</span></span>  <br/> |
|<span data-ttu-id="73cc8-131">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) (método)</span><span class="sxs-lookup"><span data-stu-id="73cc8-131">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-132">Selecciona un intervalo de nodos en una vista partiendo del nodo XML inicial especificado.</span><span class="sxs-lookup"><span data-stu-id="73cc8-132">Selects a range of nodes in a view based on the specified starting XML node.</span></span>  <br/> |
|<span data-ttu-id="73cc8-133">Método [SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="73cc8-133">[SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-134">Selecciona un intervalo de nodos en una vista partiendo del nodo XML inicial especificado y terminando en el nodo XML final.</span><span class="sxs-lookup"><span data-stu-id="73cc8-134">Selects a range of nodes in a view based on the specified starting XML node and ending XML node.</span></span>  <br/> |
|<span data-ttu-id="73cc8-135">Método [SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="73cc8-135">[SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-136">Selecciona un intervalo de nodos de una vista partiendo del nodo XML inicial especificado, terminando en el nodo XML final y en el control especificado.</span><span class="sxs-lookup"><span data-stu-id="73cc8-136">Selects a range of nodes in a view based on the specified starting XML node, the ending XML node, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="73cc8-137">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) (método)</span><span class="sxs-lookup"><span data-stu-id="73cc8-137">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-138">Selecciona el texto que se encuentra en un control modificable enlazado al nodo especificado por el objeto **XPathNavigator** pasado a este método.</span><span class="sxs-lookup"><span data-stu-id="73cc8-138">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method.</span></span>  <br/> |
|<span data-ttu-id="73cc8-139">Método [SelectText (XPathNavigator, cadena)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="73cc8-139">[SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-140">Selecciona el texto que se encuentra en un control modificable enlazado al nodo especificado por el objeto **XPathNavigator** pasado a este método y el control especificado.</span><span class="sxs-lookup"><span data-stu-id="73cc8-140">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="73cc8-141">Método [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)</span><span class="sxs-lookup"><span data-stu-id="73cc8-141">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) method</span></span>  <br/> |<span data-ttu-id="73cc8-142">Crea un mensaje de correo electrónico que contiene la vista actual.</span><span class="sxs-lookup"><span data-stu-id="73cc8-142">Creates an email message containing the current view.</span></span>  <br/> |
|<span data-ttu-id="73cc8-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) (propiedad)</span><span class="sxs-lookup"><span data-stu-id="73cc8-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) property</span></span>  <br/> |<span data-ttu-id="73cc8-144">Obtiene una referencia a un objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) asociado a la vista.</span><span class="sxs-lookup"><span data-stu-id="73cc8-144">Gets a reference to a [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span>  <br/> |
|<span data-ttu-id="73cc8-145">[Ventana](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) (propiedad)</span><span class="sxs-lookup"><span data-stu-id="73cc8-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) property</span></span>  <br/> |<span data-ttu-id="73cc8-146">Obtiene una referencia a un objeto [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) asociado a la vista.</span><span class="sxs-lookup"><span data-stu-id="73cc8-146">Gets a reference to a [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) object associated with the view.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="73cc8-147">[!NOTA] El modelo de objetos de InfoPath también proporciona las clases [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) y [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , que se pueden usar para conseguir información sobre todas las vistas implementadas en un formulario.</span><span class="sxs-lookup"><span data-stu-id="73cc8-147">The InfoPath object model also provides the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) and [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) classes, which can be used to get information about all of the views implemented in a form.</span></span> 
  
## <a name="using-the-view-class"></a><span data-ttu-id="73cc8-148">Uso de la clase View</span><span class="sxs-lookup"><span data-stu-id="73cc8-148">Using the View Class</span></span>

<span data-ttu-id="73cc8-p103">Se tiene acceso a la clase [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) a través de la propiedad [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , a la que se tiene acceso mediante la palabra clave **this** (C#) o **Me** (Visual Basic). Para obtener acceso al nombre de la vista, debe tener acceso al objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) asociado a la vista. En el siguiente ejemplo se muestra cómo mostrar un cuadro de mensaje con el nombre de la vista que está actualmente activa.</span><span class="sxs-lookup"><span data-stu-id="73cc8-p103">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class is accessed through the [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class, which is accessed using the **this** (C#) or **Me** (Visual Basic) keyword. To access the name of the view, you need to access the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view. The following example demonstrates how to display a message box with the name of the view that is currently active.</span></span> 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

<span data-ttu-id="73cc8-p104">Todas las plantillas de formulario de InfoPath contienen al menos una vista predeterminada; sin embargo, InfoPath admite también la creación de varias vistas del documento XML subyacente de un formulario. Cuando tiene varias vistas, puede usar [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) para trabajar con todas las vistas implementadas en la plantilla de formulario. Para tener acceso a la [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) de una plantilla de formulario, use la propiedad [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Puede cambiar mediante programación la vista activa usando el método [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) de [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , como se muestra en el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="73cc8-p104">All InfoPath form templates contain at least one default view; however, InfoPath also supports the creation of multiple views of a form's underlying XML document. When you have multiple views, the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) can be used to work with all of the views implemented in the form template. To access the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) of a form template, use the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class. You can programmatically change the view that is currently active by using the [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) method of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , as the following code sample demonstrates.</span></span> 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

<span data-ttu-id="73cc8-p105">El ejemplo anterior (cambiar de vista) solo funcionará una vez abierto el formulario. Para establecer una vista predeterminada durante el evento [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , use la propiedad [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) de la clase [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) como se muestra en el siguiente ejemplo. Observe, sin embargo, que este valor sólo surtirá efecto después de que se haya cerrado y abierto de nuevo el formulario.</span><span class="sxs-lookup"><span data-stu-id="73cc8-p105">The previous example for switching a view will work only after the form is opened. To set a default view during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, use the [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) property of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) class as shown in the following example. Note, however, that this value will only take effect after the form is saved and re-opened.</span></span> 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a><span data-ttu-id="73cc8-159">Seleccionar controles en una vista</span><span class="sxs-lookup"><span data-stu-id="73cc8-159">Selecting Controls in a View</span></span>

<span data-ttu-id="73cc8-p106">InfoPath proporciona dos métodos de la clase [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) . Ambos están sobrecargados para seleccionar mediante programación un control en la vista actual: los métodos [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) y [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) . El método [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) se usa para los controles de entrada de datos, como **Cuadro de texto**, y el método **SelectNodes** se usa para controles estructurales, como **Sección opcional**. Para seleccionar un control específico en la vista, debe proporcionar el nodo y, de manera opcional, el identificador de ViewContext del control. El identificador de ViewContext es necesario cuando hay varios controles dependientes del mismo nodo del origen de datos. InfoPath proporciona la información del identificador de ViewContext al diseñar el formulario.</span><span class="sxs-lookup"><span data-stu-id="73cc8-p106">InfoPath provides two methods of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class, both of which are overloaded, to programmatically select a control in the current view: the [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) and [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods. The [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method is used for data entry controls, such as a **Text Box**, while the **SelectNodes** method is used for structural controls, such as an **Optional Section**. To select a particular control in the view, you need to provide the node and, optionally, the control's ViewContext ID. The ViewContext ID is needed when you have multiple controls bound to the same node in the data source. InfoPath provides the ViewContext ID information when you design the form.</span></span>
  
<span data-ttu-id="73cc8-165">El identificador de ViewContext de un control se muestra en la ficha **Avanzadas** del cuadro de diálogo de propiedades del control. Para obtener acceso a este cuadro de diálogo, haga clic con el botón secundario del mouse en el control, haga clic en _Propiedades_ de  **nombreDeControl** y después haga clic en la pestaña **Avanzadas**. El identificador de ViewContext del control aparece en la sección **Código** de la ficha **Avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="73cc8-165">A control's ViewContext ID is displayed on the **Advanced** tab of the control's properties dialog box, which is accessed by right-clicking the control, clicking  _ControlName_ **Properties**, and then clicking the **Advanced** tab. The ViewContext ID of the control is listed in the **Code** section of the **Advanced** tab.</span></span> 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a><span data-ttu-id="73cc8-166">Cuándo utilizar SelectText y SelectNodes</span><span class="sxs-lookup"><span data-stu-id="73cc8-166">When to use SelectText and SelectNodes</span></span>

<span data-ttu-id="73cc8-167">Es posible seleccionar mediante programación los siguientes controles de entrada de datos mediante el método [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) :</span><span class="sxs-lookup"><span data-stu-id="73cc8-167">You can programmatically select the following data entry controls by using the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method:</span></span> 
  
- <span data-ttu-id="73cc8-168">Cuadro de texto</span><span class="sxs-lookup"><span data-stu-id="73cc8-168">Text Box</span></span>
    
- <span data-ttu-id="73cc8-169">Cuadro de texto enriquecido</span><span class="sxs-lookup"><span data-stu-id="73cc8-169">Rich Text Box</span></span>
    
- <span data-ttu-id="73cc8-170">Selector de fecha</span><span class="sxs-lookup"><span data-stu-id="73cc8-170">Date Picker</span></span>
    
<span data-ttu-id="73cc8-171">Es posible seleccionar los siguientes controles estructurales mediante programación utilizando el método [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) :</span><span class="sxs-lookup"><span data-stu-id="73cc8-171">You can programmatically select the following structural controls by using the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method:</span></span> 
  
- <span data-ttu-id="73cc8-172">Sección opcional</span><span class="sxs-lookup"><span data-stu-id="73cc8-172">Optional Section</span></span>
    
- <span data-ttu-id="73cc8-173">Sección de opciones</span><span class="sxs-lookup"><span data-stu-id="73cc8-173">Choice Section</span></span>
    
- <span data-ttu-id="73cc8-174">Sección extensible (elementos)</span><span class="sxs-lookup"><span data-stu-id="73cc8-174">Repeating Section (items)</span></span>
    
- <span data-ttu-id="73cc8-175">Tabla extensible (filas)</span><span class="sxs-lookup"><span data-stu-id="73cc8-175">Repeating Table (rows)</span></span>
    
- <span data-ttu-id="73cc8-176">Sección recursiva extensible</span><span class="sxs-lookup"><span data-stu-id="73cc8-176">Repeating Recursive Section (items)</span></span>
    
- <span data-ttu-id="73cc8-177">Lista con viñetas, numerada y simple</span><span class="sxs-lookup"><span data-stu-id="73cc8-177">Bulleted, Numbered, and Plain List</span></span>
    
- <span data-ttu-id="73cc8-178">Tabla extensible horizontal</span><span class="sxs-lookup"><span data-stu-id="73cc8-178">Horizontal Repeating Table</span></span>
    
<span data-ttu-id="73cc8-179">No es posible seleccionar mediante programación ni establecer el foco en los controles siguientes:</span><span class="sxs-lookup"><span data-stu-id="73cc8-179">You cannot programmatically select, or set focus to, the following controls:</span></span>
  
- <span data-ttu-id="73cc8-180">Cuadro de lista desplegable</span><span class="sxs-lookup"><span data-stu-id="73cc8-180">Drop-Down List Box</span></span>
    
- <span data-ttu-id="73cc8-181">Cuadro de lista</span><span class="sxs-lookup"><span data-stu-id="73cc8-181">List Box</span></span>
    
- <span data-ttu-id="73cc8-182">Casilla de verificación</span><span class="sxs-lookup"><span data-stu-id="73cc8-182">Check Box</span></span>
    
- <span data-ttu-id="73cc8-183">Botón de opción</span><span class="sxs-lookup"><span data-stu-id="73cc8-183">Option Button</span></span>
    
- <span data-ttu-id="73cc8-184">Botón</span><span class="sxs-lookup"><span data-stu-id="73cc8-184">Button</span></span>
    
- <span data-ttu-id="73cc8-185">Imagen (vinculada o incorporada)</span><span class="sxs-lookup"><span data-stu-id="73cc8-185">Picture (linked or included)</span></span>
    
- <span data-ttu-id="73cc8-186">Imagen de lápiz</span><span class="sxs-lookup"><span data-stu-id="73cc8-186">Ink Picture</span></span>
    
- <span data-ttu-id="73cc8-187">Hipervínculo</span><span class="sxs-lookup"><span data-stu-id="73cc8-187">Hyperlink</span></span>
    
- <span data-ttu-id="73cc8-188">Cuadro de expresión</span><span class="sxs-lookup"><span data-stu-id="73cc8-188">Expression Box</span></span>
    
- <span data-ttu-id="73cc8-189">Etiqueta vertical</span><span class="sxs-lookup"><span data-stu-id="73cc8-189">Vertical Label</span></span>
    
- <span data-ttu-id="73cc8-190">Sección de ActiveX</span><span class="sxs-lookup"><span data-stu-id="73cc8-190">ActiveX Section</span></span>
    
- <span data-ttu-id="73cc8-191">Zona horizontal</span><span class="sxs-lookup"><span data-stu-id="73cc8-191">Horizontal Region</span></span>
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a><span data-ttu-id="73cc8-192">Utilizar los métodos SelectText y SelectNodes</span><span class="sxs-lookup"><span data-stu-id="73cc8-192">Using the SelectText and SelectNodes Methods</span></span>

<span data-ttu-id="73cc8-193">En el siguiente ejemplo, la sobrecarga de [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) del método **SelectText**, que proporciona un parámetro  _xmlNode_, se usa para seleccionar un **cuadro de texto** dependiente de "my:field1".</span><span class="sxs-lookup"><span data-stu-id="73cc8-193">In the following example, the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides one  _xmlNode_ parameter, is used to select a **Text Box** that is bound to "my:field1".</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

<span data-ttu-id="73cc8-p107">Si tiene varios controles dependientes de "my:field1", debe usar la sobrecarga de [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) del método **SelectText**, que proporciona un parámetro de  _viewContext_ adicional para seleccionar un control determinado. El ejemplo siguiente da por supuesto que hay dos controles **Cuadro de texto** dependientes de "my:field1". El identificador de ViewContext del primer control es "CTRL1" y el identificador de ViewContext del segundo control es "CTRL8". El segundo control está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="73cc8-p107">If you have multiple controls bound to "my:field1", you must use the [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides an additional  _viewContext_ parameter to select a specific control. The following example assumes that there are two **Text Box** controls bound to "my:field1", with the first control having a ViewContext ID of "CTRL1" and the second control having a ViewContext ID of "CTRL8". The second control is selected.</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

<span data-ttu-id="73cc8-197">En el ejemplo siguiente, la sobrecarga de [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) del método **SelectNodes**, que proporciona sólo un parámetro de  _startNode_, se utiliza para seleccionar la primera fila de una tabla extensible dependiente del grupo extensible "my:employee".</span><span class="sxs-lookup"><span data-stu-id="73cc8-197">In the following example, the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides only one  _startNode_ parameter, is used to select the first row in a repeating table bound to the repeating group "my:employee".</span></span> 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

<span data-ttu-id="73cc8-p108">También es posible seleccionar varias filas en una tabla extensible. En el ejemplo siguiente, las tres primeras filas de una tabla extensible dependiente del grupo extensible "my:employee" se seleccionan mediante la sobrecarga de [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) del método de **SelectNodes**, que proporciona los parámetros  _startNode_ y  _endNode_:</span><span class="sxs-lookup"><span data-stu-id="73cc8-p108">You can also select multiple rows in a repeating table. In the following example, the first three rows of a repeating table bound to the repeating group "my:employee" are selected using the [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides  _startNode_ and  _endNode_ parameters:</span></span> 
  
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


