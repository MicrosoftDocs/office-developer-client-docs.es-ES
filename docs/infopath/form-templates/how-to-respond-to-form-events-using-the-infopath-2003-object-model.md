---
title: Responder a eventos de formulario con el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- form templates [infopath 2007], responding to events,InfoPath 2003-compatible form templates, responding to form events
localization_priority: Normal
ms.assetid: 59e9c1ed-32a8-4bcd-bdfc-9aa568a34d2a
description: Es posible escribir código para responder a diversos eventos que pueden ocurrir cuando un usuario rellena un formulario. Para trabajar con eventos en InfoPath, se deben crear controladores de eventos en el diseñador de InfoPath.
ms.openlocfilehash: b7347f882df991e64bdf4e76c471b1220a84dc58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300101"
---
# <a name="respond-to-form-events-using-the-infopath-2003-object-model"></a>Responder a eventos de formulario con el modelo de objetos de InfoPath 2003

Es posible escribir código para responder a diversos eventos que pueden ocurrir cuando un usuario rellena un formulario. Para trabajar con eventos en InfoPath, se deben crear controladores de eventos en el diseñador de InfoPath.
  
Los controladores de eventos de InfoPath se deben crear en el diseñador de InfoPath, ya que, al usar el modelo de objetos compatible con InfoPath 2003, InfoPath agrega automáticamente la declaración correcta y aplica un atributo ([InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) al archivo de código del formulario (FormCode.cs o FormCode.vb) para identificar y recibir el controlador de eventos. Una vez creado un controlador de eventos, no se debe modificar su declaración ni su atributo en el archivo de código del formulario. 
  
Para obtener información sobre cómo crear controladores de eventos de InfoPath, vea [Agregar un controlador de eventos mediante el modelo de objetos de infopath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="overview-of-the-event-objects"></a>Información general sobre los objetos de eventos

El modelo de objetos compatible con InfoPath 2003 implementa nueve objetos de eventos que se exponen en el espacio de nombres [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . En la siguiente tabla se muestran todos los objetos de eventos de InfoPath, los controladores de eventos a los que están asociados y la descripción de la funcionalidad que aportan. 
  
|**Name**|**Controladores de eventos**|**Descripción**|
|:-----|:-----|:-----|
|[DataDOMEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.aspx) <br/> |[OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) <br/> [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) , [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) <br/> |Devuelve una referencia al documento XML subyacente de un formulario, el estado de retorno y otras propiedades que contienen información sobre el nodo XML durante un cambio de Modelo de objetos de documento (DOM) XML. También incluye un método para generar un error.  <br/> |
|[DocActionEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocActionEvent.aspx) <br/> |[OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) <br/> |Devuelve una referencia al documento XML subyacente de un formulario, el estado de retorno y el nodo XML de origen cuando se hace clic en un botón del área del formulario.  <br/> |
|[DocContextChangeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocContextChangeEvent.aspx) <br/> |[OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx) <br/> |Devuelve información sobre el nodo del Modelo de objetos de documento XML (DOM) que es el contexto actual del documento XML subyacente del formulario.  <br/> |
|[DocEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocEvent.aspx) <br/> |[Onswitchview](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx) , [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) <br/> |Devuelve una referencia al documento XML subyacente de un formulario al realizar una operación de cambio de vista o combinación de formularios.  <br/> |
|[DocReturnEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocReturnEvent.aspx) <br/> |[OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) , [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) <br/> |Devuelve una referencia al documento XML subyacente de un formulario y el estado de retorno durante la carga o el envío de un formulario.  <br/> |
|[MergeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MergeEvent.aspx) <br/> |[OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) <br/> |Devuelve las propiedades y los métodos que se pueden utilizar durante un evento **OnMergeRequest** para interaccionar mediante programación con un documento XML subyacente del formulario y determinar las propiedades de combinación, como el número de archivos que se combinan.  <br/> |
|[SaveEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SaveEvent.aspx) <br/> |[OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) <br/> |Devuelve propiedades y métodos que se pueden usar durante la operación para guardar desde el controlador de eventos **OnSaveRequest** para interaccionar mediante programación con un documento XML subyacente del formulario, determinar las propiedades de guardado y realizar la operación de guardado.  <br/> |
|[SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) <br/> |[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Se utiliza para agregar datos adicionales a la firma digital.  <br/> |
|[VersionUpgradeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.VersionUpgradeEvent.aspx) <br/> |[OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) <br/> |Devuelve una referencia al documento XML subyacente de un formulario, el estado de retorno así como los números de versión del documento y la solución durante la operación de actualización de versiones.  <br/> |
   
## <a name="using-the-event-objects"></a>Utilizar objetos de eventos

Al crear un controlador de eventos, InfoPath crea la declaración de éste en el archivo de código de formulario del proyecto (FormCode.cs o FormCode.vb). En la declaración del controlador de eventos, InfoPath utiliza **e** como nombre del parámetro que se transmite al controlador de eventos. Este parámetro contiene el objeto de eventos que está asociado al controlador de eventos. 
  
Por ejemplo, si se crea un controlador de eventos para el evento **OnLoad** en el modo de diseño (haciendo clic en **Evento Al cargar (OnLoad)** en la ficha **Programador**), InfoPath agrega la declaración del controlador de eventos que recibe el objeto **DocReturnEvent** al archivo de código de formulario y, después, abre el Editor de código para que pueda agregar el código a la siguiente declaración del controlador de eventos. 
  
```cs
// The following function handler is created by Microsoft Office 
// InfoPath. Do not modify the type or number of arguments.
[InfoPathEventHandler(EventType=InfoPathEventType.OnLoad)]
public void FormEvents_OnLoad(DocReturnEvent e)
{
   // Write your code here.
}
```

```vb
' The following function handler is created by Microsoft Office 
' InfoPath. Do not modify the type or number of arguments.
<InfoPathEventHandler(EventType:=InfoPathEventType.OnLoad)> _
Public Sub FormEvents_OnLoad(ByVal e As DocReturnEvent)
   ' Write your code here.
End Sub
```

Al escribir código para un controlador de eventos, puede utilizar las propiedades y los métodos implementados por el objeto de eventos que se transmite mediante el parámetro **e**. Por ejemplo, en el controlador de eventos **OnBeforeChange** que se muestra a continuación, la propiedad [NewValue](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.NewValue.aspx) del objeto de eventos **DataDOMEvent** se utiliza para comprobar el valor del campo que se acaba de cambiar. Si está en blanco, la propiedad [ReturnMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnMessage.aspx) del objeto de eventos **DataDOMEvent** se utiliza para mostrar un error al usuario en un cuadro de diálogo y la propiedad [ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnStatus.aspx) se establece en **false**, para indicar que los cambios que ha realizado el usuario no se deberían aceptar.
  
```cs
[InfoPathEventHandler(MatchPath="/my:myFields/my:field1", 
    EventType=InfoPathEventType.OnBeforeChange)]
public void field1_OnBeforeChange(DataDOMEvent e)
{
   // Determine whether there is a new value.
   if ((string)e.NewValue == "")
   {
      // The value is blank, so display an error message and roll
      // back the changes.
      e.ReturnMessage = "You must supply a value for this field.";
      e.ReturnStatus = false;
      return;
   }
}
```

```vb
<InfoPathEventHandler(MatchPath:="/my:myFields/my:field1", _ EventType:=InfoPathEventType.OnBeforeChange)> _
Public Sub field1_OnBeforeChange(ByVal e As DataDOMEvent)
   ' Determine whether there is a new value.
   If (e.NewValue = "") Then
      ' The value is blank, so display an error message and roll back
      ' the changes.
      e.ReturnMessage = "You must supply a value for this field."
      e.ReturnStatus = False
      Return
   End If
End Sub
```

> [!NOTE]
> [!NOTA] Cada uno de los objetos de eventos de InfoPath del modelo de objetos compatibles con InfoPath 2003 implementa propiedades y métodos diferentes. Para obtener más información sobre un objeto de eventos concreto, haga clic en él en la tabla de objetos de eventos anterior. 
  

