---
title: Controlar errores
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- errors [infopath 2007], handling,FormErrorCollection [InfoPath 2007],InfoPath 2007, error handling,FormError [InfoPath 2007],error handling [InfoPath 2007]
localization_priority: Normal
ms.assetid: 132cb698-d9a5-4767-b3d1-5dd1343a1ff4
description: Al crear aplicaciones personalizadas, los programadores deben con frecuencia controlar errores, lo que supone escribir código de programación para comprobar los errores generados por la aplicación o para crear y generar errores personalizados. El modelo de objetos de InfoPath proporcionado por el espacio de nombres Microsoft.Office.InfoPath admite el control de errores mediante el uso de la clase FormError en asociación con la clase FormErrorCollection .
ms.openlocfilehash: 30cf649188b7e4cbc35469d2a50540bb13ecb38d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410780"
---
# <a name="handle-errors"></a>Controlar errores

Al crear aplicaciones personalizadas, los programadores deben con frecuencia controlar errores, lo que supone escribir código de programación para comprobar los errores generados por la aplicación o para crear y generar errores personalizados. El modelo de objetos de InfoPath proporcionado por el espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) admite el control de errores mediante el uso de la clase [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) en asociación con la clase [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . 
  
En InfoPath, los errores se pueden producir por las razones siguientes:
  
- Cuando los datos escritos en un formulario dan error en la validación del esquema XML.
    
- Cuando se produce un error en una restricción de validación personalizada.
    
- Cuando se genera un error o cuando se crea un error con el método [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) del objeto de evento [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) . 
    
- Cuando se crea un error definido por el usuario usando el método [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) de la clase [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . 
    
## <a name="overview-of-the-formerrorcollection-class"></a>Información general sobre la clase FormErrorCollection

La clase [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) proporciona los siguientes métodos y propiedades que los desarrolladores de formularios pueden utilizar para administrar los objetos [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) que contiene. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[Método](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) Add (+3 sobrecargas)  <br/> |Crea un objeto **FormError** y lo añade a la colección.  <br/> |
|[Método Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) (+1 sobrecarga)  <br/> |Elimina el error definido por el usuario especificado de la colección.  <br/> |
|[DeleteAll (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx)  <br/> |Elimina todos los objetos **FormError** contenidos en la colección.  <br/> |
|[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) (+1 sobrecarga)  <br/> |Devuelve todos los objetos **FormError** del nombre o tipo especificado de la colección.  <br/> |
|Propiedad [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx)  <br/> |Obtiene el número de objetos **FormError** contenidos en la colección.  <br/> |
|Propiedad [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx)  <br/> |Obtiene una referencia a un objeto **FormError** basada en el número de índice especificado.  <br/> |
   
## <a name="overview-of-the-formerror-class"></a>Información general sobre la clase FormError

La clase [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) proporciona las siguientes propiedades que los programadores de formularios pueden utilizar para tener acceso a la información sobre el error que se ha producido. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[DetailedMessage (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx)  <br/> |Obtiene o establece el mensaje de error detallado del objeto **FormError**.  <br/> |
|[ErrorCode (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx)  <br/> |Obtiene o establece el código de error del objeto **FormError**.  <br/> |
|[Site (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)  <br/> |Obtiene un objeto **XPathNavigator** que está situado en el nodo asociado con el objeto **FormError**.  <br/> |
|[Message (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx)  <br/> |Obtiene o establece el mensaje de error corto del objeto **FormError**.  <br/> |
|[FormErrorType (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx)  <br/> |Obtiene el tipo del objeto **FormError**.  <br/> |
   
## <a name="using-the-formerrorcollection-and-formerror-classes"></a>Uso de las clases FormErrorCollection y FormError

Se puede tener acceso al objeto **FormErrorCollection** asociado con un formulario mediante la propiedad [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) del objeto [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . El objeto **FormErrorCollection** está asociado a un documento XML subyacente del formulario de forma que cuando se produce un error se puede tener acceso y controlar (el error y los que se produzcan después) dentro del documento XML. En el ejemplo siguiente, se muestra el uso de un bucle para comprobar los errores que pueden existir en el documento XML subyacente del formulario. Si se producen errores, la función recorre cada uno de ellos y, con la propiedad **Message** del objeto **FormError**, muestra un cuadro de mensaje al usuario. 
  
```cs
public void CheckErrors(XPathNavigator xmlNode)
{
   foreach(FormError err in this.Errors)
   {
      if(xmlNode.InnerXml == err.Site.InnerXml)
         MessageBox.Show("The following error has occured: "
             + err.Message);
   }
}
```

```vb
Public Sub CheckErrors(ByVal xmlNode As XPathNavigator)
   Dim err As FormError
   For Each err In Me.Errors
      If xmlNode.InnerXml = err.Site.InnerXml Then
         MessageBox.Show("The following error has occured: " _
             &amp; err.Message)
   End If
End Sub
```

Se puede llamar a la función anterior desde uno de los controladores de eventos de validación de datos del formulario. Por ejemplo, cuando se utiliza en el controlador de eventos del evento [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) de un campo del formulario, la llamada a la función transmitiría el argumento del nodo XML usando la propiedad [Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) del objeto de evento [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) como se muestra a continuación. 
  
```cs
CheckErrors(e.Site);
```

```vb
CheckErrors(e.Site)
```

Además de controlar los errores generados por InfoPath, los programadores de formularios generan errores personalizados, utilizando el método [ReportError(XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) del objeto de evento [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) , o bien utilizando el método [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) de la clase [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . Para obtener información sobre el uso de los métodos [ReportError(XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) o [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) , haga clic en los vínculos de los métodos que figuran al principio de este tema. 
  
## <a name="handling-managed-code-exceptions"></a>Controlar las excepciones de código administrado

Puede utilizar el control de las excepciones try-catch para controlar aquéllas que se produzcan en una plantilla de formulario con código administrado, tal como se muestra en el siguiente ejemplo de código.
  
```cs
FileQueryConnection queryXMLFile = 
   (FileQueryConnection)this.DataConnections["form1"];
// Perform the query.
try
{
   queryXMLFile.Execute();
}
catch (Exception ex)
{
   MessageBox.Show("Failed to query." + System.Environment.NewLine 
      + ex.Message);
}
```

```vb
Dim queryXMLFile As FileQueryConnection = _
   DirectCast(Me.DataConnections("form1"), FileQueryConnection)
' Perform the query.
Try
   queryXMLFile.Execute();
Catch ex As Exception
   MessageBox.Show("Failed to query." &amp; System.Environment.NewLine 
      &amp; ex.Message)
End Try
```

Si no utiliza el control de las excepciones try-catch en el código del formulario, InfoPath mostrará información sobre las excepciones no controladas en el cuadro de diálogo de errores de InfoPath mientras se depuran y se obtiene una vista previa. Además, de manera predeterminada, estas excepciones no se muestran en el cuadro de diálogo de errores de InfoPath en tiempo de ejecución al implementar una plantilla de formulario con código administrado. Para mostrar información sobre las excepciones no controladas en tiempo de ejecución, utilice este procedimiento.
  
### <a name="enable-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Habilitación de las notificaciones sobre excepciones de código administrado no controladas en tiempo de ejecución

1. Abra el diseñador de InfoPath y a continuación haga clic en la pestaña **Archivo**. 
    
2. Haga clic en **Opciones** y a continuación haga clic en **Opciones de InfoPath** bajo la categoría **General**. 
    
3. En la ficha **Avanzadas**, active la casilla de verificación **Mostrar una notificación para los errores de código de Visual Basic o C#**. 
    

