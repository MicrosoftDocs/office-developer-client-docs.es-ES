---
title: Trabajar con vistas usando el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, views,views [InfoPath 2007], InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: feb1bfcb-1cb1-4d5c-bc84-df86a33a5934
description: Cuando se trabaja con una plantilla de formulario de InfoPath, es posible escribir código para tener acceso a las vistas del formulario y, a continuación, efectuar diversas acciones con los datos que contienen. El modelo de objetos compatible con InfoPath 2003 admite el acceso a las vistas de un formulario mediante el uso de los miembros de la interfaz ViewObject .
ms.openlocfilehash: 1cbc472993ff18b26f31e3bc28b12a75e559644a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815884"
---
# <a name="work-with-views-using-the-infopath-2003-object-model"></a><span data-ttu-id="139bd-105">Trabajar con vistas usando el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="139bd-105">Work with Views Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="139bd-p102">Cuando se trabaja con una plantilla de formulario de InfoPath, es posible escribir código para tener acceso a las vistas del formulario y, a continuación, efectuar diversas acciones con los datos que contienen. El modelo de objetos compatible con InfoPath 2003 admite el acceso a las vistas de un formulario mediante el uso de los miembros de la interfaz [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="139bd-p102">When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain. The InfoPath 2003-compatible object model supports access to a form's views through the use of the members of the [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) interface.</span></span> 
  
## <a name="overview-of-the-viewobject-interface"></a><span data-ttu-id="139bd-108">Información general sobre la interfaz ViewObject</span><span class="sxs-lookup"><span data-stu-id="139bd-108">Overview of the ViewObject Interface</span></span>

<span data-ttu-id="139bd-109">La interfaz [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) proporciona el método y las propiedades siguientes que los desarrolladores de formularios pueden utilizar para interactuar con una vista de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="139bd-109">The [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) interface provides the following methods and properties, which form developers can use to interact with an InfoPath view.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="139bd-110">[!NOTA] Los métodos y las propiedades de la interfaz [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) no están disponibles durante el evento [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) .</span><span class="sxs-lookup"><span data-stu-id="139bd-110">The methods and properties of the [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) interface are not available during the [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) event.</span></span> 
  
