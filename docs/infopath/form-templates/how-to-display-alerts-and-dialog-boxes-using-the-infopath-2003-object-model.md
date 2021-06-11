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
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a>Mostrar alertas y cuadros de diálogo con el modelo de objetos de InfoPath 2003

Cuando se escribe código para ampliar la funcionalidad de una plantilla de formulario que utiliza el modelo de objetos de InfoPath 2003, con frecuencia resulta útil proporcionar al usuario información en un cuadro de diálogo. Para mostrar mediante programación un cuadro de diálogo y los elementos relacionados de la interfaz de usuario en InfoPath, se utilizan los métodos de la interfaz [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) . 
  
## <a name="overview-of-the-uiobject-interface"></a>Información general sobre la interfaz UIObject

La interfaz [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) proporciona los siguientes métodos que los programadores de formularios pueden utilizar para mostrar distintos tipos de cuadros de diálogo a los usuarios de InfoPath mientras rellenan un formulario. 
  
|Nombre|Descripción|
|:-----|:-----|
|[Alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |Muestra un cuadro de mensaje sencillo que contiene una cadena de mensaje especificada. Utilice este método si no necesita obtener información del usuario y sólo desea mostrar un mensaje. El cuadro de diálogo que se muestra se cierra haciendo clic en el botón **Aceptar**.<br/> |
|[Confirm](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |Muestra un cuadro de mensaje con botones para obtener información de un usuario. El valor que se devuelve es una de las constantes enumeradas [XdConfirmChoice.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx)  <br/> |
|[SetSaveAsDialogFileName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |Establece el nombre de archivo predeterminado de un formulario en el cuadro de diálogo **Guardar como**.  <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |Establece la ubicación inicial desde la que empieza a examinar el cuadro de diálogo **Guardar como** al abrirlo.  <br/> |
|[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |Crea un nuevo mensaje de correo electrónico en la aplicación de correo electrónico predeterminada, con el formulario abierto actualmente adjunto al mensaje.  <br/> |
|[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |Muestra un cuadro de diálogo modal basado en el archivo .html especificado y en los argumentos posicionales. Este método debe usarse si desea mostrar más que un mensaje simple al usuario y necesita recuperar algunos datos del usuario (más allá de la confirmación sencilla que proporciona el **sí** | **No** | **Botones** de cancelación mostrados por el **método Confirm).**  <br/> |
|[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |Muestra el cuadro de diálogo integrado **Firmas digitales**.  <br/> |
   
## <a name="using-the-uiobject-interface"></a>Uso de la interfaz UIObject

El acceso a la interfaz [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) se obtiene mediante la propiedad [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) de la interfaz [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , a la que a su vez se obtiene acceso mediante la variable  `thisXDocument` que se inicializa en el método  `_Startup` de la clase de código de formulario. En el siguiente ejemplo, se muestra el uso de los métodos [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) y [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) de la interfaz [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) : 
  
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

## <a name="using-the-showmodaldialog-method"></a>Uso del método ShowModalDialog

En el siguiente ejemplo, se muestra cómo utilizar el método [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) de la interfaz [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) para mostrar un cuadro de diálogo personalizado definido en el archivo HTML show.html. 
  
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

Tanto los ejemplos de C# como los de Visual Basic dependen de un archivo HTML denominado "show.html" que define el cuadro de diálogo que invoca el método [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) . Este archivo HTML muestra algunos datos del formulario y un cuadro de texto al usuario para que éste escriba un valor. El valor del cuadro de texto se devuelve al formulario al cerrar el cuadro de diálogo. 
  
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
> [!IMPORTANTE] El método [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) requiere plena confianza para su ejecución o vista previa. Para obtener más información, vea [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md). 
  

