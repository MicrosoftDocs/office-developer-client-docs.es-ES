---
title: Controlar errores mediante el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, handling errors,InfoPath 2003-compatible form templates, error handling,form templates [InfoPath 2007], error handling,error handling [InfoPath 2007], InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: eeb05205-d6f4-4931-b9a9-55a663bb1a25
description: Al crear aplicaciones personalizadas, los programadores deben con frecuencia controlar errores, lo que supone escribir código de programación para comprobar los errores generados por la aplicación o para crear y generar errores personalizados. El modelo de objetos compatible con InfoPath 2003 admite el control de errores mediante el uso del objeto ErrorObject en asociación con la colección ErrorsCollection .
ms.openlocfilehash: 93991e33d8867f89454bec08b41ba83e98ab0a17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439481"
---
# <a name="handle-errors-using-the-infopath-2003-object-model"></a>Controlar errores mediante el modelo de objetos de InfoPath 2003

Al crear aplicaciones personalizadas, los programadores deben con frecuencia controlar errores, lo que supone escribir código de programación para comprobar los errores generados por la aplicación o para crear y generar errores personalizados. El modelo de objetos compatible con InfoPath 2003 admite el control de errores mediante el uso del objeto [ErrorObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorObject.aspx) en asociación con la colección [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) . 
  
En InfoPath, se pueden producir errores cuando al escribir datos en un formulario se genera un error en la validación del esquema XML, cuando se produce un error en una restricción de validación personalizada, cuando el método [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReportError.aspx) del objeto [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) genera un error o cuando se crea un error con el método [Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx) de la colección [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) . 
  
## <a name="overview-of-the-errorscollection-collection"></a>Información general sobre la colección ErrorsCollection

La colección **ErrorsCollection** proporciona los siguientes métodos y propiedades que los programadores de formularios pueden utilizar para administrar los objetos **ErrorObject** que contiene. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|Método [Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx)  <br/> |Crea un objeto **ErrorObject** y lo agrega a la colección.  <br/> |
|Método [Delete](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Delete.aspx)  <br/> |Elimina todos los objetos **ErrorObject** asociados al nodo XML especificado y al nombre de la condición, excepto los errores personalizados agregados mediante el método **ReportError**.  <br/> |
|[DeleteAll (método)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.DeleteAll.aspx)  <br/> |Elimina todos los objetos **ErrorObject** contenidos en la colección.  <br/> |
|Propiedad [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Count.aspx)  <br/> |Obtiene el número de objetos **ErrorObject** contenidos en la colección.  <br/> |
|Propiedad [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Item.aspx)  <br/> |Obtiene una referencia a un objeto **ErrorObject** basada en el número de índice especificado.  <br/> |
   
## <a name="overview-of-the-errorobject-object"></a>Información general sobre el objeto ErrorObject

El objeto **ErrorObject** proporciona las siguientes propiedades que pueden usar los programadores de formularios para tener acceso a la información sobre el error que se produjo. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[ConditionName (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ConditionName.aspx)  <br/> |Obtiene el nombre de la condición de error o devuelve el valor **null**, en función del tipo de objeto **ErrorObject**.  <br/> |
|[DetailedErrorMessage (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.DetailedErrorMessage.aspx)  <br/> |Obtiene o establece el mensaje de error detallado del objeto **ErrorObject**.  <br/> |
|[ErrorCode (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorCode.aspx)  <br/> |Obtiene o establece el código de error del objeto **ErrorObject**.  <br/> |
|[Node (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.Node.aspx)  <br/> |Obtiene una referencia al nodo XML asociado al objeto **ErrorObject**.  <br/> |
|[ShortErrorMessage (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ShortErrorMessage.aspx)  <br/> |Obtiene o establece el mensaje de error breve del objeto **ErrorObject**.  <br/> |
|[ErrorType (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorType.aspx)  <br/> |Obtiene el tipo del objeto **ErrorObject**.  <br/> |
   
## <a name="using-the-errorscollection-and-errorobject"></a>Uso de ErrorsCollection y ErrorObject

A la colección **ErrorsCollection** se tiene acceso a través de la propiedad [Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.Errors.aspx) del objeto [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . La colección **ErrorsCollection** está asociada al documento XML subyacente de un formulario, de modo que cuando se produce un error, se produce dentro del documento XML. En el siguiente ejemplo se muestra cómo usar un bucle **foreach** de Visual C# para comprobar si existen errores en el documento subyacente de un formulario. En caso afirmativo, la función recorre en bucle todos ellos y, utilizando la propiedad **ShortErrorMessage** del objeto **ErrorObject**, muestra un cuadro de mensaje al usuario. 
  
```cs
public void CheckErrors(IXMLDOMNode xmlNode)
{
   foreach(ErrorObject err in thisXDocument.Errors)
   {
      if(xmlNode==err.Node)
         thisXDocument.UI.Alert("The following error has occured: "
             + err.ShortErrorMessage + ".");
   }
}
```

A la función anterior se puede llamar desde uno de los controladores de eventos de validación de datos del formulario. Por ejemplo, cuando se utiliza en el evento [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) de un campo del formulario, la llamada a la función transmitiría el argumento del nodo XML usando la propiedad [Site](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.Site.aspx) del objeto [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) como se muestra a continuación. 
  
```cs
CheckErrors(e.Site);
```

Además de controlar los errores generados por InfoPath, los programadores de formularios producen errores personalizados, utilizando el método **ReportError** del objeto **DataDOMEventObject**, o bien utilizando el método **Add** de la colección **ErrorsCollection**. Para obtener información sobre el uso de los métodos **ReportError** o **Add**, haga clic en los métodos, que figuran al principio de este tema. 
  
## <a name="handling-managed-code-exceptions"></a>Controlar las excepciones de código administrado

Puede utilizar el control de las excepciones try-catch para controlar aquéllas que se produzcan en una plantilla de formulario con código administrado, tal como se muestra en el siguiente ejemplo de código.
  
```cs
DataAdapters dataAdapters;
dataAdapters = thisXDocument.DataAdapters; 
XMLFileAdapterObject queryXMLFile = 
   (XMLFileAdapterObject)dataAdapters["form1"];
// Perform the query.
try
{
   queryXMLFile.Query();
}
catch (Exception ex)
{
   thisXDocument.UI.Alert("Failed to query.\n\n" + ex.Message);
}
// Perform the submit.
try
{
   queryXMLFile.Submit();
}
catch (Exception ex)
{
   thisXDocument.UI.Alert("Failed to submit.\n\n" + ex.Message);
}
```

Si no utiliza el control de las excepciones try-catch en el código del formulario, InfoPath mostrará información sobre las excepciones no controladas en el cuadro de diálogo de errores de InfoPath mientras se depura y se obtiene una vista previa. 
  