|<span data-ttu-id="139bd-111">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="139bd-111">**Name**</span></span>|<span data-ttu-id="139bd-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="139bd-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="139bd-113">Método [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.DisableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="139bd-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.DisableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="139bd-114">Deshabilita la sincronización entre Document Object Model (DOM) XML y la vista.</span><span class="sxs-lookup"><span data-stu-id="139bd-114">Disables synchronization of the XML Document Object Model (DOM) and the view.</span></span>  <br/> |
|<span data-ttu-id="139bd-115">Método [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.EnableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="139bd-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.EnableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="139bd-116">Habilita la sincronización entre el XML DOM y la vista.</span><span class="sxs-lookup"><span data-stu-id="139bd-116">Enables synchronization of the XML DOM and the view.</span></span>  <br/> |
|<span data-ttu-id="139bd-117">Método [ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="139bd-117">[ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="139bd-118">Ejecuta una acción de edición de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="139bd-118">Executes an InfoPath editing action.</span></span>  <br/> |
|<span data-ttu-id="139bd-119">Método [Export](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Export.aspx)</span><span class="sxs-lookup"><span data-stu-id="139bd-119">[Export](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Export.aspx) method</span></span>  <br/> |<span data-ttu-id="139bd-120">Exporta la vista como archivo del formato especificado.</span><span class="sxs-lookup"><span data-stu-id="139bd-120">Exports the view as a file of the specified format.</span></span>  <br/> |
|<span data-ttu-id="139bd-121">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ForceUpdate.aspx) (método)</span><span class="sxs-lookup"><span data-stu-id="139bd-121">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ForceUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="139bd-122">Sincroniza el XML DOM y la vista.</span><span class="sxs-lookup"><span data-stu-id="139bd-122">Synchronizes the XML DOM and the view.</span></span>  <br/> |
|<span data-ttu-id="139bd-123">Método [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="139bd-123">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="139bd-124">Devuelve una referencia a la interfaz [XMLNodesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLNodesCollection.aspx) , basándose en el contexto de vista y de nodo XML especificado o en la selección actual en la vista.</span><span class="sxs-lookup"><span data-stu-id="139bd-124">Returns a reference to the [XMLNodesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLNodesCollection.aspx) interface, based on the specified XML node and view context or on the current selection in the view.</span></span>  <br/> |
|<span data-ttu-id="139bd-125">Método [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetSelectedNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="139bd-125">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetSelectedNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="139bd-126">Devuelve una referencia a la interfaz **XMLNodesCollection**, basándose en la selección actual de la vista.</span><span class="sxs-lookup"><span data-stu-id="139bd-126">Returns a reference to the **XMLNodesCollection** interface, based on the current selection in the view.</span></span>  <br/> |
|<span data-ttu-id="139bd-127">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) (método)</span><span class="sxs-lookup"><span data-stu-id="139bd-127">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="139bd-128">Selecciona un rango de nodos XML de la vista.</span><span class="sxs-lookup"><span data-stu-id="139bd-128">Selects a range of XML nodes in the view.</span></span>  <br/> |
|<span data-ttu-id="139bd-129">Método [SelectText](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="139bd-129">[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="139bd-130">Selecciona el texto contenido en el nodo XML especificado de la vista.</span><span class="sxs-lookup"><span data-stu-id="139bd-130">Selects the text contained in the specified XML node in the view.</span></span>  <br/> |
|<span data-ttu-id="139bd-131">Método [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SwitchView.aspx)</span><span class="sxs-lookup"><span data-stu-id="139bd-131">[SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SwitchView.aspx) method</span></span>  <br/> |<span data-ttu-id="139bd-132">Cambia el formulario de InfoPath a la vista especificada</span><span class="sxs-lookup"><span data-stu-id="139bd-132">Switches an InfoPath form to the specified view</span></span>  <br/> |
|<span data-ttu-id="139bd-133">[Nombre](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Name.aspx) (propiedad)</span><span class="sxs-lookup"><span data-stu-id="139bd-133">[Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Name.aspx) property</span></span>  <br/> |<span data-ttu-id="139bd-134">Devuelve un valor de cadena que indica el nombre de la vista actual.</span><span class="sxs-lookup"><span data-stu-id="139bd-134">Returns a string value indicating the name of the current view.</span></span>  <br/> |
|<span data-ttu-id="139bd-135">[Ventana](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) (propiedad)</span><span class="sxs-lookup"><span data-stu-id="139bd-135">[Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) property</span></span>  <br/> |<span data-ttu-id="139bd-136">Devuelve una referencia a la interfaz de [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) que tiene acceso a la **ventana** asociada con la vista.</span><span class="sxs-lookup"><span data-stu-id="139bd-136">Returns a reference to the [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) interface which accesses the **Window** associated with the view.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="139bd-137">[!NOTA] El modelo de objetos compatible con InfoPath 2003 también proporciona la interfaz [ViewInfosCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfosCollection.aspx) , que se puede utilizar para obtener información sobre todas las vistas implementadas en un formulario.</span><span class="sxs-lookup"><span data-stu-id="139bd-137">The InfoPath 2003-compatible object model also provides the [ViewInfosCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfosCollection.aspx) interface, which can be used to get information about all of the views implemented in a form.</span></span> 
  
## <a name="using-the-viewobject-interface"></a><span data-ttu-id="139bd-138">Uso de la interfaz ViewObject</span><span class="sxs-lookup"><span data-stu-id="139bd-138">Using the ViewObject Interface</span></span>

<span data-ttu-id="139bd-p103">El acceso a la interfaz [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) se obtiene a través de la propiedad [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) de la interfaz [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) (a la que se obtiene acceso a través de la variable  `thisXDocument` que se inicializa en el método  `_Startup` de la clase de código del formulario). Por ejemplo, el siguiente ejemplo de código muestra cómo utilizar el método [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) de la interfaz [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) para mostrar un cuadro de mensaje con el nombre de la vista actual asociada al documento XML subyacente del formulario.</span><span class="sxs-lookup"><span data-stu-id="139bd-p103">The [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) interface is accessed through the [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface (which is accessed through the  `thisXDocument` variable that is initialized in the  `_Startup` method of the form code class). For example, the following code sample demonstrates how to use the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface to display a message box with the name of the current view that is associated with a form's underlying XML document.</span></span> 
  
```cs
thisXDocument.UI.Alert("Current view name: " + 
   thisXDocument.View.Name);
```

```vb
thisXDocument.UI.Alert("Current view name: " &amp; _
   thisXDocument.View.Name)
```

<span data-ttu-id="139bd-p104">Todos los formularios de InfoPath contienen al menos una vista predeterminada; sin embargo, InfoPath admite también la creación de varias vistas del documento XML subyacente de un formulario. Cuando un formulario tiene varias vistas, el objeto **View** se puede utilizar para trabajar con la que esté activa. Es posible cambiar mediante programación la vista activa utilizando el método **SwitchView** del objeto **View**, como demuestra el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="139bd-p104">All InfoPath forms contain at least one default view; however, InfoPath also supports the creation of multiple views of a form's underlying XML document. When you have multiple views in a form, the **View** object can be used to work with the view that is currently active. You can programmatically change the view that is currently active by using the **SwitchView** method of the **View** object, as the following code sample demonstrates.</span></span> 
  
```cs
thisXDocument.View.SwitchView("MySecondView");
```

```vb
thisXDocument.View.SwitchView("MySecondView")
```

<span data-ttu-id="139bd-p105">El ejemplo anterior (cambiar a una vista) sólo funcionará una vez abierto el formulario. Para establecer una vista predeterminada durante el evento **OnLoad**, utilice la propiedad [IsDefault](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.IsDefault.aspx) de la interfaz [ViewInfoObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfoObject.aspx) , como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="139bd-p105">The previous example for switching a view will work only after the form is opened. To set a default view during the **OnLoad** event, use the [IsDefault](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.IsDefault.aspx) property of the [ViewInfoObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfoObject.aspx) interface, as shown in the following example.</span></span> 
  
```cs
thisXDocument.ViewInfos["MyDefaultView"].IsDefault = true;
```

```vb
thisXDocument.ViewInfos("MyDefaultView").IsDefault = True
```

