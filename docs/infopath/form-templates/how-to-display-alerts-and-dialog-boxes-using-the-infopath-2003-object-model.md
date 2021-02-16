---
title: Mostrar alertas y cuadros de diálogo con el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, displaying dialog boxes,form templates [InfoPath 2007], displaying dialog boxes,alerts, displaying in InfoPath 2003-compatible form templates,dialog boxes, displaying in InfoPath 2003-compatible form templates,InfoPath 2003-compatible form templates, displaying alerts
localization_priority: Normal
ms.assetid: 721ac58e-56d9-4e3b-93f1-849e0c94d010
description: Cuando se escribe código para ampliar la funcionalidad de una plantilla de formulario que utiliza el modelo de objetos de InfoPath 2003, con frecuencia resulta útil proporcionar al usuario información en un cuadro de diálogo.
ms.openlocfilehash: 12088747250037e53a3b7d8d0577936e30d6292c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409485"
---
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a><span data-ttu-id="41ce4-104">Mostrar alertas y cuadros de diálogo con el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="41ce4-104">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="41ce4-p101">Cuando se escribe código para ampliar la funcionalidad de una plantilla de formulario que utiliza el modelo de objetos de InfoPath 2003, con frecuencia resulta útil proporcionar al usuario información en un cuadro de diálogo. Para mostrar mediante programación un cuadro de diálogo y los elementos relacionados de la interfaz de usuario en InfoPath, se utilizan los métodos de la interfaz [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="41ce4-p101">When writing code to extend the functionality of a form template that uses the InfoPath 2003 object model, it is often useful to provide the user with information in a dialog box. Programmatically displaying a dialog box and related user interface elements is accomplished in InfoPath by using the methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
## <a name="overview-of-the-uiobject-interface"></a><span data-ttu-id="41ce4-107">Información general sobre la interfaz UIObject</span><span class="sxs-lookup"><span data-stu-id="41ce4-107">Overview of the UIObject Interface</span></span>

<span data-ttu-id="41ce4-108">La interfaz [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) proporciona los siguientes métodos que los programadores de formularios pueden utilizar para mostrar distintos tipos de cuadros de diálogo a los usuarios de InfoPath mientras rellenan un formulario.</span><span class="sxs-lookup"><span data-stu-id="41ce4-108">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface provides the following methods, which form developers can use to have different types of dialog boxes displayed to InfoPath users as they are filling out a form.</span></span> 
  
|<span data-ttu-id="41ce4-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="41ce4-109">Name</span></span>|<span data-ttu-id="41ce4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="41ce4-110">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41ce4-111">Alerta</span><span class="sxs-lookup"><span data-stu-id="41ce4-111">Alert</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |<span data-ttu-id="41ce4-p102">Muestra un cuadro de mensaje sencillo que contiene una cadena de mensaje especificada. Utilice este método si no necesita obtener información del usuario y sólo desea mostrar un mensaje. El cuadro de diálogo que se muestra se cierra haciendo clic en el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="41ce4-p102">Displays a simple message box that contains a specified message string. This method should be used when no input is required from the user and only a message needs to be displayed. The dialog box displayed is closed by clicking the **OK** button.  </span></span><br/> |
|[<span data-ttu-id="41ce4-115">Confirm</span><span class="sxs-lookup"><span data-stu-id="41ce4-115">Confirm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |<span data-ttu-id="41ce4-116">Muestra un cuadro de mensaje con botones para obtener información de un usuario.</span><span class="sxs-lookup"><span data-stu-id="41ce4-116">Displays a message box with buttons for input from a user.</span></span> <span data-ttu-id="41ce4-117">El valor que se devuelve es una de las constantes enumeradas [XdConfirmChoice.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx)</span><span class="sxs-lookup"><span data-stu-id="41ce4-117">The value that is returned is one of the [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) enumerated constants.</span></span>  <br/> |
|[<span data-ttu-id="41ce4-118">SetSaveAsDialogFileName</span><span class="sxs-lookup"><span data-stu-id="41ce4-118">SetSaveAsDialogFileName</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |<span data-ttu-id="41ce4-119">Establece el nombre de archivo predeterminado de un formulario en el cuadro de diálogo **Guardar como**.</span><span class="sxs-lookup"><span data-stu-id="41ce4-119">Sets the default file name for a form in the **Save As** dialog box.</span></span>  <br/> |
|[<span data-ttu-id="41ce4-120">SetSaveAsDialogLocation</span><span class="sxs-lookup"><span data-stu-id="41ce4-120">SetSaveAsDialogLocation</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |<span data-ttu-id="41ce4-121">Establece la ubicación inicial desde la que empieza a examinar el cuadro de diálogo **Guardar como** al abrirlo.</span><span class="sxs-lookup"><span data-stu-id="41ce4-121">Sets the initial location at which the **Save As** dialog box starts to browse when it is opened.</span></span>  <br/> |
|[<span data-ttu-id="41ce4-122">ShowMailItem</span><span class="sxs-lookup"><span data-stu-id="41ce4-122">ShowMailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |<span data-ttu-id="41ce4-123">Crea un nuevo mensaje de correo electrónico en la aplicación de correo electrónico predeterminada, con el formulario abierto actualmente adjunto al mensaje.</span><span class="sxs-lookup"><span data-stu-id="41ce4-123">Creates a new email message in the default email application, with the currently open form attached to the message.</span></span>  <br/> |
|[<span data-ttu-id="41ce4-124">ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="41ce4-124">ShowModalDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |<span data-ttu-id="41ce4-125">Muestra un cuadro de diálogo modal basado en el archivo .html especificado y en los argumentos posicionales.</span><span class="sxs-lookup"><span data-stu-id="41ce4-125">Displays a modal dialog box, based on the specified .html file and positional arguments.</span></span> <span data-ttu-id="41ce4-126">Este método debe usarse si desea mostrar más que un mensaje simple al usuario y necesita recuperar algunos datos  del usuario (más allá de la simple confirmación proporcionada por el sí</span><span class="sxs-lookup"><span data-stu-id="41ce4-126">This method should be used if you want to display more than a simple message to the user and you need to get back some data from the user (beyond the simple confirmation that is provided by the **Yes**</span></span> | <span data-ttu-id="41ce4-127">**No**</span><span class="sxs-lookup"><span data-stu-id="41ce4-127">**No**</span></span> | <span data-ttu-id="41ce4-128">**Botones** de cancelación mostrados por el **método Confirm).**</span><span class="sxs-lookup"><span data-stu-id="41ce4-128">**Cancel** buttons displayed by the **Confirm** method).</span></span>  <br/> |
|[<span data-ttu-id="41ce4-129">ShowSignatureDialog</span><span class="sxs-lookup"><span data-stu-id="41ce4-129">ShowSignatureDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |<span data-ttu-id="41ce4-130">Muestra el cuadro de diálogo integrado **Firmas digitales**.</span><span class="sxs-lookup"><span data-stu-id="41ce4-130">Displays the built-in **Digital Signatures** dialog box.</span></span>  <br/> |
   
## <a name="using-the-uiobject-interface"></a><span data-ttu-id="41ce4-131">Uso de la interfaz UIObject</span><span class="sxs-lookup"><span data-stu-id="41ce4-131">Using the UIObject Interface</span></span>

<span data-ttu-id="41ce4-p105">El acceso a la interfaz [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) se obtiene mediante la propiedad [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) de la interfaz [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , a la que a su vez se obtiene acceso mediante la variable  `thisXDocument` que se inicializa en el método  `_Startup` de la clase de código de formulario. En el siguiente ejemplo, se muestra el uso de los métodos [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) y [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) de la interfaz [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) :</span><span class="sxs-lookup"><span data-stu-id="41ce4-p105">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface is accessed through the [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, which itself is accessed through the  `thisXDocument` variable that is initialized in the  `_Startup` method of the form code class. The following example demonstrates using the [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) and [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
```cs
thisXDocument.UI.ShowMailItem("someone@example.com","", "", 
   "Updated Form", "Here is the updated form that you requested.");
thisXDocument.UI.Alert("The email message has been created.");
```

```vb
thisXDocument.UI.ShowMailItem("someone@example.com", "", "", _
   "Updated Form", "Here is the updated form that you requested.")
thisXDocument.UI.Alert("The email message has been created.")
```

## <a name="using-the-showmodaldialog-method"></a><span data-ttu-id="41ce4-134">Uso del método ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="41ce4-134">Using the ShowModalDialog Method</span></span>

<span data-ttu-id="41ce4-135">En el siguiente ejemplo, se muestra cómo utilizar el método [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) de la interfaz [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) para mostrar un cuadro de diálogo personalizado definido en el archivo HTML show.html.</span><span class="sxs-lookup"><span data-stu-id="41ce4-135">This example demonstrates how to use the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface to display a custom dialog box defined in the HTML file show.html.</span></span> 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Write your code here.
   thisXDocument.UI.ShowModalDialog(
      "show.html",(object)thisXDocument,200,450,50,50);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Write your code here.
   thisXDocument.UI.ShowModalDialog( _
      "show.html", _
      DirectCast(thisXDocument, Object), 200, 450, 50, 50)
End Sub

```

<span data-ttu-id="41ce4-p106">Tanto los ejemplos de C# como los de Visual Basic dependen de un archivo HTML denominado "show.html" que define el cuadro de diálogo que invoca el método [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) . Este archivo HTML muestra algunos datos del formulario y un cuadro de texto al usuario para que éste escriba un valor. El valor del cuadro de texto se devuelve al formulario al cerrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="41ce4-p106">Both the Visual C# and Visual Basic samples depend on an HTML file named "show.html" that defines the dialog box that is invoked by the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method. This HTML file displays some data from the form and shows a text box for the user to fill in a value. The value in the textbox is returned to the form when the dialog box is closed.</span></span> 
  
```html
<HTML>
   <HEAD>
      <script language="JScript">
function BtnClick()
{
   xdocument = window.dialogArguments;
   myXml = xdocument.DOM.xml
   aForm = oForm.elements;
   aForm.textBox.value = myXml;
}
      </script>
   </HEAD>
   <BODY>
      <H1><FONT face="Arial">This is a modal dialog box</FONT> &nbsp;
      </H1>
      <BUTTON onclick="BtnClick()" id="BUTTON1" type="button">
         Get XML DOM
      </BUTTON>
      <FORM ID="oForm">
         <INPUT Type="text" name="textBox">
      </FORM>
   </BODY>
</HTML>

```

> [!IMPORTANT]
> <span data-ttu-id="41ce4-139">[!IMPORTANTE] El método [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) requiere plena confianza para su ejecución o vista previa.</span><span class="sxs-lookup"><span data-stu-id="41ce4-139">The [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method requires Full Trust to run or preview.</span></span> <span data-ttu-id="41ce4-140">Para obtener más información, vea [Vista previa y depurar plantillas de formulario que requieren plena confianza.](how-to-preview-and-debug-form-templates-that-require-full-trust.md)</span><span class="sxs-lookup"><span data-stu-id="41ce4-140">For more information, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  

